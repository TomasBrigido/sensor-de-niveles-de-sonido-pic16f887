# Sensor de Niveles de Sonido con PIC16F887

Trabajo Práctico Integrador de Electrónica Digital II desarrollado sobre un microcontrolador PIC16F887. El sistema fue concebido para adquirir y representar niveles de sonido, pero en la implementación y simulación se utilizó un potenciómetro como entrada de prueba en lugar de un micrófono.

## Descripción general

El proyecto adquiere una señal analógica mediante el ADC del PIC16F887 y la procesa para:

- visualizar el nivel medido en displays de 7 segmentos,
- encender una escala de LEDs según la intensidad detectada,
- activar un buzzer al superar un umbral,
- cambiar entre distintos modos de operación mediante entradas por teclado,
- transmitir el valor medido por comunicación serie.

## Implementación real del prototipo

Aunque la idea original del sistema es funcionar como un sensor de niveles de sonido, el prototipo implementado utiliza un potenciómetro para simular la variación de la señal de entrada. Esto permitió probar el sistema de adquisición, visualización y señalización sin depender del módulo de micrófono.

## Características principales

- Microcontrolador `PIC16F887`
- Conversión analógico-digital usando el ADC interno
- Visualización numérica en display de 7 segmentos multiplexado
- Indicador de nivel mediante LEDs
- Alarma acústica con buzzer
- Selección de modos mediante teclado
- Envío de datos por EUSART
- Simulación del circuito en Proteus

## Modos de funcionamiento

El firmware está organizado en distintos modos de operación:

- `Parpadeo de funcionamiento`: indica que el sistema está encendido.
- `Adquisición ADC`: lee la entrada analógica y muestra el valor procesado.
- `Testeo`: enciende LEDs y activa el buzzer para verificar el funcionamiento.
- `Serie`: envía el valor convertido por comunicación serial.

## Estructura del proyecto

- `TPI_Grupo N°14.asm`: firmware en lenguaje ensamblador para el PIC16F887.
- `TPI_Grupo14.pdsprj`: proyecto de simulación en Proteus.
- `TPI_GRUPO N°14.pdf`: informe del trabajo con desarrollo teórico, hardware y firmware.

## Funcionamiento general

1. El sistema toma una señal analógica desde la entrada configurada en `AN0`.
2. El ADC del PIC convierte esa señal a un valor digital.
3. El firmware procesa el valor y lo convierte a formato decimal.
4. El resultado se muestra en displays de 7 segmentos.
5. Según el nivel detectado, se encienden LEDs y puede activarse el buzzer.
6. En uno de los modos, el valor también se transmite por puerto serie.

## Herramientas utilizadas

- MPLAB / ensamblador para PIC
- Proteus Design Suite

## Contexto académico

Este proyecto fue realizado como Trabajo Práctico Integrador para la cátedra de Electrónica Digital II de la Facultad de Ciencias Exactas, Físicas y Naturales de la Universidad Nacional de Córdoba.

## Autoría

- Tomas Andrés Brigido
- Facundo Luis Lugones Oviedo

