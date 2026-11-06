La mejor forma de crear módulos reutilizables es separar dos cosas:

1. **La estructura narrativa:** fórmulas de hook, explicación, cierre y CTA.
    
2. **La ejecución audiovisual:** animaciones, gráficos, sonidos, fondos y composiciones.
    

No conviene reutilizar exactamente el mismo hook o la misma introducción en todos los vídeos. Conviene reutilizar su **estructura**, cambiando el texto, los datos y algunos elementos visuales. Además de cansar al espectador, una producción excesivamente repetitiva puede dificultar que el canal se perciba como contenido original y diferenciado durante la revisión de monetización. YouTube evalúa el canal completo y busca aportación original, comentario sustancial y valor educativo o de entretenimiento. ([Soporte de Google](https://support.google.com/youtube/answer/1311392?hl=en&utm_source=chatgpt.com "YouTube channel monetization policies"))

 Recomendación principal

Usaría:

- **DaVinci Resolve** como sistema principal si quieres construir una biblioteca profesional y escalable.
    
- **CapCut Desktop** si priorizas aprender rápido y producir inmediatamente.
    
- **ElevenLabs** para narración modular.
    
- ChatGPT o una hoja de cálculo para administrar las variantes de guion.
    
- PNG, SVG, WAV y archivos de proyecto editables como formatos maestros.
    

Mi elección para tu objetivo sería:

> **Empezar en CapCut para validar el canal y migrar gradualmente los módulos importantes a DaVinci Resolve.**

DaVinci permite trabajar con edición, Fusion para gráficos animados y Fairlight para audio dentro de un mismo programa. Fusion también permite convertir composiciones en macros reutilizables, y los Power Bins sirven para compartir recursos entre proyectos. ([Blackmagic Design Documentos](https://documents.blackmagicdesign.com/UserManuals/Fusion18_Manual.pdf?_v=1702368010000&utm_source=chatgpt.com "Fusion Reference Manual 18.6"))

---

## Qué debe ser realmente un módulo

Un módulo no debería ser un vídeo cerrado con palabras incrustadas.

Debería ser una composición editable con:

- duración ajustable;
    
- campos de texto reemplazables;
    
- colores modificables;
    
- espacio para cambiar imágenes;
    
- entrada y salida animadas;
    
- efectos de sonido separados;
    
- música separada;
    
- versión horizontal y vertical.
    

Ejemplo:

```text
HOOK_NUMBER_REVEAL_01

Duración: 5-8 segundos

Campos editables:
- Cifra principal
- Unidad
- Frase de contexto
- Fuente
- Fondo
- Color positivo/negativo

Animación:
- Entrada del número
- Pequeño zoom
- Aparición de gráfico
- Golpe sonoro
```

Para un vídeo podrías escribir:

```text
$10,000
invested in the S&P 500
twenty years ago
```

Y en otro:

```text
73%
of active funds
underperformed their benchmark
```

La animación es la misma, pero el contenido sustancial cambia.

---

# Formatos recomendados

# 1. Archivo maestro editable

Este es el formato más importante.

### En DaVinci Resolve

Guarda los módulos como:

- composiciones de Fusion;
    
- macros de Fusion;
    
- Adjustment Clips;
    
- Compound Clips;
    
- timelines de plantilla;
    
- elementos dentro de Power Bins.
    

### En CapCut

Guárdalos como:

- proyectos maestros duplicables;
    
- clips compuestos;
    
- presets de texto;
    
- animaciones favoritas;
    
- plantillas de marca, cuando estén disponibles;
    
- carpetas con recursos importables.
    

CapCut ofrece sistemas de Brand Kit y plantillas de marca para centralizar logotipos, tipografías, colores y otros activos, aunque algunas funciones dependen del plan utilizado. ([CapCut](https://www.capcut.com/help/benefits-of-capcut-teams?utm_source=chatgpt.com "What are the Benefits of CapCut Teams?"))

## 2. Exportación con transparencia

Para animaciones reutilizables sin tener que abrir el proyecto original:

- **MOV ProRes 4444 con canal alfa**, cuando esté disponible.
    
- **WebM con transparencia**, cuando sea compatible.
    
- **Secuencia PNG**, si necesitas máxima compatibilidad.
    

Ejemplos:

- flecha ascendente animada;
    
- marco de cotización;
    
- gráfico apareciendo;
    
- transición;
    
- etiqueta de fuente;
    
- CTA visual.
    

No exportaría texto específico dentro de estas animaciones. Dejaría el texto editable en el programa.

## 3. Recursos gráficos estáticos

- **SVG:** iconos, flechas, logotipos y diagramas escalables.
    
- **PNG transparente:** elementos recortados y recursos generados por IA.
    
- **JPG o WebP:** fondos fotográficos.
    
- **PSD o archivo editable original:** cuando tenga capas útiles.
    

## 4. Audio

- **WAV, 48 kHz y 24 bits:** narración maestra, efectos importantes y música procesada.
    
- **MP3:** solamente para archivos de referencia o previsualización.
    

Mantén separados:

```text
Narración
Música
Whooshes
Hits
Clicks
Ambientes
```

No conviene fusionar todo en un único archivo porque después no podrás ajustar niveles o sustituir un efecto.

---

# Estructura de carpetas

```text
YOUTUBE_FINANCE_SYSTEM/
│
├── 00_BRAND/
│   ├── Fonts/
│   ├── Logos/
│   ├── Colors/
│   ├── Icons/
│   └── Style_Guide.pdf
│
├── 01_PROJECT_TEMPLATES/
│   ├── Longform_16x9/
│   └── Shorts_9x16/
│
├── 02_NARRATIVE_MODULES/
│   ├── Hooks/
│   ├── Concept_Explanations/
│   ├── Comparisons/
│   ├── Transitions/
│   ├── Closings/
│   └── CTA/
│
├── 03_VISUAL_MODULES/
│   ├── Numbers/
│   ├── Charts/
│   ├── Quotes/
│   ├── Headlines/
│   ├── Timelines/
│   ├── Lists/
│   └── Source_Cards/
│
├── 04_BROLL/
│   ├── Markets/
│   ├── Banking/
│   ├── Personal_Finance/
│   ├── Technology/
│   └── Cities/
│
├── 05_AI_IMAGES/
│   ├── Inflation/
│   ├── Investing/
│   ├── AI_Stocks/
│   ├── Recession/
│   └── Credit_Cards/
│
├── 06_AUDIO/
│   ├── Music/
│   ├── Hits/
│   ├── Whooshes/
│   ├── Clicks/
│   └── Ambience/
│
└── 07_EXPORTS/
    ├── Masters/
    ├── Shorts/
    └── Thumbnails/
```

Usaría nombres como:

```text
HOOK_STAT_01_v03
HOOK_CONTRARIAN_02_v02
EXPLAIN_COMPOUNDING_01_v04
CTA_NEXT_VIDEO_01_v02
```

Así puedes actualizar un módulo sin perder las versiones anteriores.

---

# Módulos de introducción

En tu caso, evitaría una intro de marca tradicional de 5–10 segundos.

No comenzaría con:

```text
Welcome back to Finance Insight...
```

Comenzaría directamente con el contenido.

La “intro” sería un módulo de identidad muy corto, integrado después del primer impacto:

```text
0:00-0:05  Hook
0:05-0:08  Promesa del vídeo
0:08-0:09  Identificador visual del canal
0:09+      Desarrollo
```

## Módulo recomendado

```text
INTRO_MICRO_ID_01

Duración: 0,5-1 segundo

Elementos:
- Logotipo o nombre pequeño
- Sonido identificador
- Barrido o transición breve
```

Debe sentirse como puntuación visual, no como un anuncio previo al vídeo.

Crea solamente:

- dos microintros para vídeos largos;
    
- una para Shorts;
    
- una variante sin logotipo.
    

No necesitas diez.

---

# Módulos de hooks

Los hooks deben reutilizar **patrones**, no frases.

Crearía entre seis y diez tipos.

## Hook de resultado

```text
“This is what happens when you invest $500 every month for 20 years.”
```

Visual:

- número grande;
    
- línea ascendente;
    
- resultado parcialmente oculto;
    
- revelación posterior.
    

## Hook de contradicción

```text
“Diversification can actually make your portfolio worse.”
```

Visual:

- afirmación común;
    
- tachado;
    
- palabra contraria;
    
- gráfico o evidencia.
    

## Hook de error

```text
“This ETF mistake can cost investors thousands.”
```

Visual:

- símbolo de error;
    
- cifra;
    
- caída;
    
- pantalla cortada antes de mostrar la explicación.
    

## Hook de pregunta

```text
“Why do investors keep buying a fund that consistently loses money?”
```

Visual:

- ticker;
    
- gráfico descendente;
    
- pregunta central.
    

## Hook de comparación

```text
“Two investors earned the same salary. One retired with five times more money.”
```

Visual:

- pantalla dividida;
    
- dos personajes;
    
- resultados divergentes.
    

## Hook de noticia contextualizada

```text
“The Federal Reserve just made a decision that could change your mortgage payments.”
```

Visual:

- titular;
    
- fecha;
    
- cifra;
    
- flecha hacia el impacto personal.
    

### Cómo producirlos

Crea un proyecto llamado:

```text
MASTER_HOOKS_16x9
```

Incluye diez timelines:

```text
01_NUMBER_REVEAL
02_CONTRARIAN
03_COSTLY_MISTAKE
04_COMPARISON
05_QUESTION
06_NEWS
07_COUNTDOWN
08_BEFORE_AFTER
09_MYTH_REALITY
10_HIDDEN_REASON
```

En cada una, deja campos reemplazables para:

- texto;
    
- cifra;
    
- imagen;
    
- gráfico;
    
- fuente;
    
- duración.
    

No generes narraciones fijas para los hooks. Genera la narración nueva para cada vídeo, porque la entonación debe coincidir con la frase concreta.

---

# Módulos para explicar conceptos

Aquí es donde más tiempo puedes ahorrar.

Crea módulos visuales universales para relaciones financieras frecuentes.

## Causa → efecto

```text
Higher rates
↓
More expensive borrowing
↓
Lower spending
↓
Slower economic growth
```

Formato:

- cuatro tarjetas;
    
- flechas;
    
- entrada secuencial;
    
- texto editable.
    

## Antes y después

```text
Before inflation / After inflation
```

Formato:

- pantalla dividida;
    
- mismo producto;
    
- precios diferentes;
    
- porcentaje de incremento.
    

## Comparador

```text
ETF A vs ETF B
```

Campos:

- comisión;
    
- rendimiento;
    
- volatilidad;
    
- dividendos;
    
- composición.
    

## Fórmula visual

```text
Initial investment
+
Monthly contributions
+
Compound growth
=
Final portfolio
```

## Línea temporal

```text
Year 1 → Year 5 → Year 10 → Year 20
```

## Desglose porcentual

```text
Stocks: 60%
Bonds: 30%
Cash: 10%
```

## Escenario hipotético

```text
If you invested...
If the return was...
After 10 years...
```

## Analogía visual

Ejemplo para explicar un ETF:

```text
ETF
=
basket containing many companies
```

Visual:

- cesta;
    
- logotipos o sectores;
    
- agrupación;
    
- etiqueta final.
    

### Regla de producción

Cada explicación debe tener tres capas:

```text
Capa 1: narración específica;
Capa 2: visual reutilizable;
Capa 3: datos y textos específicos.
```

Solo la capa visual permanece casi igual.

---

# Módulos de transición narrativa

También debes modularizar frases que conectan secciones:

```text
“But this is only half the story.”
“Now here is where it gets interesting.”
“To understand why, we need to go back.”
“That creates a second problem.”
“But there is one important exception.”
```

No las usaría todas literalmente. Mantendría una base de fórmulas y generaría variantes.

Visualmente puedes tener:

- cambio de capítulo;
    
- desplazamiento lateral;
    
- número de sección;
    
- mapa conceptual;
    
- barra de progreso;
    
- nueva pregunta.
    

Duración recomendada:

```text
0,3-1,5 segundos
```

Las transiciones demasiado largas reducen la densidad del vídeo.

---

# Módulos de cierre

Un cierre no debe limitarse a resumir.

Debe cumplir tres funciones:

1. resolver la promesa inicial;
    
2. dejar una conclusión fácil de recordar;
    
3. conducir al siguiente contenido.
    

## Plantilla

```text
Conclusión principal
↓
Condición o matiz
↓
Acción práctica
↓
Puente al siguiente vídeo
```

Ejemplo:

```text
“So the real advantage of index funds isn't that they always produce
the highest return. It's that they make it easier to remain invested.

But choosing the wrong fund can still cost you thousands in fees.

That's what we'll compare next.”
```

Visual:

- reaparece el gráfico inicial;
    
- se completa la información ocultada;
    
- aparecen tres conclusiones breves;
    
- entra la miniatura o tarjeta conceptual del siguiente vídeo.
    

Crea tres cierres visuales:

```text
CLOSE_SUMMARY_01
CLOSE_REVEAL_01
CLOSE_NEXT_TOPIC_01
```

La voz y el texto deben cambiar siempre.

---

# Módulos de CTA

Evita utilizar siempre:

```text
Like and subscribe.
```

Un CTA debe corresponder a la acción que deseas provocar.

## CTA de comentario

```text
“Would you choose the lower fee or the stronger historical return?”
```

Úsalo cuando exista una decisión o controversia real.

## CTA de experiencia

```text
“What was the first stock or ETF you ever bought?”
```

## CTA de corrección

```text
“Is there another cost you think investors overlook?”
```

## CTA de suscripción

```text
“If you want financial ideas explained without the jargon, subscribe.”
```

## CTA al siguiente vídeo

```text
“Now that you understand expense ratios, watch this comparison of the
three most common S&P 500 ETFs.”
```

Para acelerar la monetización, el CTA al siguiente vídeo probablemente sea más estratégico que pedir una suscripción genérica, porque intenta extender la sesión y generar más tiempo de visualización.

Crea cinco módulos visuales:

```text
CTA_COMMENT_QUESTION
CTA_SUBSCRIBE_VALUE
CTA_NEXT_VIDEO
CTA_DOWNLOAD_RESOURCE
CTA_SUMMARY_CHECKLIST
```

El gráfico puede repetirse; la pregunta y el contexto deben cambiar.

---

# Workflow recomendado

## Fase 1: crear el sistema maestro

Crea dos proyectos:

```text
FINANCE_MASTER_LONGFORM_16x9
FINANCE_MASTER_SHORTS_9x16
```

Dentro de cada uno define pistas fijas:

```text
V5 — Titulares y textos
V4 — Gráficos y módulos
V3 — B-roll e imágenes
V2 — Fondos
V1 — Base

A1 — Narración
A2 — Efectos
A3 — Música
A4 — Ambiente
```

También deja configurados:

- tipografías;
    
- subtítulos;
    
- niveles de audio;
    
- transiciones;
    
- etiqueta de fuentes;
    
- márgenes seguros;
    
- pantalla final;
    
- colorización base.
    

## Fase 2: producir los módulos

No intentes crear 100 al principio.

Primera biblioteca mínima:

```text
6 hooks
5 explicadores
3 comparadores
3 tarjetas de cifras
2 titulares
2 cronologías
3 transiciones
3 cierres
5 CTA
```

Total: **32 módulos**.

Eso es suficiente para producir bastantes combinaciones sin que todos los vídeos parezcan idénticos.

## Fase 3: escribir el guion con etiquetas

Estructura el guion así:

```text
[HOOK_CONTRARIAN_02]

Narration:
Most investors think owning more funds always means better diversification.

Visual text:
MORE FUNDS ≠ MORE DIVERSIFICATION

[EXPLAIN_OVERLAP_01]

Narration:
But many popular ETFs own exactly the same companies.

Data:
ETF A overlap: 82%
ETF B overlap: 76%

[COMPARE_TWO_FUNDS_02]

...

[CTA_NEXT_VIDEO_01]
```

Esto convierte el guion en una lista de instrucciones para ensamblar.

## Fase 4: narración modular

Genera la narración por secciones:

```text
01_Hook.wav
02_Context.wav
03_Concept_A.wav
04_Example.wav
05_Concept_B.wav
06_Conclusion.wav
07_CTA.wav
```

ElevenLabs permite trabajar con proyectos y líneas de tiempo que integran narración, vídeo, subtítulos, música y efectos, y ajustar el timing a nivel de frases. ([ElevenLabs](https://elevenlabs.io/docs/eleven-creative/audio-tools/voiceover-studio?utm_source=chatgpt.com "Voiceover studio | ElevenLabs Documentation"))

No generaría cada oración como archivo independiente porque terminarías con demasiados archivos. Una sección narrativa coherente por archivo suele ser más manejable.

## Fase 5: ensamblaje

1. Duplica el proyecto maestro.
    
2. Importa la narración.
    
3. Coloca marcadores donde cambia la idea.
    
4. Asigna un módulo a cada marcador.
    
5. Sustituye textos, datos e imágenes.
    
6. Añade B-roll solo donde ayude.
    
7. Ajusta efectos sonoros.
    
8. Añade música al final.
    
9. Revisa el ritmo sin sonido.
    
10. Revisa la claridad escuchando únicamente el audio.
    

## Fase 6: reciclaje controlado

Después de publicar:

- identifica los módulos usados;
    
- registra la retención de esa sección;
    
- anota si el hook funcionó;
    
- crea una nueva versión de los mejores;
    
- retira los que generan monotonía o confusión.
    

Hoja de control:

|Módulo|Usos|Retención|Resultado|Acción|
|---|--:|--:|---|---|
|Hook contrarian 02|4|Alta|Bueno|Crear v2|
|Timeline 01|7|Media|Neutral|Mantener|
|CTA subscribe 01|5|Baja|Débil|Reescribir|

No atribuyas toda la retención al gráfico: también influyen el tema, la frase, la posición y la promesa. Utiliza estos datos como indicios, no como causalidad definitiva.

---

# CapCut o DaVinci: decisión práctica

## Elige CapCut cuando:

- todavía estás aprendiendo edición;
    
- trabajas solo;
    
- quieres publicar cuanto antes;
    
- necesitas subtítulos y texto cinético rápidamente;
    
- todavía no sabes qué estilo funcionará.
    

CapCut puede centralizar recursos de marca y plantillas, facilitando consistencia y colaboración. ([CapCut](https://www.capcut.com/help/benefits-of-capcut-teams?utm_source=chatgpt.com "What are the Benefits of CapCut Teams?"))

## Elige DaVinci cuando:

- planeas producir decenas o cientos de vídeos;
    
- quieres gráficos verdaderamente editables;
    
- necesitas automatizar composiciones;
    
- quieres controlar mejor audio y color;
    
- puedes invertir tiempo inicial en aprender Fusion.
    

## Mi recomendación concreta

```text
Primeros 15-20 vídeos:
CapCut Desktop

Mientras validas:
Construye una biblioteca simple de proyectos duplicables

Cuando identifiques módulos ganadores:
Recréelos como macros o plantillas en DaVinci Resolve
```

No deberías dedicar varias semanas a construir una infraestructura perfecta antes de publicar. Construye el sistema mientras produces.

# Regla final

Reutiliza:

- diseño;
    
- animación;
    
- estructura;
    
- tipografía;
    
- sonidos;
    
- lógica narrativa.
    

Cambia en cada vídeo:

- afirmación;
    
- datos;
    
- ejemplos;
    
- pregunta;
    
- argumento;
    
- evidencia;
    
- conclusión.
    

En una frase:

> **El contenedor debe ser modular; el contenido debe seguir siendo específico y original.**