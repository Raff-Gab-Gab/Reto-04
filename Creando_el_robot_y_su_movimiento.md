# Colocando el Robot Prefab en el Escenario
Primero, se abre el proyecto en Unity y se busca el prefab del robot en la carpeta correspondiente y se arrastra a la escena. 
Esto permite visualizar el robot en el mundo del juego.

<p align="center">
   <img src="https://github.com/user-attachments/assets/f0fd6be1-1ffd-4d36-bff4-f6bbc2b6f91f" height="300" width="300" />
</p>

# Creando un Script de Playermovement
Luego, se crea un nuevo script en C# llamado Playermovement. Dentro del script, se declaran dos variables públicas de tipo float: speedRotation y speed. Esto permite ajustar la velocidad 
de rotación y de movimiento del robot desde el Inspector de Unity, sin necesidad de cambiar el código cada vez.

![image](https://github.com/user-attachments/assets/36027126-a55f-4d66-8192-bb685d9ae888)

# Implementando el Código en el Bloque Update
En el método Update(), se escribe el código que permite que el robot se mueva según las teclas presionadas. Se utiliza Input.GetKey para detectar las teclas W, A, S y D, y 
se usa transform.Translate() para mover al robot en la dirección deseada. Este bloque se ejecuta cada frame.

![image](https://github.com/user-attachments/assets/2564a89b-c6c5-4377-bc8d-c2b2291ffa74)

# Creando el script machine
Se crea un nuevo graph llamado PlayerMovement. Este graph se utilizará para gestionar el movimiento del robot en la escena. Dentro del graph, se crean dos variables de tipo float: speedRotation y speed. Estas últimas se configurarán para controlar la velocidad de rotación y la velocidad de movimiento del robot. Se les asignan valores desde el Inspector de Unity según se desee.

![image](https://github.com/user-attachments/assets/3ba74230-88c4-4b4a-8c05-ece56672c9d0)

# Configurando el Nodo Sequence
Se crea un nodo de tipo Sequence, que contiene tres opciones conectadas al nodo Update. Este nodo se encargará de gestionar la lógica de movimiento del jugador.

![image](https://github.com/user-attachments/assets/2483de33-c364-4d06-821b-760e4297b90c)

# Conectando la Rotación del Robot
Uno de los nodos Sequence se conecta a un nodo de Transform Rotate. A este nodo se le envían como argumento los valores de rotación para el eje Y, calculando el resultado mediante la multiplicación del eje Mouse X por speedRotation. Esto permite que el robot rote en respuesta a los movimientos del mouse.

![image](https://github.com/user-attachments/assets/0a301451-5d2b-4d0e-9202-62d205bc2bec)

# Añadiendo la Lógica de Movimiento a la derecha
El segundo nodo del Sequence se conecta a un If Statement. Este if recibe como argumento un nodo de tipo OR, que verifica si se está presionando la tecla de flecha derecha o la tecla D. Si la condición del if es cierta, se envía una señal a un nodo de Transform Translate, que recibe como argumento el resultado de la multiplicación de speed y Time.deltaTime multiplicado por -1 para el eje X. Esto mueve al robot hacia la derecha.

![image](https://github.com/user-attachments/assets/3a8dce34-01e7-404c-bd11-a3c60bdfa02f)

# Configurando el Movimiento a la Izquierda
Si el if statement es falso, se conecta a otro if que realiza la misma función, pero para las teclas A y la flecha izquierda. En este caso, la multiplicación de Transform Translate se hace positiva para mover al robot en la dirección opuesta a la tecla D o flecha derecha, permitiendo así que el robot se desplace hacia la izquierda.

![image](https://github.com/user-attachments/assets/a730060b-9f31-42ad-9d9d-adb5f9b7b300)

# Implementando el Movimiento Adelante y Atrás
En otro nodo del Sequence, se conecta un if adicional que tiene la misma lógica que los anteriores, pero esta vez para las teclas W (flecha arriba) y S (flecha abajo). Estos nodos afectan el eje Z en lugar del eje X, permitiendo que el robot se mueva hacia adelante y hacia atrás según las teclas presionadas.

![image](https://github.com/user-attachments/assets/7893a2e6-b8f9-4b59-a053-3a1fecc55c34)







