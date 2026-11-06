Sí. Partimos **completamente desde cero**, sin Kali, sin WSL, sin Hyper-V y sin máquinas virtuales.

La idea será crear en **Windows 11** varios entornos de navegador independientes y reproducibles para **investigar cómo cambia la información que un sitio puede observar**. No vamos a intentar fabricar identidades para eludir sistemas antifraude/antibot.

Hay una limitación fundamental: **varios perfiles del navegador no pueden hacer que el hardware físico de tu Lenovo se convierta en varios equipos distintos**. CPU, GPU, sistema operativo y buena parte del stack gráfico siguen siendo los mismos. Por eso hablaremos de **perfiles/entornos de prueba diferenciados**, no de “huellas 100 % únicas”. Mozilla explica precisamente que la huella puede combinar características del SO, hardware, GPU, fuentes y navegador. ([Soporte de Mozilla](https://support.mozilla.org/es/kb/firefox-protecci%C3%B3n-contra-huellas%20dactilares?utm_source=chatgpt.com "Protección de Firefox contra huellas dactilares | Ayuda de Firefox"))

# Tutorial completo: laboratorio de perfiles web en Windows 11

## 1. Arquitectura final

No vamos a instalar Kali ni ninguna VM.

Tu ordenador quedará así:

```text
                    WINDOWS 11
                        │
          ┌─────────────┼─────────────┐
          │             │             │
       Chrome         Firefox        Edge
          │             │             │
     ┌────┼────┐        │        ┌────┼────┐
     │    │    │        │        │    │    │
    P-A  P-B  P-C      F-A      E-A  E-B  E-C
```

Cada perfil tendrá separado, entre otras cosas, su almacenamiento de navegación, cookies, historial y configuraciones. Chrome documenta explícitamente esta separación mediante perfiles, y Firefox también permite múltiples perfiles precisamente para mantener configuraciones y datos independientes. ([Ayuda de Google](https://support.google.com/chrome/answer/2364824?hl=es-419WebEn&utm_source=chatgpt.com "Gestionar Chrome con varios perfiles - Ordenador - Ayuda de Google Chrome"))

Además tendremos **tres configuraciones de prueba**:

```text
PERFIL A
Desktop / español / Colombia

PERFIL B
Laptop / inglés / Estados Unidos

PERFIL C
Mobile / español / España
```

Estos perfiles no pretenden hacerse pasar por personas reales; sirven para comprobar cómo responde una aplicación web ante distintos entornos.

---

# 2. Qué navegador recomiendo

Para este laboratorio recomiendo **Chrome como navegador principal**.

La razón es que Chrome DevTools tiene herramientas oficiales para emular:

- viewport/resolución
    
- DPR
    
- tipo de dispositivo
    
- User-Agent
    
- geolocalización
    
- orientación
    
- características de red
    
- ciertos sensores
    

Google documenta explícitamente estas funciones dentro de Device Mode y Network Conditions. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode?hl=es-419&utm_source=chatgpt.com "Simula dispositivos móviles con el modo de dispositivo  |  Chrome DevTools  |  Chrome for Developers"))

Usaremos Firefox como segundo entorno de comparación, no como mecanismo para fabricar otra identidad.

---

# 3. Instalar Chrome

Descarga Chrome desde Google:

```text
https://www.google.com/chrome/
```

Instálalo normalmente.

No necesitamos:

```text
Kali
WSL
Hyper-V
VMware
VirtualBox
```

Nada de eso participará en este laboratorio.

---

# 4. Crear tres perfiles de Chrome

Abre Chrome.

Arriba a la derecha:

```text
Perfil
   ↓
Añadir perfil
```

Crea:

```text
LAB-A
LAB-B
LAB-C
```

No recomiendo iniciar sesión con tu cuenta personal de Google en estos perfiles. El objetivo es mantener los entornos de prueba separados.

Google indica que los perfiles mantienen separadas configuraciones, historial, contraseñas y otros datos del navegador. ([Ayuda de Google](https://support.google.com/chrome/answer/2364824?hl=es-419WebEn&utm_source=chatgpt.com "Gestionar Chrome con varios perfiles - Ordenador - Ayuda de Google Chrome"))

---

# 5. Configuración de LAB-A

Usaremos:

```text
LAB-A
Tipo: Desktop
Idioma: es-CO
Viewport: 1920 × 1080
DPR: 1
Geolocalización: Bogotá
Timezone: America/Bogota
```

Este será nuestro perfil de referencia.

## Abrir DevTools

Dentro de LAB-A:

```text
Ctrl + Shift + I
```

o:

```text
F12
```

Luego activa Device Mode:

```text
Ctrl + Shift + M
```

Google documenta Device Mode como una herramienta de emulación para probar diferentes dispositivos desde el ordenador. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode?hl=es-419&utm_source=chatgpt.com "Simula dispositivos móviles con el modo de dispositivo  |  Chrome DevTools  |  Chrome for Developers"))

Selecciona:

```text
Dimensions → Responsive
```

y establece:

```text
Width: 1920
Height: 1080
```

Puedes modificar también el DPR desde las opciones de Device Mode. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode?hl=es-419&utm_source=chatgpt.com "Simula dispositivos móviles con el modo de dispositivo  |  Chrome DevTools  |  Chrome for Developers"))

---

# 6. Configurar ubicación de LAB-A

En DevTools:

```text
⋮
→ More tools
→ Sensors
```

En:

```text
Location
```

puedes seleccionar una ubicación o crear una personalizada.

Para un laboratorio:

```text
Name: Bogota
Locale: es-CO
Timezone: America/Bogota
```

Chrome permite crear ubicaciones personalizadas con coordenadas, zona horaria y locale. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/settings/locations/?authuser=660&utm_source=chatgpt.com "Locations  |  Chrome DevTools  |  Chrome for Developers"))

Para pruebas reales puedes utilizar coordenadas aproximadas de una ciudad, no una dirección particular.

---

# 7. LAB-B

Ahora abrimos:

```text
Chrome
→ LAB-B
```

Configuración:

```text
LAB-B

Tipo: Laptop
Idioma: en-US
Viewport: 1366 × 768
DPR: 1
Timezone: America/New_York
Locale: en-US
Geolocalización: New York
```

En Device Mode:

```text
Width: 1366
Height: 768
```

Y en Sensors:

```text
Location:
New York
```

Puedes crear un preset personalizado desde:

```text
DevTools
→ Settings
→ Locations
→ Add location
```

Chrome permite almacenar estos presets con `latitude`, `longitude`, `Timezone ID` y `Locale`. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/settings/locations/?authuser=660&utm_source=chatgpt.com "Locations  |  Chrome DevTools  |  Chrome for Developers"))

---

# 8. LAB-C

Nuestro tercer entorno:

```text
LAB-C

Tipo: Mobile
Idioma: es-ES
Viewport: 390 × 844
DPR: 3
Timezone: Europe/Madrid
Locale: es-ES
```

En Device Mode:

```text
Dimensions
→ Responsive
```

establecemos:

```text
390 × 844
```

y:

```text
DPR = 3
```

Chrome permite modificar explícitamente viewport y DPR durante la emulación. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode?hl=es-419&utm_source=chatgpt.com "Simula dispositivos móviles con el modo de dispositivo  |  Chrome DevTools  |  Chrome for Developers"))

También podemos seleccionar:

```text
Device type → Mobile
```

para que Chrome emule características propias del modo móvil, incluyendo comportamiento de interacción táctil. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode?hl=es-419&utm_source=chatgpt.com "Simula dispositivos móviles con el modo de dispositivo  |  Chrome DevTools  |  Chrome for Developers"))

---

# 9. ¿Qué hacemos con User-Agent?

Chrome DevTools permite modificar el User-Agent desde:

```text
DevTools
→ Network
→ Network conditions
```

y desactivar:

```text
Use browser default
```

para seleccionar un User-Agent diferente. Google indica que esta función está diseñada para **pruebas de compatibilidad, diseño responsive y detección de características**. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode/override-user-agent?authuser=6&hl=es-419&utm_source=chatgpt.com "Condiciones de red: Cómo anular la string del usuario-agente  |  Chrome DevTools  |  Chrome for Developers"))

Para nuestro laboratorio, no vamos a crear cadenas inventadas. Utiliza los presets que proporciona Chrome.

Por ejemplo:

```text
LAB-A → Default Chrome desktop
LAB-B → otro preset oficial
LAB-C → Android/mobile preset
```

Esto es importante porque un User-Agent cambiado **no convierte internamente a Chrome en otro navegador**; Google lo señala explícitamente. ([Desarrollador de Chrome](https://developer.chrome.com/docs/devtools/device-mode/override-user-agent?authuser=6&hl=es-419&utm_source=chatgpt.com "Condiciones de red: Cómo anular la string del usuario-agente  |  Chrome DevTools  |  Chrome for Developers"))

---

# 10. Lo que NO vamos a hacer

No vamos a utilizar scripts como:

```javascript
Object.defineProperty(navigator, ...)
```

para falsear sistemáticamente:

```text
navigator
canvas
WebGL
AudioContext
fonts
hardwareConcurrency
deviceMemory
```

ni extensiones "anti-detect".

Hay dos razones.

Primero, esos métodos pueden producir una combinación internamente incoherente.

Segundo, convertir el laboratorio en una configuración específicamente destinada a evitar sistemas de detección sería otra cosa diferente a realizar pruebas de compatibilidad y privacidad.

Nuestro enfoque será:

```text
configuración real
        +
emulación oficial
        +
perfiles separados
        +
medición
```

---

# 11. ¿Cómo hacemos realmente independientes los perfiles?

Esto es mucho más importante que instalar decenas de extensiones.

En LAB-A:

```text
cookies A
localStorage A
IndexedDB A
historial A
caché A
extensiones A
```

En LAB-B:

```text
cookies B
localStorage B
IndexedDB B
historial B
caché B
extensiones B
```

etc.

Esto evita que una sesión de LAB-A termine compartiendo estado con LAB-B.

Los perfiles de Chrome están diseñados precisamente para separar estas categorías de información. ([Ayuda de Google](https://support.google.com/chrome/answer/2364824?hl=es-419WebEn&utm_source=chatgpt.com "Gestionar Chrome con varios perfiles - Ordenador - Ayuda de Google Chrome"))

---

# 12. No instales las mismas extensiones en todos

Para nuestro experimento:

```text
LAB-A
sin extensiones adicionales

LAB-B
una extensión de desarrollo

LAB-C
otra configuración
```

Esto permite medir qué impacto tiene el software añadido.

Pero evita instalar extensiones de "fingerprint spoofing". Es mucho mejor estudiar qué información expone el navegador de forma normal.

---

# 13. Crear también un entorno Firefox

Instala Firefox desde:

```text
https://www.mozilla.org/firefox/
```

Firefox permite múltiples perfiles independientes. Puedes administrarlos desde:

```text
about:profiles
```

o mediante el administrador de perfiles de las versiones actuales. Mozilla documenta que cada perfil conserva sus propias configuraciones y datos de navegación. ([Soporte de Mozilla](https://support.mozilla.org/es/kb/profile-management?utm_source=chatgpt.com "Administrar perfiles de Firefox | Ayuda de Firefox"))

Crea:

```text
Firefox-LAB
Firefox-Privacy
```

---

# 14. Un perfil Firefox para privacidad

Aquí hacemos algo diferente.

En:

```text
Ajustes
→ Privacidad y seguridad
```

puedes utilizar:

```text
Protección contra rastreo mejorada
→ Estricta
```

Firefox incorpora protección específica contra fingerprinting y mecanismos de aislamiento, como Total Cookie Protection. ([Soporte de Mozilla](https://support.mozilla.org/en-US/kb/firefox-privacy-and-security-features?utm_source=chatgpt.com "Firefox privacy and security features | Firefox Help"))

**No actives `privacy.resistFingerprinting` buscando una "huella distinta".**

Su finalidad es la contraria: **reducir la capacidad de los sitios para identificar de forma única el navegador**. Mozilla advierte además de que puede causar problemas de compatibilidad. ([Soporte de Mozilla](https://support.mozilla.org/en-US/products/firefox/privacy-and-security?utm_source=chatgpt.com "Privacy and security | Firefox Help"))

---

# 15. Nuestro laboratorio final

Quedaría así:

```text
WINDOWS 11
│
├── Chrome
│   │
│   ├── LAB-A
│   │     ├── Desktop
│   │     ├── 1920×1080
│   │     ├── es-CO
│   │     └── Bogotá
│   │
│   ├── LAB-B
│   │     ├── Laptop
│   │     ├── 1366×768
│   │     ├── en-US
│   │     └── New York
│   │
│   └── LAB-C
│         ├── Mobile
│         ├── 390×844
│         ├── es-ES
│         └── Madrid
│
└── Firefox
    │
    ├── LAB
    └── PRIVACY
```

Esto requiere **muy pocos recursos** comparado con ejecutar VMs y es mucho más apropiado para tus 8 GB de RAM.

---

# 16. Cómo comprobar qué ve una página

Aquí está la parte realmente interesante.

Desde **cada perfil**, visita una herramienta de diagnóstico de fingerprinting y guarda los resultados.

Hazlo por separado:

```text
LAB-A → diagnóstico
LAB-B → diagnóstico
LAB-C → diagnóstico
Firefox-LAB → diagnóstico
Firefox-Privacy → diagnóstico
```

Compara:

```text
User-Agent
viewport
screen
DPR
timezone
locale
WebGL
Canvas
audio
fonts
hardwareConcurrency
deviceMemory
cookies
storage
```

No esperes que todo sea diferente.

Por ejemplo:

```text
                  LAB-A      LAB-B      LAB-C
------------------------------------------------
Browser            Chrome     Chrome     Chrome
OS                  Windows    Windows    Windows
CPU                  i5         i5         i5
GPU                 misma      misma      misma
Viewport            diferente  diferente  diferente
Locale              diferente  diferente  diferente
Timezone            diferente  diferente  diferente
Cookies             distinto   distinto   distinto
Storage             distinto   distinto   distinto
```

Y esa precisamente es la lección importante:

> **Los perfiles permiten separar el estado y emular determinadas condiciones, pero no convierten un único ordenador físico en tres ordenadores independientes.**

---

# 17. Si quieres experimentar con "huellas"

La metodología que recomiendo es:

```text
                PERFIL A
                   │
              ┌────▼────┐
              │ Medición│
              └────┬────┘
                   │
                   ▼
              fingerprint A


                PERFIL B
                   │
              ┌────▼────┐
              │ Medición│
              └────┬────┘
                   │
                   ▼
              fingerprint B
```

Luego modificas **una variable cada vez**:

```text
1. viewport
2. DPR
3. locale
4. timezone
5. User-Agent
6. dispositivo móvil/escritorio
7. extensiones
8. protección antirrastreo
```

y vuelves a medir.

Así puedes determinar exactamente **qué cambia y qué permanece constante**.

### La conclusión para tu equipo

Con tu **i5-1135G7 + 8 GB RAM + Windows 11 Home**, descartaría completamente Kali/VMs para este proyecto.

La configuración adecuada sería:

**Chrome + 3 perfiles + Chrome DevTools Device/Sensors/Network Conditions + Firefox para comparación + perfiles separados.**

Eso te permite estudiar de forma práctica **qué componentes forman una huella web y cuáles puedes modificar legítimamente para pruebas**, sin consumir la RAM que te exigirían varias VMs.