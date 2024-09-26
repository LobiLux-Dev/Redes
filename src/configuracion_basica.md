Aquí está el formato final para la configuración de dispositivos Cisco, incluyendo routers y switches:

# Configuración Básica de Dispositivos Cisco (Router y Switch)

## Configuración del Router

### Configuración de Interfaces

1. **Seleccionar la interfaz**:

   - Selecciona la interfaz física del router para asignarle configuraciones específicas.

   ```
   Router (config)# interface <puerto_a_configurar>
   ```

   **Variables:**

   - **`<puerto_a_configurar>`**: La interfaz que se va a configurar. Ejemplo: `GigabitEthernet0/1`.

2. **Asignar dirección IP y máscara de subred**:

   - Asigna una dirección IP y una máscara de subred a la interfaz seleccionada.

   ```
   Router (config)# ip address <ip> <mascara_de_subred>
   ```

   **Variables:**

   - **`<ip>`**: La dirección IP a asignar. Ejemplo: `192.168.1.1`.
   - **`<mascara_de_subred>`**: La máscara de subred. Ejemplo: `255.255.255.0`.

3. **Activar la interfaz**:
   - Habilita la interfaz para que empiece a funcionar.
   ```
   Router (config)# no shutdown
   ```

## Configuración del Switch

### Configuración de VLAN

1. **Seleccionar la interfaz VLAN**:

   - Selecciona la VLAN predeterminada del switch.

   ```
   Switch (config)# interface vlan1
   ```

2. **Asignar dirección IP a la VLAN**:
   - Configura la IP y la máscara de subred para la VLAN.
   ```
   Switch (config)# ip address <ip> <mascara_de_subred>
   Switch (config)# no shutdown
   ```
   **Variables:**
   - **`<ip>`**: La IP de la VLAN. Ejemplo: `192.168.1.2`.
   - **`<mascara_de_subred>`**: La máscara de subred. Ejemplo: `255.255.255.0`.

### Configurar la Puerta de Enlace

- Configura la puerta de enlace predeterminada para que el switch se comunique con redes externas.

```
Switch (config)# ip default-gateway <ip_del_router>
```

**Variables:**

- **`<ip_del_router>`**: IP del router que actúa como puerta de enlace. Ejemplo: `192.168.1.254`.

## Configuración Común para Ambos Dispositivos

### Acceder al Modo de Configuración

1. **Modo privilegiado**:

   - Otorga acceso completo a la configuración.

   ```
   > enable
   ```

2. **Modo de configuración global**:
   - Permite realizar cambios en la configuración del dispositivo.
   ```
   # configure terminal
   ```

### Cambiar el Nombre del Dispositivo (Hostname)

- Cambia el nombre del dispositivo para facilitar su identificación.

```
(config)# hostname <nombre_del_equipo>
```

**Variables:**

- **`<nombre_del_equipo>`**: El nuevo nombre del dispositivo. Ejemplo: `Switch01`, `RouterA`.

### Configuración de Contraseñas

1. **Contraseña para acceso remoto (líneas VTY)**:

   - Configura la contraseña para accesos remotos, como Telnet o SSH.

   ```
   (config)# line vty <linea_de_inicio> <linea_de_fin>
   (config-line)# password <contraseña_del_vty>
   (config-line)# login
   (config-line)# exit
   ```

   **Variables:**

   - **`<linea_de_inicio> <linea_de_fin>`**: El rango de líneas VTY que se configuran para acceso remoto, que puede ir desde `0` hasta `15`, admitiendo un total de 16 líneas. Ejemplo: `0 4` para configurar las primeras cinco líneas VTY.
   - **`<contraseña_del_vty>`**: La contraseña asignada.

2. **Contraseña para acceso por consola**:

   - Define una contraseña para la consola física.

   ```
   (config)# line console 0
   (config-line)# password <contraseña_de_la_consola>
   (config-line)# login
   (config-line)# exit
   ```

   **Variables:**

   - **`<contraseña_de_la_consola>`**: La contraseña para el acceso físico.

3. **Contraseña para el modo privilegiado**:

   - Configura la contraseña para acceder al modo privilegiado. Puedes utilizar una de las dos opciones: `enable password` para establecer una contraseña simple, o `enable secret` para crear una contraseña encriptada, lo que proporciona mayor seguridad.

   **Advertencia**: elige solo una de estas opciones; utilizar ambas simultáneamente puede causar confusiones en la autenticación y anular la efectividad de la configuración.

   ```
   (config)# enable password <contraseña>
   (config)# enable secret <contraseña>
   ```

4. **Cifrar todas las contraseñas**:
   - Cifra todas las contraseñas visibles en el archivo de configuración.
   ```
   (config)# service password-encryption
   ```

### Configurar Mensaje del Día (MOTD)

- Configura un mensaje de advertencia o bienvenida que se muestra a todos los usuarios al conectarse al dispositivo. Se puede utilizar cualquier símbolo como delimitador de inicio y de fin para el mensaje.

```
(config)# banner motd #Este es un mensaje de bienvenida#
```

### Guardar la Configuración y Reiniciar el Dispositivo

1. **Salir del modo de configuración**:

   ```
   (config)# end
   ```

2. **Guardar la configuración**:

   - Guarda la configuración actual.

   ```
   # copy running-config startup-config
   ```

3. **Reiniciar el dispositivo**:
   ```
   # reload
   ```
