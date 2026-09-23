# icc-practica01-git

Integrantes:
Leonardo Paolo Blanco Medina --- Aka Pol
Josué Yahel García Rodríguez -- Aka Josu

## RETO 2
##### Preguntas 

1 ¿Qué información almacena un commit?

La etiqueta que te dice los cambios


2 ¿Qué diferencia existe entre un repositorio local y un repositorio remoto?

Repositorio local esta en el disco duro de la computadora, y el remoto es la versión accesible y puede ser clonado por cualquiera para ser modificado


3 ¿Qué esperan que ocurra cuando ambos integrantes modifican archivos distintos?

Que puedan guardarse en el local y subirse a la rama principal desde git


4 ¿Qué esperan que ocurra cuando ambos modifican exactamente la misma linea?

Dependiendo de la rama, si trabajan en diferente se guarda de forma local, si es la main la ultima actualización es la que se guarda

## Comandos observados
Touch.(Formato) Crear un archivo

Git clone Clonar una copia del repositorio remoto

Git commit -m "Etiqueta" 

Git pull "Jalar los cambios de repositorio main"

Git push "Subir los cambios a el repositorio de github"

Git add "Archivo" para subir un archivo al staging area

## Planificación

Commits que hara A:
1. Poner preguntas de reto 2 en README.md
2. Crear decimal.md y binario.md
3. Poner el diagrama de como crees que se vera el historial con los commits.
4. Cambiar algo en decimal.md.
5. Crear y subir rama decimal al repositorio.
6. Añadir preguntas y respuestas del reto 12.
7. Cambiar algo en decimal.md para ocaisonar un conflicto y hacer merge de la rama conflicto-decimal-a en main.
8. Resolver el conflicto de binario.md en main.
9. Tras registrar en README.md el diagrama de los commits y preguntas con sus respuestas del historial real.
10. Añadir reflexión final

Commits que hara B:
1. Comandos que usaremos escritos en el README.md
2. Commit de Planeación.
3. Escribir las preguntas y respuestas del reto 8 en el README.md.
4. Subir rama binario al repositorio.
5. Merge de su rama binario en main.
6. Resolver en decimal.md
7. Poner las preguntas y respuestas del Reto 15 en README.md.
8. Merge de la rama conflicto-binario-b con el archivo binario.md modificado en main.
9. Añadir reflexión final

## ¿Cuándo deberá ejecutarse pull?
Developer A:
1. Reto 03: Después de que Developer B haga push de Comandos observados.
2. Reto 05: Después de que Developer B haga push de Planeación.
3. Reto 06: Después de que Developer B haga pull para sincronizarse con el historial esperado de A.
4. Reto 08: Después de que Developer B haga push de la integración y respuestas.
5. Reto 12: Antes de integrar su rama (git pull --no-rebase) y al final del reto tras el push de B.
6. Reto 14: Antes de crear sus ramas/modificar para partir del mismo commit inicial.
7. Reto 16: Tras la resolución del conflicto y push por parte de Developer B.
8. Reto 17: Antes de iniciar el reto (sincronizar main) y en main tras el push de B para traer los cambios que provocarán el conflicto local al hacer git merge.

Developer B:
1. Reto 02: Después de que Developer A haga push de Preguntas iniciales.
2. Reto 04: Después de que Developer A cree y suba decimal.md y binario.md.
3. Reto 06: Después de que Developer A haga push de Historial esperado.
4. Reto 08: Con la opción git pull --no-rebase cuando su push sea rechazado en el Reto 07 por los cambios en el remoto.
5. Reto 12: Antes de hacer merge con la opción git pull --no-rebase para sincronizar main.
6. Reto 12: Después de que Developer A publique las respuestas del Reto 12.
7. Reto 14: Antes de iniciar para garantizar la sincronización en main.
8. Reto 14: En main (git pull --no-rebase) para traer la rama de A integrada y provocar el conflicto al hacer merge de la suya.
9. Reto 17: Antes de iniciar (para estar sincronizados en main).
10. Reto 18: Tras el push de Developer A con el Historial real.

# Reto 6
             G   E   C    
             |   |   |
     main <---------------A 
             |   |   |
             F   D   B

# Reto 7

Ambos Developers ejecutaremos git status para verififcar que ambos repositorios estan sincronizados.

Developer A va a modificar decimal.md.

Developer B modificará binario.md.

Ambos Developers ejecutaremos: git status, git diff, git add, git commit.

Developer A va a ejecutar primero git push.

Developer B va a ejecutar git push después.

Developer B va a leer el mensaje obtenido.

# Reto 8 Preguntas

1. ¿Por qué Git rechazo el primer push de Developer B?
Ya que cuando A hizo el push el repositorio contenia un commit que no tenía B en su repositorio local
2. ¿Existía un conflicto de contenido?
Si, ya que lo que modifico A, no existia en el repositorio de B
3. ¿Qué ocurrió cuando ejecutaron pull?
Permitio que ambos tubieran el contenido de la fusíon
4. ¿Qué diferencia observan entre un push rechazado y un conflicto?
Que ambos ocurren en diferentes etapas.

# Reto 12 Preguntas

¿Realizar un merge implica necesariamente que exista un conflicto?

No, tambien puede servir para trabajar en dos versiones diferentes y poder subir los cambios de forma mas ágil sin tener que esperar a que el otro acabe su versión para empezar a modificarlo. 


# Reto 15 Preguntas 

1. ¿Que representa HEAD en este momento?
El lugar donde comienza el conflicto
2. ¿Que representa el contenido entre «««< y =======?
Las primeras significan el inicio del problema. las otras nos muestran la diferencia entre las versiones que causan conflicto
3. ¿Que representa el contenido entre ======= y »»»>?
El final del conflicto
4. ¿Por que Git no pudo decidir automáticamente que contenido conservar?
Ya que merge intento integrar ambas ramas

# Reto 16
## Historia Real

                  H---I                 K               M
                 /       \             / \             / \
     A---B---C---D---E-----J---decimal---binario---L-----N---main

1.  ¿En que se parece al dibujo inicial?
   En que se presenta una ídea simplificada de las ramas y merge, tambien en la estructura que tiene.
2.  ¿En que es diferente?
   Como son colocados los puntos que representan las ramas.
3.  ¿Que partes del historial no habían anticipado?
   Lo de fusionar ramas.
3.  ¿Que entienden ahora que no entendían cuando realizaron el primer dibujo?
   Como se tenía que representar las ramas, los commits, y la fusion de estas.

# Reto 19

¿Que ventaja tiene utilizar el nombre v1.0 para identificar este punto del historial en lugar de utilizar solamente el hash del commit? 
En que al ponerle una etiqueta a la versión lo hace más identificable y fácil de nombre, mientras que los commits funcionan mas como las notas de parche

## Reflexión final

Respondan brevemente:
1. ¿Que información almacena un commit?

Los cambios que realizaste y la autoría.

2. ¿Que diferencia existe entre un repositorio local y un repositorio remoto?

Que el local esta en tu computadora y el remoto es una versión de tu repositorio subida en el internet, en este caso GitHub.

3. ¿Que ocurrió cuando modificaron archivos diferentes?

Solo cambiaban localmente en la computadora de cada uno.

4. ¿Que ocurrió cuando modificaron la misma región de un archivo?

Empezo a presentar conflictos, ya que al subirla con push lo que hacía Git era unir los cambios.

5. ¿Que diferencia existe entre commit y push?

Que el push sube los cambios al repositorio remoto, y el commit al historial del repositorio local.

6. ¿Que función tuvo pull durante la practica?

Te permitía actualizar tu repositorio local con lo que se subió al repositorio remoto.

7. ¿Por que un push puede ser rechazado aunque no exista un conflicto de contenido?

Porque el repositorio remoto tiene commits que el repositorio local no tiene

8. ¿Que representa una rama?

Una especie de repositorio local que te permite trabajar sin tener que actualizar a cada rato tu repositorio, ya que cada vez que realizas un commit se actualiza con el repo remoto automaticamente.

9. ¿Que indica HEAD? 

Indica cual es la rama o archivo en la cuál se esta trabajando.

10. ¿Que hace merge?

Fusiona cambios de una rama con otra rama

11. ¿Por que Git pudo integrar algunos cambios automáticamente y otros no?

Porque se modifican archivos diferentes, y en los casos en que se modifican la misma región no lo hace ya que no tiene instrucción para eso.

12. ¿Que representan los marcadores «««<, ======= y »»»>?

Inicio y fin de un conflicto

13. ¿Que ventaja proporciona un tag?

Mas identificable y mas facil de nombrar y recordar.

14. ¿Como cambio su interpretación de los diagramas de historial después de utilizar git log
–graph –oneline –all?

A pesar de que con nuestro diagrama no se presenta un gran cambio, nos da a entender que con la misma forma de diagramas se pueden elaborar distintas estrategias para hacer un trabajo mas rápido y eficiente con la creación y fusión de distintas ramas, los cuales pueden ayudar cuando hay un equipo de 3 o más personas. 

## Merge y Rebase
¿Por que ambos historiales pueden representar cambios semejantes y, sin embargo, tener una estructura diferente?
Merge fusiona dos historiales en un solo commit, mientras que el rebase genera nuevos commits con los cambios de forma secuencial en la otra rama (como si hubieses comenzado a trabajar en esa), por lo cual quedan en la cabeza del nodo (final del historial de la otra rama).
