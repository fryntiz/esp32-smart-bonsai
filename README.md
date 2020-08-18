# esp32-smart-bonsai

Proyecto para automatizar el cuidado básico de un bonsai controlando humedad ambiente, humedad en la tierra, riego y luz recibida.

## Dependencias platformio

Las siguientes dependencias son necesarias para poder compilar el proyecto

- Adafruit_SSD1306
- Adafruit_VEML6070
- DHT11
- ArduinoJson

## Entorno de variables para WIFI y API

Tenemos que copiar el archivo de ejemplo **api.cpp.example** al mismo nivel
de directorio y llamarlo simplemente **api.cpp** modificando posteriormente
las variables privadas de acceso a nuestro router wireless personal y la api
que tengamos en uso.

En caso de no tener o no querer utilizarlo, establecer la variable 
**upload_to_api** en **false** y las demás variables vacías tal como están en el
archivo de ejemplo actualmente.

## Hardware utilizado

- ESP32
- Módulo para reloj en tiempo real → DS1307 Tiny RTC (Como subo los datos en
  el momento y para ahorrar gastos además de energía, marco la hora tras subir)
- Pantalla LCD → SSD1306
- Sensor UV → VEML6070
- Módulo para relés
- Sensor de temperatura y humedad → DHT11
- Sensor analógico genérico para humedad
- Sensor analógico para tierra con anticorrosión: Capacitive Soil Moisture Sensor v1.2
- Batería de movil 2,6Ah 3,7v de lition (Sony Xperia Z3 Compact)

## Esquemas de Pines


### Pines analógicos

- 36 → Sensor principal de humedad en tierra
- 39 → Sensor secundario de humedad en tierra