# 📚 Ejemplos de BrincadeiraScript

## Introducción

¡Bienvenido a la sección de ejemplos de BrincadeiraScript! Aquí encontrarás una colección de ejemplos prácticos que te ayudarán a entender mejor el lenguaje y sus características.

## Ejemplos Básicos

### Hola Mundo
```brincadeira
# Hola Mundo gracioso
mostrar "¡Hola, Mundo Gracioso! 🌴"
```

### Variables y Tipos
```brincadeira
# Variables graciosas
deixa nombre = "Brincadeira"
deixa version = 1.0
deixa activo = verdadeiro

mostrar "Nombre: " + nombre
mostrar "Versión: " + version
mostrar "Activo: " + activo
```

### Operaciones Matemáticas
```brincadeira
# Operaciones matemáticas graciosas
deixa a = 10
deixa b = 5

mostrar "Suma: " + (a + b)
mostrar "Resta: " + (a - b)
mostrar "Multiplicación: " + (a * b)
mostrar "División: " + (a / b)
```

## Ejemplos Intermedios

### Funciones
```brincadeira
# Funciones graciosas
funcao saludar(nombre) {
    retornar "¡Hola, " + nombre + "! 🌴"
}

mostrar saludar("Mundo")
```

### Estructuras de Control
```brincadeira
# Estructuras de control graciosas
deixa edad = 18

se (edad >= 18) {
    mostrar "Eres mayor de edad"
} senao {
    mostrar "Eres menor de edad"
}

para (deixa i = 0; i < 5; i++) {
    mostrar "Iteración " + i
}
```

### Arrays
```brincadeira
# Arrays graciosos
deixa frutas = ["Mango", "Piña", "Coco"]
frutas.adicionar("Guayaba")

para cada (fruta em frutas) {
    mostrar fruta
}
```

## Ejemplos Avanzados

### POO
```brincadeira
# POO gracioso
classe FrutaGraciosa {
    funcao inicializar(nombre) {
        deixa self.nombre = nombre
    }
    
    funcao saludar() {
        mostrar "¡Hola, soy una " + self.nombre + "!"
    }
}

mango = FrutaGraciosa("Mango")
mango.saludar()
```

### Eventos
```brincadeira
# Eventos graciosos
evento.on("click", funcao() {
    mostrar "¡Click gracioso!"
})

evento.on("keypress", funcao(tecla) {
    mostrar "Tecla presionada: " + tecla
})
```

### Asincronía
```brincadeira
# Asincronía graciosa
async funcao obtener_datos() {
    deixa resultado = await gracioso.api.obtener("/datos")
    mostrar resultado
}

obtener_datos()
```

## Siguiente Paso

¿Quieres ver más ejemplos o aprender sobre otras características? Visita nuestra [sección de características avanzadas](../avanzado/README.md). 