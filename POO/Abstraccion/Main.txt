public class Main {
	public static void main(String[] args) {
		//Instancia de Clase Planta....
		//Si es posible instanciar de esta clase pues no esta como clase abstracta
		Planta pl = new Planta();
		//Invocamos metodo alimentarse de clase Planta
		pl.alimentarse();
		
		
		//Instancia clase AnimalCarnivoro...
		AnimalCarnivoro animal = new AnimalCarnivoro();
		//Invocamos metodo alimentarse de clase AnimalCarnivoro
		animal.alimentarse();
		
		//Instancia clase AnimalHerbivoro...
		AnimalHerbivoro herbivoro = new AnimalHerbivoro();
		//Invocamos metodo alimentarse de clase AnimalHerbivoro
		herbivoro.alimentarse();
		
		

	}

}
