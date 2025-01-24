# Herencia

## Índice
- [Volver al Índice Principal](index.md)
---
- [Herencia en java](#herencia-en-java)
- [Instanciando objetos con herencia](#instanciando-objetos-con-herencia)
- [Sobreescritura de los metodos](#sobreescritura-de-los-metos-herededados)
- [Palabra super](#sobreescritura-palabra-super)

### Herencia en java
```java
package animales;

public class Animal {
    protected void comer(){
        System.out.println("Como muchas veces al día");
    }

    protected void dormir(){
        System.out.println("Duermo muchas horas");
    }
}

class Perro extends Animal{
    public void hacerSonido(){
        System.out.println("Puedo ladrar");
    }
}
```
### Instanciando objetos con Herencia
```java
package animales;

public class Animal {
    protected void comer(){
        System.out.println("Como muchas veces al día");
    }

    protected void dormir(){
        System.out.println("Duermo muchas horas");
    }
}

class Perro extends Animal{
    public void hacerSonido(){
        System.out.println("Puedo ladrar");
    }
}

class PruebaAnimal{
    public static void main(String[] args) {
        System.out.println("*** Ejemplo de Herencia ***");
        System.out.println("Clase Padre, soy un Animal");
        var animal1 = new Animal();
        animal1.comer();
        animal1.dormir();
        // animal1.hacerSonido(); // este metodo no existe en la clase padre

        System.out.println("\nClase Hija, soy un Perro");
        var perro1 = new Perro();
        perro1.comer();
        perro1.dormir();
        perro1.hacerSonido();
    }
}
```

### Sobreescritura de los metos herededados

```java
package animales;

public class Animal {
    protected void comer(){
        System.out.println("Como muchas veces al día");
    }

    protected void dormir(){
        System.out.println("Duermo muchas horas");
    }
}

class Perro extends Animal{
    public void hacerSonido(){
        System.out.println("Puedo ladrar");
    }

    @Override 
    protected void dormir(){
        System.out.println("Duermo 15 horas al dia");
    }

}

class PruebaAnimal{
    public static void main(String[] args) {
        System.out.println("*** Ejemplo de Herencia ***");
        System.out.println("Clase Padre, soy un Animal");
        var animal1 = new Animal();
        animal1.comer();
        animal1.dormir();
        // animal1.hacerSonido(); // este metodo no existe en la clase padre

        System.out.println("\nClase Hija, soy un Perro");
        var perro1 = new Perro();
        perro1.comer();
        perro1.dormir();
        perro1.hacerSonido();
    }
}
```

### Sobreescritura palabra Super
**Se ocupa la palabra super cuando queremos acceder a el metodo del padre cuando ya esta sobreescrito ese mismo método.**
```java
package animales;

public class Animal {
    protected void comer(){
        System.out.println("Como muchas veces al día");
    }

    protected void dormir(){
        System.out.println("Duermo muchas horas");
    }
}

class Perro extends Animal{
    public void hacerSonido(){
        System.out.println("Puedo ladrar");
    }

    @Override
    protected void dormir(){
        System.out.println("Duermo 15 horas al dia");
        System.out.println("Método clase padre: ");
        super.dormir();
    }

}

class PruebaAnimal{
    public static void main(String[] args) {
        System.out.println("*** Ejemplo de Herencia ***");
        System.out.println("Clase Padre, soy un Animal");
        var animal1 = new Animal();
        animal1.comer();
        animal1.dormir();
        // animal1.hacerSonido(); // este metodo no existe en la clase padre

        System.out.println("\nClase Hija, soy un Perro");
        var perro1 = new Perro();
        perro1.comer();
        perro1.dormir();
        perro1.hacerSonido();
    }
}
```
