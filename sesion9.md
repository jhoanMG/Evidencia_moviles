<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

## Superclase Conversor
public abstract class Conversor {
    protected String unidadOrigen;
    protected String unidadDestino;

    public Conversor(String unidadOrigen, String unidadDestino) {
        this.unidadOrigen = unidadOrigen;
        this.unidadDestino = unidadDestino;
    }
    
     public abstract double convertir(double cantidad);
}

## Subclase Temperatura
public class Temperatura extends Conversor {

    public Temperatura(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
        if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Fahrenheit")) {
            // Celsius a Fahrenheit
            return (cantidad * 9 / 5) + 32;
        } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Celsius")) {
            // Fahrenheit a Celsius
            return (cantidad - 32) * 5 / 9;
        } else if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Kelvin")) {
            // Celsius a Kelvin
            return cantidad + 273.15;
        } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Celsius")) {
            // Kelvin a Celsius
            return cantidad - 273.15;
        } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Kelvin")) {
            // Fahrenheit a Kelvin
            double celsius = (cantidad - 32) * 5 / 9;
            return celsius + 273.15;
        } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Fahrenheit")) {
            // Kelvin a Fahrenheit
            double celsius = cantidad - 273.15;
            return (celsius * 9 / 5) + 32;
        } else {
            throw new IllegalArgumentException("Unidades de temperatura no compatibles");
        }
    }
}

## Subclase Longitud
public class Longitud extends Conversor {

    public Longitud(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
     if (unidadOrigen.equals("Metros") && unidadDestino.equals("Pies")) {
            // metros a pies
            return (cantidad * 3.28084) ;
    } else if (unidadOrigen.equals("Pies") && unidadDestino.equals("Metros")) {
            // Pies a metros
            return (cantidad * 0.3048) ;
    } else if (unidadOrigen.equals("Kilometros") && unidadDestino.equals("Millas")) {
            // Kilometros a millas
            return (cantidad * 0.621371) ;
    } else if (unidadOrigen.equals("Millas") && unidadDestino.equals("Kilometros")) {
            // Millas a Kilometros
            return (cantidad  * 1.60934) ;
    } else if (unidadOrigen.equals("Centimetros") && unidadDestino.equals("Pulgadas")) {
            // Centímetros a Pulgadas.
            return (cantidad * 0.39) ;
    } else if (unidadOrigen.equals("Pulgas") && unidadDestino.equals("Centimetros")) {
            // Pulgadas a centimetros.
            return (cantidad * 2.54) ;
            
    } else if (unidadOrigen.equals("Yardas") && unidadDestino.equals("Metros")) {
            // Yardas a Metros
            return (cantidad * 0.9144) ;
    } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Yardas")) {
            // Metros a Yardas
            return (cantidad * 0.9144) ;
    
    } else if (unidadOrigen.equals("Millas Nauticas") && unidadDestino.equals("Kilogramos")) {
            // Millas Nauticas a kilogramos
            return (cantidad * 1.852) ;

    } else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Millas Nauticas")) {
            // Kilogramos a Millas Nauticas
            return (cantidad * 0.539957) ;
    } else if (unidadOrigen.equals("Micrometros") && unidadDestino.equals("Milimetros")) {
            // Micrometros a Milimetros
            return (cantidad * 0.001) ;
    } else if (unidadOrigen.equals("Milimetros") && unidadDestino.equals("Micrometros")) {
            // Milimetros a Micrometros
            return (cantidad * 1000) ;
    } else if (unidadOrigen.equals("Decimetros") && unidadDestino.equals("Metros")) {
            // Decimetros a metros
            return (cantidad * 0.1) ;
    } else if (unidadOrigen.equals("Decimetros") && unidadDestino.equals("Metros")) {
            // Decimetros a metros
            return (cantidad * 0.1) ;
    } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Decimetros")) {
            // Metros a Decímetros.
            return (cantidad * 0.1) ;
    } else {
            throw new IllegalArgumentException("Unidades de Longitud no compatibles");
       
   
    }
    }
}
## Subclase Peso
public class Peso extends Conversor {

    public Peso(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
       if(unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2.20462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.453592;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.00220462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 453.592;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 16;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.0625;
            return resultado;
        }else if (unidadOrigen.equals("Gramos ") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 0.035274;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 28.3495;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2204.62;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000453592;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000000001;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else{
            throw new IllegalArgumentException("Pesos no compatibles");
        }
    }

}

5. Subclase Divisas

## public class Divisas extends Conversor{

    public Divisas(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
       if (unidadOrigen.equals("Dolar") && unidadDestino.equals("Euro")){
            double resultado = cantidad * 0.98;
            return resultado;
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Dolar")) {
            double resultado = cantidad * 1.06;
            return resultado;
        } else if (unidadOrigen.equals("Dólar") && unidadDestino.equals("Peso colombiano")) {
            double resultado = cantidad * 4073.34;
            return resultado;
        } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Dólar")) {
            double resultado = cantidad * 0.00025;
            return resultado;
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Peso colombiano")) {
            double resultado = cantidad * 4312.24;
            return resultado;
        } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Euro")) {
            double resultado = cantidad * 0.00023;
            return resultado;
        }else {
            throw new IllegalArgumentException("Divisas no compatibles");
        }
    }
    
}



