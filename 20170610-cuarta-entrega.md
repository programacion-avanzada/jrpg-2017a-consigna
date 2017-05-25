# Trabajo Práctico - cuarta entrega

Esta entrega se propone programar el primer incremento del proyecto WoME.

## Fase de mantenimiento
1. Realizar las correcciones indicadas en la devolución anterior. 
2. De no haberlo hecho anteriormente, llevar las métricas a los valores esperados.
3. Actualizar todos los archivos README.md, agregando como primera línea el indicador de integración continua de Travis CI. Éste se obtiene desde la página del proyecto dentro de travis, haciendo clic en el indicador de construcción. Por ejemplo, el del proyecto dominio de la cátedra es este: [![Build Status](https://travis-ci.org/programacion-avanzada/jrpg-2017a-dominio.svg?branch=master)](https://travis-ci.org/programacion-avanzada/jrpg-2017a-dominio)
4. Actualizar el README.md para especificar el uso de Java 1.8
5. Especificar los integrantes en los README.md de cada proyecto

## Fase de mejoras

### Pruebas de Servidor / Cliente
Las pruebas de esos proyectos tienen la inconveniencia de necesitar del otro para poder ejecutarse. Esas son pruebas de integración, y no queremos ese tipo de pruebas en el proyecto.  
Reescriban, eliminen o modifiquen las pruebas existentes para que no requieran de un Servidor funcionando.
> Nota: La compilación **va a necesitar** del enlace de proyectos, lo cual deberán resolver en TravisCI.

El objetivo secundario de esta entrega es obtener _builds_ estables en los tres proyectos del juego.

## Fase de evolución

Vamos a implementar la existencia de un inventario.

### Especificaciones de alto nivel
1. Todo Personaje (jugable o no) tiene un inventario.
2. En el inventario, dispone de algunos ítems.
3. Todo ítem en el inventario se considera equipado. Esto es una simplificación, ya que de otro modo se requiere mucho más trabajo y escapa a los objetivos de este incremento.
4. Los ítems modifican al menos un atributo del Personaje (salud, energía, destreza, etc) tanto en uno como en otro sentido.
5. Los ítems no pueden "soltarse". Una vez adquirido, no se elimina. Sin embargo, se solicita **no modificar los atributos directamente**.
6. Los ítems se consiguen mediante el triunfo en una batalla. Aleatoriamente el ganador adquiere un ítem (favorable, o no).
7. Si se sale de la partida y se vuelve a ingresar con el mismo jugador, deben obtenerse los mismos ítems que se tenían antes de salir.

Junto al código que resuelve estos puntos, se solicita agregar las Historias de Usuario correspondientes.

### Criterio de "listo"
1. Se puede visualizar el inventario del personaje.
2. Se visualizan los ítems que el personaje posee, y no otros.
3. Se puede apreciar el efecto de los ítems en los atributos del personaje. Por ejemplo: +10 pts de salud, -5% de fuerza, 2x de energía, etc.
4. Se hace evidente el efecto dentro de los combates.
5. Se consigue un ítem al finalizar una batalla, que cumple lo anteriormente dicho.
6. Se conservan los ítems (y sus efectos) al reingresar al juego.

### Bonus
El grupo que así lo desee, puede programar la funcionalidad de "soltar" un ítem, siempre y cuando esto sea desencadenado por una acción específica del usuario y no por eventos diversos, es decir, no se admite que se pierda un ítem al perder un combate o similares.  
Por supuesto, esto desencadenará efectos en los atributos del personaje.

## Forma de entrega

Siempre se trabajará sobre los repositorios de GitHub. De ese modo, todo el trabajo se verá reflejado en forma automática apenas esté realizado.

## Fecha de entrega

El Trabajo Práctico se tomará automáticamente de sus repositorios el día 10 de Junio de 2017, a las 8:00 AM (dos horas antes del primer turno del Taller).