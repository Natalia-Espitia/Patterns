# Laboratorio 2
## Jesus Alberto Jauregui Conde
## Natalia Espitia Espinel

### La Herramienta Maven
La herramienta Apache Maven se usa para gestionar y manejar proyectos de software. La base de maven para un proyecto es el concepto de un modelo de objeto de proyecto (POM), Maven puede gestionar la compilación, los informes y la documentación de un proyecto a partir de este modelo, que se concreta en el archivo pom.xml.

Ingresar a la página de la herramienta y entender:

- Cuál es su mayor utilidad

    Su mayor utilidad es gestionar y automatizar el ciclo de vida del desarrollo de proyectos de software.

- Fases de maven

    - validate: Valida que el proyecto sea correcto y que la informacion este disponiblel.
    - compile: Compila el codigo fuente del proyecto.
    - test: Prueba el codigo fuente compilado utilizando pruebas unitarias adecuadas, estas pruebas no requieren que el codigo se empaquete o implemente.    
    - package: Toma el codigo compilado y lo empaqueta en su formato distribuible, como un JAR.
    - verify: Realizar comprobaciones de los resultados de las pruebas de integración para garantizar que se cumplen los criterios de calidad.
    - install: Instalar el paquete en el repositorio local, para usarlo como dependencia en otros proyectos localmente. 
    - deploy: Se hace en el entorno de compilacion, copia el paquete final en el repositorio remoto para compartirlo con otros desarrolladores. 

- Ciclo de vida de la construcción

    Son tres ciclos de vida principales.
    - default: Es el mas importante y cubre todas las fases necesarias para construir, probar y desplegar un proyecto.
    - clean: Se utiliza para limpiar el proyecto, eliminando los archivos generados en compilaciones anteriores. 
    - site: Genera documentación del proyecto y publica un sitio web con informacion relevante. 

- Para qué sirven los plugins

    Los plugins son herramientas de Maven y permiten ejecutar tareas especificas en las distintas fases del ciclo de vida de construccion. Los plugins son responsables de realizar las acciones concretas en cada fase. Sirve para:
    - Automatizar tareas especificas.
    - Personalizar el ciclo de vida.
    - Manejo de dependencias adicionales.
    - Facilitar la integracion con herramientas externas.  

- Qué es y para qué sirve el repositorio central de maven

    El repositorio central es un almacen en linea que contiene una amplia coleccion de bibliotecas, frameworks, plugins y dependencias utilizadas en proyectos Maven. 
    Es un repositorio publico y centralizado, accesible a traves de internet, donde se almacenan artefactos listos para ser usados en proyectos Maven.
    Provee dependencias, ahorra tiempo, gestiona versiones, acceso global y resolucion de dependencias transitivas. 

### Ejercicio de las Figuras
- Crear un proyecto con Maven

![](/assets/images/1.png)
![](/assets/images/2.png)

### Ajustar algunas configuraciones en el proyecto
- Edite el archivo pom.xml

![](/assets/images/3.png)

### Compilar y Ejecutar
- Para compilar ejecute el comando: mvn package

![](/assets/images/4.1.png)
![](/assets/images/4.2.png)

- Busque cuál es el objetivo del parámetro "package" y qué otros parámetros se podrían enviar al comando mvn.

    Su objetivo es compilar el código fuente, ejecutar pruebas y empaquetar el proyecto en un archivo distribuible, como un archivo .jar, en el directorio target. Es un comando crucial para obtener un paquete ejecutable de tu aplicación Java.

    - mvn clean install: este comando ayuda a ejecutar un ciclo de vida de compilación limpio e instala la fase de compilación en el ciclo de compilación predeterminado.
    - mvn compile: se utiliza para compilar el código fuente. También compila las clases que se almacenan en un objetivo o clase en particular
    - mvn test: Maven también proporciona la facilidad de probar unidades de códigos particulares. Ejecuta las pruebas utilizando marcos de prueba adecuados.
    - mvn deploy: implementa el código para el proyecto. Esta implementación se realiza en un entorno de integración o lanzamiento. Copia todo el paquete final en el repositorio remoto y está disponible para compartir con otros desarrolladores.
    - mvn site: este comando crea un sitio que se basa en la información del pom del proyecto.
- Busque cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass".

![](/assets/images/5.1.png)
![](/assets/images/5.2.png)

- Realice el cambio en la clase App.java para crear un saludo personalizado, basado en los parámetros de entrada a la aplicación.
- Utilizar la primera posición del parámetro que llega al método "main" para realizar elsaludo personalizado, en caso que no sea posible, se debe mantener el saludo como se encuentra actualmente:

![](/assets/images/6.1.png)

- Buscar cómo enviar parámetros al plugin "exec".
Con el comando: mvn exec:java -D"exec.mainClass"="Ruta a la clase main" -D"exec.args"="Parametro a pasar"

- Ejecutar nuevamente la clase desde línea de comandos y verificar la salida: Hello World!

![](/assets/images/6.2.png)

- Ejecutar la clase desde línea de comandos enviando su nombre como parámetro y verificar la salida. Ej: Hello Pepito!

![](/assets/images/6.3.png)

- Ejecutar la clase con su nombre y apellido como parámetro. ¿Qué sucedió?
Solo tomo el nombre y no el apellido.

![](/assets/images/6.4.png)

- Verifique cómo enviar los parámetros de forma "compuesta" para que el saludo se realice con nombre y apellido.
Se modifico el codigo de la clase App.java

![](/assets/images/6.5.png)

- Ejecutar nuevamente y verificar la salida en consola. Ej: Hello Pepito Perez!

![](/assets/images/6.6.png)

### Hacer esqueleto de la aplicacion 
- Cree el paquete edu.eci.cvds.patterns.shapes y el paquete edu.eci.cvds.patterns.shapes.concrete.

![](/assets/images/7.1.png)

-Cree una interfaz llamada Shape.java en el directorio src/main/java/edu/eci/cvds/patterns/shapes de la siguiente manera:

![](/assets/images/7.2.png)

- Cree una enumeración llamada RegularShapeType.java en el directorio src/main/java/edu/eci/cvds/patterns/shapes así:

![](/assets/images/7.3.png)

- En el directorio src/main/java/edu/eci/cvds/patterns/shapes/concrete cree las diferentes clases (Triangle, Quadrilateral, Pentagon, Hexagon), que implementen la interfaz creada y retornen el número correspondiente de vértices que tiene la figura.

![](/assets/images/7.4.png)
![](/assets/images/7.5.png)

- Cree el archivo ShapeMain.java en el directorio src/main/java/edu/eci/cvds/patterns/shapes con el metodo main:

![](/assets/images/7.6.png)
