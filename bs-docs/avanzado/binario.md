# 🔢 Operaciones Binarias en BrincadeiraScript

## Introducción

¡Bienvenido al mundo de los bits graciosos! 🎉 BrincadeiraScript ahora incluye soporte nativo para operaciones binarias, donde los 0s y 1s bailan samba y forró. Aquí aprenderás a manejar datos en su forma más pura y graciosa.

## Operaciones Básicas

### AND, OR, XOR
```brincadeira
# Operaciones AND, OR, XOR graciosas
deixa a = 0b1010
deixa b = 0b1100

deixa and_resultado = a & b  # 0b1000
deixa or_resultado = a | b   # 0b1110
deixa xor_resultado = a ^ b  # 0b0110
```

### Desplazamiento de Bits
```brincadeira
# Desplazamiento gracioso de bits
deixa numero = 0b1010

deixa izquierda = numero << 2  # 0b101000
deixa derecha = numero >> 1    # 0b0101
```

## Estructuras de Datos

### BitArray Gracioso
```brincadeira
classe BitArrayGracioso {
    funcao inicializar(tamanho) {
        deixa self.bits = nuevo Array(tamanho).llenar(0)
    }
    
    funcao establecer(posicion, valor) {
        se (posicion >= 0 && posicion < self.bits.longitud) {
            self.bits[posicion] = valor & 1
        }
    }
    
    funcao obtener(posicion) {
        se (posicion >= 0 && posicion < self.bits.longitud) {
            retornar self.bits[posicion]
        }
        retornar 0
    }
    
    funcao voltear(posicion) {
        se (posicion >= 0 && posicion < self.bits.longitud) {
            self.bits[posicion] = 1 - self.bits[posicion]
        }
    }
    
    funcao contar_uno() {
        deixa contador = 0
        para cada (bit em self.bits) {
            contador += bit
        }
        retornar contador
    }
}
```

## Operaciones Avanzadas

### Compresión de Bits
```brincadeira
# Compresión graciosa de bits
funcao comprimir_bits(bits) {
    deixa resultado = []
    deixa contador = 1
    
    para (deixa i = 1; i < bits.longitud; i++) {
        se (bits[i] == bits[i-1]) {
            contador++
        } senao {
            resultado.adicionar([bits[i-1], contador])
            contador = 1
        }
    }
    
    resultado.adicionar([bits[bits.longitud-1], contador])
    retornar resultado
}
```

### Codificación de Bits
```brincadeira
# Codificación graciosa de bits
funcao codificar_bits(bits) {
    deixa resultado = ""
    deixa buffer = ""
    
    para cada (bit em bits) {
        buffer += bit
        se (buffer.longitud == 8) {
            resultado += String.de_codigo(parseInt(buffer, 2))
            buffer = ""
        }
    }
    
    se (buffer.longitud > 0) {
        buffer = buffer.padStart(8, "0")
        resultado += String.de_codigo(parseInt(buffer, 2))
    }
    
    retornar resultado
}
```

### Paridad
```brincadeira
# Cálculo de paridad gracioso
funcao calcular_paridad(bits) {
    deixa paridad = 0
    para cada (bit em bits) {
        paridad ^= bit
    }
    retornar paridad
}
```

### Corrección de Errores
```brincadeira
# Corrección de errores graciosa
funcao corregir_errores(bits) {
    deixa paridad = calcular_paridad(bits)
    se (paridad == 1) {
        # Encontrar y corregir el bit erróneo
        para (deixa i = 0; i < bits.longitud; i++) {
            bits[i] = 1 - bits[i]
            se (calcular_paridad(bits) == 0) {
                retornar bits
            }
            bits[i] = 1 - bits[i]
        }
    }
    retornar bits
}
```

## Comunicación

### Comunicación Serial
```brincadeira
# Comunicación serial graciosa
classe ComunicacionSerial {
    funcao inicializar(velocidad) {
        deixa self.velocidad = velocidad
        deixa self.buffer = []
    }
    
    funcao enviar(datos) {
        para cada (byte em datos) {
            self.buffer.adicionar(byte)
        }
    }
    
    funcao recibir() {
        se (self.buffer.longitud > 0) {
            retornar self.buffer.eliminar(0)
        }
        retornar null
    }
}
```

## Siguiente Paso

¿Quieres ver más ejemplos de operaciones binarias o aprender sobre otras características? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#binario-avancado). 
¿Quieres ver ejemplos prácticos de operaciones binarias o aprender sobre otras características técnicas? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#binario-avancado). 