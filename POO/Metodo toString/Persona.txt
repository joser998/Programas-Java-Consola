
public class Persona {
    //Atributos
    private String nombre;
    private double sueldo;
    private boolean eliminado;

    public Persona(String nombre, double sueldo, boolean eliminado) {
        this.nombre = nombre;
        this.sueldo = sueldo;
        this.eliminado = eliminado;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public double getSueldo() {
        return sueldo;
    }

    public void setSueldo(double sueldo) {
        this.sueldo = sueldo;
    }

    public boolean isEliminado() {
        return eliminado;
    }

    public void setEliminado(boolean eliminado) {
        this.eliminado = eliminado;
    }
    //El metodo toString() imprime en consola los atributos de esta clase mediante los gettes y setters 
    //Se coloca una notacion @Override para indicar que se esta haciendo una sobre escritura del metodo toString()
    //debido a que este metodo ya existe por que pertenece a la clase object la cual es la clase Padre de todos los
    //objetos en Java.
    
    //Metodo toString()
    @Override
    public String toString() {
        return "Persona\nNombre: " + nombre + " \nSueldo: " + sueldo + "\nEliminado: " + eliminado;
    }

}
