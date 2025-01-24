# Variables

## Índice

- [Volver al Índice Principal](index.md)
---
- [Ejercicio de reserva de hoteles](#ejercicio-de-reserva-de-hoteles)


Variables

### Ejercicio de reserva de hoteles

```java
import java.sql.SQLOutput;

public class ReservaHoteles {
    public static void main(String[] args) {
        /*
        Sistema de reserva de Hoteles

        Captura el detalle de la reservacion de hoteles.

        El detalle que se debe de capturar es:
        - Nombre del cliente
        - Dias de estancia
        - Tarifa diaria
        - Indicar si la habitacion cuenta con vista al mar

        Debe asignar valores iniciales y mandar a imprimir el valor de cada variable.
        Por ultimo se les pide modificar algunos valores de la reservacion y mandar a imprimr nuevamente cada
        variable para observar los cambios
        * */

        System.out.println("*** Reserva de hoteles ***");

        //Definimos variables
        var nombreCliente="Miguel flores";
        var diasEstancia=7;
        var tarifaDiaria=1300;
        var tienesVistaMar=true;

        //Mostramos el detalle de la reserva con soutv (con esto imprimimos las variables)
        System.out.println("nombreCliente = " + nombreCliente);
        System.out.println("diasEstancia = " + diasEstancia);
        System.out.println("tarifaDiaria = " + tarifaDiaria);
        System.out.println("tienesVistaMar = " + tienesVistaMar);

        //Modificando valores
        diasEstancia=4;
        tarifaDiaria=1111;
        tienesVistaMar=false;

        //Nuevos datos de la reservacion
        System.out.println("Nuevos datos de la reservacion");
        System.out.println("nombreCliente = " + nombreCliente);
        System.out.println("diasEstancia = " + diasEstancia);
        System.out.println("tarifaDiaria = " + tarifaDiaria);
        System.out.println("tienesVistaMar = " + tienesVistaMar);
    }
}
```

***