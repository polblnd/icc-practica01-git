# icc-practica01-git

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

