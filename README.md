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