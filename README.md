
# Repositorio de Scripts Bash para Automatización de Tareas

Este repositorio contiene varios scripts bash diseñados para automatizar tareas en servidores Linux. A continuación se proporciona una descripción detallada de cada script y su propósito.

## Índice

1. [Scripts](#scripts)
    - [multios_websetup.sh](#multios_websetupsh)
    - [webdeploy.sh](#webdeploysh)
    - [remhosts](#remhosts)
    - [testfile.txt](#testfiletxt)
2. [Documentación](#documentación)

## Scripts

### `multios_websetup.sh`

Este script configura un servidor web en sistemas operativos CentOS y Ubuntu. Realiza las siguientes acciones:

1. Verifica si el sistema es CentOS o Ubuntu.
2. Instala los paquetes necesarios (`httpd`, `wget`, `unzip` para CentOS y `apache2`, `wget`, `unzip` para Ubuntu).
3. Inicia y habilita el servicio web correspondiente.
4. Descarga y despliega un artefacto web desde una URL especificada.
5. Limpia los archivos temporales.

#### Uso:

```bash
sudo ./multios_websetup.sh
```

### `webdeploy.sh`

Este script se utiliza para desplegar el script `multios_websetup.sh` en múltiples hosts especificados en el archivo `remhosts`. Realiza las siguientes acciones:

1. Lee la lista de hosts desde el archivo `remhosts`.
2. Copia el script `multios_websetup.sh` a cada host.
3. Ejecuta el script en cada host.
4. Elimina el script del host remoto después de su ejecución.

#### Uso:

```bash
./webdeploy.sh
```

### `remhosts`

Este archivo contiene la lista de hosts remotos donde se desplegará el script `multios_websetup.sh`. Cada host debe estar en una nueva línea.

### `testfile.txt`

Archivo de prueba sin contenido específico.

## Documentación

Para obtener más información sobre los comandos y herramientas utilizados en estos scripts, consulta la documentación oficial:

- [Documentación de `yum`](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/software_management_guide/yum)
- [Documentación de `apt`](https://help.ubuntu.com/lts/serverguide/apt.html)
- [Documentación de `systemctl`](https://www.freedesktop.org/software/systemd/man/systemctl.html)
- [Documentación de `scp`](https://linux.die.net/man/1/scp)
- [Documentación de `ssh`](https://linux.die.net/man/1/ssh)


