# Segundo-Parcial-Paradigmas-de-Programaci-n_Ana-Maria-Hernandez

1. Modelamiento de un Perceptrón usando el paradigma de Agentes
# Modelamiento de un Perceptrón usando el Paradigma de Agentes

## 1. Diseño de la Solución

### A. Modelo Matemático
El perceptrón es una red neuronal simple capaz de clasificar datos linealmente separables. Su funcionamiento se basa en la ecuación:

$$ y = f(w_1x_1 + w_2x_2 + b) $$

donde:
- $ w_1, w_2 $ son los pesos asociados a cada entrada.
- $ b $ es el sesgo o bias.
- $ f(z) $ es la función de activación tipo signo.

La actualización de los pesos se realiza mediante la siguiente regla:

$$ w_i = w_i + \eta (y_{real} - y_{predicho})x_i $$
$$ b = b + \eta (y_{real} - y_{predicho}) $$

donde $ \eta $ representa la tasa de aprendizaje.

---

### B. Diseño del Sistema con MESA

Para implementar el modelo bajo el paradigma de agentes se establecen los siguientes elementos:
- **Agente:** representa un punto del conjunto de datos con coordenadas (x, y) y una etiqueta (1 o -1).
- **Modelo:** el perceptrón, encargado de ajustar los pesos y el sesgo con base en el rendimiento de los agentes.
- **Espacio:** un plano bidimensional continuo donde se ubican los agentes.
- **Interfaz:** incluye controles deslizantes (sliders) para definir la tasa de aprendizaje y las iteraciones, y botones para iniciar o reiniciar la simulación.

---

## 2. Código del Perceptrón (Implementación con MESA


## 3. Entrenamiento y Visualización

Durante la simulación los puntos cambian de color según la clasificación:
- **Verde:** punto correctamente clasificado.
- **Rojo:** punto mal clasificado.

Los controles permiten modificar la tasa de aprendizaje y el número de iteraciones, observando en tiempo real cómo el perceptrón ajusta sus pesos y mejora su desempeño.

---

## 4. Evaluación

Para calcular el rendimiento final se puede medir la precisión:

$$ \text{Precisión} = \frac{\text{Puntos Correctos}}{\text{Total de Puntos}} \times 100 $$

Esto permite verificar qué tan bien el perceptrón clasifica los datos después del entrenamiento.

---

## 5. Informe de Resultados

**Título:** Modelamiento de un Perceptrón usando el Paradigma de Agentes

**Objetivo:** Implementar un perceptrón que clasifique datos linealmente separables mediante el paradigma de agentes en MESA.

**Metodología:** Los puntos del plano se modelan como agentes con etiquetas positivas o negativas. El perceptrón actúa como modelo global que ajusta sus parámetros de acuerdo con los errores de clasificación observados. A medida que avanzan las iteraciones, los pesos se estabilizan y la frontera de decisión se aproxima a la línea real de separación.

**Resultados:** Se observó que el modelo logra una clasificación satisfactoria tras varias iteraciones, alcanzando un alto porcentaje de precisión dependiendo de la tasa de aprendizaje seleccionada.

**Conclusión:** El uso del paradigma de agentes permite visualizar de forma clara el proceso de aprendizaje del perceptrón y comprender cómo las interacciones locales contribuyen al ajuste global de los parámetros del modelo.
