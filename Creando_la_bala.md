# Creando la Forma de la Bala
Se comienza creando una esfera que se aplana. 

![image](https://github.com/user-attachments/assets/544d9080-beba-400f-bc0f-49be08c730e4)

Luego, se crea un cilindro y se ajusta para que se vea como el cuerpo de la bala. 

![image](https://github.com/user-attachments/assets/31167a94-5a55-4147-97f4-dcd5ff442873)


Para darle más forma, se añade una cápsula dentro del cilindro, sobresaliendo un poco del extremo.
Esto simula la parte frontal de la bala.

![image](https://github.com/user-attachments/assets/2177759f-ee77-4a94-8a0a-4c75ee51e942)


Se coloca la esfera aplanada en un extremo del cilindro, dándole un aspecto más realista. Se altera la base hasta que tenga la forma deseada.

# El material
Se crea un material amarillo en la carpeta de materiales. 

![Screenshot 2024-10-04 125126](https://github.com/user-attachments/assets/08e5a30d-413f-430b-9ff3-44124f0dfc31)

Se aplica al cilindro y a la cápsula para darles color.

![image](https://github.com/user-attachments/assets/05172709-8561-405a-8d7c-ce958ba8e644)

Para agregar más detalles, se duplica el material y se cambia su color a un tono más oscuro.
Luego, se aplica este nuevo material a la base de la bala.

![image](https://github.com/user-attachments/assets/ead202fd-080c-444f-b7e4-22feb1ca303f)

# Script para la Bala
Se crea un nuevo script llamado BulletMovement. En este script, se define una variable pública de tipo float llamada speed.

![image](https://github.com/user-attachments/assets/ac8f746f-da8e-4b25-9fae-1e3ae6107d8b)

Dentro del método Update(), se utiliza transform.Translate(0, 0, speed * Time.deltaTime) para mover la bala hacia adelante.

![image](https://github.com/user-attachments/assets/00fdefa9-9712-4096-814c-34efaab7caf5)

# Agregando el Script a la Bala
Finalmente, se arrastra el script a la bala en el Inspector. 

<p align>
   <img src="https://github.com/user-attachments/assets/462d5113-b26e-4c0a-b7be-44b051a2bc72" height="700" width="500" />
</p>

[Volver al Readme](README.md)




