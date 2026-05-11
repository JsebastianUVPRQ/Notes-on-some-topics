# Tutorial De Credenciales SAR

Este es el inventario completo de cuentas, credenciales y claves que debes crear tú para que SAR funcione con Firebase, WhatsApp Cloud API y LLMs. No pongas ningún secreto en Git. Todo termina en tu archivo local `.env` o en variables de entorno del hosting.

## 1. Firebase / Google Cloud

Crea una cuenta Google y entra a [Firebase Console](https://console.firebase.google.com/).

1. Crea un proyecto Firebase, por ejemplo `sar-restaurant-prod`.
2. Entra a `Build > Firestore Database`.
3. Haz clic en `Create database`.
4. Elige `Production mode`, no `Test mode`.
5. Elige región cercana a tus usuarios, idealmente una región estable para Colombia/LatAm como `nam5`, `us-central`, `southamerica-east1` si aparece disponible.
6. Guarda el `Project ID`.

Variables:

```env
FIREBASE_PROJECT_ID=tu-project-id
```

Ahora crea la credencial del backend:

1. En Firebase ve a `Project settings`.
2. Abre la pestaña `Service accounts`.
3. Haz clic en `Generate new private key`.
4. Descarga el JSON.
5. Guárdalo fuera del repo, por ejemplo:

```text
C:\Users\Sebastian\Secrets\sar-firebase-service-account.json
```

Variable recomendada para local:

```env
FIREBASE_CREDENTIALS=C:\Users\Sebastian\Secrets\sar-firebase-service-account.json
```

Alternativa para hosting, cuando no quieras subir archivo JSON:

```env
FIREBASE_CREDENTIALS_JSON={"type":"service_account",...}
```

Opcional compatible con Google ADC:

```env
GOOGLE_APPLICATION_CREDENTIALS=C:\Users\Sebastian\Secrets\sar-firebase-service-account.json
```

Para desarrollo con emulador local:

```env
FIRESTORE_EMULATOR_HOST=localhost:8080
```

En producción, no pongas `FIRESTORE_EMULATOR_HOST`.

## 2. Meta / WhatsApp Cloud API

Necesitas una cuenta personal de Facebook, acceso a [Meta for Developers](https://developers.facebook.com/apps/) y un Business Portfolio en [Meta Business Suite](https://business.facebook.com/).

1. Entra a Meta for Developers.
2. Crea una app nueva.
3. Añade el producto `WhatsApp`.
4. Meta creará o vinculará un WhatsApp Business Account, también llamado WABA.
5. En `WhatsApp > API Setup`, copia el `Phone number ID`.
6. Para pruebas, puedes usar el número de prueba de Meta.
7. Para producción, añade un número real desde `Add phone number`.

Importante: el número real no puede estar activo al mismo tiempo en WhatsApp Messenger o WhatsApp Business App. Si ya está usado, tendrás que migrarlo/liberarlo antes.

Variables:

```env
WHATSAPP_PHONE_ID=tu-phone-number-id
WHATSAPP_PHONE_NUMBER_ID=tu-phone-number-id
```

`WHATSAPP_PHONE_NUMBER_ID` es alias legado; pon el mismo valor que `WHATSAPP_PHONE_ID`.

### Token De WhatsApp

Para pruebas, Meta te da un token temporal en `WhatsApp > API Setup`.

Variable:

```env
WHATSAPP_TOKEN=EAAB...
WHATSAPP_ACCESS_TOKEN=EAAB...
```

Para producción necesitas un token permanente o de larga duración mediante usuario de sistema en Meta Business. El token debe tener permisos de WhatsApp, normalmente:

```text
whatsapp_business_messaging
whatsapp_business_management
business_management
```

Usa el token permanente en `WHATSAPP_TOKEN`.

### App Secret

En Meta for Developers:

1. Abre tu app.
2. Ve a `App settings > Basic`.
3. Copia `App Secret`.
4. Guárdalo como:

```env
META_APP_SECRET=tu-app-secret
```

SAR lo usa para validar `X-Hub-Signature-256` en webhooks.

### Webhook Verify Token

Este valor lo inventas tú. Debe ser largo, aleatorio y privado. Ejemplo conceptual, no uses este:

```text
sar_webhook_7Nq4_local_2026_private
```

Ponlo en:

```env
WEBHOOK_VERIFY_TOKEN=tu-token-privado-largo
META_VERIFY_TOKEN=tu-token-privado-largo
```

En Meta, cuando configures el webhook, pega exactamente el mismo valor en `Verify token`.

### Webhook URL

En producción será algo como:

```text
https://tu-dominio.com/api/v1/webhook
```

Para local necesitas un túnel HTTPS tipo ngrok o Cloudflare Tunnel:

```text
https://xxxx.ngrok-free.app/api/v1/webhook
```

En Meta debes suscribir el webhook al campo:

```text
messages
```

## 3. OpenAI O Groq

SAR soporta OpenAI o Groq. Recomiendo empezar con OpenAI por estabilidad de JSON mode y luego dejar Groq como alternativa de coste/latencia.

### OpenAI

1. Entra a [OpenAI Platform](https://platform.openai.com/).
2. Crea o selecciona un proyecto.
3. Ve a configuración del proyecto.
4. Crea una API key.
5. Cópiala una sola vez y guárdala.

Variables:

```env
LLM_PROVIDER=openai
OPENAI_API_KEY=sk-...
OPENAI_MODEL=gpt-4o-mini
```

Para producción seria, mejor crea una service account del proyecto y usa esa key, no una key personal.

### Groq

1. Entra a [Groq Console](https://console.groq.com/).
2. Crea una API key.
3. Guárdala en:

```env
LLM_PROVIDER=groq
GROQ_API_KEY=gsk_...
GROQ_MODEL=llama-3.1-70b-versatile
```

Solo debes activar un proveedor principal con `LLM_PROVIDER`.

## 4. Seguridad Interna De SAR

Genera una clave JWT fuerte. En PowerShell puedes crear una así:

```powershell
[Convert]::ToBase64String((1..48 | ForEach-Object { Get-Random -Maximum 256 }))
```

Variables:

```env
JWT_SECRET_KEY=valor-largo-aleatorio
JWT_ALGORITHM=HS256
```

No reutilices esta clave entre desarrollo y producción.

Configura entorno y logs:

```env
APP_ENV=development
LOG_LEVEL=INFO
```

En producción:

```env
APP_ENV=production
LOG_LEVEL=INFO
```

Rate limit del webhook:

```env
RATE_LIMIT_WINDOW_SECONDS=60
RATE_LIMIT_MAX_REQUESTS=120
```

## 5. Archivo `.env` Final Local

Plantilla mínima para desarrollo real:

```env
APP_ENV=development
LOG_LEVEL=INFO

FIREBASE_PROJECT_ID=sar-restaurant-prod
FIREBASE_CREDENTIALS=C:\Users\Sebastian\Secrets\sar-firebase-service-account.json

WEBHOOK_VERIFY_TOKEN=pon-un-token-largo
META_VERIFY_TOKEN=pon-el-mismo-token-largo
META_APP_SECRET=app-secret-de-meta

WHATSAPP_TOKEN=token-de-meta
WHATSAPP_ACCESS_TOKEN=token-de-meta
WHATSAPP_PHONE_ID=phone-number-id
WHATSAPP_PHONE_NUMBER_ID=phone-number-id
WHATSAPP_API_VERSION=v20.0

LLM_PROVIDER=openai
OPENAI_API_KEY=sk-...
OPENAI_MODEL=gpt-4o-mini

GROQ_API_KEY=
GROQ_MODEL=llama-3.1-70b-versatile

JWT_SECRET_KEY=clave-jwt-larga
JWT_ALGORITHM=HS256

RATE_LIMIT_WINDOW_SECONDS=60
RATE_LIMIT_MAX_REQUESTS=120
```

## 6. Checklist De Verificación

Antes de probar SAR:

- Firebase Firestore existe en `Production mode`.
- El JSON de service account está fuera del repo.
- `.env` existe localmente y `.env.example` no contiene secretos.
- `FIREBASE_PROJECT_ID` coincide exactamente con el proyecto real.
- `WHATSAPP_PHONE_ID` es el Phone Number ID, no el número telefónico.
- `WHATSAPP_TOKEN` tiene permisos para enviar mensajes.
- `META_APP_SECRET` viene de la app correcta.
- `WEBHOOK_VERIFY_TOKEN` coincide exactamente con el token configurado en Meta.
- El webhook público termina en `/api/v1/webhook`.
- El webhook está suscrito a `messages`.
- `OPENAI_API_KEY` o `GROQ_API_KEY` está activo y con saldo/cuota.
- `JWT_SECRET_KEY` es distinto para local y producción.

## Fuentes Oficiales Consultadas

- [Firebase Admin SDK setup](https://firebase.google.com/docs/admin/setup)
- [Cloud Firestore quickstart](https://firebase.google.com/docs/firestore/quickstart)
- [Meta WhatsApp Cloud API overview](https://meta-preview.mintlify.io/docs/whatsapp/cloud-api/overview)
- [Meta WhatsApp add phone number](https://meta-preview.mintlify.io/docs/whatsapp/cloud-api/get-started/add-a-phone-number)
- [OpenAI API authentication](https://developers.openai.com/api/reference/overview#authentication)
- [OpenAI project API keys and service accounts](https://help.openai.com/en/articles/9186755-managing-your-work-in-the-api-platform-with-projects/)
- [Groq API overview](https://console.groq.com/docs/overview)
