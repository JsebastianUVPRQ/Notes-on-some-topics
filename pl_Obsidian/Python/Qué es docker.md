Antes de comenzar nuestro paseo introductorio por los contenedores de Docker, echemos un vistazo a cómo nuestro equipo desarrolla e implementa las aplicaciones. También se describirán brevemente algunos de los desafíos a los que se enfrentan nuestros equipos.

El proceso de desarrollo y administración de aplicaciones de su empresa normalmente incluye uno o más equipos. Hay un equipo de desarrollo que crea el software y un equipo de operaciones responsable de la implementación de estas aplicaciones. El equipo de operaciones también es responsable de la administración de la infraestructura de hospedaje de las aplicaciones.

Por ejemplo, imagine que se va a desarrollar un portal de seguimiento de pedidos que usarán las tiendas de la empresa. Varios entornos hospedan nuestras aplicaciones durante su proceso de desarrollo y de publicación. En primer lugar, el equipo de desarrollo crea y prueba el software en un entorno de desarrollo. Después, el software se implementa en un entorno de control de calidad (QA), luego pasa a un entorno de preproducción y a un entorno de producción final.

Hay varios desafíos que se deben tener en cuenta en el escenario anterior:

- **Administración de entornos de hospedaje**
    
    Todos los distintos entornos requieren una administración de software y hardware. Tenemos que asegurarnos de que el software instalado y el hardware configurado en cada uno de ellos son los mismos. También necesitamos configurar aspectos como el acceso a la red, el almacenamiento de datos y la seguridad por entorno de una manera coherente y fácil de reproducir.
    
- **Continuidad en la entrega de software**
    
    La implementación de aplicaciones en los entornos se debe realizar de forma coherente. Cada paquete de implementación debe incluir todos los paquetes de sistema, archivos binarios, bibliotecas, archivos de configuración y otros elementos que garantizan que la aplicación será totalmente funcional. También tenemos que asegurarnos de que todas estas dependencias coinciden con las versiones de software y la arquitectura.
    
- **Uso eficaz del hardware**
    
    Cada aplicación implementada debe ejecutarse de tal forma que esté aislada de otras aplicaciones que se ejecutan en el mismo hardware. Nos esforzamos por ejecutar varias aplicaciones en cada servidor para aprovechar al máximo los recursos sin ponerlas en peligro.
    
- **Portabilidad de las aplicaciones**
    
    Hay varias razones por las que la portabilidad de la aplicación es tan importante. Podría producirse un error en un entorno de hospedaje o podría ser necesario escalar horizontalmente la aplicación. En ambos casos, el resultado potencial es una nueva implementación del software en un entorno nuevo. Debemos mover el software de un host a otro incluso si la infraestructura subyacente es diferente. Este cambio debe llevarse a cabo lo más rápido posible para reducir el tiempo de inactividad para nuestros clientes.
    

Antes de explorar las características de Docker que ayudan a resolver estos desafíos, analizaremos algunos conceptos y veremos una breve descripción de la arquitectura de Docker.

## ¿Qué es un contenedor?

Un contenedor es un entorno aislado de forma flexible que nos permite compilar y ejecutar paquetes de software. Estos paquetes de software incluyen el código y todas las dependencias para ejecutar aplicaciones de forma rápida y fiable en cualquier entorno informático. Llamamos a estos paquetes _imágenes de contenedor_.

La imagen de contenedor es la unidad que usamos para distribuir nuestras aplicaciones.

## ¿Qué es la creación de contenedores de software?

La contenedorización de software es un método de virtualización del sistema operativo que se usa para implementar y ejecutar contenedores sin utilizar una máquina virtual (VM). Los contenedores se pueden ejecutar en hardware físico, en la nube, en máquinas virtuales y en diferentes sistemas operativos.

## ¿Qué es Docker?

Docker es una plataforma de creación de contenedores que se usa para desarrollar, distribuir y ejecutar contenedores. Docker no usa un hipervisor y se puede ejecutar en equipos de escritorio o en portátiles para desarrollar y probar las aplicaciones. La versión de escritorio de Docker es compatible con Linux, Windows y macOS. En el caso de los sistemas de producción, Docker está disponible para entornos de servidor, incluidos muchas variantes de Linux, Microsoft Windows Server 2016 y versiones posteriores. Muchas nubes, incluida la nube de Azure, son compatibles con Docker.

## Arquitectura de Docker

La plataforma Docker consta de varios componentes que usamos para desarrollar, ejecutar y administrar nuestras aplicaciones en contenedores.

### Motor de Docker

El motor de Docker está formado por varios componentes configurados como una implementación de cliente y servidor en la que ambos se ejecutan simultáneamente en el mismo host. El cliente se comunica con el servidor mediante una API REST, la cual le permite comunicarse también con una instancia del servidor remoto.

![Diagrama en el que se muestra información general de la arquitectura de Docker.](https://learn.microsoft.com/es-es/training/modules/intro-to-docker-containers/media/2-docker-architecture.svg)

Algunas flechas muestran la comunicación entre el servidor de Docker, los contenedores en ejecución y las imágenes de contenedor almacenadas. Estas flechas indican cómo el servidor de Docker carga imágenes de contenedor almacenadas y administra contenedores en ejecución.

#### El cliente Docker

Hay dos alternativas para el cliente de Docker: Una aplicación de la línea de comandos denominada `docker` o una aplicación basada en la interfaz gráfica de usuario (GUI), denominada Docker Desktop. Tanto la CLI como Docker Desktop interactúan con un servidor de Docker. Los comandos `docker` de la CLI o Docker Desktop usan la API REST de Docker para enviar instrucciones a un servidor local o remoto, y funcionan como la interfaz principal que se usa para administrar los contenedores.

#### El servidor de Docker

El servidor de Docker es un demonio denominado `dockerd`. El demonio `dockerd` responde a las solicitudes del cliente a través de la API de REST de Docker y puede interactuar con otros demonios. El servidor de Docker también es responsable de realizar un seguimiento del ciclo de vida de nuestros contenedores.

#### Objetos de Docker

Hay varios objetos que creará y configurará para admitir las implementaciones de contenedores. Estos incluyen redes, volúmenes de almacenamiento, complementos y otros objetos de servicio. Aquí no trataremos todos estos objetos, pero es conveniente tener en cuenta que son elementos que se pueden crear e implementar según sea necesario.

### Docker Hub

Docker Hub es un registro de contenedores de Docker de software como servicio (SaaS). Los registros de Docker son repositorios que se usan para almacenar y distribuir las imágenes de contenedor que se crean. Docker Hub es el registro público predeterminado que usa Docker para administrar las imágenes.

Tenga en cuenta que puede crear y usar un registro de Docker privado o usar una de las muchas opciones disponibles de los proveedores de servicios en la nube. Por ejemplo, puede usar Azure Container Registry para almacenar imágenes de contenedor que se usarán en varios servicios habilitados para contenedores de Azure.