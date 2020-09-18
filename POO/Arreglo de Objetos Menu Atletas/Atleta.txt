package operaciones;

public class Atleta {
    //Atributos
    String nombre;
    int numeroAtleta, tiempoCarrera;

    //Constructor
    public Atleta(String nombre, int numeroAtleta, int tiempoCarrera) {
        this.nombre = nombre;
        this.numeroAtleta = numeroAtleta;
        this.tiempoCarrera = tiempoCarrera;
    }

    
    public String getNombre() {
        return nombre;
    }
    public int getTiempoCarrera() {
        return tiempoCarrera;
    }
    public int getNumeroAtleta() {
        return numeroAtleta;
    }
    

    @Override
    public String toString() {
        return "Atleta{" + "nombre=" + nombre + ", numeroAtleta=" + numeroAtleta + ", tiempoCarrera=" + tiempoCarrera + '}';
    }
    
    
    
    
    
    
    
    
    
}   
