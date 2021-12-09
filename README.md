# SQAChallenges

### Contenido del Proyecto

Se creó un proyecto llamado `MyFirstChallengeSqa` en el cual se crearon varias carpetas y clases, estructuradas de la siguiente manera:

![ImagenProyectoGeneral](https://user-images.githubusercontent.com/95836335/145440959-99a50b7f-150a-420c-ba51-6e5a33542baa.png)

### Features

###  myFirstSearch.feature

Este archivo contiene la historia de usuario para la cual se crearon escenarios en Cucumber que permiten hacer una búsqueda en una pagina web; leyendo un archivo excel.

![Imagen1](https://user-images.githubusercontent.com/95836335/145418156-a8ac27e0-71ef-4c84-a74a-135e5af8fe58.png)

### MyFirstSearchSteps

En el directorio `steps` se creó una clase llamada `MyFirstSearchSteps`, la cual contiene todos los pasos necesarios para ejecutar los escenarios anteriormente mencionados.

![Imagen2](https://user-images.githubusercontent.com/95836335/145433292-f34ed42e-921c-4935-ab72-51c9843ab389.png)

En el **@Given** se configura el método para que permita abrir la página web en la cual queremos buscar los productos. Para ello, se declaró un objeto llamado *driver* que ejecuta la prueba a través de *ChromeDriver*. También, se estableció un tiempo de espera implícito de 20 segundos para esperar que la página cargue.

En el **@When** se configura un método para escribir los cinco productos en la barra de busqueda de la página web, darle click al botón de busqueda, y por último, dar click en el producto seleccionado. Para ello, hace el llamado de dos clases: `MyFirstSearchHomePage` y `MyFirstSearchProductsPage`.

En el **@Then** se configura un método que permite validar que el nombre del producto buscado, coincida en el archivo excel y en la página web.

### MyFirstSearchHomePage

En el directorio `pages` tenemos la clase `MyFirstSearchHomePage`, en la cual se mapeó la pagina web para obtener los xpath de la página principal. Se relacionan dos xpath; uno para ubicar la barra de busqueda del producto, y otro para ubicar el botón de *buscar*. Luego, tenemos dos métodos que permiten escribir el producto deseado en la barra de busqueda y dar click.

![Imagen3](https://user-images.githubusercontent.com/95836335/145444932-1aef9613-6478-4a50-8d4f-e74cc7bcfcda.png)

### MyFirstSearchProductsPage

En el directorio `pages` tenemos una segunda clase llamada `MyFirstSearchProductsPage`. En esta clase, hacemos uso del método *replace()*, el cual, se utiliza para reemplazar un carácter especifico en una cadena, en este caso especifico, fue usado para reemplazar el nombre del producto en el *xpath* general.

Con el método *clickOnProduct* le estamos indicando al programa que de click al producto encontrado con el xpath.

![Imagen4](https://user-images.githubusercontent.com/95836335/145447739-f1a50fb9-7921-4bdc-822c-3bc1468cd4ec.png)

### MyFirstSearchResultPage

En el directorio `pages` tenemos una tercera clase llamada `MyFirstSearchResultPage`. En esta clase estamos buscando el nombre del producto en la página donde se encuentra el producto, y lo estamos retornando para poder hacer la comparación con lo que tenemos en Cucumber.

![Imagen5](https://user-images.githubusercontent.com/95836335/145452046-379a7402-5f58-4e1e-b9d9-2373dc9e6d7e.png)
