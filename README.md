# Prueba de evaluación ioled BACKEND.

Si tienes ganas trabajar en iOLED y crees que tienes los conocimientos básicos de backend para ser parte de nuestro equipo, eres bienvenido a realizar esta prueba. 

Es una prueba bastante simple, pero a la vez mezcla diversos temas sobre desarrollo web, por lo tanto no solo se enfoca en saber programar. Por el momento, no se evaluarán temas de seguridad para no aumentar la dificultad, pero si evaluaremos el funcionamineto y como lograste el resultado.

La prueba consiste en realizar un microservicio capaz de autenticar usuarios y guardar información de sesión en una cookie. Como estamos enfocando el desarrollo a una arquitectura serverless en GCP, es necesario que montes este microservicio en GCP.

Requisitos:
- Montar el microservicio en [google cloud functions](https://cloud.google.com/functions/docs/).
- Utilizar el entorno de desarrollo node.js 8.
- Guardar información de sesión en la cookie. Puedes usar [cookie-session](https://github.com/expressjs/cookie-session) o cualquier otro middleware.
- Usar alguna base de datos NoSQL para emplear persistencia para extraer los datos de sesión. Recomendamos utilizar [mlab](https://mlab.com/), [mongodb](https://www.mongodb.com/cloud) o [google cloud storage](https://cloud.google.com/storage/). Si utilizas alguno basado en mongodb, debes utilizar la biblioteca [mongoose](https://mongoosejs.com/). El desarrollo en Google cloud storage queda a tu criterio.
- Para la autenticación, es necesario utilizar el protocolo oauth2.0, idealmente con Google. Puedes usar [passport.js](http://www.passportjs.org/) u otro middleware.
- El microservicio debe tener las siguientes rutas:
  - /auth/google: para realizar el proceso de autenticación.
  - /auth: muestra el usuario actual. 
  - /auth/logout: para finalizar la session

Aca te dejamos un ejemplo como base para poder guiarte: 

- https://us-central1-harambe-functions.cloudfunctions.net/auth/google : autenticación.
- https://us-central1-harambe-functions.cloudfunctions.net/auth/ : retorna un json con el usuario actual 
- https://us-central1-harambe-functions.cloudfunctions.net/auth/logout : terminar la sesión

