# 🎭 Programación Orientada a Objetos en BrincadeiraScript

## Introducción

¡Bienvenido al mundo de la POO graciosa! 🎉 BrincadeiraScript implementa un sistema de programación orientada a objetos único, donde las clases pueden bailar samba y los objetos tienen personalidad propia.

## Clases Básicas

### Clase Fruta
```brincadeira
classe Fruta {
    funcao inicializar(nome, cor, origem) {
        deixa self.nome = nome
        deixa self.cor = cor
        deixa self.origem = origem
    }
    
    funcao apresentar() {
        retornar "Sou uma " + self.nome + " " + self.cor + " do " + self.origem
    }
}
```

### Clase FrutaGraciosa
```brincadeira
classe FrutaGraciosa extends Fruta {
    funcao inicializar(nome, cor, origem) {
        super.inicializar(nome, cor, origem)
        deixa self.sorriso = true
    }
    
    funcao sorrir() {
        retornar "😊"
    }
}

manga = FrutaGraciosa("Manga", "laranja", "Brasil")
```

## Herencia Múltiple

### Clase Artista
```brincadeira
classe Artista {
    funcao apresentar() {
        retornar "Sou um artista!"
    }
}

classe Dançarino {
    funcao dançar() {
        retornar "💃"
    }
}

classe Cantor {
    funcao cantar() {
        retornar "🎵"
    }
}

classe ArtistaGracioso extends Dançarino, Cantor {
    funcao apresentar() {
        retornar "Sou um artista gracioso!"
    }
}
```

## Mixins

### Mixin Dança
```brincadeira
mixin DançaGraciosa {
    funcao sambar() {
        retornar "🎵"
    }
    
    funcao forró() {
        retornar "💃"
    }
}

classe Bailarino {
    usar DançaGraciosa
}
```

## Polimorfismo

### Clase Animal
```brincadeira
classe Animal {
    funcao fazer_som() {
        retornar "..."
    }
}

classe Cachorro extends Animal {
    funcao fazer_som() {
        retornar "Au au!"
    }
}

classe Gato extends Animal {
    funcao fazer_som() {
        retornar "Miau!"
    }
}
```

## Encapsulamiento

### Clase Conta
```brincadeira
classe Conta {
    funcao inicializar(saldo) {
        deixa self._saldo = saldo
    }
    
    funcao depositar(valor) {
        self._saldo += valor
    }
    
    funcao sacar(valor) {
        se (valor <= self._saldo) {
            self._saldo -= valor
            retornar true
        }
        retornar false
    }
    
    funcao get_saldo() {
        retornar self._saldo
    }
}
```

## Abstracción

### Clase Forma
```brincadeira
classe abstrata Forma {
    funcao abstrata calcular_area()
    funcao abstrata calcular_perimetro()
}

classe Circulo extends Forma {
    funcao inicializar(raio) {
        deixa self.raio = raio
    }
    
    funcao calcular_area() {
        retornar 3.14 * self.raio * self.raio
    }
    
    funcao calcular_perimetro() {
        retornar 2 * 3.14 * self.raio
    }
}
```

## Interfaces

### Interface Graciosa
```brincadeira
interface Graciosa {
    funcao sorrir()
    funcao dançar()
    funcao cantar()
}

classe PessoaGraciosa implements Graciosa {
    funcao sorrir() {
        retornar "😊"
    }
    
    funcao dançar() {
        retornar "💃"
    }
    
    funcao cantar() {
        retornar "🎵"
    }
}
```

## Factory

### Fábrica de Frutas
```brincadeira
classe FabricaFrutas {
    funcao estatica criar_fruta(tipo, nome) {
        se (tipo == "gracioso") {
            retornar FrutaGraciosa(nome)
        }
        retornar Fruta(nome)
    }
}

manga = FabricaFrutas.criar_fruta("gracioso", "Manga")
```

## Siguiente Paso

¿Quieres ver más ejemplos de POO o aprender sobre otras características? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#poo-avancado). 