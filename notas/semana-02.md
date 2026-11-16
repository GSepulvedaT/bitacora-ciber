# Nota semanal 02 — Semana 2 del Nivel 0 (09-11 al 15-11-2026)

## 1. ¿Qué aprendí esta semana?

- En la sala **HTTP in Detail** (TryHackMe) hice peticiones **GET, POST, PUT y DELETE** y entendí para qué sirve cada una.
- Aprendí la **estructura de un comando** en la terminal: `comando [opciones] [argumentos]`. El comando es la acción, la opción indica cómo se hace y el argumento indica sobre qué se aplica (por ejemplo, un archivo).
- Aprendí que hay varias formas de **atacar o comprometer** una organización: ataques **DoS y DDoS**, robo de contraseñas (fuerza bruta, diccionario, rainbow tables) y ataques de **hombre en el medio**, que interceptan la comunicación entre 2 dispositivos.
- Practiqué Linux en **OverTheWire Bandit**, del nivel 0 al 5: archivos con guion, con espacios, ocultos y binarios (`cat ./-`, `ls -a`, `file ./*`).
- Vi un video del día a día de un analista SOC: la prioridad que pone la herramienta no siempre es la prioridad real, y el analista la decide investigando (**triage**). La alerta alta más común es el **phishing**.

## 2. Mini informe de un caso

- **Situación:** en la terminal estoy guardando en un archivo (`bandit.txt`) las contraseñas de OverTheWire Bandit, un desafío de práctica de terminal por internet.
- **Qué hice:** para guardar cada contraseña usaba la flecha ↑, que trae el comando con el que guardé la contraseña anterior, y editaba a mano la contraseña copiando y pegando.
- **Hallazgo:** al guardar la contraseña N.º 5 me di cuenta de que el rótulo `bandit3` estaba repetido 2 veces; la segunda línea debía decir `bandit4`. **Causa raíz:** al reusar el comando con ↑ cambié la contraseña, pero no el rótulo. Corregí el error con el editor **nano**.
- **Lección:** después de cada `>>`, reviso con `cat` que la línea quedó bien. Para corregir una línea ya guardada uso nano, no un nuevo `echo`.

## 3. ¿Qué me costó y por qué?

Lo que más me costó esta semana fue aprender la estructura de los comandos en la terminal. No basta con escribirlos en orden: también hay que conocer los comandos y las combinaciones necesarias para ejecutar un comando más complejo.

## 4. Meta para la semana 3

- **Original:** dominar el funcionamiento y comprender en profundidad la estructura de los comandos en la terminal.
- **Versión medible:** aprender a resolver los desafíos de Bandit con un máximo de 2 pistas por nivel. Para eso, primero profundizar y practicar los comandos en seco (en mi VM) antes de ir a Bandit.
