<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

## Actividad 1
```java
abstract class Vehiculo {
    
    abstract void acelerar();
    abstract void frenar();
    abstract void girar();
}

class Coche extends Vehiculo {

    @Override
    void acelerar() {
        System.out.println("El coche acelera");
    }

    @Override
    void frenar() {
        System.out.println("El coche frena");
    }

    @Override
    void girar() {
        System.out.println("El coche gira");
    }

 
}

class Bicicleta extends Vehiculo {

    @Override
    void acelerar() {
        System.out.println("La bicicleta acelera");
    }

    @Override
    void frenar() {
        System.out.println("La bicicleta frena");
    }

    @Override
    void girar() {
        System.out.println("La bicicleta gira");
    }
    
}

class Moto extends Vehiculo {

    @Override
    void acelerar() {
        System.out.println("La moto acelera"); 
    }

    @Override
    void frenar() {
        System.out.println("La moto frena");
    }

    @Override
    void girar() {
        System.out.println("La moto gira");
    }
    
}
```