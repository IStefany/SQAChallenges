# SQAChallenges

### Contenido del Proyecto

Se creó un proyecto llamado `MyFirstChallengeSqa` en el cual se crearon varias carpetas y clases, estructuradas de la siguiente manera:

![ImagenProyectoGeneral](https://user-images.githubusercontent.com/95836335/145440959-99a50b7f-150a-420c-ba51-6e5a33542baa.png)

### Features

###  myFirstSearch.feature

Este archivo contiene la historia de usuario para la cual se crearon escenarios en Cucumber que permiten hacer una búsqueda en una pagina web; leyendo un archivo excel.

![Imagen1](https://user-images.githubusercontent.com/95836335/145418156-a8ac27e0-71ef-4c84-a74a-135e5af8fe58.png)

### MyFirstSearchSteps

En la carpeta `steps` se creó una clase llamada `MyFirstSearchSteps`, la cual contiene todos los pasos necesarios para ejecutar los escenarios anteriormente mencionados.

![Imagen2](https://user-images.githubusercontent.com/95836335/145433292-f34ed42e-921c-4935-ab72-51c9843ab389.png)

En el **@Given** se configura el método para que permita abrir la página web en la cual queremos buscar los productos. Para ello, se declaró un objeto llamado *driver* que ejecuta la prueba a través de *ChromeDriver*. También, se estableció un tiempo de espera implícito de 20 segundos para esperar que la página cargue.

En el **@When** se configura un método para escribir los cinco productos en la barra de busqueda de la página web, darle click al botón de busqueda, y por último, dar click en el producto seleccionado. Para ello, hace el llamado de dos clases: `MyFirstSearchHomePage` y `MyFirstSearchProductsPage`.

En el **@Then** se configura un método que permite validar que el nombre del producto buscado, coincida en el archivo excel y en la página web.
