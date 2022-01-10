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

## Variables

- enteros: int (type name = val;)
- flotante: float 6/7 digitos
- double: 15 digitos
- boolean: true o false
- char: codigo ASCII
- byte: 0-255

## Operadores
- Aritmeticos:{+ - * / = %}
- Comparación: { >= <= == != > <}
- Booleanos: {&& || !}
- Compuestos {++ -- -= += *= /= %=}

## Variables Datos
- string (tipo de dato y clase): ```ino string H = "Hola"; ```
- array: ```ino int a[] = 10 ``` se manejan atravez de un indice
- void: ```ino void setup() {} ``` tipo de dato vacio o sin retorno

## Simulacion de Operadores
- [Simulacion](https://www.tinkercad.com/things/7R1S8E5HIRT)

**Primer Programa**
```ino 
// Declaracioin de variables

int res;
float result;
byte var1 = 10;
byte var2 = 8;
int del = 1000;
float v1 = 10;
int v2 = 8;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);// Serial. begin(9600); Esta instrucción le indica al Arduino que inicie comunicación con la computadora (o cualquier dispositivo conectado a los pines RX y TX) con una velocidad de comunicación serial de 9600 bits por segundo (baudios) 
  pinMode(13, OUTPUT);

  // suma
  res = var1 + var2;
  Serial.println(res);
  
  // resta
  res = var1 - var2;
  Serial.println(res);
  
  // multiplicacion
  res = var1 * var2;
  Serial.println(res);
  
  //divición
  result = v1 / v2;
  Serial.println(result);
  
  // modulo
  res = var1 % var2;
  Serial.println(res);
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(13, HIGH); //turn the led on
  delay(del);
  digitalWrite(13, LOW); //turn the led of
  delay(del);
}
```
## Condicionales

- if else
```ino
// Declaracioin de variables

float temp = 32;
int del = 1000;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);// Serial. begin(9600); Esta instrucción le indica al Arduino que inicie comunicación con la computadora (o cualquier dispositivo conectado a los pines RX y TX) con una velocidad de comunicación serial de 9600 bits por segundo (baudios) 
  pinMode(13, OUTPUT);
  
  if (temp >= 32) {
    Serial.println("Temperatura alta");
    digitalWrite(13, LOW);
  } else {
  	Serial.println("Temperatura aceptable");
    digitalWrite(13, HIGH);
  }
```
- switch
```ino
// Declaracioin de variables

int temp = 22; //el switch solo trabaja con int o char
int del = 1000;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);// Serial. begin(9600); Esta instrucción le indica al Arduino que inicie comunicación con la computadora (o cualquier dispositivo conectado a los pines RX y TX) con una velocidad de comunicación serial de 9600 bits por segundo (baudios) 
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(8, OUTPUT);
  
  switch (temp){
    case 22 :
    Serial.println("La temperaturaes de 22 grados");
    digitalWrite(13, HIGH);
    break;
    
    case 28:
    Serial.println("La temperaturaes de 28 grados");
    digitalWrite(12, HIGH);
    break;
    
    case 32:
    Serial.println("La temperaturaes de 32 grados");
    digitalWrite(11, HIGH);
    break;
    
    case 5:
    Serial.println("La temperaturaes de 5 grados");
    digitalWrite(8, HIGH);
    break;
  }

}

void loop() {

}
```

## Estructuras Iterativas
- for
```ino
int pinLed = 11;

void setup(){
  Serial.begin(9600);
  pinMode(pinLed, OUTPUT);
}

void loop(){
  for(int i=0; i<255; i++){
    analogWrite(pinLed, i);
    delay(10);
  }
}

```

- while
```ino

int pinLed2=10;

void setup(){
  Serial.begin(9600);
  pinMode(pinLed2, OUTPUT);
}

void loop(){

  int var =0;
  while(var<255){
    analogWrite(pinLed2, var);
    var++;
  }
}
```

- do while

```ìno

int pinLed2=10;

void setup(){
  Serial.begin(9600);
  pinMode(pinLed2, OUTPUT);
}

void loop(){

  int var =0;
  do {
    analogWrite(pinLed2, var);
    var++;
  } while(var<255);
}
```

# Conceptos Basicos de Electrónica
## Electronica Analogica
- Variacion en el tiempo
- Cualquier numero dentro de un rengo
- Parametros

**Componentes**
- Resistencias(limita corriente)
- Condensadores(almacena corriente)
- Inductores(fuerzas FEM)
- Diodos(Rectificadores de corriente)
- Transistores bjt npn, mos

## Electronica Digital
- Valores discretos
- Circuitos combinacionales
- Circuitos secuenciales

## Ley de OHM
- V=RI

# Interactuando con Arduino

## Push Button
```ino

int pinLed2=2;
int pinButton=7;

void setup(){
  Serial.begin(9600);
  pinMode(pinLed2, OUTPUT);
  pinMode(pinButton, INPUT);
}

void loop(){
  int BOTON;
  BOTON = digitalRead(pinButton);
  if(BOTON == HIGH){
  	digitalWrite(pinLed2,HIGH);
  } else{
  	digitalWrite(pinLed2, LOW);
  }
  delay(15);
}
```

Mantener la señal del boton
```ino
byte ledP =13;
byte button =2;
byte buttonState =0;
byte buttonStateBefore =0;

int salida=0;

void setup(){
	pinMode(ledP, OUTPUT);
	pinMode(buttonState, OUTPPUT);
}

void loop(){
	buttonState = digitalRead(button);

	if((buttonState == HIGH) && (buttonStateBefore == LOW)){
	salida =1 - salida;
	delay(20); // para que la señal del boton se estabilice

	}

	buttonStateBefore = buttonState;

	if(salida == 1){
		digitalWrite(pinL, HIGH);
	} else{
		digitalWrite(pinL, LOW);
	}
}

```
