# INFORME DE PRÁCTICA PROFESIONAL SUPERVISADA

**Empresa:** Metalúrgica Moscariello  
**Alumno:** Moscariello, Christian — DNI: 37.056.3307  
**Tutor Académico:** Lukaszewicz, Cristian  
**Tutor Institucional:** Colatruglio, Mariano — Jefe Oficina Técnica  

---

## Índice

1. Reservado a la Facultad para evaluación  
2. [Resumen](#2-resumen)  
3. [Descripción del lugar de trabajo](#3-descripción-del-lugar-de-trabajo)  
4. [Descripción general del trabajo](#4-descripción-general-del-trabajo)  
   - [4.1 Partes del proyecto](#41-partes-del-proyecto)  
   - [4.2 Componentes electrónicos y electromecánicos](#42-componentes-electrónicos-y-electromecánicos)  
   - [4.3 Partes Mecánicas](#43-partes-mecánicas)  
   - [4.4 Circuito Eléctrico](#44-circuito-eléctrico)  
5. [Conclusiones](#5-conclusiones)  

---

## 2. Resumen

El presente trabajo consiste en el diseño y armado de un brazo robótico de **2 grados de libertad**, comandado por una **placa Arduino Uno**, para uso didáctico.

El proyecto incluye diseño CAD, impresión 3D, ensamblaje y control con motores **NEMA 17** y drivers **A4988**.

Su objetivo principal es servir para la **capacitación del personal técnico**, como paso previo a la implementación futura de un **brazo soldador automatizado**. Permite abordar fundamentos de robótica como **cinemática directa e inversa**, planificación de trayectorias y control de motores, a bajo costo y con fines educativos.

---

## 3. Descripción del lugar de trabajo

La práctica se realizó en la **Metalúrgica Moscariello**, una empresa familiar dedicada al mantenimiento de hornos industriales y fabricación de estructuras metálicas.

📍 Dirección: *Av. Valette 955, Monte Grande, Buenos Aires*

Equipamiento: corte, plegado, cilindrado, soldadura.  
El diseño se realizó en **SolidWorks** y **Fusion 360**, y las piezas fueron fabricadas por **impresión 3D**.

---

## 4. Descripción general del trabajo

### 4.1 Partes del proyecto

- Detalle de los **componentes electrónicos y electromecánicos**
- Diseño, modelado y **fabricación en 3D**
- **Armado** y puesta a punto del sistema
- **Desarrollo del software** de control

---

### 4.2 Componentes electrónicos y electromecánicos

#### Arduino UNO R3

- Microcontrolador ATmega328P  
- 14 pines digitales, 6 PWM  
- 6 entradas analógicas  
- Interfaz UART  
- Alimentación por USB o fuente externa  
- Programación en C/C++ vía Arduino IDE  

#### NEMA 17

- Motor paso a paso, 200 pasos por vuelta (1.8°/paso)  
- Tensión: 12–24 V  
- Corriente: 1.2–2 A  
- Par de retención: ~45 N·cm  
- Diámetro del eje: 5 mm  
- Dimensiones: 42 x 42 mm  

> 📸 *(Aquí podés insertar una imagen del motor y la placa Arduino, ejemplo:)*  
> `![Arduino y NEMA 17](images/nema_arduino.jpg)`

#### A4988

- Driver para motores bipolares  
- Microstepping: 1, 1/2, 1/4, 1/8, 1/16  
- Control con pines STEP y DIR  
- Ajuste de corriente con potenciómetro  
- Protección térmica y sobrecorriente  

---

### 4.3 Partes Mecánicas

- **Base:** Impresa en 3D, con alojamiento para NEMA 17 y espacio para cables  
- **Base giratoria intermedia:**  
  - Encastre superior para segundo motor  
  - Rodamiento tipo pista con bolillas  
  - Fijación central para eje del motor  

- **Efector final:**  
  - Acople directo al eje del segundo motor  
  - Encaje sin tornillos

> 📸 *(Ejemplo:)*  
> `![Partes mecánicas](images/brazo_ensamble.png)`

---

### 4.4 Circuito Eléctrico

- **2 motores NEMA 17 + 2 drivers A4988**
- **Alimentación:** 8V a VMOT + masa común (con capacitor entre VMOT y GND)
- **Control:**  
  - Arduino → pines STEP/DIR de cada driver  
  - STEP = paso  
  - DIR = dirección  
- **Conexión del motor:**  
  - Pines 1A, 1B, 2A, 2B del A4988  
- **Masa común:** debe unificar Arduino, drivers y fuente  

> 📸 *(Podés incluir el esquema eléctrico aquí:)*  
> `![Esquema eléctrico](images/esquema_electrico.png)`

---

## 5. Conclusiones

Este proyecto integró múltiples áreas de conocimiento: **mecánica, electrónica, automatización y programación**. 

Se desarrollaron:

- Diseño mecánico y CAD  
- Implementación de **cinemática directa e inversa**  
- Programación en **Arduino C/C++**  
- Integración de hardware real

Fue un acercamiento concreto a la robótica aplicada, permitiendo comprender y experimentar con componentes reales, construcción y puesta a punto de un brazo robótico funcional y educativo.

---

> Hecho en: Universidad Nacional de Lomas de Zamora — Facultad de Ingeniería  
> Año: 2025

