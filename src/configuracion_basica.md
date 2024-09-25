# Configuración Basica

# Router
```
Router> enable
Router# configure terminal
```
#### Hostname
```
Router (config)# hostname <nombre_del_equipo>
```
#### Contraseñas
```
Router (config)# line vty <linea_de_inicio:int(0, 15)> <linea_de_fin:int(0, 15)>
Router (config-line)# password <contraseña_del_vty>
Router (config-line)# login
Router (config-line)# exit

Router (config)# line console 0
Router (config-line)# password <contraseña_de_la_consola>
Router (config-line)# login
Router (config-line)# exit

Router (config)# enable password/secret enable
Router (config)# service password encription
```
#### Mensaje del día
```
Router (config)# banner motd #Estoy en el Router#
```
#### Configuración de interfaces
```
Router (config)# interface <puerto_a_configurar>
Router (config)# ip address <ip> <mascara_de_subred>
Router (config)# no shutdown
```
#### Guardar la configuracion y reiniciar
```
Router (config)# end
Router# copy running-config startup-config
Router# reload
```

# Switch
```
Switch> enable
Switch# configure terminal
```
#### Hostname
```
Switch (config)# hostname <nombre_del_equipo>
```
#### Contraseñas
```
Switch (config)# line vty <linea_de_inicio:int(0, 15)> <linea_de_fin:int(0, 15)>
Switch (config-line)# password <contraseña_del_vty>
Switch (config-line)# login
Switch (config-line)# exit

Switch (config)# line console 0
Switch (config-line)# password <contraseña_de_la_consola>
Switch (config-line)# login
Switch (config-line)# exit

Switch (config)# enable password/secret enable
```
#### Mensaje del día
```
Switch (config)# banner motd #Estoy en el Switch#
```
#### Configuración de vlan
```
Switch (config)# interface vlan1
Switch (config)# ip address <ip> <mascara_de_subred>
Switch (config)# no shutdown
```
#### Configurar la puerta de enlace del switch
```
Switch (config)# ip default-gateway <ip_del_router>
```
#### Guardar la configuracion y reiniciar
```
Switch (config)# end
Switch# copy running-config startup-config
Switch# reload
```
