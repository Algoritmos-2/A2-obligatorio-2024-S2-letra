# Ejercicio 9 - El mejor once

## Descripción
Eres el asistente del director técnico de un famoso club de fútbol que actualmente atraviesa dificultades económicas. El DT te ha encargado la tarea de analizar la calidad del plantel y realizar una selección tentativa del once inicial de cara a la próxima temporada.

Dispones de archivos que detallan las características y habilidades de cada jugador, incluyendo información sobre los contratos y otros aspectos relevantes. Tu misión es seleccionar un once inicial que maximice la calidad del equipo, a la vez que cumpla con las restricciones del club.

Luego de una larga reunión con la directiva, se tomaron las siguientes medidas:

El presupuesto del club se reducirá respecto a la temporada pasada y se tendrá un límite de jugadores extranjeros, dado que estos suponen un coste extra para el equipo.

Aprovechando tus conocimientos adquiridos en la asignatura de Estructuras de Datos y Algoritmos 2, decides desarrollar un algoritmo que analice los datos de los jugadores. Este algoritmo debe procesar la información y proporcionarte el mejor once inicial (de mayor valoración), cumpliendo con las limitaciones de presupuesto y el cupo máximo de jugadores extranjeros permitidos.


### Valoracion de un jugador

Definimos la valoración de un jugador como el promedio de sus atributos (ritmo, tiro, pase, regate, defensa y físico). Al mismo tiempo, se considera la condición actual del jugador, de forma que su confianza y forma física también afectan a su valoración:

#### Confianza
Baja -> resta 5 puntos de valoración. \
Regular -> no afecta a la valoración. \
Alta -> incrementa en 5 puntos la valoración. 

#### Forma física
Lesionado -> la valoración de un jugador lesionado sera de 0. \
Mala -> resta 5 puntos de valoración. \
Normal -> no afecta a la valoración. \
Buena -> incrementa en 5 puntos la valoración. 


## Entrada

Cantidad de Jugadores (J): representa cuántos jugadores hay en el plantel.

Para cada jugador, se recibe la siguiente información:

 - Ritmo (45-99)
 - Tiro (45-99)
 - Pase (45-99)
 - Regate (45-99)
 - Defensa (45-99)
 - Físico (45-99)
 - Forma Física (Lesionado, Mala, Normal, Buena)
 - Sueldo (10-10000)
 - Extranjero (Si/No)
 - Confianza (Alta, Regular, Baja)


#### Presupuesto Monetario del Club (P): 1 <= P <= 100000
#### Cupo Máximo de Jugadores Extranjeros (E):  0 <= E <= 11

## Salida

El promedio de valoración del once inicial obtenido maximizando la valoración sobre el presupuesto monetario y el cupo máximo de jugadores extranjeros.


## Restricciones

 - Utilizar la técnica de tabulación y resolver con programación dinámica
 - Orden temporal y espacial (J * P * E)


## Ejemplo
 
### Input

<span style="color:red">15</span> \
75 84 64 95 45 77 Buena 2582 Si Alta \
54 81 62 74 83 88 Mala 379 No Baja \
63 77 58 46 54 96 Buena 108 No Alta \
71 63 48 63 45 67 Buena 4538 No Regular \
95 76 91 45 75 60 Buena 3651 Si Alta \
59 69 63 57 96 92 Mala 3590 No Alta \
87 63 83 81 54 78 Mala 342 No Alta \
81 90 91 52 74 45 Mala 2474 Si Baja \
67 83 75 79 83 86 Normal 2314 No Alta \
99 86 77 98 66 54 Mala 2253 No Alta \
79 76 64 66 53 88 Buena 2465 Si Regular \
91 85 79 51 91 52 Buena 3831 No Regular \
59 56 48 93 64 63 Mala 4193 Si Alta \
65 88 69 62 60 72 Lesionado 684 Si Regular \
83 75 56 93 70 84 Mala 1739 No Alta \
<span style="color:green">50000</span> <span style="color:blue">2</span>




### Output
75


### Explicación

<span style="color:red">15</span>~ Cantidad de jugadores \
(Le siguen 15 líneas representado los atributos de los jugadores) \
<span style="color:green">50000</span>~ Presupuesto monetario del club \
<span style="color:blue">2</span> ~ Cupo máximo de jugadores extranjeros



## Notas

No se pide llevar registro de los jugadores del once inicial seleccionado por el algoritmo, solamente se requiere la valoración promedio de sus integrantes.
