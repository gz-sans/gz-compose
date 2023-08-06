GzCompose - Aplicación de Mensajería con Compose
Este documento proporciona una descripción general del código en los archivos MainActivity.kt y SampleData.kt de la aplicación GzCompose. La aplicación es una interfaz de mensajería implementada utilizando la biblioteca de UI moderna de Jetpack Compose. Permite a los usuarios visualizar conversaciones con mensajes y expandir los mensajes para ver su contenido completo.

-Estructura del Código-
Paquete y Clases Principales
El código está organizado en el paquete co.edu.sena.gzcompose. Las clases principales son las siguientes:

-MainActivity-
MainActivity hereda de ComponentActivity. En el método onCreate, se configura el contenido de la actividad utilizando el tema GzComposeTheme y se crea la interfaz de usuario principal mediante el composable Conversation.

-SampleData-
SampleData es un objeto que proporciona datos de muestra para la conversación en la aplicación. Contiene una lista de mensajes simulados que se utilizan para demostrar la funcionalidad de la interfaz.

-Modelo de Datos-
El modelo de datos incluye una clase Message que representa un mensaje en la conversación. Cada mensaje tiene un autor y un cuerpo.

-Composables Principales-
MessageCard: Este composable muestra un mensaje individual en forma de tarjeta. Contiene la imagen del autor, el nombre del autor, el cuerpo del mensaje y la posibilidad de expandir el mensaje para ver su contenido completo.

Conversation: Este composable utiliza un LazyColumn para mostrar una lista de mensajes. Utiliza el composable MessageCard para representar cada mensaje en la conversación.

-Uso de Datos de Muestra-
La clase SampleData proporciona una lista llamada conversationSample que contiene varios objetos Message. Estos mensajes de muestra se utilizan para previsualizar cómo se verían los mensajes en la conversación.

-Ejemplo de Datos de Muestra-
kotlin
Copy code
object SampleData {
    // Sample conversation data
    val conversationSample = listOf(
        Message(
            "Camilo",
            "¡Hola parcero! ¿Qué piensan hacer pa' la tarde? 😄"
        ),
        Message(
            "Andrés",
            "Estaba pensando en ir al parque a hacer un picnic 🧺🌳"
        ),
        // ... otros mensajes de muestra ...
    )
}
-Vistas Previa-
El código también incluye un composable de vista previa GreetingPreview que muestra cómo se vería la conversación completa utilizando el tema GzComposeTheme.

-Nota-
Este es solo un resumen de alto nivel del código proporcionado en los archivos MainActivity.kt y SampleData.kt. Consulta el código fuente completo para obtener detalles adicionales y ver cómo se implementan las funcionalidades de la aplicación.
