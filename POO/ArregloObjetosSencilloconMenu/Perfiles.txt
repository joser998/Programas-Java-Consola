package operaciones;
import java.util.Scanner;
public class Perfiles {
    //Clase Scanner
    Scanner sc=new Scanner (System.in);
    //Atributos
    String nombre, apPat, apMat;
    int edad, cant;

    //Constructor de Clase
    public Perfiles(String nombre, String apPat, String apMat, int edad) {
        this.nombre = nombre;
        this.apPat = apPat;
        this.apMat = apMat;
        this.edad = edad;
    }
    
     public void Mostrar(){  //Metodo muestra todos los atributos guardados en clase Control, no necesitamos hacer instancia
                                //puesto que los metodos getters se encuentran dentro de la misma clase...
        sc.nextLine();
        System.out.println("Nombre: "+getNombre());
        System.out.println("Apellido Paterno: "+getApPat());
        System.out.println("Apellido Materno: "+getApMat());
        System.out.println("Edad: "+getEdad()); 
         System.out.println("\n\n");
     }
    
    //Getters y Setters 
    public String getNombre() {
        return nombre;
    }
    public String getApPat() {
        return apPat;
    }
    public String getApMat() {
        return apMat;
    }
    public int getEdad() {
        return edad;
    }
}
