# Informe Técnico - Paradigmas de Programación

## 1. Modelamiento de un Perceptrón usando el Paradigma de Agentes

### Descripción General
El perceptrón es un modelo matemático de neurona artificial utilizado para la clasificación binaria de datos linealmente separables. Implementarlo bajo el paradigma de agentes permite representar el proceso de aprendizaje como una interacción dinámica entre componentes autónomos.

### Diseño y Modelo Matemático
El perceptrón se define mediante:

$$ y = f(w_1x_1 + w_2x_2 + b) $$

donde \(x_1, x_2\) son las entradas, \(w_1, w_2\) los pesos y \(b\) el sesgo. La función de activación \(f(z)\) devuelve 1 o -1 dependiendo del signo del resultado.

Las reglas de aprendizaje son:

$$ w_i = w_i + \eta (y_{real} - y_{predicho})x_i $$
$$ b = b + \eta (y_{real} - y_{predicho}) $$

### Implementación en MESA

#### Estructura del proyecto
```
perceptron_mesa/
├── agent.py
├── model.py
└── server.py
```

- **agent.py:** Define la clase `PerceptronAgent`, encargada de realizar las predicciones y entrenarse modificando sus pesos.
- **model.py:** Contiene `PerceptronModel`, que genera puntos de datos aleatorios y coordina el entrenamiento a través del scheduler.
- **server.py:** Inicia el servidor visual de MESA, permitiendo ajustar parámetros como la tasa de aprendizaje e iteraciones.

#### Ejecución
1. Instalar dependencias:
   ```bash
   pip install mesa
   ```
2. Ejecutar el servidor:
   ```bash
   python server.py
   ```
3. Acceder a `http://localhost:8521` para visualizar la simulación.

Durante la ejecución, la frontera de decisión del perceptrón se ajusta visualmente a medida que el agente aprende.

### Resultados
El modelo logra convergencia cuando los datos son linealmente separables. La precisión final se calcula como:

$$ Precisión = \frac{\text{Puntos Correctos}}{\text{Total de Puntos}} \times 100 $$

### Conclusión
MESA permite representar de manera visual e interactiva el aprendizaje autónomo del perceptrón, demostrando la utilidad del paradigma de agentes en sistemas de inteligencia distribuida.


## 2. Calculadora Basada en el Paradigma de Agentes

### Descripción General
Este sistema implementa una calculadora descentralizada en la cual cada agente ejecuta una operación matemática independiente. El enfoque permite observar cómo la cooperación de múltiples agentes genera un resultado final coherente.

### Diseño del Sistema
```
calculadora_agentes/
├── agent.py
├── model.py
└── main.py
```

- **agent.py:** Contiene la clase `OperationAgent`, que define agentes para las operaciones `+`, `-`, `*`, `/` y `^`.
- **model.py:** Implementa `CalculatorModel`, que distribuye las operaciones entre los agentes y coordina su ejecución.
- **main.py:** Crea el modelo, procesa la expresión y muestra el resultado final.

### Ejemplo de Uso
1. Ejecutar el script:
   ```bash
   python main.py
   ```
2. Resultado esperado:
   ```bash
   Resultado: 5.0
   ```
   (para la expresión `2 + 3`)

### Flujo de Operación
1. El usuario introduce una expresión (por ejemplo `2 * 4 + 3`).
2. El modelo la interpreta y distribuye las operaciones a los agentes.
3. Cada agente calcula su parte de forma independiente.
4. El sistema combina los resultados finales respetando la jerarquía de operaciones.

### Conclusión
La calculadora demuestra cómo el paradigma de agentes puede aplicarse en el procesamiento distribuido de operaciones, ilustrando cooperación, modularidad y escalabilidad en el diseño.


## 3. Calculadora Científica en Kotlin (Paradigma Orientado a Objetos)

### Descripción General
Esta calculadora aplica los principios de la Programación Orientada a Objetos (POO) para extender funcionalidades matemáticas de manera modular y reutilizable.

### Estructura del Proyecto
```
calculadora_cientifica_kotlin/
├── Calculadora.kt
├── CalculadoraCientifica.kt
└── Main.kt
```

- **Calculadora.kt:** Clase base con operaciones básicas (`sumar`, `restar`, `multiplicar`, `dividir`).
- **CalculadoraCientifica.kt:** Subclase que añade funciones científicas (`seno`, `coseno`, `log10`, `raíz`, etc.).
- **Main.kt:** Ejemplo práctico de uso e impresión de resultados.

### Uso del Programa
1. Compilar el código:
   ```bash
   kotlinc *.kt -include-runtime -d Calculadora.jar
   ```
2. Ejecutar:
   ```bash
   java -jar Calculadora.jar
   ```
3. Salida esperada:
   ```
   Suma: 5.0
   Seno(45°): 0.7071
   ```

### Principios POO Aplicados
- **Encapsulamiento:** Cada clase protege su lógica interna.
- **Herencia:** `CalculadoraCientifica` extiende la funcionalidad de `Calculadora`.
- **Polimorfismo:** Permite reutilizar métodos con diferentes tipos de datos y comportamientos.

### Conclusión
El enfoque orientado a objetos permite construir software mantenible, modular y extensible. Kotlin facilita una sintaxis clara para expresar herencia y abstracción de manera natural.



## Conclusiones Generales
Estos tres proyectos ilustran la aplicación de distintos paradigmas de programación:
- **Paradigma de Agentes:** Útil en simulaciones e inteligencia colectiva.
- **Paradigma Orientado a Objetos:** Ideal para sistemas escalables y reutilizables.

Ambos enfoques resaltan la importancia de elegir el paradigma adecuado según el contexto del problema, fortaleciendo el diseño lógico y la comprensión de los fundamentos de programación moderna.
