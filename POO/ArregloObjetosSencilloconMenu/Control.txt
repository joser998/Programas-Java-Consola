/*
Arreglo de objetos en Java
*/
/*
    Este programa muestra un menu con 2 opciones guardar perfiles y mostrar perfiles...
    pedimos datos mediante opcion 1 con el arreglo de objetos de forma estatica para que exista en toda la clase
    pero la inicializacion del mismo esta dentro del case 1 para poder mandarlo al metodo que pide los datos
*/
package control;
import java.util.Scanner;
import operaciones.Perfiles;
public class Control { 
    static Perfiles perfiles[]; //Declaracion del arreglo de objetos de forma estatica para que el mismo exista en toda la clase
    static Scanner sc = new Scanner (System.in); //Clase Scanner estatica
    static String nombre,apPat,apMat; //atributos estaticos de la clase para que existan en toda la clase
    static int edad, cantidad; //atributos estaticos de la clase para que existan en toda la clase
    public static void main(String[] args) {
    int opc=0;
    
    System.out.println("Bievenido a Arreglo de Objetos\n");   
    
    
    do{      
    System.out.println("Selecciona una opcion:\n1.-Pedir Datos.\n2.-Mostrar Datos.\n3.-Salir\n");  
    opc=sc.nextInt();
        switch(opc){
            case 1:     sc.nextLine(); //Limpiamos buffer
                        System.out.println("¿Cuantos perfiles deseas guardar?: ");
                        cantidad=sc.nextInt();
                        perfiles=new  Perfiles[cantidad]; //Inicializacion de arreglo de objetos con atributo cantidad                        
                        PedirDatos(); //Llamada a metodo para pedir datos dentro de esta misma clase
            break;            
            case 2:     sc.nextLine(); //Limpiamos buffer
                        MostrarDatosDeClasePerfiles();//Invocamos metodo para mostrar datos desde otro metodo en clase Perfiles 
            break;           
            case 3:     System.out.println("Fin del Programa\n\n");
            break;
            default:    System.out.println("Opcion no valida, intentalo nuevamente...\n\n");
        }
    }while(opc!=3);
      
    }
    public static void MostrarDatosDeClasePerfiles(){
        System.out.println("Mostrando Datos\n");
               for(int i=0; i<perfiles.length; i++){
                   sc.nextLine();
                   perfiles[i].Mostrar(); //Llamamos metodo para mostrar datos en Clase Perfiles, usando el arreglo de objetos
                                             //dentro del for y con el operador punto para interceder al metodo Mostrar()                       
               }
    }
    
    public static void PedirDatos(){
        System.out.println("Se Guardaran "+cantidad+" perfiles.\n"); 
        sc.nextLine();
        for(int i=0; i<perfiles.length; i++){         
            System.out.println((i+1)+".-Perfil:");
            System.out.print("Nombre: ");
            nombre=sc.nextLine();
            System.out.print("Apellido Paterno: ");
            apPat=sc.nextLine();
            System.out.print("Apellido Materno: ");
            apMat=sc.nextLine();
            System.out.print("Edad: ");
            edad=sc.nextInt();
            sc.nextLine();
            perfiles[i]= new Perfiles(nombre,apPat,apMat,edad ); //Mandamos todos los datos del arreglo de objetos al 
                                                                    //constructor con mismos parametros de clase Perfiles
        }
    }   
}