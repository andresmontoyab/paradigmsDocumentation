# Programacion Orientada A Objetos.

La programacion oientada a objetos es un paradigma que utliza diferentes herramientas como clases, instancias, referencias, objetos, herencias, polimorfismo y entre otras.

En este documento podremos observar la explicacion de cada uno de los conceptos que arriba se describen.

## Clases

Las clases son los elementos bases de la programacion orientada objeto, en estas podemos definir "objetos" con sus respectivas caracteristicas y comportanmientos.

		public class Car {

		    private int doors;
		    private int wheels;
		    private String model;
		    private String engine;
		    private String colour;

		    public void setModel(String model) {
		        String validModel = model.toLowerCase();
		        if(validModel.equals("carrera") || validModel.equals("commodore")) {
		            this.model = model;
		        } else {
		            this.model = "Unknown";
		        }
		    }

		    public String getModel() {
		        return this.model;
		    }

## Constructores

Los constructores son la forma como inicializamos un objeto, estos deben de tener el mismo nombre de la clase y deberan llevar los paramostros necesarios para que sea construido el objeto.

			public class Account {
			    private String number;
			    private double balance;
			    private String customerName;
			    private String customerEmailAddress;
			    private String customerPhoneNumber;

			    public Account() {
			        this("56789", 2.50, "Default name", "Default address", "default phone");
			        System.out.println("Empty constructor called");
			    }

			    public Account(String number, double balance, String customerName, String customerEmailAddress,
			                   String customerPhoneNumber) {
			        System.out.println("Account constructor with parameters called");
			        this.number = number;
			        this.balance = balance;
			        this.customerName = customerName;
			        this.customerEmailAddress = customerEmailAddress;
			        this.customerPhoneNumber = customerPhoneNumber;
			    }

			    public Account(String customerName, String customerEmailAddress, String customerPhoneNumber) {
			        this("99999",100.55, customerName, customerEmailAddress, customerPhoneNumber);
			    }
			}

Si dentro de la misma clase utilicamos el metodo this(), este llamará a un constructo de la misma clase y la forma como seleccionar que constructor llamar dependerá de los argumentos utilizados.

## Herencia.

Herencia es una principal importante de la programacion orientada objetos, esta consiste en "heredad" caracteristicas o comportamientos de una clase padre a una clase hija.

Clase Padre

			public class Animal {

			    private String name;
			    private int brain;
			    private int body;
			    private int size;
			    private int weight;

			    public Animal(String name, int brain, int body, int size, int weight) {
			        this.name = name;
			        this.brain = brain;
			        this.body = body;
			        this.size = size;
			        this.weight = weight;
			    }

			    public void eat() {
			        System.out.println("Animal.eat() called");

			    }

			    public void move(int speed) {
			        System.out.println("Animal.move() called.  Animal is moving at " +speed);

			    }
			}

Como se puede observar la clase padre tiene unas caracteristicas en particular y unos metodos o comportamientos llamados move and eat.

Clase hija.

La clase hija heredará de Animal con la palabra extends, una vez hecho esto, la clase hija tendrá todas las propiedades y metodos de la clase padre.

			public class Dog extends Animal {

			    private int eyes;
			    private int legs;
			    private int tail;
			    private int teeth;
			    private String coat;

			    public Dog(String name, int size, int weight, int eyes, int legs, int tail, int teeth, String coat) {
			        super(name, 1, 1, size, weight);
			        this.eyes = eyes;
			        this.legs = legs;
			        this.tail = tail;
			        this.teeth = teeth;
			        this.coat = coat;
			    }

			    @Override
			    public void eat() {
			        System.out.println("Dog.eat() called");
			        chew();
			        super.eat();
			    }			

			}

Adicionalmente como pueden observar tanto en la clase hija como en la clase padre existe el metodo eat(), por ende cuando una clase hija tiene el mismo nombre del metodo implementado se conoce como metodo sobreescrito.

## this vs super.

La palabra this hace referencia a la informacion que se encuentra en una misma clase, ya sea atributos, metodos o constructores.

La palabra this hace referencia a la informacion que se encuentra en la clase padre, ya sea atributos, metodos o constructores.

## Reference VS Object VS Instance VS Class

Los terminos anteriores estan altamente relacionados, sin embargo es fundamental clarificar el concepto de cada uno de estos.

	1. Class : Es donde se abstraen las propiedades y comportamientos.

	2. Instancia o Objeto : Es la creacion de un objeto con ayuda de la clase y de la palabra new.

	3. Referencia : Es la direccion en memoria donde esta ubicada el objeto instanciado. 

## Overloading Vs Overridiing.

Overloading son los concidos metodos sobrecargados, que tienen las siguientes condiciones.

	1. Los metodos se deben llamar igual.
	2. Los metodos deben tener diferentes parametros.

Overrinding son los metodos que se implementan tanto en una clase hija o una clase padre.

	1. Significa la definicion de un metodo en la clase hija que ya esta definido en la clase padre con la misma firma.

	2. Mismo nombre y mismos argumetos.

	3. El tipo de retorno puede ser una subclase del tipo de retorno de la clase padre.

## Composicion.

Composicion en una herramienta de OOP similar a la herencia, en la cual compondremos nuestro objeto o clase deseado con la ayuda de otros objetos.


La clase PC esta compuesta por las clases monitor y motherBoard.

			public class PC {

			    private Monitor monitor;
			    private Motherboard motherboard;

			    public PC(Monitor monitor, Motherboard motherboard) {

			        this.monitor = monitor;
			        this.motherboard = motherboard;
			    }
			}

			public class Monitor {
			    private String model;
			    private String manufacturer;
			    private int size;
			    private Resolution nativeResolution;

			    public Monitor(String model, String manufacturer, int size, Resolution nativeResolution) {
			        this.model = model;
			        this.manufacturer = manufacturer;
			        this.size = size;
			        this.nativeResolution = nativeResolution;
			    }
			}

			public class Motherboard {

			    private String model;
			    private String manufacturer;
			    private int ramSlots;
			    private int cardSlots;
			    private String bios;

			    public Motherboard(String model, String manufacturer, int ramSlots, int cardSlots, String bios) {
			        this.model = model;
			        this.manufacturer = manufacturer;
			        this.ramSlots = ramSlots;
			        this.cardSlots = cardSlots;
			        this.bios = bios;
			    } 
			}



