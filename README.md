![Portada A1U2_page-0001](https://user-images.githubusercontent.com/124212032/224834301-c1836756-bda0-41b4-a031-e47e558be247.jpg)

# DHT22

![download](https://user-images.githubusercontent.com/124212032/224832891-0496af79-1fe6-4fcc-b9f1-02ca9c6fd026.jpg)

##### Sensor digital de humedad y temperatura. 🌫💧

###### Es un sensor digital de temperatura y humedad relativa de buen rendimiento y bajo costo. Utiliza un sensor capacitivo de humedad y un termistor para medir el aire circundante, y muestra los datos mediante una señal digital en el pin de datos.

###### El DHT22 utiliza un solo cable digital para la comunicación de datos, lo que hace que su conexión sea sencilla y fácil de implementar en proyectos de electrónica.
###### Este sensor proporciona mediciones de temperatura y humedad de alta precisión, con una precisión de +/-0.5 °C para la temperatura y +/-2-5% para la humedad.

###### El DHT22 es compatible con una amplia gama de microcontroladores y placas de desarrollo, y es comúnmente utilizado en proyectos de automatización del hogar, sistemas de monitoreo ambiental, control de climatización, y otras aplicaciones en las que se requiere medir la temperatura y la humedad del ambiente

### Especificaciones tecnicas 🖥

* Voltaje de alimentación: 3.3 V a 5 V DC
* Corriente de operación: 2.5 mA (máximo)
* Rango de medición de temperatura: -40 °C a 80 °C
* Precisión de la medición de temperatura: +/-0.5 °C
* Resolución Temperatura: 0.1°C
* Rango de medición de humedad: 0% a 100% RH
* Precisión de la medición de humedad: +/-2-5% dependiendo de la temperatura
* Resolución Humedad: 0.1%RH
* Tiempo de sensado: 2s
* Tamaño: 15.1 mm x 25 mm x 7.7 mm

### Pines 📍

| PIN                   | 
|-----------------------|
| Alimentación +5V (VCC)| 
| Datos                 | 
| No Usado (NC)         | 
| Tierra (GND)          |

Es recomendado utilizar una resistencia de 4.7K Ohm en modo Pull-up, entre el pin de datos y vcc

### Precio 💰
###### Ronda entre 80 y 190 pesos mexicanos 

### Simulador
https://wokwi.com/projects/358671401024094209


#### Circuito 🔌⚡

![image](https://user-images.githubusercontent.com/124212032/224838309-a40b652e-8ae3-49ca-b3b9-4bec0e94257f.png)


#### Simulación 💡

![image](https://user-images.githubusercontent.com/124212032/224838835-3c1f5962-69fb-44e0-a15b-13e84988275e.png)

### Código Utilizado 💻☺

```Python

import dht
import machine
import time

global temp
global hum

d = dht.DHT22(machine.Pin(4))

while(True):
    time.sleep(2)
    d.measure()
    temp = d.temperature()
    hum = d.humidity()
    print(f"Temperatura: {temp}")
    print(f"Humedad: {hum}")
    
```

## Bibliografia
* https://www.todomicro.com.ar/arduino/225-sensor-de-humedad-y-temperatura-dht22-arduino.html#:~:text=El%20DHT22%20es%20un%20sensor,en%20el%20pin%20de%20datos
* https://listado.mercadolibre.com.mx/sensor-de-temperatura-dht22
