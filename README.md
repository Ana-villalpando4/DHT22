![Portada A1U2_page-0001](https://user-images.githubusercontent.com/124212032/224834301-c1836756-bda0-41b4-a031-e47e558be247.jpg)

# DHT22

![download](https://user-images.githubusercontent.com/124212032/224832891-0496af79-1fe6-4fcc-b9f1-02ca9c6fd026.jpg)

##### Sensor digital de humedad y temperatura. 馃尗馃挧

###### Es un sensor digital de temperatura y humedad relativa de buen rendimiento y bajo costo. Utiliza un sensor capacitivo de humedad y un termistor para medir el aire circundante, y muestra los datos mediante una se帽al digital en el pin de datos.

###### El DHT22 utiliza un solo cable digital para la comunicaci贸n de datos, lo que hace que su conexi贸n sea sencilla y f谩cil de implementar en proyectos de electr贸nica.
###### Este sensor proporciona mediciones de temperatura y humedad de alta precisi贸n, con una precisi贸n de +/-0.5 掳C para la temperatura y +/-2-5% para la humedad.

###### El DHT22 es compatible con una amplia gama de microcontroladores y placas de desarrollo, y es com煤nmente utilizado en proyectos de automatizaci贸n del hogar, sistemas de monitoreo ambiental, control de climatizaci贸n, y otras aplicaciones en las que se requiere medir la temperatura y la humedad del ambiente

### Especificaciones tecnicas 馃枼

* Voltaje de alimentaci贸n: 3.3 V a 5 V DC
* Corriente de operaci贸n: 2.5 mA (m谩ximo)
* Rango de medici贸n de temperatura: -40 掳C a 80 掳C
* Precisi贸n de la medici贸n de temperatura: +/-0.5 掳C
* Resoluci贸n Temperatura: 0.1掳C
* Rango de medici贸n de humedad: 0% a 100% RH
* Precisi贸n de la medici贸n de humedad: +/-2-5% dependiendo de la temperatura
* Resoluci贸n Humedad: 0.1%RH
* Tiempo de sensado: 2s
* Tama帽o: 15.1 mm x 25 mm x 7.7 mm

### Pines 馃搷

| PIN                   | 
|-----------------------|
| Alimentaci贸n +5V (VCC)| 
| Datos                 | 
| No Usado (NC)         | 
| Tierra (GND)          |

Es recomendado utilizar una resistencia de 4.7K Ohm en modo Pull-up, entre el pin de datos y vcc

### Precio 馃挵
###### Ronda entre 80 y 190 pesos mexicanos 

### Simulador
https://wokwi.com/projects/358671401024094209


#### Circuito 馃攲鈿?

![image](https://user-images.githubusercontent.com/124212032/224838309-a40b652e-8ae3-49ca-b3b9-4bec0e94257f.png)


#### Simulaci贸n 馃挕

![image](https://user-images.githubusercontent.com/124212032/224838835-3c1f5962-69fb-44e0-a15b-13e84988275e.png)

### C贸digo Utilizado 馃捇鈽?

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
