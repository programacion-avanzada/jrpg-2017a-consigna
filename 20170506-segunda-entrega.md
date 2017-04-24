# Trabajo Práctico - segunda entrega

Esta entrega se propone aumentar la calidad del componente `dominio`. Para ello utilizaremos herramientas de integración contínua. Sobre los resultados del conjunto de pruebas automatizadas mejoraremos nuestro software.

## Instrucciones

Este incremento requiere de mayor trabajo, y de un seguimiento cuidadoso de las instrucciones.

1. Sacar una cuenta en [Travis CI](https://travis-ci.org/). Se identifican con su cuenta de GitHub.
2. Ingresar a [su perfil en Travis CI](https://travis-ci.org/profile) y verificar que la organización que crearon es visible. Si NO fuera visible, diríjanse [aqui](https://github.com/settings/connections/applications/f244293c729d5066cf27) y otórguenle acceso a la organización haciendo clic en el botón _"Grant access"_ que figura junto al nombre de su organización, en el listado.
3. Una vez que verificaron el acceso, [vuelvan a Travis CI](https://travis-ci.org/profile) y luego de seleccionar en el menú de la izquierda su organización, habiliten el repositorio del grupo para integración contínua. Esto se hace mediante el interruptor correspondiente en el listado. Si NO apareciera, es cuestión de esperar unos minutos hasta que sí lo haga, refrescando la pantalla cada cierto tiempo.
4. Si todo funcionó correctamente, en una dirección similar a `https://travis-ci.org/programacion-avanzada/jrpg-2017a-dominio`, pero con el nombre de su grupo en lugar de `programacion-avanzada` encontrarán el historial de construcciones de esta pieza de software.
5. Durante la próxima clase veremos cómo trabajar con esta herramienta. Sin embargo, los alentamos a intentar leer los detalles de cada trabajo construído en la herramienta.

## Consigna (¡ahora sí!)

* Mantenimiento evolutivo
    * Actualizar el archivo README.md, agregando sus nombres de usuario de GitHub donde corresponde. Eliminen las líneas sobrantes, o agreguen según sean necesarias. 
    * Actualizar el diagrama de clases conforme a las correcciones recibidas durante la entrega anterior.
    * Documentar mediante JavaDoc los métodos restantes de *todas las clases del proyecto `dominio`*.

* El proyecto fue entregado con incidencias de estilo, falencias y cobertura limitada. Mejoraremos esas métricas.
    *  El conteo de incidencias de estilo entregadas asciende a 522. Es probable que hayan reducido algunas al documentar las clases en la entrega anterior. Para esta entrega queremos reducirlas por lo menos hasta el 50% (261 o menos).
        *  Para visualizar las incidencias de estilo necesitan instalar un plugin de Eclipse llamado "Checkstyle", o utilizar las lecturas de la salida de Travis CI. Estudiantes avanzados encontrarán más práctico instalar y construir el proyecto localmente con `gradle`, lo cual queda para su propia investigación (es realmente útil).
            > **Nota:** se adjunta al repositorio un ejemplo de los reportes obtenidos por la herramienta `gradle`, para tener como referencia.

        *  Encontrarán muy simple la reducción de incidencias. Se alienta llevar el número a algo tan bajo como sea posible.
        *  En el camino se sugiere enfáticamente no modificar los nombres de las clases ni de los métodos y atributos públicos de las mismas, ni tampoco los paquetes.

	* La métrica de cobertura de código asciende a 86.2%. Deberemos llevar ese valor a un 95%.
	    * Para visualizar dichas cifras necesitan instalar un plugin de Eclipse llamado "EclEmma", o utilizar el comando local `gradle` para visualizar dicho reporte.
	    * La cobertura de código representa el porcentaje del código que es probado. Para aumentar ese valor, hay que agregar pruebas sobre los casos no probados por el equipo que desarrolló el código originalmente.

    * Según los reportes de código duplicado, se puede ver que las clases `Personaje` y `NonPlayableCharacter` comparten mucho código. Diseñen una abstracción que pueda evitar tanta duplicación de código, y no haga fallar las pruebas existentes (ni las agregadas).
    
    * Todas las razas (`Orco`, `Humano` y `Elfo`) tienen un problema con sus constructores: el código duplicado, que puede llevar a futuros errores. Solucionen ese problema, utilizando las técnicas vistas durante la clase. Nuevamente, presten especial cuidado en no hacer fallar las pruebas.
    
    * Dentro de la clase `Personaje` encontrarán el uso del operador `instanceof`. Como hemos discutido, está desalentado y queremos eliminarlo. Cambien el código para que no afecte al funcionamiento, pero se evite dicho operador. No es válido reemplazarlo por invocaciones a `getClass()`.
```
		if (casta instanceof Guerrero)
			fuerza += 5;
		if (casta instanceof Hechicero)
			inteligencia += 5;
		if (casta instanceof Asesino)
			destreza += 5;
```

* Existen más apariciones del operador `instanceof`. Implementen arreglos para no utilizar dicho operador, sin introducir el conocido `getClass()`.
* Encontrarán comentarios en medio del código. Elimínenlos.

## Forma de entrega

Siempre se trabajará sobre los repositorios de GitHub. Por lo tanto:

1. El Diagrama de Clases (fuente y exportación a `.png`) se ubicarán en el directorio `documentacion`, en la raíz del proyecto (deberá ser creado).
2. Los JavaDoc ya estarán entre el código, por lo que no hay problemas ni ambigüedades.
3. Las mejoras sobre el código también formarán parte del proyecto.

## Fecha de entrega

El Trabajo Práctico se tomará automáticamente de sus repositorios el día 6 de Mayo de 2017, a las 8:00 AM (dos horas antes del primer turno del Taller).