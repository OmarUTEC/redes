# Cmandos básicos de redes para configuracion de router y switch

## modos de entrada al CLI

```
>enable
#configure terminal
(config)#
```

## Cambiar hostname
```
#hostname R1
```

## Para guardar
```
#write/copy running-config startup-config (copy run start)

(config)#do write/copy running-config startup-config
```

## Para ejecutar comandos de verificacion (SHOW)
```
#show ...
(config)#do show ...
```

## Crear VLAN 
```
vlan 10
name VLAN10
exit

vlan 20
name VLAN20
exit
```

# Configurar tipo de puerto
## Trunk
```
interface g1/0/1
switchport mode trunk
switchport trunk native vlan 99
```

## Acces
```
interface g1/0/2
switchport mode access
switchport access vlan 99
```

## Configurar IP en Switch
```
interface vlan 10
no shutdown 
ip add 192.168.99.130 255.255.255.240
```

## Configurar Gateway
```
ip default-gateway 192.168.99.129
```

## Comandos de verificación 
```
show running-config (sh run) //mostrar la configuracion
show vlan brief //mostrar la tabla vlan
show ip interface brief (sh ip int brief) //mostrar el estado del puerto y su ip
```

