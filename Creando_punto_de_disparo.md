# Creando un Objeto Vacío para el Punto de Disparo
En el Hierarchy, se crea un objeto vacío y se nombra "shootPoint". Esto se usará como el punto de origen de las balas.

![Screenshot 2024-10-04 131627](https://github.com/user-attachments/assets/0aa93bbd-16d9-45dc-9007-fee0d74c8aeb)

# Posicionando el shootPoint
Se arrastra el shootPoint como hijo de la pistola del robot y se posiciona donde se desea que las balas sean disparadas. Esto asegura que las balas salgan del lugar correcto.

![Screenshot 2024-10-04 131957](https://github.com/user-attachments/assets/eb2b5ad1-3dc4-4adb-bed9-9998b4ae8f82)

# Actualizando el Script del Robot
Se abre el script de Playermovement y se crean dos nuevas variables públicas de tipo GameObject: prefab y shootPoint. Esto permite referenciar tanto la bala como el punto de disparo desde el script.

![image](https://github.com/user-attachments/assets/fc2ea52e-3e52-4e71-8ff1-496d3d753b69)

# Agregando el Código para Disparar la Bala
Se añade un bloque de código en el script de Playermovement para que cada vez que se presione el botón izquierdo del mouse, la bala aparezca en el shootPoint y se lance hacia adelante.

![image](https://github.com/user-attachments/assets/aa132c6a-c3ec-426e-baf4-c39829de3401)

# Ahora para el script machine
En el script machine para player movement, se agregan las dos variables tipo GameObject, prefab y shootPoint, tal como se hizo anteriormente.

![image](https://github.com/user-attachments/assets/d07c591d-9734-403d-8def-dc58d013c3ce)

# Conectando las Funciones de Disparo en el Graph
Se añade una función más al nodo de sequence y se conectan los nuevos GameObjects al nodo. Esto facilita la integración de la lógica de disparo.

![image](https://github.com/user-attachments/assets/f74de6a6-5225-4e3c-9fbb-327798ffbbb3)

# Implementando la Lógica de Disparo
El if creado se conecta a un nodo de instantiate, donde se envía como argumento el objeto prefab. 
Para obtener la posición y la rotación del shootPoint, se utilizan nodos de get position y get rotation, asegurando que las balas se instancien en el lugar correcto y con la orientación deseada.

![image](https://github.com/user-attachments/assets/a818c709-6155-49ca-ab1c-66b4c8b7d8e2)

[Volver al Readme](README.md)


