Configurando mi nueva computadora, me encontré con el desafío de configurar Git y GitHub nuevamente para comenzar a trabajar y desarrollar proyectos en mi repositorio remoto. Este archivo incluye los pasos necesarios para la configuración después de la instalación de Git, desde la creación de nuestra llave pública hasta nuestro primer commit

## Guía de Configuración

Si eres nuevo en el uso de Git y GitHub, sigue estos pasos para comenzar a desarrollar y colaborar en proyectos:

### Instalación de Git

1. Descarga e instala Git desde [sitio web oficial de Git](https://gitforwindows.org/).

### Configuración de Git

1. Abre tu terminal o línea de comandos.
2. Configura tu nombre de usuario global de Git ejecutando el siguiente comando:

`git config --global user.name "Tu Nombre"`

3. Configura tu dirección de correo electrónico global de Git ejecutando el siguiente comando:

`git config --global user.email "tu@email.com"`

### Generación de una Clave SSH

1. Genera un nuevo par de claves SSH ejecutando el siguiente comando:

`ssh-keygen -t ed25519 -C "tu@email.com"`

2. Sigue las instrucciones en pantalla para completar el proceso de generación de claves, cuando te pregunte si deceas colocar una frace de seguridad puedes simplemnte dar enter para no incluir ninguna.

3. Copia el contenido de la clave pública (id_ed25519.pub) y agrégala a tu cuenta de GitHub en la sección "SSH and GPG keys" de la configuración de tu cuenta. Puedes encontrar el contenido de la llave pública rastreando la dirección que hayas colocado en el paso anterior y abriendo el archivo con cualquier editor de texto, copia el contenido del archivo.

    - Para agregar la clave a tu cuenta de GitHub:
        1. Inicia sesión en tu cuenta de GitHub.
        2. Haz clic en tu foto de perfil en la esquina superior derecha y selecciona "Settings" (Configuración) en el menú desplegable.
        3. En la barra lateral izquierda, haz clic en "SSH and GPG keys" (Claves SSH y GPG).
        4. Haz clic en "New SSH key" (Nueva clave SSH).
        5. En el campo "Title" (Título), proporciona un nombre descriptivo para la clave, como el nombre de tu computadora o una descripción que te ayude a identificarla más tarde.
        6. En el campo "Key" (Clave), pega la clave pública SSH que copiaste anteriormente.
        7. En el apartado de Key Type deja seleccionada la opcion Authentication Key. 
        8. Haz clic en "Add SSH key" (Agregar clave SSH) para guardar y agregar la clave a tu cuenta de GitHub.

![Ejemplo de rura](img/Captura%20de%20pantalla%20(3).png)
![Ejemplo de rura](img/Captura%20de%20pantalla%20(4).png)
![Ejemplo de rura](img/Captura%20de%20pantalla%20(5).png)


### Clonación del Repositorio

1. Copia la URL de clonación de tu repositorio desde GitHub.
2. Abre tu terminal o línea de comandos y navega hasta el directorio donde deseas clonar el repositorio.
3. Ejecuta el siguiente comando para clonar el repositorio:

`git clone <URL_del_repositorio>


### Realización del Primer Commit

1. Navega al directorio del repositorio clonado.
2. Realiza tus cambios en los archivos del repositorio.
3. Agrega los cambios al área de preparación de Git ejecutando:`

`git add .`

4. Haz un commit de tus cambios ejecutando:

`git commit -m "First commit"`

5. Envía tus cambios al repositorio remoto en GitHub ejecutando:

`git push origin main`

¡Y eso es todo! Ahora has configurado Git, generado una clave SSH y realizado tu primer commit en el repositorio. ¡Bienvenido al mundo de Git y GitHub!