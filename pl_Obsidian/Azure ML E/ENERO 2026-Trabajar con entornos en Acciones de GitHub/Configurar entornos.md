
---
# error kernel
El mensaje que ves en el Visor de eventos (o en la pantalla azul/negra) es un **BSOD (Blue Screen of Death)** clásico de Windows:

**Bug Check 0x0000007F: UNEXPECTED_KERNEL_MODE_TRAP**  
Con parámetros:  
- **0x0000000000000008** (esto es clave)  
- 0xfffff802365fae70  
- 0xfffff802365ea1f0  
- 0xfffff8024ef00f6f  

El volcado se guardó en **C:\WINDOWS\Minidump\013026-16375-01.dmp** (del 30 de enero 2026, como indica el nombre del archivo).

### ¿Qué significa exactamente este error?
- **0x7F** indica que el **CPU Intel generó una "trampa" (trap/exception)** en modo kernel que Windows no pudo manejar o capturar correctamente.
- El **primer parámetro 0x8** (0x0000000000000008) corresponde a **EXCEPTION_DOUBLE_FAULT** (doble fallo o double fault).  
  Esto es grave: significa que ocurrió un error (fault) mientras el CPU ya estaba manejando **otro error anterior**. El kernel no puede recuperarse de esto y el sistema se reinicia forzosamente.

Causas más comunes (en orden de probabilidad en tu caso: laptop Lenovo LOQ 15IAX9 con Intel Core i5 + NVIDIA RTX, crash jugando Warzone):
1. **Problemas de hardware, especialmente RAM (memoria)** → La causa #1 en casi todos los casos documentados de 0x7F con parámetro 0x8. RAM defectuosa, mal asentada, incompatible o con overclock/XMP activado inestable.
2. **Stack overflow en kernel** (desbordamiento de pila) → Múltiples drivers "enganchados" en la misma pila (común con drivers gráficos NVIDIA + Intel híbrido en laptops gaming), o drivers corruptos/buggy.
3. **Drivers defectuosos o inestables** → Especialmente NVIDIA (nvlddmkm.sys), pero también WiFi (Intel), chipset, o incluso antivirus/seguridad. En laptops Lenovo LOQ, los drivers híbridos (Optimus/Advanced Optimus) a veces causan esto bajo carga pesada como Warzone.
4. **Sobrecalentamiento o throttling extremo** → CPU/GPU se pone en estado inestable, genera faults en cadena.
5. **Menos común**: BIOS desactualizado, CPU defectuoso, o corrupción de archivos del sistema.

En gaming con NVIDIA + Intel (como tu setup), este error aparece frecuentemente por conflictos de drivers o RAM inestable bajo estrés (Warzone es muy exigente en CPU/RAM/GPU).

### Pasos para diagnosticar y solucionar (en orden prioritario)
1. **Chequea y prueba la RAM (lo más probable)**:
   - Ejecuta **Windows Memory Diagnostic** (busca "Diagnóstico de memoria de Windows" → reinicia y prueba).
   - O descarga **MemTest86** (gratuito, booteable desde USB) → corre al menos 4-8 pases completos (puede tardar horas). Si detecta errores → RAM defectuosa → quita módulos uno por uno para identificar cuál falla, o reemplaza.
   - En BIOS (presiona F2 o Fn+F2 al encender): **desactiva XMP/DOCP** si está activado (perfil de overclock RAM). Prueba con velocidades stock (ej: 4800MHz o lo que sea default).

2. **Analiza el minidump para confirmar el driver culpable**:
   - Descarga **BlueScreenView** (de nirsoft.net, portátil y gratis).
   - Abre la carpeta **C:\Windows\Minidump** → selecciona el archivo 013026-16375-01.dmp.
   - Mira la sección inferior: te dirá el driver/module responsable (ej: nvlddmkm.sys = NVIDIA, ntoskrnl.exe = genérico/kernel, hal.dll, etc.).
   - Si es NVIDIA → ve al paso 3.
   - Pega aquí la info de BlueScreenView (o captura) para ayudarte más preciso.

3. **Limpia e instala drivers NVIDIA limpios** (muy común en LOQ):
   - Descarga **DDU (Display Driver Uninstaller)** → ejecútalo en Modo Seguro (presiona F8 o Shift+Reinicio → Solucionar problemas → Opciones avanzadas → Configuración de inicio → Modo Seguro).
   - Borra drivers NVIDIA + Intel gráficos.
   - Reinicia normal → ve a **support.lenovo.com** → busca "LOQ 15IAX9" exacto → Drivers → Graphics → descarga la versión más reciente certificada por Lenovo (no uses GeForce Experience directo, evita conflictos).
   - Instala → reinicia → prueba Warzone.

4. **Otras comprobaciones rápidas**:
   - Actualiza **BIOS y todos drivers** desde Lenovo Vantage (o sitio web Lenovo). Hay BIOS nuevas que arreglan inestabilidad en estos modelos.
   - En Lenovo Vantage → chequea "Hybrid Mode" o "Advanced Optimus" → prueba desactivarlo (fuerza solo NVIDIA o solo Intel) para ver si estabiliza.
   - Monitorea temps/FPS con MSI Afterburner + HWMonitor: GPU/CPU no deben pasar 90-95°C sostenido. Limpia polvo/ventiladores si es necesario.
   - Ejecuta **sfc /scannow** y **DISM /Online /Cleanup-Image /RestoreHealth** en CMD admin para reparar archivos corruptos.
   - Desactiva temporalmente **Core Isolation / Memory Integrity** en Windows Security → Device Security (a veces causa conflictos con drivers).

Si después de probar RAM y drivers limpios sigue pasando, probablemente sea hardware (RAM o GPU/CPU inestable). En laptops gaming como la tuya, RAM defectuosa es lo más reportado con este exacto 0x7F + 0x8.

Pega lo que te diga BlueScreenView o MemTest86 y seguimos afinando. ¡La mayoría se soluciona con RAM/drivers!
---
---
Para implementar entornos al trabajar con modelos de Machine Learning, puede usar una plataforma como GitHub. Para automatizar las tareas que necesitan ejecutarse en entornos independientes, deberá hacer lo siguiente:

- Configurar los entornos en GitHub.
- Usar los entornos de Acciones de GitHub.
- Agregar aprobaciones para asignar los revisores necesarios.

## Configuración de los entornos en GitHub

Para crear un entorno en el repositorio de GitHub:

1. Vaya a la pestaña **Configuración** del repositorio.
2. Seleccione **Entornos**.
3. Cree un **entorno nuevo**.
4. Escriba un nombre.
5. Seleccione **Configure environment** (Configurar el entorno).

Para asociar un entorno a un área de trabajo de Azure Machine Learning específica, puede crear un **secreto de entorno** para proporcionar acceso al entorno únicamente a un área de trabajo de Azure Machine Learning.

 Nota:

Para conceder a GitHub acceso a cualquier área de trabajo de Azure Machine Learning, debe crear una entidad de servicio en Azure. Después, debe proporcionar acceso al área de trabajo de Azure Machine Learning en Azure a la entidad de servicio. Aprenda la [Integración de Azure Machine Learning con herramientas de DevOps como GitHub](https://learn.microsoft.com/es-es/training/modules/introduction-development-operations-principles-for-machine-learn/4-integrate-azure-development-operations-tools).

Puede crear un secreto en el repositorio para almacenar las credenciales de la entidad de servicio. Al trabajar con entornos, querrá crear un secreto de entorno en su lugar para definir qué entorno específico de GitHub debe tener acceso al área de trabajo de Azure Machine Learning.

Para crear un secreto de entorno, vaya a la pestaña **Entornos** de la pestaña **Configuración**.

1. Vaya al nuevo entorno.
2. Vaya a la sección **Environment secrets** (Secretos de entorno).

![Captura de pantalla de la configuración de un entorno en GitHub.](https://learn.microsoft.com/es-es/training/wwl-data-ai/work-environments-github-actions/media/04-01-settings.png)

3. Agregue un nuevo secreto.
4. Escriba `AZURE_CREDENTIALS` para el nombre.
5. Escriba las credenciales de la entidad de servicio en el campo de valor.

## Uso de entornos en Acciones de GitHub y adición de aprobaciones

Después de crear entornos en el repositorio de GitHub, puede hacer referencia al entorno desde los flujos de trabajo de Acciones de GitHub. Siempre que quiera agregar una comprobación manual entre entornos, puede agregar **aprobaciones**.

Por ejemplo, siempre que desencadene un trabajo de Azure Machine Learning en el flujo de trabajo de Acciones de GitHub, la tarea se puede ejecutar correctamente en el flujo de trabajo. Pero, puede ser que durante el entrenamiento del modelo en el área de trabajo de Azure Machine Learning, se produzca un error debido a un problema con el script de entrenamiento. O después del entrenamiento del modelo, al evaluar las métricas del modelo, puede decidir que necesita volver a entrenar el modelo en lugar de implementarlo.

Para darle la oportunidad de revisar el resultado del entrenamiento del modelo en el área de trabajo de Azure Machine Learning, puede agregar una aprobación para un entorno. Siempre que un flujo de trabajo de Acciones de GitHub quiera ejecutar una tarea en un entorno específico, se notificará a los revisores necesarios y deberá aprobar las tareas antes de que se ejecuten.

 Sugerencia

Obtenga más información sobre [cómo usar entornos en Acciones de GitHub y cómo agregar aprobaciones](https://learn.microsoft.com/es-es/training/modules/continuous-deployment-for-machine-learning/).

---
---
# Siga estas instrucciones para completar el desafío:

- Vea el [repositorio de desafíos en GitHub](https://microsoftlearning.github.io/mslearn-mlops/).
- Complete el desafío 5: trabajar con entornos.