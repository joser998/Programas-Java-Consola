package control;
import java.util.Scanner;
import operaciones.Atleta;
public class Principal {
        static Scanner sc = new Scanner (System.in);
        static String nombre;
        static int numeroAtleta, tiempoCarrera, indice=0;
        static Atleta corredores[];
        
        
    public static void main(String[] args) {
        int opc=0;
        System.out.println("Bienvenido a carrera de Atletas\n");
        
     do{
        System.out.println("Selecciona una opcion: \n1.-Guardar Atletas.\n2.-Atleta mas rapido.\n"
                + "3.-Buscar Atleta por registro.\n4.-Buscar por Nombre.\n5.-Salir.\n");    
        opc=sc.nextInt();
        switch(opc){
            case 1:     GuardarAtletas();
                break;
            case 2:     MasRapido();
                break;
            case 3:     BuscarRegistro();
                break;
            case 4:     BuscarporNombre();
                break;
            case 5:     System.out.println("Fin del programa\n");
                break;
        }
     }while(opc!=5);
       
        
        
        
        
       
        
        
    }
    public static void BuscarporNombre(){
        sc.nextLine();
        System.out.println("\n\n¿Que nombre de atleta estas buscando?: ");
        String buscarNombre=sc.nextLine();
        
        for(int i=0; i<corredores.length; i++){
            if(corredores[i].getNombre().equals(buscarNombre)){
                buscarNombre=corredores[i].getNombre();
                indice=i;
            }
            else{
                System.out.println("Nombre no encontrado: "+buscarNombre);
            }
        }
        System.out.println("Nombre encontrado: "+buscarNombre+" el perfil es: "+corredores[indice].toString());
    }
    
    public static void GuardarAtletas(){
        System.out.print("¿Cuantos atletas deseas guardar?: ");
        int cant=sc.nextInt();
        
        corredores= new Atleta[cant];
        
         for(int i=0; i<corredores.length; i++){
            System.out.println((i+1)+".-Perfil: \n");
            sc.nextLine();
            System.out.print("Nombre: ");
            nombre=sc.nextLine();
            System.out.print("Numero Atleta: ");
            numeroAtleta=sc.nextInt();
            System.out.print("Tiempo de Carrera: ");
            tiempoCarrera=sc.nextInt();
            sc.nextLine();
            corredores[i]= new Atleta(nombre, numeroAtleta, tiempoCarrera);
        }
    }
    
    
    public static void BuscarRegistro(){
         System.out.println("\n\n¿Que numero de atleta estas buscando?: ");
        int buscarNumero=sc.nextInt();
        indice=0;
        for(int i=0; i<corredores.length; i++){
            if(corredores[i].getNumeroAtleta() == buscarNumero){
                buscarNumero=corredores[i].getNumeroAtleta();
                indice=i;
            }
            else{
                
                System.out.println("Registro no Encontrado: "+buscarNumero);
            }
        }
        System.out.println("El numero de atleta  "+buscarNumero+" su registro es: "+corredores[indice].toString());
    }
    
    public static void MasRapido(){
        //Mas rapido
        int menor= corredores[0].getTiempoCarrera();
         indice=0;
        for(int i=0; i<corredores.length; i++){
            if(corredores[i].getTiempoCarrera() < menor){
                menor=corredores[i].getTiempoCarrera();
                indice=i;
            }
        }
        System.out.println("El atleta mas rapido es: "+corredores[indice].toString());
    }
}
