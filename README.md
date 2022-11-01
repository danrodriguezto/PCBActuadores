# PCBActuadores
Proceso de diseño de la PCB para la asignatura Diseño de Sistemas Electronicos.

Para definir que componentes se encuentran en la PCB, es necesario primero listar los componentes que se van a utilizar para controlar el gabinete.
 - Celda Peltier con disipacion y ventiladores.
 - Ultrasonido como humidificador.
 - Matriz LED.
 - Luz para toma de imagen de la camara.

Para el control de la celda Peltier y de sus ventiladores se va a utilizar un puente H, compuesto de transistores THT, que permitan que se garantice la potencia necesaria en la celda, ademas se incluyen unos diodos para evitar que existan retornos al sistema. Esta celda tambien tiene dos ventiladores, que permiten mantener el delta de temperatura entre las caras de la celda. El puente H entonces estaria compuesto por los transistores Q6,Q7,Q8 y Q9 y los diodos D1,D2,D3,D4. Para el control de los ventiladores se usan dos transitores MOSFET, que son Q1 y Q2.

Para poder usar el humidificador se debe hace un oscilador, que permita obtener la frecuencia necesaria para que el ultrasonido eleve la temperatura del agua hasta la temperatura requerida. Este oscilador se realiza haciendo uso de un integrado 555, el cual se encuentra en la placa como U1, ademas necesita dos condensadores y dos resistencias que se encuentran aledañas a este integrado. Este oslicador se puede apagar y encender a traves del MOSFET Q3. 

Para el control de la matriz LED, se planea hace uso de una placa adicional que es la referencia PCA9865, esta placa permite obtener 16 salidas PWM a traves de una conexion I2C.

En cuanto a la luz necesaria para obtener la imagen de manera correcta, esta se va a hacer a traves de un tira LED, la cual se controla a traves del MOSFET Q4.


Caras superior e inferior de la PCB. 

![image](https://user-images.githubusercontent.com/88418156/198914280-0804817b-d4b4-45b5-9bec-d75b848acc45.png)

Vista 3D de la PCB.

![image](https://user-images.githubusercontent.com/88418156/198914986-d754912c-bb14-42b3-81e0-0955b63901ca.png)
