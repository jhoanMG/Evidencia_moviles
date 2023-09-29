<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

## ACTIVIDAD 4

public class Producto {
    public String Nombre;
    private double Precio;
    protected int Cantidad;
    final String Fabricante;
    static String Marca;
    String Categoria;

    public Producto(String Nombre, double Precio, int Cantidad, String Fabricante, String Categoria) {
        this.Nombre = Nombre;
        this.Precio = Precio;
        this.Cantidad = Cantidad;
        this.Fabricante = Fabricante;
        this.Categoria = Categoria;
    }

    public String getNombre() {
        return Nombre;
    }

    public void setNombre(String Nombre) {
        this.Nombre = Nombre;
    }

    public double getPrecio() {
        return Precio;
    }

    public void setPrecio(double Precio) {
        this.Precio = Precio;
    }

    public int getCantidad() {
        return Cantidad;
    }

    public void setCantidad(int Cantidad) {
        this.Cantidad = Cantidad;
    }

    public static String getMarca() {
        return Marca;
    }

    public static void setMarca(String Marca) {
        Producto.Marca = Marca;
    }

    public String getCategoria() {
        return Categoria;
    }

    public void setCategoria(String Categoria) {
        this.Categoria = Categoria;
    }
}

## MAIN

public static void main(String[] args) 
    {
   Producto producto = new Producto("Producto1", 29.99, 100, "Fabricante1", "Electrónicos");


        System.out.println("Nombre: " + producto.getNombre());
        System.out.println("Precio: " + producto.getPrecio());
        System.out.println("Cantidad: " + producto.getCantidad());
        System.out.println("Fabricante: " + producto.Fabricante);
        System.out.println("Marca: " + Producto.getMarca());
        System.out.println("Categoría: " + producto.getCategoria());


        producto.setPrecio(39.99);
        producto.setCantidad(50);
        producto.setCategoria("Electrónicos y Accesorios");


        Producto.setMarca("Nueva Marca");


        System.out.println("\nDetalles Actualizados:");
        System.out.println("Nombre: " + producto.getNombre());
        System.out.println("Precio: " + producto.getPrecio());
        System.out.println("Cantidad: " + producto.getCantidad());
        System.out.println("Fabricante: " + producto.Fabricante);
        System.out.println("Marca: " + Producto.getMarca());
        System.out.println("Categoría: " + producto.getCategoria());
    
    }
    
}



