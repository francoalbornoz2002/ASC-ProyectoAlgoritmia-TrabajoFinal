# Espacio para preguntas y/o dudas

## Diseño de procedimientos personalizados
¿Cuan complejo y costoso sería implementar que los alumnos puedan diseñar sus propios procedimientos y funciones (habilidades especiales)?

## Cantidad de ejercicios
¿Cuantos ejercicios en total se deberían diseñar para cada capitulo de la historia? -> Actualmente, los trabajos prácticos de la materia suman 72 ejercicios en total donde varía su complejidad y algunos están anidados.

## Resolución y evaluación del ejercicio
Revisar como sería la evaluación del ejercicio. Agregar a los requisitos de información los datos o entidad clave para lograr esto. Asociar la entidad con mision.

### Desarrollo
Analicemos
Un enunciado dado nos da un problema para resolver y debe funcionar para todos los casos posibles. El flujo de corrección y de prueba de que si el algoritmo funciona correctamente es:

1. Leemos el enunciado, comprendemos el problema y las reglas y limitaciones del enunciado.
2. Diseñamos un algoritmo para resolver dicho problema.
3. Se prueba el algoritmo en todos los casos posibles teniendo en cuenta las limitaciones y reglas del enunciado.
4. Si en alguno de los casos se encuentra una falla o excepción, se refactoriza el algoritmo para poder resolver esa falla o excepción.

Tomemos de ejemplo un ejercicio de carlitos. 

*Recorrer toda la avenida 60 depositando papeles en todas las esquinas e informando las calles en las que encuentra una flor.*

**Algoritmo propuesto**
pos(1,60) -> posiciona en la calle 1 avenida 60
mientras posCa < 100 hacer
    Si HayFlorEnLaEsquina entonces
        informar(posCa) -> informa la calle que hay flor
    depositarPapel -> Coloca el papel
    mover
// estamos en la esquina 100 y no entra en el mientras, evaluamos la última esquina
Si HayFlorEnLaEsquina entonces
    informar(posCa) -> informa la calle que hay flor
depositarPapel -> Coloca el papel en la esquina

Primero, analicemos el enunciado y los posibles casos que puedan ocurrir:
1. Recorrer toda la avenida 60: la ciudad es de 100x100, y como estamos recorriendo una sola avenida la posición que cambiará es la de la calle, entonces el límite sería la calle 100. Esto ya lo controlamos con el mientras posCa < 100
2. Depositar papeles en todas las esquinas:
   1. que pasaría si no tengo papeles en la bolsa? no contemplamos eso en el algoritmo. Asumimos que tenemos al menos 100 papeles para colocar, pero eso no lo sabemos al menos que lo definamos en el editor del Davinci. Lo ideal siempre sería preguntarse si tenemos un papel en la bolsa para colocar, ya que si no lo tenemos, el sistema arrojará una excepción y se detendrá la ejecución. Y si esto lo tenemos controlado, si no tenemos papel para colocar, simplemente no entramos en el "SI" y no accionamos el "depositarPapel".
   2. Que pasaría si ya hay un papel en la esquina? Desconozco si el davinci permite que haya mas de un papel en la esquina. Pero, asumamos que se limita y por cada esquina podemos tener como máximo dos objetos: un papel y una flor. Si intentamos colocar un papel en la esquina la cual ya tiene un papel, el sistema arrojaría una excepción y se detendría la ejecución del sistema. Entonces, si es que existe esta limitación, sería recomendable preguntarse primero si existe un papel ya en la esquina antes de colocarlo.
3. Informar las calles en las que se encuentra una flor: Esto ya está contemplado y controlado en el sistema. Si no existe la flor, simplemente no informa.

Con esto en cuenta, refactoricemos el algoritmo

pos(1,60)
mientras posCa <= 100 hacer
    Si HayFlorEnLaEsquina entonces
        Informar(posCa)
    Si (HayPapelEnLaBolsa && ~HayPapelEnLaEsquina) entonces -> Si tenemos papel para colocar y no hay papel en la esquina (suponiendo una limitación)
        depositarPapel
    Si (posCa != 100) entonces -> Control extra para eliminar las ultimas lineas de codigo. Si estamos en la ultima calle, no se mueve.
        mover

¿Como se lleva a cabo la corrección de un algoritmo?
Generalmente, los docentes revisan los algoritmos de los alumnos y realizan la "prueba de escritorio" para confirmar si el algoritmo funciona correctamente. Esto pueden hacerlo con datos ficticios o no, ya que el sistema del davinci le indicas que queres que se generen papeles y flores en el escenario, pero estos papeles o flores se distribuirán aleatoriamente en el escenario. Es decir, si el enunciado dice que "recorrer la calle x tomando las flores de cada esquina", no es seguro que todas las esquinas tengan flores, y esto está bien, porque las flores pueden existir o no. Pero estos algoritmos se pueden decir que "funcionan" o no. No se determina una puntuación o una "nota".
Entonces, tengo dudas sobre como llevar la corrección de las misiones, como puedo determinar si el algoritmo del alumno funcionaría en todos los casos posibles. Una de ellas es que los enunciados tengan reglas o condiciones claras y concisas, y que al momento de que el sistema "evalúe y corrija" la solución del alumno se base en esas reglas o condiciones para evaluar si el algoritmo funciona o no para el enunciado propuesto, pero aun tengo muchas dudas de como plantear esto.

Puntos importantes para el diseño de enunciados:
**1. Ser específico con los enunciados**: colocar supuestos, valores de objetos, no dejar ambiguedades o libre interpretación. Por ejemplo con el enunciado anterior, que deja a libre interpretación acerca de los papeles, algunos alumnos pueden asumir que tienen papeles infinitos y otros podrían proponer cosas como que los papeles podrían ser limitados y no tendríamos al menos 100 para colocar en todas las esquinas.}


**Ejemplo de enunciado para mi sistema**
"Haz conseguido entrar al templo, ahora debes superar la primer sala para seguir avanzando. 



## Forma de dar feedback formativo
Revisar como sería el feedback formativo. Como se daría el feedback, los datos que se mostrarían, etc. Agregar a los requisitos de información todos los datos correspondientes