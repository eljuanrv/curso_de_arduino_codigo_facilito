# curso_de_arduino_codigo_facilito
Aquí voy a llevar el seguimiento del curso de Arduino de código facilito
Arduino IDE es para programar

Fritzng es para documentar el proyecto pero ahora ya es de paga


Instalaciones
- [ARDUINO IDE](https://www.arduino.cc/en/software)
- [Fritzing](https://fritzing.org/download/)
- [Tinker Cad](https://www.tinkercad.com)

Microcontrolador

Circuito Integrado programable capaz de ejecutar instrucciones de forma secuencial con la finalidad de automatizar algún proceso

- Memoria(guardar funciones o datos volatiles)
- Perifericos contadors para aumentar el numero de entradas etc
- U de P: se encargan de ejecutar las instrucciones de la memoria
- Puertos: entradas y salidas que permiten comunicación

Difrencia entre un Microcontrolador(Arduino) y un Microordenador(Raspberrypi)

- Velocidad: Mz(1024HZ) y Gz(1024Mz)
- Elementos:Circuito integrado, RAM ROM Circuito integrado y perifericos o internet

Tipos de Microcontroladores

- Arduino Mega
- Ardiuno Leonardo: Microprocesador más potente
- Lyli pad de Arduino, wearables

Arduino
[Diagrama](https://web.archive.org/web/20180329025056/http://pighixxx.com:80/unov3pdf.pdf)

## Introduccion A La Programacion con el Arduino IDE

- Lenguaje de maquina
- Se usa un compilador para traducir a lenguaje de maquina

**Primer programa para encender un LED**

```ino
void setup() {
  // put your setup code here, to run once:
  pinMode(LED_BUILTIN, OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(LED_BUILTIN, HIGH); //turn the led on
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW); //turn the led of
  delay(1000)
}
```
