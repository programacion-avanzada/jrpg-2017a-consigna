# Trabajo Práctico - primera entrega

Se deberá crear un diagrama de clases utilizando una herramienta CASE, y la documentación (JavaDocs) para cada una de las clases suministradas.

## Metodología de trabajo

Por ser el primer trabajo práctico, será más simple porque demanda la organización de los grupos. Detallaremos a continuación los pasos necesarios para poder trabajar correctamente:

1. Formar grupos de 4 a 6 personas. Este grupo se mantendrá durante la cursada del taller. La flexibilidad cubre casos en los que haya abandonos, o que sean impares, etc. Utilicen dicha flexibilidad con sabiduría.

2. Escoger un nombre para el grupo. Dicho nombre se utilizará de ahora y hasta la finalización de la cursada para referirse al grupo completo. Mantengan la compostura, sin por eso ser necesariamente demasiado estructurados.

3. Crear una organización (con plan gratuito) en GitHub con dicho nombre. Eso se hace [desde esta página](https://github.com/organizations/new), y debe hacerlo *sólamente un integrante por equipo*. Ese integrante será el _dueño_ de la organización, momentáneamente.

4. Garantizar el acceso a la organización al resto de los integrantes del grupo. Eso se hace desde una dirección similar a esta, suponiendo que la organizacion se llamase "los-magios": `https://github.com/orgs/los-magios/people`.

5. Hacer el fork del repositorio suministrado por la cátedra *en el GitHub de la organización*. Esto se hace [desde este enlace](https://github.com/programacion-avanzada/jrpg-2017a-dominio), donde deben presionar el botón "Fork" que tiene un contador, en la parte superior derecha de la pantalla.  
**Nota:** Es muy importante que lo hagan a nombre de la organización, y no a nombre de sus usuarios individuales. Si se equivocan, lo pueden borrar e intentar nuevamente.

6. Habilitar los _issues_ en el repositorio recientemente "forkeado". Esto lo usaremos desde la cátedra, y se hace desde una dirección similar a esta: `https://github.com/los-magios/jrpg-2017a-dominio/settings`, chequeando la casilla "Issues".

7. Sacar una captura de pantalla de los resúmenes de Repositorios y Personas de la organización, y enviarla a los docentes. Las direcciones de estos resúmenes son similares a estas:
	* Repositorios: `https://github.com/los-magios`
	* Personas: `https://github.com/orgs/los-magios/people`

8. Cuando quieran importar el proyecto en Eclipse, [lean el README](https://github.com/programacion-avanzada/jrpg-2017a-dominio/blob/master/README.md) ya que necesitarán hacer algunos ajustes en su workspace.

## Consigna (¡ahora sí!)

* Generar un diagrama de clases del proyecto, teniendo en cuenta sólamente las clases de la carpeta `src/main/java`.
	* Para ello utilizarán alguna herramienta CASE.
	* Se desaconseja el uso de herramientas pagas o versiones pirata de las mismas. Hay alternativas de código abierto que son muy buenas, como ser [ArgoUML](http://argouml.tigris.org/) o [StarUML](http://staruml.io/).
	* Se prohibe el uso de herramientas no-CASE, como ser el Microsoft Paint, Microsoft Visio, Adobe Illustrator, etc.
	* No se aceptarán entregas a mano alzada.

* Escribir los JavaDoc de cada una de las clases alcanzadas por la consigna anterior.
	* Los JavaDoc se escriben [de esta manera](http://documentandosistemas.blogspot.com.ar/2013/10/javadoc-como-documentar-el-codigo.html).
	* Se documentará la clase (propósito de la misma) y dos métodos representativos (por ejemplo, `atacar` y `serAtacado` en `Persona`.
	* No se utilizarán los tags `@author` y `@version` en la documentación.

## Forma de entrega

Siempre se trabajará sobre los repositorios de GitHub. Por lo tanto:

1. El diagrama de clase (fuente y exportación a `.png`) se ubicarán en el directorio `documentacion`, en la raíz del proyecto (deberá ser creado).
2. Los JavaDoc ya estarán en medio del código, por lo que no hay problemas ni ambigüedades.

Adicionalmente *y por única vez*, se pide una impresión de dicho diagrama, para facilitar la corrección en clase.

## Fecha de entrega

El Trabajo Práctico se tomará automáticamente de sus repositorios el día 22 de Abril de 2017, a las 8:00 AM (dos horas antes del primer turno del Taller).