# Modos

1. **Modo usuario (User EXEC mode)**:
    
    - **Símbolo**: `>`
    - **Descripción**: Es el modo más básico de un router o switch, al cual se entra al iniciar sesión. En este modo solo tienes acceso a comandos de monitoreo y visualización de estado del dispositivo. No puedes hacer configuraciones.
    - **Ejemplo de prompt**: `Router>`
2. **Modo privilegiado (Privileged EXEC mode)**:
    
    - **Símbolo**: `#`
    - **Descripción**: Desde este modo tienes acceso a todos los comandos de visualización, además de poder acceder al modo de configuración. Puedes entrar al modo privilegiado desde el modo usuario con el comando `enable`.
    - **Ejemplo de prompt**: `Router#`
3. **Modo de configuración global (Global configuration mode)**:
    
    - **Símbolo**: `#`, pero el prompt cambia para reflejar que estás en configuración.
    - **Descripción**: Permite realizar configuraciones a nivel global del dispositivo (interfaces, routing, etc.). Se accede escribiendo `configure terminal` desde el modo privilegiado.
    - **Ejemplo de prompt**: `Router(config)#`
4. **Modos de configuración específicos (sub-config modes)**:
    
    - **Símbolo**: `#` con detalles adicionales en el prompt.
    - **Descripción**: Existen varios submodos dentro de la configuración global, por ejemplo:
        - **Configuración de interfaces**: `Router(config-if)#`
        - **Configuración de líneas de consola o vty (telnet/SSH)**: `Router(config-line)#`
        - **Configuración de routing o protocolos**: `Router(config-router)#`

### Resumen de los símbolos:

- `>`: Modo usuario (User EXEC)
- `#`: Modo privilegiado (Privileged EXEC)
- `#` con `config`: Modo de configuración global y submodos de configuración.
