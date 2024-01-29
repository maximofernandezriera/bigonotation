# Big O notation o complejidad algoritmica

- Cuando hablamos de rendimiento y optimización, es importante tener un modo de determinar qué tan bueno o eficiente es un algoritmo en algunos casos y qué tan malo puede ser para otros. Para esto existe Big O notation.

- Big O notation nos permite dar una nomenclatura o simbología matemática a la complejidad de los algoritmos.

## Algunos ejemplos de expresiones Big O notation, que debemos sabernos, son:

En la notación O(1), el tiempo de ejecución es constante y no se ve afectado por el tamaño de la entrada, es decir, realizar una tarea toma el mismo tiempo tanto para pocos como para muchos elementos. 

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


