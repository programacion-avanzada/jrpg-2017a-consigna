# Trabajo Práctico - tercera entrega

Esta entrega se propone integrar los componentes restantes del proyecto WoME.

## Fase de mantenimiento
1. Realizar las correcciones indicadas en la devolución anterior. 
2. De no haberlo hecho anteriormente, llevar las métricas a los valores esperados (menos de 260 incidencias de estilo, y por lo menos un 95% de cobertura de pruebas).
3. Actualizar el archivo README.md, agregando como primera línea el indicador de integración continua de Travis CI. Éste se obtiene desde la página del proyecto dentro de travis, haciendo clic en el indicador de construcción. Por ejemplo, el del proyecto dominio de la cátedra es este: [![Build Status](https://travis-ci.org/programacion-avanzada/jrpg-2017a-dominio.svg?branch=master)](https://travis-ci.org/programacion-avanzada/jrpg-2017a-dominio)
4. Actualizar el README.md para especificar el uso de Java 1.8

## Fase de mejoras

### Test de MyRandom
Cualquier método que esté basado en la generación de un número aleatorio, resultará en una imposibilidad de ser probado. Se debe estar 100% seguro de que las pruebas, bajo las condiciones establecidas, son positivas. Es por ello que se confía en ellas para encontrar defectos.  
La forma de probar un método que necesita números aleatorios, es mediante un Stub, o un doble de pruebas. `MyRandom` es un doble de pruebas, que fue creado para evitarles ese problema durante las primeras dos entregas. Ya no más :)  
`MyRandom` debería arrojar números realmente aleatorios con cada ejecución. Se necesita programar esa característica. Adicionalmente, crear una clase `MyRandomStub`, a la cual se le instruye en el constructor qué valores debe devolver para cada método. Estas dos clases deben heredar de otra, por ejemplo, RandomGenerator.  
Por último, es necesario que las clases que dependen ahora mismo de `MyRandom`, utilicen por defecto el nuevo `MyRandom`. Y que si reciben una invocación en el setter asignándole un nuevo generado de números aleatorios, utilice éste en lugar del establecido por defecto. Habrá que adaptar las pruebas a esta nueva situación.  
Luego, para poder probar las ramas condicionales no probadas debido a los generadores de aleatorios, deberán generar nuevas pruebas que instancien un `MyRandomStub` y que devuelva diferentes valores.  
Tienen un ejemplo de pruebas sobre números aleatorios [en este gist](https://gist.github.com/delucas/b1622618f511e95a1522f79835ca9be4).

### Hacia el encapsulamiento y el ocultamiento de la información, parte 1
1. En la clase `Alianza`, dentro del proyecto dominio, deberemos eliminar el método `setAliados`. También se debe evitar devolver **la misma colección** que se tiene como atributo en el getter de Aliados. Sin embargo, se puede devolver *una copia* del mismo.

## Fase de integración
1. Fork y clone del [proyecto cliente](https://github.com/programacion-avanzada/jrpg-2017a-cliente). Ante cualquier duda, remitirse a las instrucciones de la primera entrega.
2. Fork y clone del [proyecto servidor](https://github.com/programacion-avanzada/jrpg-2017a-servidor). Ante cualquier duda, remitirse a las instrucciones de la primera entrega.
3. Agregar ambos proyectos a integración contínua en Travis CI, tal como lo hicimos para la entrega anterior. Y agregar los badges de integración como primera línea del README.md
4. Enlazar los tres proyectos dentro de Eclipse. El proyecto **cliente** debe referir al proyecto **dominio**, y el proyecto **servidor** a **cliente** y **dominio*.
5. Ejecutar servidor, luego cliente. Crear un nuevo jugador, loguearse y probarlo. Crear un segundo jugador en una nueva ejecución paralela del cliente, loguearse y establecer un combate con el otro jugador.
6. Ambos proyectos se entregan con una modesta batería de pruebas. Funcionan... ocasionalmente. Se sugiere analizarlas, porque en próximas entregas las haremos funcionar correctamente.

## Fase de relevamiento
1. Encontrar y relevar al menos dos fallas en el uso del proyecto. Documentarlas [armando issues en el repositorio](https://help.github.com/articles/creating-an-issue) del proyecto correspondiente (cliente o servidor) de su organización.

### Hacia el encapsulamiento y el ocultamiento de la información, parte 2
2. En la clase `Personaje`, los siguientes métodos deben ser eliminados: `setSalud`, `setEnergia`, `setFuerza`, `setDestreza`, `setInteligencia`, `setCasta`, `setExperiencia`, `setNivel`, `setIdPersonaje`, `setDefensa`, `setSaludTope`, `setEnergiaTope`.  
**Esto generará un problema de integración. El primero que deberán resolver durante la cursada.** Cuando logren estabilizarlo, deberán actualizar los tres repositorios en el GitHub de su organización.

## Forma de entrega

Siempre se trabajará sobre los repositorios de GitHub. De ese modo, todo el trabajo se verá reflejado en forma automática apenas esté realizado.

## Fecha de entrega

El Trabajo Práctico se tomará automáticamente de sus repositorios el día 20 de Mayo de 2017, a las 8:00 AM (dos horas antes del primer turno del Taller).