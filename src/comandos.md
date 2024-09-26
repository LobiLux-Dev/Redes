# Comandos

| **Comando**                            | **Ejemplo**                            | **Tipo de Usuario**   |
| -------------------------------------- | -------------------------------------- | --------------------- |
| **?**                                  | `?`                                    | `>`, `#`, `(config)#` |
| **banner motd**                        | `banner motd #Acceso Restringido#`     | `(config)#`           |
| **configure terminal**                 | `configure terminal`                   | `#`                   |
| **copy running-config startup-config** | `copy running-config startup-config`   | `#`                   |
| **description**                        | `description Conexión a servidor`      | `(config)#`           |
| **do**                                 | `do show running-config`               | `(config)#`           |
| **enable password**                    | `enable password contraseña_simple`    | `(config)#`           |
| **enable secret**                      | `enable secret contraseña_segura`      | `(config)#`           |
| **enable**                             | `enable`                               | `>`                   |
| **exit**                               | `exit`                                 | `>`, `#`, `(config)#` |
| **hostname**                           | `hostname Switch01`                    | `(config)#`           |
| **interface**                          | `interface FastEthernet 0/1`           | `(config)#`           |
| **ip address**                         | `ip address 192.168.1.1 255.255.255.0` | `(config)#`           |
| **line console**                       | `line console 0`                       | `(config)#`           |
| **line vty**                           | `line vty 0 4`                         | `(config)#`           |
| **login**                              | `login`                                | `(config)#`           |
| **no shutdown**                        | `no shutdown`                          | `(config)#`           |
| **password**                           | `password contraseña_simple`           | `(config)#`           |
| **reload**                             | `reload`                               | `#`                   |
| **service password-encryption**        | `service password-encryption`          | `(config)#`           |
| **show running-config**                | `show running-config`                  | `#`                   |
| **shutdown**                           | `shutdown`                             | `(config)#`           |

## Descripción de los Comandos

- **`?`**:
  Muestra una lista de los comandos disponibles en el modo actual.

- **`banner motd`**:
  Configura un mensaje de advertencia o bienvenida que se muestra a todos los usuarios al conectarse al dispositivo. Se puede utilizar cualquier símbolo como delimitador de inicio y de fin para el mensaje.

  - **Parámetros**:
    - `mensaje`: Texto que se mostrará como mensaje de bienvenida.

- **`configure terminal`**:
  Accede al modo de configuración global para modificar la configuración del dispositivo.

  - **Abreviación**: `conf t`

- **`copy running-config startup-config`**:
  Guarda la configuración actual en la memoria de inicio, asegurando que persista después de un reinicio.

  - **Abreviación**: `copy run start`

- **`description`**:
  Añade una descripción a la interfaz para facilitar la identificación de su propósito.

  - **Abreviación**: `desc`
  - **Parámetros**:
    - `texto_descripción`: Texto que describe la función de la interfaz.

- **`do`**:
  Permite ejecutar comandos de nivel privilegiado desde el modo de configuración global.

  - **Parámetros**:
    - `comando`: Comando que deseas ejecutar.

- **`enable`**:
  Cambia al modo privilegiado, donde se pueden ejecutar comandos de administración avanzada.

  - **Abreviación**: `en`

- **`enable password`**:
  Configura una contraseña simple para acceder al modo privilegiado del dispositivo.

  - **Parámetros**:
    - `contraseña`: La contraseña que se establecerá.

- **`enable secret`**:
  Establece una contraseña cifrada para acceder al modo privilegiado del dispositivo.

  - **Parámetros**:
    - `contraseña`: La contraseña cifrada que se utilizará.

- **`exit`**:
  Sale del modo actual, ya sea de configuración de interfaz o global.

- **`hostname`**:
  Cambia el nombre del dispositivo.

  - **Parámetros**:
    - `nombre_del_dispositivo`: El nuevo nombre que se asignará al dispositivo.

- **`interface`**:
  Entra en el modo de configuración de una interfaz específica, como un puerto físico.

  - **Abreviación**: `int`
  - **Parámetros**:
    - `tipo_interfaz número_interfaz`: Especifica el tipo y número de la interfaz a configurar.

- **`ip address`**:
  Asigna una dirección IP a la interfaz seleccionada.

  - **Abreviación**: `ip add`
  - **Parámetros**:
    - `ip_dirección máscara_subred`: La dirección IP y la máscara de subred que se asignarán.

- **`line console`**:
  Configura la línea de consola física para establecer una contraseña de acceso.

  - **Parámetros**:
    - `número_línea`: El número de línea de consola que se configurará (siempre 0).

- **`line vty`**:
  Configura las líneas de acceso virtual (VTY) utilizadas para conexiones remotas, como Telnet o SSH.

  - **Abreviación**: `line`
  - **Parámetros**:
    - `rango_línea`: Especifica el rango de líneas VTY que se configuran para acceso remoto, que puede ir desde `0` hasta `15`, admitiendo un total de 16 líneas. Ejemplo: `0 4` para configurar las primeras cinco líneas VTY.

- **`login`**:
  Habilita el requerimiento de contraseña para las conexiones de consola o VTY.

- **`no shutdown`**:
  Activa una interfaz que estaba deshabilitada.

  - **Abreviación**: `no shut`

- **`password`**:
  Establece una contraseña simple para el acceso a las líneas VTY o la consola física.

  - **Parámetros**:
    - `contraseña`: La contraseña que se establecerá para acceso.

- **`reload`**:
  Reinicia el dispositivo.

- **`service password-encryption`**:
  Encripta las contraseñas en la configuración del dispositivo para mejorar la seguridad.

- **`show running-config`**:
  Muestra la configuración actual en ejecución del dispositivo.

  - **Abreviación**: `show run`

- **`shutdown`**:
  Deshabilita una interfaz de red.
  - **Abreviación**: `shut`
