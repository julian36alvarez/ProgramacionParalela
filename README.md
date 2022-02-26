# Programacion Paralela.

## Programa Definicion?

Programacion Concurrente.

**Etimologia concurrente.**

+ Quiere decir Juntarse en un mismo lugar o "Tiempo".

+ Que existe o acontece al mismo tiempo.

+ que hay mas de uno.

+ que se ejecuta en paralelo.
+ actuan en conjunto para solucionar algo.
+ la programacion concurrente parte de la programacion secuencial, arquitectura Von Neumann


![imagen](https://user-images.githubusercontent.com/31891276/151661108-e4cae093-57f9-4758-a115-26084c78d2ce.png)

la programacion concurrente es independiente de la cantidad de procesadores.

la concurrencia es inherente a los procesos ejecutados al tiempo

## Overlapping Multiples procesadores.

Cuando se cubre parcialmente un proceso con varios procesadores.


Time Sharing . tiempo compartido de ejecucion intercambiandola en el tiempo, cumple la definicion de concurrencia porque se cubre parcialmente antes de la finalizacion de los procesos que se estan ejecutando.

la concurrencia no depende del numerop de procesadores,
desde los años 70 se tiene concurrencia, 

Porque los lenjuages actuales no facilitan la concurrencia?

Interleaving. single processor

Sistema complejo

Sistema con muchas interacciones.

LImitacion de la programacion concurrente.

el resultado debe ser independiente de la velocidad en la que se computa.

Errores dependiendo del tiempo.


Riesgos de los Threads.

Programacion imperativa. fueron creados secuencialmente.

Los threads no forman parte del lenguaje se forman con librerias adicionales por tanto el compilador no sabe ya que el intenta hacerlo en secuencia.

Asembler

## Estrategias concurrentes.

Interacciones entre los procesos

+ No interactuan se separan los datos de manera disyunta y se reduce el tiempo.
+ se piensa para un numero abstracto


![imagen](https://user-images.githubusercontent.com/31891276/151663695-84c8173f-e5d8-4f29-a960-02cd2dde31fd.png)


## Procesos que cooperan directamente.

## Procesos que cooperan indirectamente y tambien compiten.

compiten en el sentido en que un dato es de asceso comun, puede que ambos no lean el mismo dato en memoria comun.

## Recursos.

 +competencia entre procesos.
 +sistema operativo.
 

## Procesos Disyuntos

Funciona siempre y cuando se puda hacer particion de datos.

Cada proceso corre la misma computacion.

# tema de grado, generar codigo con threds en que se diga la computacion digo los procesos y genere codigo con thread java o pyhon o C .


## Paso de mensajes o procesos que cooperan directamente.

Descomposicion apartir de la funcionalidad

Los porcesos trabajan para resolver una tarea tienen yn common task.

cada proceso sabe de la existencia de los otros y sabe con cual comunicarese para obtener la solucion.

depende directamente el uno del otro ya que tienen una interaccion directa.  

los mecanismos de comunicacion entre los procesos es el paso de mensajes  

se pueden catalogar en dos categorias  
 
procesos que producen datos y los envian.  
y procesos que reciben informacion y la consumen.  

Un proceso en particular puede pertenecer a ambas categorias.  

si se envian grandes cantidades de datos se generan cuellos de botella en memoria o en red es por ello que se envia una porcion discreta delos datos.  

la comunicadion el es nucleo de este sistema de concurrencia.

Sender y Receiver... Origen y destino y obiamente el mensaje y un medio.

![imagen](https://user-images.githubusercontent.com/31891276/155820639-b07aac86-3fa7-4b6b-bd7e-ffc777718791.png)


Se realiza bajo un area en el sistema operativo que se llama el area de comunucaccion de buffer. o area temporar de almacenamiento.

comunicacion punto a punto

var b: buffer max of T;

el buffer se maneja como una variable;

Un buffer al que no se le da el tamaño se le llama canal. y los proces lo que estan compartiendo son los canales.

el canal debe ser unidereccional. para disminuer los tiempos de espera, exclusivo para enviar, exclusivo para recibir.

los procesos no continuan hasta que se garantiza que se envio el mensaje.

![imagen](https://user-images.githubusercontent.com/31891276/155821069-128e6a26-102f-49be-8cad-bbd1fef67b80.png)


# Procesos que coperan Indirectamente.


Existen dos maneras de hacerlo.

Son procesos que tienen acceso a variables comunes.

Tienen recursos físicos limitados y existe competencia de los porcesos por este.

Se usa para comunicar datos se hablan atravez del area comun
para poder compartir esos recursos los procesos se deben sincornizarce es decir se ordenan las operaciones en el tiempo.


Competencia entre procesos para acceder al recursos 

son recursos fisicos normalmente sensillos compartidos por procesos concurrentes que compiten por ello.

Basicamente es una coperacion basado en competencia. 

Se espera que los procesos usen los recursos por un periodo finito.

no se pueden usar esos procesos al mismo tiempo. 



## Principio de exclusion multiple

NIngun thread deberia acceder a una variable que este en uso por otro Thread.

Si existe competencia de recurso se debe tener en cuenta y se deben encapsular las variables.

Datos atomicos.

Protocolo para este paradigma es

Reservar el recurso.

use el recurso  

liberelo cuando lo deje de usar.  

Antes de reservar tenemos que esperar que este libre, se aplica para todos los recursos.


Se debe declarar si se debe compartir o no la variable, para definir un area.

Compartido y global

Critical region

Cuando el proceso quiere entrar al area definida se debe garantizar que entre en un periodo finito.

Que pasa si tengo mas de una zona compartida?

Son compartidas concurrentemente.

## Deadlock:

## Livelock:


Prologue: Cuuando s e verifica que un porceso puede entrar a la region critica, si no puede entrar queda en cola de espera.

Epilogo: Cuando ya se sale de la region critica entra otro proceso.

Semaforos.

Entero Especial (0-1 O pare 1 siga).

Solo existe tres operaciones.

+ Darle un valor inicial.  
+ Incrementarlo.   
+ Decrementarlo.

Como se Implementa

Se dice que es un semaphoro.

se le da un valor inicial 

Incrementar Signal:(P)

Incrementa si se puede 0 o 1

Decremetar Wait(V)
s:= s-1, if s=1

Los semaforos se encadenan con una cola en el sistema operativo.

Se llama semaforo fuerte si tiene una cola. 

Si tienen una lista se llamam semaforo debil.  

Semaforo multivalor: puden entrar varios procesos ya que se tienen varios recursos; se complica el trabajo del sistema operativo.

Cual seria el valor inical logico para el semaphoro debe ser 1;


![image](https://user-images.githubusercontent.com/31891276/155841927-4d6f0d52-1f01-4e2f-a529-0b286462b3ee.png)

Signal y wait se sincornizan o se emparejan en el tiempo no en el codigo.



Los regions no son estructurados desde el puinto de vista de la concurrencia.

Las soluciones con semaforos son altamente desordenadas.

Esperas Activas: Ciclos que hacen nada
