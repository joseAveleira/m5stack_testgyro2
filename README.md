# TEST ACELEROMETRO 

Este proyecto es una aplicación de IoT que utiliza el M5Stack Core para leer datos del sensor IMU y publicarlos en un servidor MQTT cuando ciertas condiciones se cumplen.

## Características

- Utiliza el sensor IMU del M5Stack Core para leer los datos de pitch.
- Publica los datos en un servidor MQTT cuando el pitch supera los 50 grados o es inferior a -40 grados.
- Solo publica en el servidor MQTT cuando el estado del relé cambia.

## Funcionalidad del Código

El código inicializa el M5Stack Core y el sensor IMU en la función `setup()`. También configura el color del texto y el fondo de la pantalla LCD.

En el loop principal, el código verifica si está conectado al servidor MQTT y, si no, intenta reconectarse.

Luego, lee los datos del sensor IMU y comprueba si el pitch es mayor que 50 o menor que -40. Si se cumple alguna de estas condiciones, cambia el estado del relé a "1" o "0" respectivamente.

Finalmente, si el estado del relé ha cambiado desde la última lectura, publica el nuevo estado en el servidor MQTT.

## Cómo Usar

1. Clona este repositorio en tu máquina local.
2. Abre el archivo `main.cpp` en tu IDE preferido.
3. Configura tu servidor MQTT en el código.
4. Compila y sube el código a tu M5Stack Core.
5. Observa los datos publicados en tu servidor MQTT.

## Contribuir

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para sugerir cambios o mejoras.