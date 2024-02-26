# UT3 – Ejercicio refuerzo – Juguetes 

La tienda de juguetes "Juguetrónica" necesita un sistema básico para gestionar su inventario y las ventas de juguetes. Este sistema debe manejar diferentes tipos de juguetes y empleados, de forma simplificada.

## Juguetes

De los juguetes se necesita conocer su nombre, precio sin IVA, edad recomendada y stock. Inicialmente, cada juguete comenzará con un stock por defecto de 100 unidades. Además, hay una serie de tipos de juguetes con información fundamental: 

- Educativo del que se necesita conocer el área educativa. 
- Electrónico del que se necesita conocer el número de pilas requeridas. 
- Mecánico con información sobre el tipo de material con el que se ha construido. 

## Empleados

De los empleados es importante saber el nombre, su DNI y su sueldo base. Podremos disponer de dos tipos de empleados: 

- Vendedor con información sobre su comisión de ventas y el número de ventas y con la cantidad de juguetes vendidos. 
- PersonalAlmacén con información sobre el número de horas extras que ha realizado. 

## Ventas

Dispondremos de una clase Ventas que gestionará las ventas de los juguetes. Esta clase dispondrá de un método llamado ventaJuguete que recibirá un juguete, una cantidad y un vendedor, y devolverá un ticket de venta (clase TicketVenta). Además, en la venta se llamará a un método de control de stock, que controlará el stock de cada juguete. Solo se podrá vender un tipo de juguete en cada venta, aunque de un mismo tipo se podría vender más de un juguete (cierta cantidad de ese juguete). 

## ControladorTienda

Además, se dispondrá de una clase de llamada ControladorTienda que dispondrá de información sobre juguetes y personal. IMPORTANTE: Al menos tendrá un juguete de cada tipo, 2 vendedores y 1 PersonalAlmacén. Opcionalmente podría tener 3 juguetes educativos, 3 electrónicos y 3 mecánicos. Además, se podrá disponer de 4 personas de almacén y 3 vendedores. 

## Se pide: 

1. Crear todas las clases, junto con su herencia, getter/setter, toString. 
2. Crear un método toString que muestre la información sobre la tienda, es decir, muestre los juguetes que hay disponibles, junto con sus empleados. Solo deberá mostrar lo que se tenga disponible. 
3. Desarrollar la clase TicketVenta completamente. En el propio constructor se deberá calcular el coste de la venta, teniendo en cuenta que solo recibirá información sobre quién ha realizado la venta (nombre y dni), y el nombre del juguete vendido, su precio unitario y la cantidad. 
4. La clase TicketVenta dispondrá de un método que se llamará getTicketVenta que devolverá un String con la información sobre el ticket, el coste de la venta y la fecha (será la fecha y hora del momento al que se invoque este método). Para calcular el coste de venta se dispondrá de un método privado que aplicará un IVA normal para los juguetes. 
5. La clase TicketVenta dispondrá de otros métodos similares a los anteriores, que recibirá además como parámetro descuento del vendedor, que permitirá descontar algo sobre la propia venta. Se deberá reflejar sobre el propio String devuelto. 
6. Los vendedores dispondrán de un método que permita calcular la cantidad obtenida de comisiones de ventas. Para este cálculo se tendrá en cuenta que si el número de ventas es mayor de 5 tiene una comisión del 2%, si es mayor de 10, un 4% y si es mayor de 30, un 6%. Además, podrá tener un incremento del 2% adicional si el número de juguetes vendido es mayor de 20 unidades. 

NOTA: Se puede obviar alguna de las clases si ves que su funcionalidad se puede meter en otra. De forma que nos ahorremos código.
