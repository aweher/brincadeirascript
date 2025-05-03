# 📋 Políticas de Red en BrincadeiraScript

## Introducción

¡Bienvenido al mundo de las políticas de red en BrincadeiraScript! 🎉 Aquí aprenderás a configurar y gestionar políticas de red de manera divertida y eficiente.

## Políticas Básicas

### Política de Sonrisa
```brincadeira
# Política básica de sonrisa
politica = gracioso.network.Politica({
    "nombre": "sonrisa-basica",
    "condiciones": [
        {"tipo": "paquete", "accion": "permitir"},
        {"tipo": "trafico", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "sonrisa"},
        {"tipo": "priorizar", "valor": "alta"}
    ]
})
```

### Política de Diversión
```brincadeira
# Política de diversión
politica = gracioso.network.Politica({
    "nombre": "diversion-basica",
    "condiciones": [
        {"tipo": "paquete", "accion": "permitir"},
        {"tipo": "trafico", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "diversion"},
        {"tipo": "priorizar", "valor": "media"}
    ]
})
```

### Política de Fiesta
```brincadeira
# Política de fiesta
politica = gracioso.network.Politica({
    "nombre": "fiesta-basica",
    "condiciones": [
        {"tipo": "paquete", "accion": "permitir"},
        {"tipo": "trafico", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "fiesta"},
        {"tipo": "priorizar", "valor": "baja"}
    ]
})
```

## Políticas Avanzadas

### Política de Seguridad
```brincadeira
# Política de seguridad
politica = gracioso.network.Politica({
    "nombre": "seguridad-avanzada",
    "condiciones": [
        {"tipo": "origen", "valor": "192.168.1.0/24", "accion": "permitir"},
        {"tipo": "destino", "valor": "any", "accion": "permitir"},
        {"tipo": "puerto", "valor": "80,443", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "seguro"},
        {"tipo": "priorizar", "valor": "alta"},
        {"tipo": "registrar", "valor": "true"}
    ]
})
```

### Política de QoS
```brincadeira
# Política de QoS
politica = gracioso.network.Politica({
    "nombre": "qos-avanzada",
    "condiciones": [
        {"tipo": "protocolo", "valor": "tcp", "accion": "permitir"},
        {"tipo": "puerto", "valor": "80,443", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "qos"},
        {"tipo": "priorizar", "valor": "alta"},
        {"tipo": "limitar", "valor": "10M"}
    ]
})
```

### Política de Filtrado
```brincadeira
# Política de filtrado
politica = gracioso.network.Politica({
    "nombre": "filtrado-avanzado",
    "condiciones": [
        {"tipo": "origen", "valor": "any", "accion": "permitir"},
        {"tipo": "destino", "valor": "any", "accion": "permitir"},
        {"tipo": "tamaño", "valor": ">1000", "accion": "denegar"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "filtrado"},
        {"tipo": "registrar", "valor": "true"}
    ]
})
```

## Políticas de Red

### Política de Enrutamiento
```brincadeira
# Política de enrutamiento
politica = gracioso.network.Politica({
    "nombre": "enrutamiento-avanzado",
    "condiciones": [
        {"tipo": "origen", "valor": "192.168.1.0/24", "accion": "permitir"},
        {"tipo": "destino", "valor": "10.0.0.0/8", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "enrutado"},
        {"tipo": "priorizar", "valor": "alta"},
        {"tipo": "registrar", "valor": "true"}
    ]
})
```

### Política de Balanceo
```brincadeira
# Política de balanceo
politica = gracioso.network.Politica({
    "nombre": "balanceo-avanzado",
    "condiciones": [
        {"tipo": "origen", "valor": "any", "accion": "permitir"},
        {"tipo": "destino", "valor": "any", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "balanceado"},
        {"tipo": "balancear", "valor": "round-robin"},
        {"tipo": "registrar", "valor": "true"}
    ]
})
```

### Política de Caché
```brincadeira
# Política de caché
politica = gracioso.network.Politica({
    "nombre": "cache-avanzada",
    "condiciones": [
        {"tipo": "origen", "valor": "any", "accion": "permitir"},
        {"tipo": "destino", "valor": "any", "accion": "permitir"}
    ],
    "acciones": [
        {"tipo": "marcar", "valor": "cacheado"},
        {"tipo": "cachear", "valor": "true"},
        {"tipo": "registrar", "valor": "true"}
    ]
})
```

## Siguiente Paso

¿Quieres ver más ejemplos de políticas de red o aprender sobre otras características? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#politicas-avancado). 