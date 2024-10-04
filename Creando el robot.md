# Colocando el Robot Prefab en el Escenario:
Primero, se abre el proyecto en Unity y se busca el prefab del robot en la carpeta correspondiente y se arrastra a la escena. 
Esto permite visualizar el robot en el mundo del juego.

![image](https://github.com/user-attachments/assets/f0fd6be1-1ffd-4d36-bff4-f6bbc2b6f91f)

# Creando un Script de Playermovement:
Luego, se crea un nuevo script en C# llamado Playermovement. Dentro del script, se declaran dos variables públicas de tipo float: speedRotation y speed. Esto permite ajustar la velocidad 
de rotación y de movimiento del robot desde el Inspector de Unity, sin necesidad de cambiar el código cada vez.

![image](https://github.com/user-attachments/assets/36027126-a55f-4d66-8192-bb685d9ae888)

# Implementando el Código en el Bloque Update:
En el método Update(), se escribe el código que permite que el robot se mueva según las teclas presionadas. Se utiliza Input.GetKey para detectar las teclas W, A, S y D, y 
se usa transform.Translate() para mover al robot en la dirección deseada. Este bloque se ejecuta cada frame.

![image](https://github.com/user-attachments/assets/2564a89b-c6c5-4377-bc8d-c2b2291ffa74)

# Ejecutando el Programa para Probar el Movimiento:
Luego se ejecuto el programa

>>Video va aqui



