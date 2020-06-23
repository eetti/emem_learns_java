# Java


![java](src/imgs/emem_learns_java.png)

Revisions:

- Classes
- Packages
- main method
- Constructors
- Print statements
- Interfaces


### IAnimal.java

```java

package com.emem.tutorials;

public interface IAnimal {
	public void speak();
	public void print();
	public void eat(String foodItem);

}
```

### Animal.java

```java
package com.emem.tutorials;
public class Animal implements IAnimal {
	
	private String name; //name property
	private int legs; //legs property
	private String sound; //sound property
	private String type; //type property
	
	/*
	 * Default Constructor
	 */
	public Animal() {
		super();
	}
	
	/**
	 * Constructor with single input
	 * @param type
	 */
	public Animal(String type) {
		super();
		this.type = type; 
	}

	/**
	 * Constructor with multiple inputs
	 * @param name
	 * @param legs
	 * @param sound
	 * @param type
	 */
	public Animal(String name, int legs, String sound, String type) {
		super();
		this.name = name;
		this.legs = legs;
		this.sound = sound;
		this.type = type;
	}

	
	/*
	 * Setters and Getters
	 */
	public String getName() {
		return name;
	}
	
	public void setName(String name) {
		this.name = name;
	}
	
	public int getLegs() {
		return legs;
	}
	
	public void setLegs(int legs) {
		this.legs = legs;
	}
	
	public String getSound() {
		return sound;
	}
	public void setSound(String sound) {
		this.sound = sound;
	}

	public String getType() {
		return type;
	}

	public void setType(String type) {
		this.type = type;
	}

	@Override
	public void speak() {
		System.out.println(this.getSound());
	}

	@Override
	public String toString() {
		return "Animal [name=" + name + ", legs=" + legs + ", sound=" + sound + ", type=" + type + "]";
	}

	@Override
	public void print() {
		System.out.println(this.toString());
		
	}


	@Override
	public void eat(String foodItem) {
		// TODO Auto-generated method stub
		
	}

	
}
```

### AnimalFarm.java
```java
package com.emem.tutorials.test;

import com.emem.tutorials.Animal;

public class AnimalFarm {

	public static void main(String[] args) {
		Animal dog = new Animal("Woofy",4,"woof!!","Dog"); //initialize dog object
		Animal cat = new Animal("Jerry",4,"Meow!!","Cat"); //initialize cat object
		Animal chicken = new Animal("Ben",2,"cluck cluck!!","Chicken"); //initialize cat object
        dog.print();
        cat.print();
        chicken.print();
    }
}		
```