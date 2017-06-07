# Trabajo Práctico - entrega final

Esta entrega se propone programar el segundo incremento del proyecto WoME. Al ser la última entrega, se aceptarán entregas parciales cuando los grupos así lo dispongan.  
Todo lo que aquí se presente, deberá reflejar el trabajo del cuatrimestre: buenas métricas de checkstyle, buena cobertura, una cantidad apropiada de pruebas y código prolijo a lo largo de los tres subproyectos. Travis CI deberá estar funcionando y con resultado _verde_ sin excepción.

## Requisitos de alto nivel

Para cada uno de los tres requisitos, deberán mostrar el antes y después en cuanto a diagrama de clases de dominio, escribir el requisito en varias historias de usuario y preparar los casos de prueba que comprobarán la aceptación del requisito. Esto debe ser mostrado a los docentes ANTES de la entrega final.

### Integrar chat dentro de WoME

1. Se debe poder chatear en público.
2. Se debe poder chatear en privado con otro jugador, amigo o enemigo.
3. No es necesario implementar, pero es un adicional, el chat en grupos privados.

Todo esto debe suceder al mismo tiempo que el juego sigue funcionando, en tiempo real.

> #protip: Recuerden juegos en los que se ingresa a la ventana del chat con una simple combinación de teclas. Y pueden mencionar a otros usuarios para hablarles en privado, utilizando una notación similar a la de Twitter.

### Mercado de Ítems

1. Se deberá implementar un mercado, ubicado dentro del mapa.
2. Todos los jugadores que estén en dicho mercado en el mismo momento, acceden a una pantalla de comercio especial.
3. En dicha pantalla, se ofrecen ítems y se requieren otros.
4. Si se puede encontrar una coincidencia entre oferta y demanda, se pueden intercambiar dichos ítems.
5. No es necesario, pero deseable, poder intercambiar un conjunto de ítems por uno solo; o un conjunto por otro conjunto.

### Mejorar la selección y despacho de mensajes

El método `run` de la clase `servidor.EscuchaCliente`, del proyecto `Servidor`, tiene una gran estructura `switch/case`. Debemos eliminarla, utilizando polimorfismo de mensajería.  
Una vez hecho esto, es trivial remover el `switch/case` del método `run` de la clase `cliente.Cliente`. Háganlo también. En ese mismo proyecto, encontrará más `switch/case` en `cliente.EscuchaMensajes`. También deseamos reemplazar esa estructura.

Por lo tanto, se desean eliminar todos los `switch/case` que están relacionados con el polimorfismo de mensajería.

## Forma de entrega

Siempre se trabajará sobre los repositorios de GitHub. De ese modo, todo el trabajo se verá reflejado en forma automática apenas esté realizado.  
Sin embargo, para esta entrega, se deberá descargar el proyecto desde GitHub en las máquinas del laboratorio, y luego de una mínima configuración, así debe funcionar. Tendrán 5 minutos para preparar el ambiente en las computadoras de la entrega.

## Fecha de entrega

El Trabajo Práctico se tomará automáticamente de sus repositorios el día 8 de Julio de 2017, a las 8:00 AM (dos horas antes del primer turno del Taller).