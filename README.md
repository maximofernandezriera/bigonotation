# Big O notation o complejidad algoritmica

### “Programa siempre tu código como si el tipo que va a tener que mantenerlo en el futuro fuera un violento psicópata que sabe dónde vives”. Martin Goldin

- Cuando hablamos de rendimiento y optimización, es importante tener un modo de determinar qué tan bueno o eficiente es un algoritmo en algunos casos y qué tan malo puede ser para otros. Para esto existe Big O notation.

- Big O notation nos permite dar una nomenclatura o simbología matemática a la complejidad de los algoritmos.

### Algunos ejemplos de expresiones Big O notation, que debemos sabernos, son:

## 1. En la notación O(1), o tiempo de ejecución es constante.

- No se ve afectado por el tamaño de la entrada, es decir, realizar una tarea toma el mismo tiempo tanto para pocos como para muchos elementos. 

- Las operaciones O(1) típicas incluyen el acceso directo a elementos (como en arrays) y operaciones aritméticas simples.
- Los algoritmos O(1) no usan bucles ni reursividad, no se llaman a ellos mismos. Son dependientes del tamaño de la entrada, ya que estos introducirían una variabilidad en el tiempo de ejecución.

### Ejemplo 1:

    public boolean esPar(int numero) {
        return numero % 2 == 0; // O(1)
    }

### Ejemplo 2:

    public int getElemento(int[] array, int index) {
        return array[index]; // O(1)
    }

## 2. La notación O(n^2), o tiempo cuadrático.

Describe algoritmos cuyo tiempo de ejecución aumenta cuadráticamente con el tamaño de la entrada. Esto significa que si el tamaño de la entrada se duplica, el tiempo de ejecución aumenta aproximadamente cuatro veces. 
Los ejemplos típicos de O(n^2) incluyen bucles anidados y ciertos algoritmos de ordenamiento.

### Ejemplo 1:

        public void imprimirPares(int[] array) {
            for (int i = 0; i < array.length; i++) {
                for (int j = 0; j < array.length; j++) {
                    System.out.println(array[i] + ", " + array[j]); //Usamos 2 bucles
                }
            }
        }

### Ejemplo 2

        public boolean contieneDuplicados(int[] array) {
            for (int i = 0; i < array.length; i++) {
                for (int j = i + 1; j < array.length; j++) {
                    if (array[i] == array[j]) {
                        return true; // Con dos bucles revisamos si existen duplicados
                    }
                }
            }
            return false;
        }

## El tercer ejemplo, nos va genial para adentrarnos en el campo de los algoritmos de ordenación, en concreto el método de la burbuja.

3. La notación O(log n) se refiere a algoritmos donde el tiempo de ejecución aumenta logarítmicamente con el tamaño de la entrada, haciéndolos eficientes para grandes cantidades de datos.

Indica que el tiempo aumenta linealmente, mientras que n sube exponencialmente. Entonces, si se tarda 1 segundo en calcular 10 elementos, se necesitarán 2 para 100, 3 para 1000 y así sucesivamente. Un ejemplo de ello es la búsqueda binaria.

## Quiero acabar recomendando este libro: https://github.com/cjbt/Free-Algorithm-Books/blob/master/book/Grokking%20Algorithms%20-%20An%20illustrated%20guide%20for%20programmers%20and%20other%20curious%20people.pdf 

#### Incluso las empresas de blockchain lo tienen en su cabecera.
