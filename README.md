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

##Recursos.

 +competencia entre procesos.
 +sistema operativo.
 







