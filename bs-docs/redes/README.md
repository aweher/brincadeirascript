# 🌐 Configuración de Redes en BrincadeiraScript

## Introducción

¡Bienvenido al mundo de las redes en BrincadeiraScript! 🎉 Aquí aprenderás a configurar y gestionar redes de manera divertida y eficiente.

## Routers Soportados

- BrincadeiraRouter Pro X1
- BrincadeiraRouter Lite
- BrincadeiraRouter Enterprise

## Switches Soportados

- BrincadeiraSwitch 24P
- BrincadeiraSwitch 48P
- BrincadeiraSwitch PoE

## Protocolos de Enrutamiento

### OSPF
```brincadeira
# Configurar OSPF
importar "gracioso.network"

router = gracioso.network.Router({
    "hostname": "router-sonrisa",
    "area": 0,
    "interfaces": ["eth0", "eth1"]
})

router.configurar_ospf({
    "process_id": 1,
    "area": 0,
    "redes": ["192.168.1.0/24", "10.0.0.0/8"]
})
```

### BGP
```brincadeira
# Configurar BGP
router.configurar_bgp({
    "as": 65000,
    "vecinos": [
        {"ip": "192.168.1.2", "as": 65001},
        {"ip": "10.0.0.2", "as": 65002}
    ]
})
```

## Seguridad

### ACLs
```brincadeira
# Configurar ACL
router.configurar_acl({
    "nombre": "sonrisa-acl",
    "reglas": [
        {"accion": "permitir", "origen": "192.168.1.0/24", "destino": "any"},
        {"accion": "denegar", "origen": "any", "destino": "any"}
    ]
})
```

### VPN
```brincadeira
# Configurar VPN
router.configurar_vpn({
    "tipo": "ipsec",
    "fase1": {
        "encriptacion": "aes-256",
        "hash": "sha256",
        "dh": 14
    },
    "fase2": {
        "encriptacion": "aes-128",
        "hash": "sha1"
    }
})
```

## VLANs

### Configuración Básica
```brincadeira
# Crear VLANs
switch = gracioso.network.Switch({
    "hostname": "switch-sonrisa",
    "puertos": 48
})

switch.crear_vlan({
    "id": 10,
    "nombre": "VLAN-Sonrisas",
    "puertos": ["1-12"]
})

switch.crear_vlan({
    "id": 20,
    "nombre": "VLAN-Diversion",
    "puertos": ["13-24"]
})

switch.crear_vlan({
    "id": 30,
    "nombre": "VLAN-Fiesta",
    "puertos": ["25-36"]
})
```

### Trunking
```brincadeira
# Configurar trunk
switch.configurar_trunk({
    "puerto": "48",
    "vlans": [10, 20, 30],
    "modo": "802.1q"
})
```

## Configuración del Router

### Configuración Inicial
```brincadeira
# Configuración básica
router.configurar({
    "hostname": "router-sonrisa",
    "dominio": "sonrisa.local",
    "timezone": "America/Sao_Paulo",
    "interfaces": {
        "eth0": {
            "ip": "192.168.1.1",
            "mascara": "255.255.255.0"
        },
        "eth1": {
            "ip": "10.0.0.1",
            "mascara": "255.0.0.0"
        }
    }
})
```

### SNMP
```brincadeira
# Configurar SNMP
router.configurar_snmp({
    "comunidad": "sonrisa-public",
    "ubicacion": "Sala de Sonrisas",
    "contacto": "admin@sonrisa.local"
})
```

### Syslog
```brincadeira
# Configurar syslog
router.configurar_syslog({
    "servidor": "192.168.1.100",
    "facilidad": "local7",
    "nivel": "informacion"
})
```

## Configuración del Switch

### Configuración Inicial
```brincadeira
# Configuración básica
switch.configurar({
    "hostname": "switch-sonrisa",
    "dominio": "sonrisa.local",
    "timezone": "America/Sao_Paulo",
    "vlan_management": 10,
    "ip_management": "192.168.1.2"
})
```

### Spanning Tree
```brincadeira
# Configurar STP
switch.configurar_stp({
    "modo": "rapido",
    "prioridad": 4096,
    "costos": {
        "1-24": 100,
        "25-48": 200
    }
})
```

### Port Security
```brincadeira
# Configurar port security
switch.configurar_port_security({
    "puertos": "1-24",
    "max_mac": 2,
    "violacion": "restrict"
})
```

## Monitoreo

### SNMP
```brincadeira
# Configurar monitoreo SNMP
monitor = gracioso.network.Monitor({
    "servidor": "192.168.1.100",
    "comunidad": "sonrisa-public",
    "intervalo": 300
})

monitor.configurar({
    "interfaces": ["eth0", "eth1"],
    "metricas": ["trafico", "errores", "estado"]
})
```

### Syslog
```brincadeira
# Configurar monitoreo syslog
monitor.configurar_syslog({
    "servidor": "192.168.1.100",
    "facilidad": "local7",
    "nivel": "informacion"
})
```

## Mantenimiento

### Backup
```brincadeira
# Configurar backup
router.configurar_backup({
    "servidor": "192.168.1.100",
    "ruta": "/backup/router-sonrisa",
    "intervalo": "diario"
})
```

### Actualizaciones
```brincadeira
# Configurar actualizaciones
router.configurar_actualizaciones({
    "servidor": "192.168.1.100",
    "ruta": "/firmware",
    "intervalo": "mensual"
})
```

## Siguiente Paso

¿Quieres ver ejemplos prácticos de configuración de redes o aprender sobre otras características técnicas? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#redes-avancado). 