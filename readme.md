# 📈 Predicción de raíces de una función cuadrática con TensorFlow.js

Este proyecto es una aplicación web interactiva desarrollada con **HTML**, **JavaScript**, **TensorFlow.js** y **Chart.js**, que entrena un modelo de red neuronal para **predecir las raíces reales** (𝑥₁ y 𝑥₂) de una función cuadrática de la forma:

y = 2x² - 3x + 1

Dado un valor de **Y**, el modelo predice qué valores de **X** (raíces reales) cumplen con la ecuación. La app:

- Entrena un modelo con **ejemplos generados automáticamente**.
- Permite al usuario **predecir** las raíces correspondientes a un valor de entrada Y.
- Muestra el **gráfico de pérdida** durante el entrenamiento, para visualizar el aprendizaje del modelo.

## 📂 Estructura del HTML

```html
<body>
  <h1>Modelo: y = 2x² - 3x + 1 (ambas raíces)</h1>
  <input type="number" id="entradaY" placeholder="Ingrese un valor Y">
  <button onclick="entrenarModelo()">Entrenar</button>
  <button onclick="predecir()">Predecir X₁ y X₂</button>
  <p id="resultado"></p>
  <canvas id="graficoPerdida"></canvas>
</body>

input: Campo para ingresar el valor de Y.
Botones: Entrena el modelo o predice las raíces.
p: Muestra los resultados.
canvas: Renderiza el gráfico de pérdida del entrenamiento.

Para cada valor x, se calcula:
y = 2x² - 3x + 1
Para entrenar el modelo con la inversa, se resuelve:

2x² - 3x + (1 - y) = 0
Se obtienen las raíces reales con:

x₁ = (-b + √(b² - 4ac)) / 2a
x₂ = (-b - √(b² - 4ac)) / 2a
📉 Gráfico de pérdida
Se utiliza Chart.js para graficar la pérdida (loss) durante el entrenamiento. Esto permite observar cómo mejora el modelo en cada época.

Tecnologías usadas:
TensorFlow.js – Red neuronal y entrenamiento.
Chart.js – Visualización del gráfico de pérdida.
HTML y JavaScript – Interfaz web y lógica principal.

Cómo usarlo
Ingresá un valor de Y en el campo correspondiente.
Hacé clic en “Entrenar” (el proceso puede tardar unos segundos).
Una vez entrenado, hacé clic en “Predecir X₁ y X₂” para ver las raíces.
Observá el gráfico de pérdida para entender el proceso de aprendizaje.

fue realizado para aprender sobre redes neuronales en el navegador