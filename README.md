# PCBActuadores
Proceso de diseño de la PCB para la asignatura Diseño de Sistemas Electronicos.

Para definir que componentes se encuentran en la PCB, es necesario primero listar los componentes que se van a utilizar para controlar el gabinete.
 - Celda Peltier con disipacion y ventiladores.
 - Ultrasonido como humidificador.
 - Matriz LED.
 - Luz para toma de imagen de la camara.

Para el control de la celda Peltier y de sus ventiladores se va a utilizar un puente H, compuesto de transistores THT, que permitan que se garantice la potencia necesaria en la celda, ademas se incluyen unos diodos para evitar que existan retornos al sistema. Esta celda tambien tiene dos ventiladores, que permiten mantener el delta de temperatura entre las caras de la celda. El puente H entonces estaria compuesto por los transistores Q6,Q7,Q8 y Q9 y los diodos D1,D2,D3,D4. Para el control de los ventiladores se usan dos transitores MOSFET, que son Q1 y Q2.

Para poder usar el humidificador se hace uso del MOSFET Q3, el cual controla todo el modulo, el cual se compro de manera que se pudiera dejar mas cerca al interion del gabinete, ya que por lo general lo ultrasonidos que se utilizan como salida no tienen mucha extension en la longitud del cable. 

Para el control de la matriz LED, se planea hace uso de una placa adicional que es la referencia PCA9865, esta placa permite obtener 16 salidas PWM a traves de una conexion I2C, dentro de esta matriz se encuentran los colores azul y rojo, ademas de unos LED's blancos que van a permitir iluminar el gabinete cuando se deba tomar la imagen de la camara.

Caras superior e inferior de la PCB. 

![image](https://user-images.githubusercontent.com/88418156/206550978-9d26c42c-ec2c-486a-9584-ebbb7352ad6d.png)


Vista 3D de la PCB.

![image](https://user-images.githubusercontent.com/88418156/206551128-6b7fe51d-6504-48c2-b194-09030264bebe.png)

Una vez que se mando a imprimir la PCB y se empezaron a realizar las pruebas de cada uno de los modulos fue posible observar que existian varios errores, que no permitian el correcto funcionamiento de la placa, por lo que se necesito adicionar una PCB universal con transistores que permitieran corregir los errores, que principalmente se deben a que no se consegui la suficiente diferencia de potencial con la salida del ESP para apagar los MOSFETS P.

El resultado final del montaje de la PCB se muestra en la siguiente imagen, donde se puede observar tambien el modulo PCA, el cual es de color morado y encima de este la baquela que se debio agregar para que la placa funcionara correctamente.

![image](https://user-images.githubusercontent.com/88418156/206553662-80146f2c-ec49-4e88-8e28-4fcbed4f6200.png)

