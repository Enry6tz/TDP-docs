---
sidebar_position: 2
---

# Enunciado

### Proyecto cuatrimestral

**Modelado e implementación de una versión simplificada de un juego.**

**Caso de estudio: Super Mario Bros.**

Super Mario Bros. es un icónico videojuego de plataformas desarrollado por Nintendo. Lanzado en 1985 para la consola NES, el juego sigue las aventuras de Mario, un fontanero que debe rescatar a la Princesa Peach del malvado Bowser. El juego se desarrolla en el Reino Champiñón, donde Mario debe superar diversos niveles llenos de obstáculos, enemigos y trampas. Con su diseño de niveles ingenioso y su jugabilidad adictiva, Super Mario Bros. se ha convertido en uno de los videojuegos más influyentes y reconocidos de todos los tiempos.

El juego está dividido en ocho mundos, cada uno con cuatro niveles. Cada nivel presenta una combinación de plataformas, enemigos y obstáculos. Mario puede correr, saltar y usar power-ups para superar desafíos. La jugabilidad se centra en saltar sobre plataformas y enemigos para avanzar. El juego incluye varios power-ups como el Super Champiñón (que hace crecer a Mario), la Flor de Fuego (que permite lanzar bolas de fuego) y la Estrella (que otorga invulnerabilidad temporal). También existen enemigos, que varían desde Goombas y Koopa Troopas hasta el temido Bowser, cada uno con patrones de movimiento y ataques específicos.

A lo largo de los niveles, hay monedas y bloques que Mario puede romper para obtener objetos o puntos adicionales. Los jugadores obtienen puntos al recolectar monedas, derrotar enemigos y completar niveles. También hay un sistema de vidas basado en la acumulación de 100 monedas. El objetivo principal del juego es llegar al final de cada nivel y, finalmente, rescatar a la Princesa Peach del malvado Bowser.

### Requisitos del proyecto

A partir de la descripción general realizada previamente, el proyecto consiste en el diseño e implementación en Java de una versión simplificada e inspirada en Super Mario Bros, en la que se deben respetar todas y cada una de las siguientes condiciones:

- **Al menos 2 modos de juego**: la aplicación debe permitir, al iniciar la partida, seleccionar el modo de juego utilizado. El comportamiento de las entidades será el mismo, pero los aspectos gráficos deberán ser diferentes.
  
- **Al menos 3 niveles**: la aplicación debe tener al menos 3 niveles con dificultad creciente. Cada nivel debe cargarse desde un archivo de texto plano cuyo formato es a elección de la comisión.
  
- **Al menos 6 enemigos**: el juego debe incluir a los 6 enemigos descritos en la Tabla 1.

- **Al menos 5 power-ups**: el juego debe incluir los 5 power-ups descritos en la Tabla 2.

- **Al menos 4 plataformas**: el juego debe permitir interactuar con al menos las 4 plataformas de la Tabla 3.

- **Patrones de diseño**: se espera que se utilice al menos un patrón de diseño creacional y un patrón de comportamiento.

- **Transiciones y movimientos**: los movimientos y transiciones visuales deben implementarse con **Threads**.

- **Gráficos**: se debe usar únicamente Java Swing para el desarrollo gráfico.

- **Jugador**: solo se puede controlar a Mario usando las teclas AWD y la barra espaciadora para lanzar bolas de fuego.

- **Información disponible**: el juego debe mostrar en todo momento el nivel, puntaje acumulado y tiempo disponible.

- **Ranking**: el juego debe llevar un ranking persistente con el Top 5 de jugadores.

- **Sonidos**: se deben incluir sonidos para los cambios de estado y las interacciones con las entidades.


#### Tabla 1: Tipos de enemigos requeridos
| Enemigo         | Comportamiento                                                                 |
|-----------------|--------------------------------------------------------------------------------|
| Goomba          | Se mueven lentamente y se derrotan con un salto.                               |
| Koopa Troopa    | Se derrotan con dos saltos.                                                    |
| Piranha Plant   | Solo se pueden derrotar cuando están retraídas en la tubería.                  |
| Lakitu          | Vuela y lanza Spinys desde una nube.                                           |
| Spiny           | Erizos con pinchos, no se pueden derrotar con un salto, pero sí con bolas de fuego. |
| Buzzy Beetle    | Se pueden eliminar con bolas de fuego o golpeando una vez su caparazón.        |

#### Tabla 2: Tipos de power-ups requeridos
| Power-up        | Efecto                                                                                 |
|-----------------|----------------------------------------------------------------------------------------|
| Super Champiñón  | Hace que Mario crezca y pueda romper bloques.                                          |
| Flor de Fuego    | Permite lanzar bolas de fuego.                                                         |
| Estrella         | Otorga invulnerabilidad temporal.                                                      |
| Champiñón Verde  | Da una vida extra.                                                                     |
| Bloques de Pregunta | Contienen power-ups o monedas.                                                      |

#### Tabla 3: Tipos de plataformas
| Plataforma       | Descripción                                                                           |
|------------------|---------------------------------------------------------------------------------------|
| Ladrillo sólido   | Mario puede moverse sobre ellos y romperlos si está en estado Super Mario.            |
| Bloque sólido     | Mario puede moverse sobre ellos y obtener monedas o power-ups si los golpea desde abajo. |
| Tuberías          | Algunas contienen enemigos y Mario puede caminar sobre ellas.                         |
| Vacío             | Mario puede caer y perder una vida.                                                   |

#### Tabla 4: Puntajes
| Power-up / Enemigo / Plataforma | Puntaje Asociado                                      |
|---------------------------------|------------------------------------------------------|
| Super Champiñón                 | +10 en estado normal; +50 si está en estado Super Mario. |
| Flor de Fuego                   | +5 en estado normal; +30 con flor de fuego previa.    |
| Estrella                        | +20 en estado normal; +35 con estrella previa.        |
| Champiñón Verde                 | +100 en cualquier estado.                             |
| Moneda                          | +5 por cada moneda.                                   |
| Goomba                          | +60 por destruir; -30 por muerte.                     |
| Koopa Troopa                    | +90 por destruir; -45 por muerte.                     |
| Piranha Plant                   | +30 por destruir; -30 por muerte.                     |
| Lakitu                          | +60 por destruir.                                     |
| Spiny                           | +60 por destruir; -30 por muerte.                     |
| Buzzy Beetle                    | +30 por destruir; -15 por muerte.                     |
| Vacío                           | -15 por muerte.                                       |

### Condiciones de aprobación y entrega

- **Fecha límite de entrega y reentrega**: debe respetarse.
- **Defensas obligatorias**: 7 defensas obligatorias y de evaluación individual.
- **Calificación**: se calificará con una escala de A, B, C, D.
- **Participación**: Se analizará el nivel de participación de cada integrante.

