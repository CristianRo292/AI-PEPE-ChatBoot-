<img width="851" height="462" alt="Captura de pantalla 2026-06-18 104324" src="https://github.com/user-attachments/assets/03c8c562-525f-47b3-a43e-2889c69dfcc1" />

# APRENDIZAJE DE INGLÉS MEDIANTE PROGRESIÓN DE EXPRESIONES PUNTUALES Y ESPONTÁNEAS (AI-PEPE)

Demo en vídeo: https://youtu.be/ZQBsguLvDLM?si=qEJkvoDEAmEhubtg

# Descripción:

El proyecto AI-PEPE ofrece a los hablantes hispanos una forma viable, amigable y sin estrés de aprender y practicar inglés. Para lograrlo, se implementó una aplicación móvil minimalista que funciona como un compañero de conversación, eliminando la barrera psicológica del miedo a equivocarse. Todo esto está soportado por una base de datos en la nube utilizando una hoja de cálculo de Google, la cual contiene columnas específicas regulando el acceso y la personalización. La primera columna, "Usuario", se utiliza para registrar el nombre de acceso, y la columna "Contraseña" valida el ingreso, garantizando una cuenta única. Otra sección muy importante, y en la que se centra la lógica de personalización, es la columna de "Datos Relevantes". Aquí registramos el nombre del usuario, su edad y sus intereses (¿qué te gusta hacer?) en formato de una sola oración. Estos datos se inyectan en el historial de conversación para que la IA adapte las respuestas a los gustos del usuario. El programa inicia en una pantalla de inicio de sesión. Si el usuario es nuevo, se redirige a la pantalla de registro. Al iniciar sesión correctamente, pasa a una pantalla de bienvenida. Desde ahí, accede a la pantalla principal del ChatBot. Aquí el usuario puede enviar mensajes de texto; si escribe en español o comete errores gramaticales en inglés, la IA le sugiere la traducción o corrección de manera amigable, utilizando emojis para asociar palabras con sus significados. En la parte inferior encontramos el botón de "Modo Voz" (icono de teléfono). Al pulsarlo, la interfaz cambia a una simulación de llamada. En esta pantalla, el sistema activa el reconocimiento de voz, escucha al usuario, convierte el audio a texto y lo envía a la IA. La respuesta se muestra en pantalla como un subtítulo y se reproduce mediante texto a voz. Importante: la IA está configurada para no cortar la comunicación; si el usuario habla en otro idioma, la IA sugiere cómo decirlo en inglés sin interrumpir la fluidez de la "llamada".

# Important Aspectos 
• Se implementó una función de limpieza de cadenas de texto para la respuesta de la IA, eliminando los primeros dos y el último elemento de la cadena, ya que por lo general son valores basura o formatos no deseados de la API.
• Para proporcionar mayor fluidez en el modo de voz, se utiliza un temporizador (extensión de reloj) que genera un "delay" controlado. Esto detiene el programa momentáneamente permitiendo que el texto a voz termine su ejecución y el usuario pueda leer el subtítulo antes de que se vuelva a activar el micrófono, evitando que el sistema se escuche a sí mismo.
• Toda la conversación y los datos relevantes del usuario se concatenan en un historial (lista) que se envía en cada prompt a la IA, garantizando que el chatbot mantenga el contexto, la personalidad y el nivel progresivo del usuario.
• El sistema no corrige de manera punitiva; si el usuario se equivoca, la IA pregunta por la intención o sugiere la forma correcta, fomentando un aprendizaje orgánico y sin estrés.

#How para ejecutarlo por primera vez: 
Configurar el entorno es muy sencillo. Los requisitos mínimos son una cuenta de MIT App Inventor, una cuenta de Google (para la hoja de cálculo) y una clave API de Google AI Studio. Primero, descarga el archivo `.aia` del proyecto y la plantilla de la hoja de cálculo de Google. Haz una copia de la hoja de cálculo en tu Google Drive y asegúrate de que tenga las columnas para Usuario, Contraseña y Datos Relevantes. Abre MIT App Inventor, importa el archivo `.aia` y ve a la extensión `TCBGeminiBot1`. Deberás generar una clave API gratuita en Google AI Studio y pegarla en el bloque de código donde se inicializa la IA. Finalmente, conecta la extensión de Google Sheets con el enlace de tu hoja de cálculo publicada. Una vez configuradas las claves y los enlaces, puedes empaquetar el archivo APK para instalarlo en tu dispositivo Android o usarlo en tiempo real mediante el MIT AI2 Companion.

# Tecnologías utilizadas: 
• MIT App Inventor (Plataforma de desarrollo visual y lógica de la aplicación)
• Google Sheets (Soporte para base de datos en la nube)
• Google Gemini API (Modelo de lenguaje de IA para las conversaciones)
• TCBGeminiBot1 (Extensión para integrar Gemini en App Inventor)
• Reconocimiento de Voz (Speech-to-Text para el modo llamada)
• Texto a Voz (Text-to-Speech para la reproducción de respuestas)

# Estructura

• Proyecto 
    - AI-PEPE.aia (Archivo de proyecto de MIT App Inventor que contiene todas las pantallas y bloques de lógica)
    - assets/ (Carpeta) 
        • logo.png (Distintivo logotipo de la aplicación)
        • iconos/ (Iconos para los botones de enviar, micrófono, colgar, etc.)
    - google_sheets_template.csv (Plantilla de la hoja de cálculo para la base de datos de usuarios)
    - README.md (Este archivo)
