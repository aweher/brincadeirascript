# 🤖 Inteligencia Artificial en BrincadeiraScript

## Introducción

¡Bienvenido a la sección de IA! Aquí encontrarás una colección de herramientas y ejemplos para trabajar con inteligencia artificial en BrincadeiraScript.

## Redes Neuronales

### Red Neuronal Básica
```brincadeira
# Crear red neuronal
importar "gracioso.ai"

rede = gracioso.ai.RedeNeural({
    "camadas": [2, 3, 1],
    "funcao_ativacao": "sigmoid",
    "taxa_aprendizado": 0.1
})

# Entrenar red
dados = [
    {"entrada": [0, 0], "saida": [0]},
    {"entrada": [0, 1], "saida": [1]},
    {"entrada": [1, 0], "saida": [1]},
    {"entrada": [1, 1], "saida": [0]}
]

rede.treinar(dados, epocas=1000)
```

### Red Neuronal Avanzada
```brincadeira
# Crear red neuronal avanzada
rede = gracioso.ai.RedeNeural({
    "camadas": [784, 128, 64, 10],
    "funcao_ativacao": "relu",
    "dropout": 0.2,
    "batch_size": 32
})

# Configurar optimizador
rede.configurar_optimizador({
    "tipo": "adam",
    "learning_rate": 0.001,
    "beta1": 0.9,
    "beta2": 0.999
})
```

## Aprendizaje por Refuerzo

### Agente Básico
```brincadeira
# Crear agente
agente = gracioso.ai.Agente({
    "estados": ["feliz", "triste", "neutro"],
    "acoes": ["sonrisa", "baile", "fiesta"],
    "recompensas": {
        "sonrisa": 1.0,
        "baile": 0.8,
        "fiesta": 0.5
    }
})

# Entrenar agente
agente.treinar(epocas=1000)
```

### Agente Avanzado
```brincadeira
# Crear agente avanzado
agente = gracioso.ai.Agente({
    "tipo": "dqn",
    "memoria": 10000,
    "gamma": 0.99,
    "epsilon": 0.1
})

# Configurar red
agente.configurar_rede({
    "camadas": [64, 32],
    "funcao_ativacao": "relu"
})
```

## Procesamiento de Lenguaje Natural

### Análisis de Sentimiento
```brincadeira
# Crear analizador de sentimiento
analisador = gracioso.ai.AnalisadorSentimento({
    "modelo": "bert",
    "idioma": "pt"
})

# Analizar texto
texto = "Estou muito feliz hoje!"
sentimento = analisador.analisar(texto)
```

### Generación de Texto
```brincadeira
# Crear generador de texto
gerador = gracioso.ai.GeradorTexto({
    "modelo": "gpt",
    "tamanho": "pequeno",
    "temperatura": 0.7
})

# Generar texto
texto = gerador.gerar("Era uma vez", max_tokens=100)
```

## Visión por Computadora

### Reconocimiento de Imágenes
```brincadeira
# Crear reconocedor de imágenes
reconhecedor = gracioso.ai.ReconhecedorImagem({
    "modelo": "resnet",
    "classes": ["sonrisa", "baile", "fiesta"],
    "confianca_minima": 0.8
})

# Reconocer imagen
imagem = carregar_imagem("festa.jpg")
resultado = reconhecedor.reconhecer(imagem)
```

### Detección de Objetos
```brincadeira
# Crear detector de objetos
detector = gracioso.ai.DetectorObjetos({
    "modelo": "yolo",
    "classes": ["pessoa", "cadeira", "mesa"],
    "confianca_minima": 0.5
})

# Detectar objetos
imagem = carregar_imagem("sala.jpg")
objetos = detector.detectar(imagem)
```

## Siguiente Paso

¿Quieres ver más ejemplos de IA o aprender sobre otras características? Visita nuestra [sección de ejemplos avanzados](../ejemplos/README.md#ia-avancado). 