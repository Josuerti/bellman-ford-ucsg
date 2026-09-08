# Simulador de Bellman–Ford — UCSG

Aplicación educativa para explorar caminos mínimos en grafos dirigidos con pesos positivos y negativos.

## Uso

Descarga `index.html` y ábrelo en un navegador moderno. No requiere instalación ni servidor.

1. Selecciona un ejemplo o edita el grafo.
2. Elige el nodo de origen y ejecuta el algoritmo.
3. Avanza por las relajaciones para observar distancias y predecesores.
4. Explora la comparación con Dijkstra, el ejemplo de arbitraje y la prueba de escala.

Puedes importar y exportar grafos JSON. Los identificadores admiten de 1 a 32 letras ASCII, números, guiones o guiones bajos; deben ser únicos. Los extremos de las aristas y el origen deben existir y los pesos deben ser números finitos.

## Conceptos

Bellman–Ford realiza hasta |V|−1 pasadas de relajación. Una comprobación adicional permite detectar ciclos negativos alcanzables desde el origen. Los nodos afectados no tienen un camino mínimo finito.

Dijkstra requiere pesos no negativos para garantizar resultados correctos. Los ejemplos con pesos negativos muestran por qué puede fallar.

## Organización

`index.html` contiene la interfaz, los estilos y la lógica para facilitar su distribución como un único archivo. No utiliza bibliotecas externas.

## Verificación

Con Node.js: `node tests.js`. Incluye caminos mínimos, ciclos negativos y validación de archivos importados.
