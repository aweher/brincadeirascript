# 🔧 Solución de Problemas en BrincadeiraScript

## Introducción

¡Bienvenido a la guía de solución de problemas! 🎉 Aquí encontrarás soluciones a los problemas más comunes que puedes encontrar al programar en BrincadeiraScript.

## Problemas Comunes

### Errores de Sintaxis
```brincadeira
# ❌ Error: Falta punto y coma
deixa nome = "João"
mostrar nome

# ✅ Solución: Agregar punto y coma
deixa nome = "João";
mostrar nome;
```

### Errores de Tipo
```brincadeira
# ❌ Error: Tipos incompatibles
deixa numero = 5
deixa texto = "10"
deixa soma = numero + texto

# ✅ Solución: Convertir tipos
deixa numero = 5
deixa texto = "10"
deixa soma = numero + gracioso.string.para_numero(texto)
```

### Errores de Acceso
```brincadeira
# ❌ Error: Acceso a índice inválido
frutas = ["sonrisa", "maçã"]
mostrar frutas[5]

# ✅ Solución: Verificar índice
frutas = ["sonrisa", "maçã"]
se (5 < frutas.tamanho()) {
    mostrar frutas[5]
} senao {
    mostrar "Índice inválido"
}
```

## Depuración

### Logging
```brincadeira
# Logging gracioso
importar "gracioso.log"

gracioso.log.info("Iniciando programa")
gracioso.log.erro("Erro ao processar arquivo")
gracioso.log.debug("Valor da variável: " + valor)
```

### Breakpoints
```brincadeira
# Breakpoints graciosos
gracioso.debug.parar()

# Breakpoint condicional
gracioso.debug.parar_se(contador > 100)
```

## Optimización

### Rendimiento
```brincadeira
# ❌ Ineficiente: Bucle anidado
para (i = 0; i < 1000; i = i + 1) {
    para (j = 0; j < 1000; j = j + 1) {
        processar(i, j)
    }
}

# ✅ Eficiente: Bucle simple
para (i = 0; i < 1000; i = i + 1) {
    processar(i)
}
```

### Memoria
```brincadeira
# ❌ Ineficiente: Crear objetos innecesarios
para (i = 0; i < 1000; i = i + 1) {
    objeto = criar_objeto()
    processar(objeto)
}

# ✅ Eficiente: Reutilizar objetos
objeto = criar_objeto()
para (i = 0; i < 1000; i = i + 1) {
    processar(objeto)
}
```

## Siguiente Paso

¿Necesitas más ayuda? Visita nuestra [sección de ejemplos](../ejemplos/README.md) para ver más casos de uso. 