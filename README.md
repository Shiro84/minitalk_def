🔄 push_swap - Ordenando Números con Eficiencia
👋 Bienvenido a push_swap
push_swap es un proyecto de ordenamiento en C diseñado para ordenar una lista de enteros con el mínimo número de movimientos posibles, utilizando dos pilas (stack A y stack B) y una serie de operaciones predefinidas. Este proyecto desafía tu capacidad de optimizar algoritmos y profundizar en estructuras de datos.

🌟 Propósito del Proyecto
El objetivo de push_swap es crear un programa que reciba una secuencia de números desordenados en stack A y los ordene en orden ascendente usando una cantidad limitada de operaciones. El reto radica en optimizar el algoritmo para alcanzar la solución más rápida y con la menor cantidad de movimientos posibles, lo que convierte a push_swap en un excelente ejercicio de algoritmos de ordenamiento y manipulación de pilas.

🧩 Operaciones Permitidas
Para este proyecto, tienes un conjunto específico de operaciones con las que puedes manipular las pilas A y B. Es fundamental entender estas operaciones y cómo usarlas de forma eficiente.
Swap (sa, sb, ss): Intercambian los dos primeros elementos de la pila.
sa: Swap en A.
sb: Swap en B.
ss: Swap en ambas pilas.
Push (pa, pb): Mueve el primer elemento de una pila a la otra.
pa: Mueve el primer elemento de B a A.
pb: Mueve el primer elemento de A a B.
Rotate (ra, rb, rr): Desplaza hacia arriba todos los elementos de la pila, el primer elemento pasa al final.
ra: Rotate en A.
rb: Rotate en B.
rr: Rotate en ambas pilas.
Reverse Rotate (rra, rrb, rrr): Desplaza hacia abajo todos los elementos de la pila, el último elemento pasa al inicio.
rra: Reverse rotate en A.
rrb: Reverse rotate en B.
rrr: Reverse rotate en ambas pilas.
Estas operaciones son la base para manipular las pilas y deben combinarse estratégicamente para ordenar stack A con el mínimo número de movimientos.

📖 Estrategias Comunes
Debido a las limitaciones de movimiento, la elección del algoritmo de ordenamiento es crucial. Algunas estrategias populares para optimizar el número de movimientos incluyen:
Ordenación de 3 a 5 Números: Para listas cortas, los números pueden ordenarse utilizando combinaciones simples de sa, ra, rra y pa/pb.
Quick Sort Adaptado: Para listas más largas, una técnica basada en quick sort permite dividir los números en grupos y ordenarlos progresivamente en ambas pilas. Los números menores van a stack B y los mayores permanecen en stack A hasta alcanzar el orden final.
Radix Sort (Binario): En pilas grandes, radix sort es una técnica efectiva y se adapta bien al push_swap, ya que permite ordenar números usando una serie de pases basados en los bits del número.
Ejemplo Básico
Para ordenar un conjunto de 5 números en stack A como [3, 2, 5, 1, 4], puedes emplear una secuencia de movimientos como los siguientes:
text
Copia el codi
pb      # Mueve 3 a stack B -> A = [2, 5, 1, 4], B = [3]
pb      # Mueve 2 a stack B -> A = [5, 1, 4], B = [2, 3]
sa      # Intercambia los dos primeros en A -> A = [1, 5, 4]
ra      # Desplaza hacia arriba en A -> A = [5, 4, 1]
pb      # Mueve 5 a stack B -> A = [4, 1], B = [5, 2, 3]
...
pa      # Repite hasta que A esté ordenada en orden ascendente

Cada operación debe estar bien justificada y evitarse cualquier movimiento innecesario para mantener la eficiencia.

🚀 Cómo Empezar
Para empezar a trabajar en push_swap, sigue estos pasos:
Clona el repositorio:
bash
Copia el codi
git clone https://github.com/tu_usuario/push_swap.git


Compila el proyecto:
bash
Copia el codi
make


Ejecuta el programa:
bash
Copia el codi
./push_swap "3 2 5 1 4"


El programa debería imprimir una secuencia de operaciones para ordenar los números en stack A.

💡 Consejos de Optimización
Analiza el Tamaño de la Lista: Usa algoritmos diferentes según la cantidad de elementos (ej. un enfoque de radix para 100 o más elementos).
Memoria y Eficiencia: Asegúrate de liberar la memoria y minimizar el número de operaciones para optimizar tanto la ejecución como el uso de recursos.
Testing: Haz pruebas con listas de diferentes tamaños para evaluar la eficiencia y detectar posibles errores.

📖 Estrategias Comunes
Debido a las limitaciones de movimiento, la elección del algoritmo de ordenamiento es crucial. Algunas estrategias populares para optimizar el número de movimientos incluyen:
Ordenación de 3 a 5 Números: Para listas cortas, los números pueden ordenarse utilizando combinaciones simples de sa, ra, rra y pa/pb.
Quick Sort Adaptado: Para listas más largas, una técnica basada en quick sort permite dividir los números en grupos y ordenarlos progresivamente en ambas pilas. Los números menores van a stack B y los mayores permanecen en stack A hasta alcanzar el orden final.
Radix Sort (Binario): En pilas grandes, radix sort es una técnica efectiva y se adapta bien al push_swap, ya que permite ordenar números usando una serie de pases basados en los bits del número.
Ejemplo Básico
Para ordenar un conjunto de 5 números en stack A como [3, 2, 5, 1, 4], puedes emplear una secuencia de movimientos como los siguientes:
text
Copia el codi
pb      # Mueve 3 a stack B -> A = [2, 5, 1, 4], B = [3]
pb      # Mueve 2 a stack B -> A = [5, 1, 4], B = [2, 3]
sa      # Intercambia los dos primeros en A -> A = [1, 5, 4]
ra      # Desplaza hacia arriba en A -> A = [5, 4, 1]
pb      # Mueve 5 a stack B -> A = [4, 1], B = [5, 2, 3]
...
pa      # Repite hasta que A esté ordenada en orden ascendente

Cada operación debe estar bien justificada y evitarse cualquier movimiento innecesario para mantener la eficiencia.

🚀 Cómo Empezar
Para empezar a trabajar en push_swap, sigue estos pasos:
Clona el repositorio:
bash
Copia el codi
git clone https://github.com/tu_usuario/push_swap.git


Compila el proyecto:
bash
Copia el codi
make


Ejecuta el programa:
bash
Copia el codi
./push_swap "3 2 5 1 4"


El programa debería imprimir una secuencia de operaciones para ordenar los números en stack A.

💡 Consejos de Optimización
Analiza el Tamaño de la Lista: Usa algoritmos diferentes según la cantidad de elementos (ej. un enfoque de radix para 100 o más elementos).
Memoria y Eficiencia: Asegúrate de liberar la memoria y minimizar el número de operaciones para optimizar tanto la ejecución como el uso de recursos.
Testing: Haz pruebas con listas de diferentes tamaños para evaluar la eficiencia y detectar posibles errores.
