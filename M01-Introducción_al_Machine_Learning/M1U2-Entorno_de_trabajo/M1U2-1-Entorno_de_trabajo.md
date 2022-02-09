# Entorno de trabajo
M1U2 - Ejercicio 1

## ¿Qué vamos a hacer?
- (Opcional) Crear una instancia de VM local
- Instalar JupyterLab y las librerías de Python en nuestro entorno de trabajo
- Resolución de problemas

Recuerda seguir las instrucciones para las entregas de prácticas indicadas en [Instrucciones entregas](https://github.com/Tokio-School/Machine-Learning/blob/main/Instrucciones%20entregas.md).

## Instrucciones
Estas instrucciones te mostrarán cómo instalar una máquina virtual localmente para completar los ejercicios de este curso y a JupyterLab y las librerías numéricas de Python necesarias.

No es necesario crear una VM local para realizar los ejercicios, es sólo una opción más. Otras opciones disponibles son:
- Google Colaboratory
- Crear un entorno virtual en tu SO Linux/Mac
- Usar Windows Subsystem for Linux
- Usar Vertex AI Workbench de Google Cloud Platform, o cualquier otro servicio en la nube similar.
- Crear una VM en la nube o en una infraestructura remota similar.

Recomendamos utilizar:
- Google Colaboratory
- Si utilizas Windows: WSL con Ubuntu
- Si utilizas Linux/macOS: entorno virtual de Python
- Crear una VM local

### Crear una VM local (opcional)

Para crear una VM local tenemos varias opciones, según nuestro sistema operativo: Oracle VM VirtualBox, Vagrant, QEMU, entornos propios de Windows Professional Edition y MacOs, etc.

Si no estás familiarizado con el uso de VMs, por simpleza, recomendamos que utilices VirtualBox.

Para ello, sigue las instrucciones de instalación del software de virtualización escogido para tu sistema operativo. P. ej., para VirtualBox: www.virtualbox.com

#### Descargar Ubuntu

Como sistema operativo para el curso vamos a escoger Ubuntu, principalmente por simpleza. Si tienes suficiente manejo en cualquier otra distribución de Linux que soporte las librerías de Python a utilizar, puedes utilizar otra distribución o incluso SO, aunque no te podremos dar soporte para resolver problemas con el entorno de trabajo.

Descarga Ubuntu Desktop para tu arquitectura: [descarga Ubuntu Desktop](https://ubuntu.com/download/desktop)

#### Crear la VM

Ahora sigue las instrucciones de tu software de virtualización para crear una VM con dicha imagen de Ubuntu Desktop. P. ej. para VirtualBox: [Crear tu primera VM](https://www.virtualbox.org/manual/UserManual.html#gui-createvm).

Crea una VM con suficiente capacidad, según los recursos disponibles en tu PC. Se recomienda una VM de, al menos, 8 GB de memoria y unos 20-30 GB en disco. Según el software de virtualización, los recursos de la VM se pueden cambiar a posteriori con la VM apagada.

#### Instala Ubuntu en la VM

Enciende la VM por primera vez e instala el SO de Ubuntu Desktop en la misma. Así mismo, busca online e instala cualquier componente adicional de invitado o “guest” en la VM recomendable para tu software de virtualización.

Estos componentes habitualmente nos permiten realizar tareas como conectar dispositivos USB a la VM, importar y exportar archivos desde la VM, y en general soportar funciones que hacen nuestro trabajo más cómodo.

P. ej. para VirtualBox: [Adiciones de anfitrión](https://www.virtualbox.org/manual/ch04.html)

### Entorno de Python

Para este curso, usaremos Python 3 en exclusiva. Ubuntu Desktop versión 20+ usa Python 3 como versión por defecto. Aún así, asegúrate de que ejecutas la versión de Python correcta, usas Pip para Python 3 e instalas librerías para Python 3.

*NOTA:* En Google Colab o Vertex AI Platform ya dispondrás de un entorno con las librerías instaladas.

#### Entorno virtual

Si usamos una VM sólo para este curso, generalmente, no deberíamos tener problemas de conflictos de versiones, al no usarla para otras aplicaciones.

Puesto que añade una cierta complejidad añadida al curso, este paso es opcional. Sin embargo, si tienes suficiente soltura con entornos virtuales para Python, puedes utilizarlos. Algunas opciones son:
- Pipenv: [docs](https://pipenv-fork.readthedocs.io/en/latest/), [guía](https://realpython.com/pipenv-guide/)
- Venv: [docs](https://docs.python.org/3/library/venv.html), [guía](https://realpython.com/python-virtual-environments-a-primer/#using-virtual-environments) (ojo a la nota: para Python 3 usa “venv”, para Python 2 instala “virtualenv”)

#### Actualizar listado de dependencias

Asegúrate de que el listado de dependencias local está actualizado con el comando `sudo apt update` antes de comenzar a usar el entorno.

#### Pip

Como gestor de paquetes de Python, usaremos Pip, que viene ya por defecto instalado con Ubuntu. En algunos entornos, podemos usar los comandos `python` y `pip` en lugar de `python3` y `pip3`. 

Si has utilizado un entorno donde su versión de Python por defecto es Python 2, asegúrate siempre de usar los comandos adecuados. En Ubuntu Desktop 20+, debemos usar `python3` y `pip3`.

Los comandos habituales son:
- Instalar: `sudo apt-get install python3-pip`
- Comprobar la versión: `pip3 --version`
- Actualizar Pip (no suele ser necesario): `pip3 install --upgrade pip` (puede ser necesario añadir `sudo -H` al inicio)
- Instalar módulos de Python: `pip3 install nombre_del_modulo`
- Actualizar módulos de Python: `pip3 install --upgrade nombre_del_modulo`
- Comprobar módulos instalados y sus versiones: `pip3 freeze` o `pip3 freeze | grep nombre_del_modulo`

#### Instalar las librerías necesarias

Instalaremos las librerías Numpy, Matplotlib, Scikit-learn y JupyterLab:

```pip3 install numpy matplotlib scikit-learn jupyter jupyterlab```

Si es necesario, podemos encontrar una guía de instalación con diferentes opciones en cada una de las páginas de documentación de dichos proyectos.

#### JupyterLab

JupyterLab es una extensión de Jupyter, que a su vez es una evolución sobre los cuadernos de IPython. Tienes toda la documentación de JupyterLab disponible en sus [docs](https://jupyterlab.readthedocs.io/en/stable/getting_started/starting.html) online.

Para iniciar JupyterLab en cada sesión, hazlo con el comando `jupyter lab`

PD: En ocasiones deberás reiniciar tu VM o tu sesión en la misma para que reconozca el nuevo comando jupyter por primera vez.

Sigue las instrucciones en tu terminal para conectarte a la extensión de JupyterLab del servidor de Jupyter iniciado, que estará en la localización `http(s)://<server:port>/<lab-location>/lab`

Al terminar la sesión de trabajo, simplemente apaga el servidor Jupyter volviendo a la terminal con las teclas `CTRL + C`.

Para instalar extensiones de JupyterLab, sigue las instrucciones de la documentación: [JupyterLab extensions](https://jupyterlab.readthedocs.io/en/stable/user/extensions.html)

#### Posibles problemas

Ante cualquier posible problema, lo mejor es que te pongas en contacto con el profesor a través de un mensaje en la plataforma.
Estaremos más que encantados de ayudarte a solucionarlo cuanto antes.

## Entregables

Envía una captura de pantalla en formato de imagen con tu entorno de JupyterLab listo para usar 😀.
