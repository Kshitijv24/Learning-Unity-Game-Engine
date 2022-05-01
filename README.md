# Learning-Unity-Game-Engine

DATE:	02-12-2021
	
1. Destroying Objects
    - destorying my object that the script is attached to
    - destorying object with my object that script is attached to
   
2. Detecting Mouse Clicks
    - destorying object with mouse click
   
3. Taking Keyboard input
    - destorying object with Keyboard input like pressing the space key
   
4. Adding Physics to the object
	- like adding forse in the pertecular direction to the object to make
	  it move using Vectors
	- moving objects with Velocity
	
5. Detecting Collisions
	- by detecting collisions we can make any object that collied with
	  my object disappear
	  
6. Loading New Level using UnityEngine.SceneManagement
	- we can load any scene or level with the press of a keyboard key.
	
7. Display Text On The Screen
	- we displyed "You Win" text on the screen after
	
DATE:	03-12-2021
	
8. Spawning GameObjects in Unity 3D
	- learned how to spawn a 3D game object
	- learned how to spawn a 3D game object with the keyboard input
	- learned how to spawn a 3D game object with the mouse click at mouse position
	- changing colour on collision(One colour or Random)
	
9. Creating Materials for Unity 3D objects
	- and changing there properties within C# Script

DATE:	04-12-2021

10. Prefabs and Materials in Unity 3D
	- learned how to make Prefabs of objects in unity
	- learned how to make and apply materials to the objects
	
11. Creating 3D Player Movement
	- learned how to rotate main camera to where player goes
	- fixing some camera view problems so that our input don't change
	  when player get too far away from camera
	  
12. Creating Collectable Coins
	- making some Sphere object and convert them into coins
	- making Coins child of a parent empty object "Coins Parent" so when we 
	  change there shapes but want to keep there rotation same as parent 
	- making our player can collect coins when it touch them and after
	  that make coins object disappear
	- Adding Rotation to the Coins so they spin instead of stay still
	
13. Playing Audio in Unity Engine
	- learned how to play audio when our player collect a coin
	
DATE:	05-12-2021

14. Taking input form mouse
	
	- Taking input form mouse in screen cordinates
	  and converting it to the world cordinates
	- Vector3 mousePosition = Camera.main.ScreenToWorldPoint(Input.mousePosition);
	
15. 2D Player Movement using trasform component of unity without using physics(rigidbody2D)
	
	- 2D Player Movement using trasform component of unity
	  without using physics(rigidbody2D)
	- 2D Player follows our mouse position
	- 2D Player goes where our mouse clicks
	
16. Working with 2D Sprites
	
	- make our 2d sprite player move in horizontal directions
	- make our 2d sprite player flip when it goes from left to right
	
DATE:	06-12-2021

17. Working with Tags
	
	- Search and Find any one GameObject with tag
	  Using-> 
	  GameObject cube = GameObject.FindWithTag("Cube");
	  
	- Search and Destroy all game objects with the same tag with the help of Arrays
	  Using-> 
	  GameObject[] cubes;
	  cubes = GameObject.FindGameObjectsWithTag("Cube");
	  
	- Destroy an game object with the tag "Cube" with mouse click
	  Using-> 
	  void OnMouseDown() function
	  
DATE:	07-12-2021

HOLIDAY FOR ESCAPING FROM BURNOUT

DATE:	08-12-2021

18. Adding Delay Using Invoke Function

	- Destroy all game objects after a delay using Invoke Function
	  Using-> 
	  Invoke("DestroyAll", 2f);
	  
19. Adding Delay Using Coroutine
	
	- IEnumerator FunctionName(){
	     yield return new WaitForSeconds(2);
	  }
	- call in the start function
	Using-> 
	StartCoroutine(FunctionName());
	- Adding delay inbetween Loops
	- Passing delay value in function parameters
	
20. Finding Game Objects and doing Advanced stuff to it

	- finding game object using GameObject.Find
	- finding game object child
	  Using-> 
	  GameObject.Find("Cube/Cube2/Enemy");
	- setting an game object to inactive
	  Using-> 
	  GameObject.Find("Cube").SetActive(false);
	  
21. Working with Rigidboyd Wihtin C# script

	- setting the default value of game object gravity
	- changing the default Mass value
	
22. Working with Mesh Renderer Wihtin C# script
	- changing the colour of game object 
	  Using-> 
	  GetComponent<MeshRenderer>().material.color = Color.blue;
	  
DATE:	09-12-2021

23. Accessing a C# Script form another C# Script
	
	- changing a script variable values from another script
	- Accessing a game object value in a script form a script that is attached to that game object
	  Using-> 
	  GameObject.Find("Cube").GetComponent<AnotherScript>().lives = 5;
	- same way changing a game object Gravity value in a script form a script that is attached to that game object
	  Using-> 
	  GameObject.Find("Cube").GetComponent<Rigidbody>().useGravity = false;

DATE:	10-12-2021

24. Accessing the rigidbody component of a game object from his parent game object

	- changing the gravity function of a child game object form a parent game object
	  Using-> 
	  GetComponentInChildren<Rigidbody>().useGravity = true;

25. Learning Vectors in Unity in-depth

	- Learning the 3 Axis of Vector3 -> X,Y and Z
	- Printing the Position of all 3 Axis of a game object using Vector3
	  Using-> 
	  
	Vector3 position;
	void Start(){
		position = new Vector3(1f, 2f, 3f);
		print(position.y);
	}
26. Working with the Transform Component of a 3D game object
  
	- printing the game object default position values
	  Using-> 
	  print(transform.position);
	- we know that we can not change the game object position values directly
	  for that we need to use a new Vector3 for example
	  Using-> 
	  transform.position = new Vector3(2f, transform.position.y, transform.position.z);
	- constantly changing the game object position
	  Using-> 
	  void Update(){
		transform.position += new Vector3(2f, 0, 0);
	  }
	- Another way of achiving same thing
	  Using-> 
	  transform.position += transform.up * speed * Time.deltaTime;

DATE:	11-12-2021

	- transform.position += transform.forward * speed * Time.deltaTime;  // this means (0,0,1);
	- transform.position += transform.right * speed * Time.deltaTime;    // this means (1,0,0);
	
27. Working with transform.Translate Game Component

	- moving our 3D game object using Unity built in feature called Transform
	- transform.Translate(speed * Time.deltaTime, 0, 0);
	
28. Working with Rotation of 3D game object

	- rotating our game object using Unity built in feature called Rotate
	- transform.Rotate(0, speed, 0);

29. Working with Scale function in Unity

	- changing game object size using Unity built in feature called localScale
	- transform.localScale += new Vector3(0, speed, 0);
	
	- another way of doing the same thing 
	- transform.localScale += transform.up * speed;
	
	- rotating and scaling game object at the same time to test the 3D game object Physics behaviour

DATE:	12-12-2021

BREAK

DATE:	13-12-2021

31. Working with Arrays

	-  creating an array of game objects

30. Working with Prefabs

	- created a prefab of a 3D sphere game object so it can be used with the same properties 
	  as many time as we want
	  
31. Working with Instantiating Game Object

	- Spawning a ball game object from a cube
	  Using-> 
	  Instantiate(ball, transform.position, Quaternion.identity); 
	  
	- Spawning a game object form a mouse click
	  Using-> 
	  if (Input.GetMouseButtonDown(0)){
	      Instantiate(ball, transform.position, Quaternion.identity);
          }
	
32. Working with Random Component of Unity Engine
	
	- Randomly creating an array of game objects and instantiating it
	  Using-> 
	  public GameObject[] balls;
	  
	  if (Input.GetMouseButtonDown(0)){
		int randomNumber = Random.Range(0, balls.Length);
		Instantiate(balls[randomNumber], transform.position, Quaternion.identity);
	  }

	- Creating a Random Ball Genrator function to handle all our random gen tasks
	
	- Calling random ball function repeatedly using InvokeRepeating
 	
	- public GameObject[] balls;
	
	- void RandomBallGen(){
          int randomNumber = Random.Range(0, balls.Length);
          Instantiate(balls[randomNumber], transform.position, Quaternion.identity);
          }
	
	- void Start(){
          InvokeRepeating("RandomBallGen", 1f, 1f);
          }

DATE:	14-12-2021

	- Stopping the InvokeRepeating function by
	  Using-> CancelInvoke("RandomBallGen");
	  after the left mouse click
	  
33. All the ways of getting inputs in unity

	- changing the colour of a game object to yellow while our space key is down and when we realise it change it to green
	  by using-> 
	    if (Input.GetKeyDown(KeyCode.Space)){
            GetComponent<Renderer>().material.color = Color.green;
        }

        if (Input.GetKeyUp(KeyCode.Space)){
            GetComponent<Renderer>().material.color = Color.yellow;
        }

	- using different function to get the input using Unity Input Manager
	  by using->
	  
	  if (Input.GetButtonDown("Jump")){
            GetComponent<Renderer>().material.color = Color.red;
      }

	- creating multiple game object and managing them from unity game engine interface using Arrays

DATE:	15-12-2021

	- Working with input.getAxis in unity to get the more smooth movement rather than using 
	  anyother form of input because it gives us movement values in float variable not in int
	  so it can go in decimal values
	  
	- testing it in Horizontal and Vertical built-in unity function
	
	 float xInput = Input.GetAxis("Horizontal");
	 
	 float yInput = Input.GetAxis("Vertical");
	 
	- if we don't press any key than the value of xInput will be 0 in Idle
	  and when we press left arrow key on keyboard than the value of xInput will slowley increase to -1
	  
	- -1 is the minimum value of left horizontal input 
	
	- same when we press right arrow key on keyboard than the value of xInput will slowley increase to +1
	
	- +1 is the maximum value of right horizontal input
	
	- If we print the xInput we can clearly see the value of them changing in float value from 0 to 0.1,0.5,0.9 to 1
	  when we press right arrow key Which is the maximum value of horizontal input

	- Same as when we press left arrow key we can see the value of xInput changing from 0 to -0.1,-0.5,-0.9 to -1
	  Which is the minimum value of horizontal input

DATE:	16-12-2021

34. Working with Time.deltaTime

	- we know that the update function called every second so if we write our player movement code simply
	  in update function that because update function runs every second than all the computers gonna have 
	  different speed because of FPS
	  
	- to fix this issue we gonna use Time.deltaTime in update function to make our player movement
	  FPS independent and make it update in real seconds 
	  
	  using-> 
	  
	- float xInput = Input.GetAxis("Horizontal") * speed * Time.deltaTime;
    	- float yInput = Input.GetAxis("Vertical") * speed * Time.deltaTime;

    	- transform.Translate(xInput, yInput, 0);
	
	- input.GetAxisRaw is another way of taking input from the player but there is slight differance in this one
	  this function takes input in integer value raher than float values so the player movement is not that smooth
	  compared to input.GetAxis
	
	- float xInput = Input.GetAxisRaw("Horizontal") * speed * Time.deltaTime;
    	- float yInput = Input.GetAxisRaw("Vertical") * speed * Time.deltaTime;

    	- transform.Translate(xInput, yInput, 0);

DATE:	17-12-2021
	
35. Using Unity built-in input system to get input form mouse

	- we have a input function in unity called "Fire1" that we can use to get input form our left mouse click
	
	Using->
	
	- if (Input.GetButtonDown("Fire1")){
          print("left click");
      }
	  
	- here "Fire1" refers to as left mouse click
	
36. Creating a Player Controller with Jump Functionality

	public class PlayerController : MonoBehaviour
{
    public float speed;
    public float jumpForse;

    Rigidbody rb;
    float xInput, yInput;
    bool jump = false;

    private void Awake(){
        rb = GetComponent<Rigidbody>();
    }

    void Update(){
        xInput = Input.GetAxis("Horizontal") * speed;
        yInput = Input.GetAxis("Vertical") * speed;

        if (Input.GetKeyDown(KeyCode.Space)){
            jump = true;
        }
    }

    private void FixedUpdate(){
        rb.velocity = new Vector3(xInput, rb.velocity.y, yInput);

        if(jump == true){
            Jump();
            jump = false;
        }
    }

    void Jump(){
        rb.AddForce(0, jumpForse, 0);
    }
}

DATE:	18-12-2021

37. Complete Player Movement with Jump and Shooting Machanics

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float speed;
    public float jumpForse;

    public float bulletSpeed;
    bool shoot = false;
    public GameObject bullet;
    public Transform bulletPos;

    Rigidbody rb;
    float xInput, yInput;
    bool jump = false;

    private void Awake(){
        rb = GetComponent<Rigidbody>();
    }

    void Update(){
        xInput = Input.GetAxis("Horizontal") * speed;
        yInput = Input.GetAxis("Vertical") * speed;

        if (Input.GetKeyDown(KeyCode.Space)){
            jump = true;
        }

        if (Input.GetMouseButtonDown(0)){
            shoot = true;
        }
    }

    private void FixedUpdate(){
        rb.velocity = new Vector3(xInput, rb.velocity.y, yInput);

        if(jump == true){
            Jump();
            jump = false;
        }

        if(shoot == true){
            Shoot();
            shoot = false;
        }
    }

    void Jump(){
        rb.AddForce(0, jumpForse, 0);
    }

    void Shoot(){
        GameObject bulletSpawn = Instantiate(bullet, bulletPos.position, bullet.transform.rotation);
        bulletSpawn.GetComponent<Rigidbody>().velocity = new Vector3(0, 0, bulletSpeed);
    }
}

DATE:	19-12-2021

	- added enemys and gravity to the bullets in the prototype demo
	
	- created a C# Script called "DestroyObject" and added it to the bullet prefab
	  so the enemys will destory after colliding with the bullet
	  
	private void OnCollisionEnter(Collision collision){
        if(collision.gameObject.tag == "Enemy"){
            Destroy(collision.gameObject);
        }
    }
	
38. Working with Triggers in Unity

	- created a 3D cube game object called "Color Changer" and created a script for it called "ColorChangerScript"
	
	- and made it so when ever our player game object enter the Color Changer cube than our player changes color to yellow
	
	- and when it exits it changes our player color to green
	
	public class ColorChangerScript : MonoBehaviour
{
    private void OnTriggerEnter(Collider col){
        col.gameObject.GetComponent<Renderer>().material.color = Color.yellow;
    }

    private void OnTriggerExit(Collider col){
        col.gameObject.GetComponent<Renderer>().material.color = Color.green;
    }
}

DATE:	20-12-2021

BREAK

DATE:	21-12-2021

39. Working with the LookAt Unity game engine Function in-depth

	- we created an cube 3D game object and a sphere 3D game object
	
	- attached a C# script called "LookAtTheObject" to the cube
	
	- using this script our cube gonna follow the sphere movement where it goes
	
	- void Update(){
        transform.LookAt(target.transform);    
    }
	
	- working with the local and global interface of UnityEngine
	
	- restrict the cube from follow y axis of sphere
	
	- using->
	
	void Update(){
        Vector3 newPos = new Vector3(target.transform.position.x, transform.position.y, target.transform.position.z);
        transform.LookAt(newPos);
    }
	
40. Working with the UnityEngine.SceneManagement in-depth

	- creating two different scenes and changing from one scene to another by pressing left mouse click
	
using UnityEngine;
using UnityEngine.SceneManagement;

public class LevelLoaderScript : MonoBehaviour
{
    void Update(){
        if (Input.GetMouseButtonDown(0)){
            LoadLevel();
        }       
    }

    void LoadLevel(){
        SceneManager.LoadScene("Level2");
    }
}

DATE:	22-12-2021	

	- changing Scenes by using Build Index
	
	using->
	
	- SceneManager.LoadScene(1);
	
	- changing Scenes from next level to previous level by attaching the same C# Script to both level game object
	  and by using public build index number that we can change form the unity interface
	
	- Reloading a level from C# Script
	
using UnityEngine;
using UnityEngine.SceneManagement;

public class LevelLoaderScript : MonoBehaviour
{
    void Start(){
        print("level Loaded ");    
    }

    void Update(){
        if (Input.GetMouseButtonDown(0)){
            ReloadLevel();
        }       
    }

    void ReloadLevel(){
        SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex);
    }
}

DATE:	23-12-2021

41. Understanding the OOPS Concepts in Unity Game Engine in-depth

	- Creating a C# Script called "CarScript" but removing the MonoBehaviour inharitance form it 
	  and not attaching to it any game object to create a Structure for other Script to use from it
	  
	- Creating an another C# Script and using all the properties of that script by creating an instense of that class which is a Object
	
	- creating two different dummy car modles from "CarScript" class using objects and giving them different properties and printing it
	  to the console to see the differance
	  
	- Creating a Constructer insted of using default constructer 
	
	- Constructer Overloading
	
	- creating multiple constructer to use constructer overloading
	  

	 public class CarScript {
    
    public float speed;
    public string color;
    public int highestSpeed;
    
    public CarScript(){
        Debug.Log("CarScript() is called");
    }

    public CarScript(float speed){
        Debug.Log("CarScript(float speed) is called");
    }

    public CarScript(float speed, string color){
        Debug.Log("CarScript(float speed, string color) is called");
    }

    public void Move(){
        Debug.Log("Moving");
    }

    public void ApplyBreak(){
        Debug.Log("Applying Break");
    }

    public void carSpeed(){
        Debug.Log(speed);
    }
}



public class CubeScript : MonoBehaviour
{
    void Start(){
        CarScript myCar = new CarScript();
        myCar.speed = 10.5f;
        myCar.color = "red";
        myCar.highestSpeed = 20;

        CarScript otherCar = new CarScript();
        otherCar.speed = 14.5f;
        otherCar.color = "blue";
        otherCar.highestSpeed = 50;

        CarScript myNewCar = new CarScript(5f);
        CarScript myOldCar = new CarScript(10f, "red");

        myCar.carSpeed();
        myCar.Move();
        myCar.ApplyBreak();
        Debug.Log(myCar.color);
        Debug.Log(myCar.highestSpeed);


        otherCar.carSpeed();
        otherCar.Move();
        otherCar.ApplyBreak();
        Debug.Log(otherCar.color);
        Debug.Log(otherCar.highestSpeed);
    }
}

DATE:	24-12-2021

42. Understanding what this keyword means

	public float speed;
    	public string color;
	
	public CarScript(float speed, string color){
        this.speed = speed;
        this.color = color;
        Debug.Log("CarScript(float speed, string color) is called");
    }
	
43. Using System.Serializable To Initialize Objects

	[System.Serializable]
	public class CarScript {
    
    	public float speed;
    	public string color;
    	public int highestSpeed;
	
	public void PrintCarDetails(){
        Debug.Log("Speed = " + speed);
        Debug.Log("Color = " + color);
        Debug.Log("Highest Speed = " + highestSpeed);
    }
}

	public CarScript carScript;
	
	void Start(){
	carScript.PrintCarDetails();
}

DATE:	25-12-2021

44. Working with Properties in C# Script in UnityEngine

	- Creating Properties Script

public class Score
{
    private int point;

    public int Point{
        get{
            return point;
        }
        
        set{
            if(value > 5 && value < 10)
            point = value;
        }
    }
} 

	- Using Properties within a Script

public class Player : MonoBehaviour
{
    private void Start(){
        Score score = new Score();
        score.Point = 5;
        print(score.Point);

        score.Point = 9;
        print(score.Point);
    }
}

	- Calling a Function from within Properties
	
	- Creating Properties Script
	
public class Score
{
    private int point;

    public int Point{
        get{
            return point;
        }
        
        set{
            if(value > 5 && value < 10){
                point = value;
            }
            PrintFunction();
        }
    }

    void PrintFunction(){
        Debug.Log(point);
    }
}

	- Using Properties within a Script

public class Player : MonoBehaviour
{
    private void Start(){
        Score score = new Score();
        score.Point = 5;
        score.Point = 9;
    }
}

	- Auto Properties
	
	- Creating Auto Properties Script
	
public class Score
{
    private int lives;

    public int Lives { get; set; }
}

	- Using Auto Properties within a Script
	
public class Player : MonoBehaviour
{
    private void Start(){
        Score score = new Score();
        score.Lives = 6;
        print(score.Lives);
    }
}

	- Making Properties Read Only
	
public class Score
{
    private int lives;

    public int Lives { get; }
}

DATE:	26-12-2021

45. Understanding enums in Unity C# Scripting

	- creating enum type
	
	enum GameState { Ready, Playing, Pause, GameOver };
	
	- creating enum variable
	
	GameState state;
	
	- using enums
	
	public class EnumsScript : MonoBehaviour{

    enum GameState { Ready, Playing, Pause, GameOver };

    GameState state;

    void Start(){
        state = GameState.Ready;    
    }

    void Update(){
        switch (state){
            case GameState.Ready:
                print("You are ready");
                break;
            case GameState.Playing:
                print("You are plying");
                break;
            case GameState.Pause:
                print("game is paused");
                break;
            case GameState.GameOver:
                print("game over");
                break;
        }
    }
}

	- Making enums Public so we can access it form unity interface
	
	public enum GameState { Ready, Playing, Pause, GameOver };

    public GameState state;
	
	- insted of printing our own string now we are gonna print GameState itself
	
	switch (state)
        {
            case GameState.Ready:
                print(GameState.Ready);
                break;
            case GameState.Playing:
                print(GameState.Playing);
                break;
            case GameState.Pause:
                print(GameState.Pause);
                break;
            case GameState.GameOver:
                print(GameState.GameOver);
                break;
        }
		
	- type casting the enums to print it's internal values
	
	switch (state)
        {
            case GameState.Ready:
                print((int)GameState.Ready);
                break;
            case GameState.Playing:
                print((int)GameState.Playing);
                break;
            case GameState.Pause:
                print((int)GameState.Pause);
                break;
            case GameState.GameOver:
                print((int)GameState.GameOver);
                break;
        }
		
	- changing enums internal values
	
	public enum GameState { Ready=2, Playing=1, Pause=6, GameOver=5 };

DATE:	27-12-2021

46. Understanding Inheritance in Unity C# Scripting

	- understanding what "is a relation" is
	
	- creating a C# script called "Inheritance" where we are gonna create all the classes objects
	
	- creating a C# script called "Enemy" Where we are gonna make a function called Attack which all other inharited classes gonna use
	
	- creating a C# script called "Dragon" which is gonna inharit from the Enemy class
	
	- creating a C# script called "Robot" which is gonna inharit from the Enemy class
	
	- Enemy C# Script
	
public class Enemy{

    public void Attack(){
        Debug.Log("Enemy Attack");
    }
}

	- Inheritance C# Script
	
	- using Attack function from the Enemy class in Inheritance class by creating a new object of Enemy class
	
public class Inheritance : MonoBehaviour{

    void Start(){

        Enemy enemy = new Enemy();
        enemy.Attack();

    }
}

	- Dragon C# Script
	
public class Dragon : Enemy{

}

	- calling Attack function of Enemy class by creating a new object of Dragon class
	  because Dragon class inharit from Enemy class so it has all the properties of Enemy class
	  
public class Inheritance : MonoBehaviour{
    
	void Start(){

        Dragon dragon = new Dragon();
        dragon.Attack();

    }
}

DATE:	28-12-2021

	- Inheriting our Enemy Script from MonoBehaviour

	- because now Enemy is inheriting from MonoBehaviour then all the classes that inherit from Enemy are also have properties of

	 MonoBehaviour

	- we also know that if a script does not inherit from MonoBehaviour then it can not be added to a script

	- but in this case, because Enemy is inheriting from MonoBehaviour and the Dragon Script inherit from Enemy Script

	 so Dragon Script also has the properties of MonoBehaviour so it can be added to any game object even if it does not

	 directly inherit from MonoBehaviour

	- calling Attack function of Enemy class from Dragon class Script

	- Enemy C# Script

public class Enemy : MonoBehaviour{

    public void Attack(){

    Debug.Log("Enemy Attack");

    GetComponent<Renderer>().material.color = Color.red;
  }
}

	- Dragon C# Script

public class Dragon : Enemy{

  public bool attacking = false;
  private void Update(){
    if(attacking){
      Attack();
    }
  }
}

	- Creating same name Function in Dragon class that is in Enemy class to see which one is getting called

	- Dragon C# Script
	
public class Dragon : Enemy{
	
  public bool attacking = false;

  private void Update(){
	if(attacking){
    Attack();
   }
  }

  void Attack(){
    Debug.Log("Dragon Attack");
  }
}

	- the Attack function of child class is called which is Dragon and not the parent which is Enemy
	 because the child class will hide the parent class same name function in this case which is a function named "Attack"

	- now if we want to access the same name function of parent class rather than child class then we need to call it by 
	Using-> base keyword

	for example - Dragon C# Script
	
public class Dragon : Enemy{
  public bool attacking = false;
  private void Update(){
    if(attacking){
      base.Attack();
    }
  }
  
  void Attack(){
    Debug.Log("Dragon Attack");
  }
}

	- using base keyword before function we can call the base/parent class function

DATE:	29-12-2021



47. Working with Protected Access Modifiers



	- we already know that a public access modifier make every function and variable of a class to be accessible by anyone

	 that is inheriting from it and even those classes that are not inheriting from it can access that public variable by

	 creating a new object of that class

	  

	- and a private access modifier makes it not accessible by anyone so what if we need something in between 

	  

	- for example what if we need a variable or a function from a class only accessible by its children and not by any other class

	 that is not inheriting from that parent then we can use an access modifier called Protected

	  

	- so by using the Protected keyword we can be sure that a variable or a function can only be accessible by its child class and

	 not by any other class even after making a new object of that class

	  

	- Enemy C# Script by using Protected access modifier

	

	public class Enemy : MonoBehaviour{



  protected void Attack(){

    Debug.Log("Enemy Attack");

    GetComponent<Renderer>().material.color = Color.red;

  }

}



	- now only those classes that inherit from the Enemy class will be able to use it and not any other class like previously

	 we created a class called Inheritance so that class now can not use an Enemy class function or variable

	  

	- on the other hand, the Dragon class which is inherited from the Enemy class can still access its properties

	

	- Dragon C# Script

	

	public class Dragon : Enemy{



  public bool attacking = false;



  private void Update(){

    if(attacking){

      Attack();

    }

  }

}

DATE:	30-12-2021

48. Understanding Polymorphism Virtual Functions & Overriding in Unity C#

	- Creating three different classes named
		- Dragon which inherit from the MonoBehaviour
		- BlueDragon which inherit from the Dragon class
		- RedDragon which also inherit from the Dragon class
		
	- Creating the same name function "Attack" in all three classes than make the parent class Dragon "Attack" function virtual 
	  so we can use override function in all the child classes
	  
	-  and making all the child classes BlueDragon,RedDragon "Attack" function override so we can call the child function form the 
	   parent class because without making the main function virtual and child classes function override we can not call child classes
	   functions from the parent class
	   
	- creating a new referance of a Dragon class and than storing a new instense of BlueDragon class
	  so this way we can call child class function from the parent class
	  
	- Dragon C# script -> all the classes are in this single script -> Dragon,BlueDragon,RedDragon
	
public class Dragon : MonoBehaviour{

    private void Start(){
        Dragon dragon = new Dragon();
        dragon.Attack();

        Dragon dragon2 = new BlueDragon();
        dragon2.Attack();
		
		Dragon dragon3 = new RedDragon();
        dragon3.Attack();
    }

    public virtual void Attack(){
        print("Dragon Attack");
    }
} // End of Dragon Class

public class BlueDragon : Dragon{

    public override void Attack(){
        print("Blue Dragon Attack");
    }
}

public class RedDragon : Dragon{

    public override void Attack()
    {
        print("Red Dragon Attack");
    }
}

DATE:	31-12-2021

49. Understanding Static Variables, Functions & Classes in Unity C# Scripting

	- we know already that we can access one class variable from the other class by making a new object in that class
	 and then we can access that variable or function and change it accordingly 
		    
	- for example

public class StaticTest : MonoBehaviour{
  void Start(){

    Bullets bullet1 = new Bullets();
    Bullets.noOfbullets = 10;

    Bullets bullet2 = new Bullets();
    Bullets.noOfbullets = 20;

    print(Bullets.noOfbullets);
    print(Bullets.noOfbullets);
  }
}
		    
public class Bullets{
  public static int noOfbullets;
}

	- so by using the above method we can change one class variable from another class by making a new object
	 but every new object gonna have there own version of that variable

	- by creating a Static Variable we can be sure that every new object of that class is gonna have the same instance or version
	 of that variable

	- one instance of that class is gonna be shared in all the objects
		    
	- for example

public class StaticTest : MonoBehaviour
{
  void Start(){
    Bullets bullet1 = new Bullets();
    Bullets.noOfbullets = 10;
		    
    Bullets bullet2 = new Bullets();
    Bullets.noOfbullets = 20;
		    
    print(Bullets.noOfbullets);
  }
}

public class Bullets{
  public static int noOfbullets;
}
	- static variables can be used to check how many instances are created of that class

	- for example

public class StaticTest : MonoBehaviour{

  void Start(){
    Bullets bullet1 = new Bullets();
    Bullets bullet2 = new Bullets();
    print(Bullets.noOfbullets);
  }
}
		    
public class Bullets{
  public static int noOfbullets;
  public Bullets(){
    noOfbullets++;
  }
}
	- here we created a constructor so we can increment the no of times when an instance of that class is created
	 because we know that constructor is called automatically whenever an intense of a class is created

	- one important thing to remember is that whenever we create a static variable that variable will always be in the memory
	 and never get cleared automatically it will only clear after our program is closed
		    
	- because whenever we create a static variable it will always reserve some memory for that variable

		    
DATE:	01-01-2022

Break

DATE:	02-01-2022

	- Static Functions
	
public class StaticTest : MonoBehaviour
{
    void Start(){

        Bullets bullet1 = new Bullets();
        
        Bullets bullet2 = new Bullets();

        Bullets.ShowBullets();
    }
}

public class Bullets{

    public static int noOfbullets;

    public Bullets(){
        noOfbullets++;
    }

    public static void ShowBullets(){
        Debug.Log("No of Bullets " + noOfbullets);
    }
}

	- note an static function can not call an non-static variable
	
	- note when ever we create class static than we can not create an instense of that class
	  and also we can not create a constructor in static class
	  
	  
50. Understanding Method Overloading in Unity C# Scripting

	- as we know that we can not create same name function twice in same class, we have to name them slightly differently
	  something like this
	  
public class Fun{
    public void printInt(int i){
        Debug.Log(i);
    }

    public void printfloat(float i)
    {
        Debug.Log(i);
    }

    public void printString(string i)
    {
        Debug.Log(i);
    }
}

	- To slove that problem we can use Method Overloading with this we can create same name functions with just different perameters
	  
	- for example
	
public class MethodOverloading : MonoBehaviour
{
    void Start(){
        Fun fun = new Fun();

        fun.Print(2);
        fun.Print(1.2f);
        fun.Print("this is a String");
    }
}

public class Fun{

    public void Print(int i){
        Debug.Log("Print(int i) is getting called");
        Debug.Log(i);
    }

    public void Print(float i){
        Debug.Log("Print(float i) is getting called");
        Debug.Log(i);
    }

    public void Print(string i){
        Debug.Log("Print(string i) is getting called");
        Debug.Log(i);
    }
}
	
	- this way we can keep the same name for all the functions and can still call different functions by just changing the parameters

DATE:	03-01-2022
	
	- we can even call the function with the same name and same data type without any error buy just changing the number of parameters
	
	for example
	
	 public void Print(int i, int j){
        Debug.Log("Print(int i, int j) is getting called");
        Debug.Log(i);
        Debug.Log(j);
    }
	
	- and we can call this function by this
	
	fun.Print(2, 3);
	
51. Understanding NameSpaces in Unity C# Scripting

	- by using namespaces we can use others prewritten code without writing them form scratch by ourself
	
	- for example if we remove using UnityEngine form any C# script that we create in unity than all the functions
	  that depend on UnityEngine API are not gonna work like MonoBehaviour and rigidbody
	  
	- we can also remove using UnityEngine from top and still keep using MonoBehaviour and rigidbody and all the functions
      that depend on it by adding this in front of them "UnityEngine."
	  
	- for example
	
	- UnityEngine.MonoBehaviour
	
	- UnityEngine.Rigidbody rb;
	
	- Nested NameSpaces
	
	- another example of this is Text or UI in Unity
	
	- we can only use UI functions in unity if we add this at the top of the C# script "using UnityEngine.UI;"
	  Text text;

	- or we can do this "UnityEngine.UI.Text text;"
	
	- this way we can use nested namespaces means a namespace inside another namespace
	
	- Creating our own NameSpaces
	
	- we created an namespace C# script called "CustomNameSpaceScript"
	
	- in that we created an class called "Utilities"
	
	- inside that class we created an satatic function called "PrintHelloWorld"
	
	- we created it satatic so we don't have to make an instense of that class
	
	- we can just use it by using it's class name
	
	- we are using UnityEngine api so that we can call Debug.Log function
	
	- here is that NameSpace C# Script
	
using UnityEngine;

namespace CustomNameSpace{
    public class Utilities{
        public static void PrintHelloWorld(){
            Debug.Log("Hellow World");
        }
    }
}

	- now we are gonna use our custom namespace C# script in another C# script
	
public class NameSpaceScript : MonoBehaviour
{
    void Start(){
        CustomNameSpace.Utilities.PrintHelloWorld();
    }
}

	- like all the other namespaces we can use our namespace class like this calling the nested namespace first
	  than the function name like
	  
	- CustomNameSpace.Utilities.PrintHelloWorld();
	
	- or we can use it like we use UnityEngine namespace
	
	- like this
	
using CustomNameSpace;

public class NameSpaceScript : MonoBehaviour
{
    void Start(){
        Utilities.PrintHelloWorld();
    }
}

DATE:	04-01-2022

	- Creating Custom Nested NameSpaces
	
using UnityEngine;

namespace CustomNameSpace{
    public class Utilities{
        public static void PrintHelloWorld(){
            Debug.Log("Hello World");
        }
    }
}

namespace UI{
    public class UIWork{
        public static void UIFunction(){
            Debug.Log("this is a UI Function");
        }
    }
}

	- using this nested namespace in another C# script
	
using CustomNameSpace;

public class NameSpaceScript : MonoBehaviour
{
    void Start(){
        Utilities.PrintHelloWorld();
        UI.UIWork.UIFunction();
    }
}

52. Understanding Attributes in Unity C# Scripting

	- Attributes are very usefull some of the use cases of Attributes are
	
	- if we want to make an variable private but also want it to be accessable in unity inspertor
	
	- we know only public variables are shown in unity inspertor but by using an Attribute property called
	  [SerializeField] we can keep it private so this variable can not be accessed by anyother script but we still can 
	  access it in the unity inspertor
	  
	- for example
	
	- [SerializeField]
      private int speed;
	  
	- by writing this [SerializeField] we can make speed variable accessable in unity inspertor
	
	- another use of Attributes is
	
	- if we want to make an variable accessable by all the other scripts so we need to make it public
	  but by making it public this variable is also gonna show in unity inspertor, what if we don't want it to show
	  on inspertor but still want to keep it public 
	  
	- in this case we can use an Attribute called [HideInInspector]
	
	- for example
	
	- [HideInInspector]
	  public int speed;
	  
	- we can also create an slider in unity inspertor by using an Attribute called [Range]
	  in this we need to pass to parameters for the minimum and maximum values
	
	- for example
	
	- [Range(0,40)]
      public int speed;
	  
53. Adding Component only using Attributes inside the C# script without using unity inspertor

	- this is a really inportant feature of unity
	
	- we can add any component of unity to any game object only using C# Script
	
	- in this example we are gonna add Rigidbody Component using an Attribute called "RequireComponent"
	
	- for example
	
	- [RequireComponent(typeof(Rigidbody))]
	
	- now even if we previously did not add that physics component Rigidbody to the game object
	  but because we use RequireComponent Attribute so when ever we are gonna run this game unity automaticaly
	  gonna add it to the game object
	  
	- complete C# script showing the use case of RequireComponent
	
[RequireComponent(typeof(Rigidbody))]
public class AttributesScript : MonoBehaviour
{
    Rigidbody rb;

    void Start(){
        rb = GetComponent<Rigidbody>();
        rb.isKinematic = true;
    }
}

DATE:	05-01-2022

54. Understanding Coroutines in Unity C# Scripting in-depth

	- by using Coroutines we can hold the execution of a perticular function and can resume it after sometimes
	  means we can do some tasks in intervals of some seconds or minutes
	  
	- so in this example we are creating an C# script called "CoroutineScript" and attaching it to the cube

	- and changing the cube color after 2 seconds to cyan and than agin changing the cube color after 1 second
	  to blue using Coroutine functions
	  
	- Coroutine C# Script
	
public class CoroutinesScript : MonoBehaviour
{
    private GameObject cube;
    void Start(){
        StartCoroutine(Test());
    }

    IEnumerator Test(){
        print("Coroutine Started");
        yield return new WaitForSeconds(2f);
        GetComponent<Renderer>().material.color = Color.cyan;

        yield return new WaitForSeconds(1f);
        GetComponent<Renderer>().material.color = Color.blue;
        print("Coroutine Ends");
    }
}

	- using Coroutines on per frame bases
	
	- we can halt the execution of the code unitl the current frame finish executing
	
	Using->
	
	- yield return null;
	
55. Understanding Coroutines per frame in-depth

public class CoroutinesScript : MonoBehaviour
{
    void Start(){
        Test2();
        for (int i = 0; i < 6; i++){
            print("Start()");
        }
    }
	
	void Test2(){
        for(int i=0; i<6; i++){
            print("Test2()");
        }
    }
}

	- in above example we can see that first all the Test2 calls is gonna complete of the loop after that
	  anything that is written after Test2 is gonna get called in this case for loop
	  
	- we can fix this problem by using Coroutines 
	
	- by using Coroutine we can call the Test2 with parallelly anyother function that is written after that
	  in this case that for loop
	  
	- here is the example of that Coroutine Function
	
public class CoroutinesScript : MonoBehaviour
{
    void Start(){
        StartCoroutine(Test3());
        for (int i = 0; i < 6; i++){
            print("Start()");
        }
    }
	
	IEnumerator Test3(){
        for (int i = 0; i < 6; i++){
            print("Test3()");
            yield return null;
        }
    }
}

	- so in this case first call of Coroutine Test3 is gonna happen and it is gonna print "Test3()"
	
	- and after that all the calls of function that is written after the Test3 is gonna happen
	
	- after all the calls of other functions happend than the Test3 Coroutine is gonna continue
	
	- so in this way Coroutines are really helpfull to run more than one funcion simultaneously
	

DATE: 06-01-2022

56. Creating An 2D Candy Catch Game

- All the Graphics Stuff

- Importing all the graphics assets of the game after editing them in GIMP

- Adding a Background Image to the Game and adjusting its Pixel Per Unit Property from Unity Inspector
 to fit it perfectly on the screen
  
- Adding player sprite to the scene and also adjusting its Pixel Per Unit Property from Unity Inspector
 to fit it perfectly on the screen
  
- Adding Candy sprite to the game and also adjusting its Pixel Per Unit Property from Unity Inspector
 to fit it perfectly on the screen
  
- Separating Candy sprite form group to individual sprite by using Unity built-in feature called "Sprite Editor"

- And setting its sprite mode to Multiple form single sprite
  
- Making Sorting layers to see our player apart from our Game Background

- Give Background a sorting layer called Background

- Give Player a sorting layer called MiddleGround

- Give Candies a sorting layer called ForeGround

- Creating an Empty GameObject where our Candies are gonna spawn from random Positions

- All the Physics Stuff

- Adding Circle Collider to our player and resizing it to only on its Mouth

- Adding Rigidbody2D and Circle Collider2D and Box Collider2D to our Candies according to the shape of Candies

- Creating an Empty GameObject and Attaching a Box Collider2D to it 

- and stretching its size so it fits our Game Screen in Bottom

- We need this because for those Candies that our player is unable to catch so they need to be destroyed

- after they are out of the screen this is where our Box Collider2D comes in 

- that will gonna know if something hit that

  - then we will gonna Destroy that Candy Game Object


- Creating Prefabs

- Making all the Sprites an Prefabs so we don't have to do all the Physics Stuff again and again

DATE:	07-01-2022
	
- All the C# Programming Stuff

	- Creating an simple Player Movement Script without using Rigidbody2D because this is the movement we need in our
	  game only using transform.position component
	  
- PlayerController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    private bool canMove = true;

    [SerializeField]
    private float maxPos;

    [SerializeField]
    private float moveSpeed;
    
    private float xInput;

    void Update(){
        if (canMove){
            Move();
        }
    }

    void Move(){
        xInput = Input.GetAxis("Horizontal");
        transform.position += Vector3.right * xInput * moveSpeed * Time.deltaTime;

        float xPos = Mathf.Clamp(transform.position.x, -maxPos, maxPos);
        transform.position = new Vector3(xPos, transform.position.y, transform.position.z);
    }
}

	- in player movement script we created movement for our Player Sprite model
	
	- And also we need to clamp the player position so we our player don't go our of the screen
	
	- to achive this functionality we used an Unity build in feature called Mathf.Clamp

DATE: 08-01-2022

Break

DATE: 09-01-2022

- Creating An C# Script called CandyScript

- in this script we are only gonna make our Candies Disappear if they Collide with our Player Game Object

- or if they collide with the Boundary Box Collider2D GameObject
 using Unity built-in funcion called "OnTriggerEnter2D"
  
- CandyScript C# Unity Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CandyScript : MonoBehaviour
{
  private void OnTriggerEnter2D(Collider2D collision){
    if(collision.gameObject.tag == "Player"){
      // Increment the Score
      collision.isTrigger = true;
      Destroy(gameObject);
    }else if (collision.gameObject.tag == "Boundary"){
      // Decrement the lives
      Destroy(gameObject);
    }
  }
}

- we are doing all these checks what collide with what by using an unity built-in feature called Tags

- we have given our player a Tag called "Player"

- and our Boundary a Tag called "Boundary"

DATE: 10-01-2022

- Spawning Random Candies

- we are spawning random candies from 20 Candies in our game

- and they all are gonna spawn from a random place

- we created an separate script for this feature called "CandySpawnerScript"

- CandySpawnerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CandySpawnerScript : MonoBehaviour
{
  [SerializeField]
  private float maxX;

  [SerializeField]
  private float spawnIntervals;

  public GameObject[] candies;

  public static CandySpawnerScript instance;

  private void Awake(){
    if(instance == null){
      instance = this;
    }
  }

  void Start(){
    //SpawnCandy();  

    StartCoroutineCandySpawner();
  }

  void SpawnCandy(){
    int randomCandy = Random.Range(0, candies.Length);
    float randomNumber = Random.Range(-maxX, maxX);
     
    Vector3 randomPosition = new Vector3(randomNumber, transform.position.y, transform.position.z);
    Instantiate(candies[randomCandy], randomPosition, transform.rotation);
  }

  IEnumerator CoroutineCandySpawner(){
    yield return new WaitForSeconds(2f);

    while (true){
      SpawnCandy();
      yield return new WaitForSeconds(spawnIntervals);
    }
  }

  public void StartCoroutineCandySpawner(){
    StartCoroutine(CoroutineCandySpawner());
  }

  public void StopCoroutineCandySpawner(){
    StopCoroutine(CoroutineCandySpawner());
  }
}

DATE: 11-01-2022

- Working with UI of our Game

- Creating a Pannel at the top and adding text and image to it

- resizing all of those according to our screen Resolution

- adding some lines of code in our "GameManager" Script to increment the number whenever a player catches a Candy
  
- "GameManager" C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;

public class GameManager : MonoBehaviour{

  public static GameManager instance;

  private int score = 0;

  bool gameOver = false;

  public Text scoreText;

  private void Awake(){

    instance = this;
  }

  public void IncrementScore(){
    score++;
    scoreText.text = score.ToString();
    print(score);
  }
}

- Adding Lives in our Game

- Creating and Lives Counter in our Game so we can keep track of lives

- "GameManager" C# Script code for Lives Counter

private int lives = 3;

public void DecreaseLife(){
    if(lives > 0){
      lives--;
      print(lives);
    }

    if(lives <= 0){
      gameOver = true;
      GameOver();
    }
  }

  public void GameOver(){
    print("Game Over!!");
  }

DATE: 12-01-2022

- Adding UI Representation to Lives in our Game

- creating and importing lives sprites for our game

- adding another UI Pannel and Image panel for Lives

- resizing and repositioning UI Pannel and Image

- added these lines of code to make our UI Respond to our actual lives count

public GameObject livesHolder;

private int lives = 3;

public void DecreaseLife(){
    if(lives > 0){
      lives--;
      livesHolder.transform.GetChild(lives).gameObject.SetActive(false);
    }
}

- Stoping the Candies from spawning after all the lives of the player has been lost

- Stoping Player from moving after all the lives of the player has been lost

- These changes were made in GameManager C# Script

public void GameOver(){
    CandySpawnerScript.instance.StopCoroutineCandySpawner();
    GameObject.Find("Player").GetComponent<PlayerController>().canMove = false;
}

- Creating the Main Menu Screen for our Game

- for that, we first created a new screen called "menu" in Unity

- then we added a background to it

- Creating UI for our menu

- for that, we first added a pannel 

- and two texts because we want to give our menu text "Candy Catch" different color to both of the words
 that is why we need to create two different text
  
- Created two buttons called "Play" and "Exit" for our Menu

- Adding functionality to our Play and Exit buttons in our menu

- for that, we first created an empty game object called "MainMenuController"

- and added a C# Script called "MainMenuControllerScript" to that game object

- in our C# Script we are Creating two public functions called "Play" and "Exit"

- and we are loading a scene called "Game" which is our main game scene whenever we press the Play button

- and we quit our game whenever we press exit in our game menu

- here is C# Script called "MainMenuControllerScript"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class MainMenuControllerScript : MonoBehaviour{

  public void Play(){
    SceneManager.LoadScene("Game");
  }

  public void Exit(){
    Application.Quit();
  }
}

DATE: 13-01-2022

- Adding an HighScore functionality in our game

- first we are creating an UI our HighScore

- added an panel called HighScore

- added an image for the logo of HighScore

- added an text to show the number of HighScore

- added another text to show text HighScore in front of the HighScore Number

- modified the funcion called IncrementScore in our GameManager C# Script

- wiht this

public Text highScoreText;

private void Start(){
    highScoreText.text = PlayerPrefs.GetInt("HighScore", 0).ToString();
}

public void IncrementScore(){
    if (!gameOver){
      score++;
      scoreText.text = score.ToString();

      if (score > PlayerPrefs.GetInt("HighScore", 0)){
        PlayerPrefs.SetInt("HighScore", score);
        highScoreText.text = score.ToString();
      }
    }
}

- for storing our HighScore In player device we are using a Unity built-in function called "PlayerPrefs"
	
DATE: 14-01-2022

- Creating an Button called "ResetScore" to reset player HighScore

- for resetting our player HighScore we are creating an function called "ResetScore"

- and again using Unit built-in feature called "PlayerPrefs" for deleting the HighScore

- Updated GameManager C# Script

public void ResetScore(){
    PlayerPrefs.DeleteKey("HighScore");
    highScoreText.text = "0";
}

- we are calling it from Unity Inspertor OnClick() Function 

- by selecting GameManager C# Script where is our ResetScore() Function exists

- and choosing ResetScore() Function from that Script

DATE: 15-01-2022

- Adding a new Feature of Decreasing Point

- we are adding a Feature in which we are gonna decrease Player Point if the Player Toches a Bad Candy

- we added some sprites for bad candies

- and make them spawn randomly with the good candies

- we created a function in GameManager script called "DecrementScore"

public void DecrementScore(){
  if (!gameOver){
    score--;
    scoreText.text = score.ToString();
  }
}

- we created an seprate script for the enemy candies called "EnemeyScript"

- and we are calling DecrementScore Function from GameManager in EnemeyScript using "instance"

- EnemeyScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EnemyScript : MonoBehaviour{
  private void OnTriggerEnter2D(Collider2D collision){
    if (collision.gameObject.tag == "Player"){
      GameManager.instance.DecrementScore();
      Destroy(gameObject);
    }

    else if (collision.gameObject.tag == "Boundary"){
      Destroy(gameObject);
    }
  }
}

DATE: 16-01-2022

BREAK

DATE: 17-01-2022

- adding music in our game

- first, we are creating our own music using a Software called "Bosca Ceoil"

- created a simple 4 instrument-based music for our game

- imported it in the unity

- Creating an Empty GameObject and naming it "BackGroundMusic"

- and adding Audio Source to it

- then adding our music file to AudioClip in Audio Source

- with all of that our First Game Project called "Candy Catch" is finished

DATE: 18-01-2022

- Creating My Second Project, an Android Game called "Destroy Balls"

- Introduction of the game

- in this game, there are 6 balls in front of the player that is bouncing in a random direction

- and the player can destroy the ball by touching them

- when the player destroys all the balls then a message appeared called "YOU WIN :)"

- Creating an Android Project in Unity

- importing all the Sprites for the game and resizing them according to the player screen

- all the Visual Stuff

- Creating a Boundary for the game so our balls don't go out of the screen

- Creating a You Win text to display when the player Destroy all the balls 

- Creating a Restart Button

DATE:	19-01-2022
	
- all the Programming Stuff

	- Creating an Physics2D Material to add Bounciness to it
	
	- Creating an empty gameobject called GameManager 
	
	- Creating an C# Script called "GameManagerScript" and attaching it to the GameManager empty gameobject 
	
	- with this script we are adding functionality to both our winText and RestartButton
	
	- we are creating an Scrore int variable to store every ball the player Destroy
	
	- whenever player destory a ball the we call an function called scoreUP()
	
	- in this function we are incrementing the score by one
	
	- and if the score is bigger than or equal to 6 the we call another function called "Win()" inside of this function
	
	- we also created an function called Restart(), 
	  which will gonna restart our game whenever player presses that button
	  
- "GameManagerScript"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class GameManagerScript : MonoBehaviour
{
    public GameObject winText;
    public GameObject restartButton;

    int score = 0;

    public void scoreUP()
    {
        score++;
        if(score >= 6)
        {
            Win();
        }
    }

    void Win()
    {
        winText.SetActive(true);
        restartButton.SetActive(true);

    }

    public void Restart()
    {
        SceneManager.LoadScene("Game");
    }
}

DATE:	20-01-2022

	- Creating an C# Script called "BallScript" and attaching it to the all the Ball GameObject
	
	- using OnMouseDown() Function to register the player input 
	
	- this function works with both pc with mouse and Android with Touch input
	
	- in this script we are using GameObject.Find function to find the GameManagerScript
	
	- and calling the scoreUP() function form it
	
	- and we are also calling Destroy(gameobject) Unity Function to Destroy the balls gameobject
	
- "BallScript"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallScript : MonoBehaviour
{
    private void OnMouseDown()
    {
        GameObject.Find("GameManager").GetComponent<GameManagerScript>().scoreUP();
        Destroy(gameObject);
    }
}

DATE:	21-01-2022

- Adding Music to our game
	
	- Designing Audio for our game
	
	- we are creating an empty gameobject called "AudioManager"
	
	- and attaching an audio source to it
	
	- and we are putting our game audio file inside AudioClip 
	
	- and cheching the loop box inside Unity Inspector

- with that our Second Game Project is Completed

DATE: 22-01-2022

- Porting our Candy Catch PC Game to Android

- With the knowledge of our previous Android Game Project, now we can Port our PC Game into Android

- for that first, we need to change our project in Unity from pc to android

- and choose a screen resolution that fits our android device

- in this case 2340 x 1080 pixels

- now some of our game UI is goona be cropped out of the screen because of our android phone resolution

- so we are fixing it in the unity scenes by using the Move tool

DATE: 23-01-2022

- Creating Player Movement for Android

- we are creating two buttons one is for the left and another is for right

- and placing the left one on the left end of the screen

- and placing the right one on the right end of the screen

- now we are gonna import some Sprites for our Buttons to make them look good

- now we are gonna attach a Unity Standard Assets C# Script called "AxisTouchButton" to both of our buttons

- "AxisTouchButton" C# Script

using System;
using UnityEngine;
using UnityEngine.EventSystems;

namespace UnityStandardAssets.CrossPlatformInput
{
public class AxisTouchButton : MonoBehaviour, IPointerDownHandler, IPointerUpHandler
{
// designed to work in a pair with another axis touch button
// (typically with one having -1 and one having 1 axisValues)
public string axisName = "Horizontal"; // The name of the axis
public float axisValue = 1; // The axis that the value has
public float responseSpeed = 3; // The speed at which the axis touch button responds
public float returnToCentreSpeed = 3; // The speed at which the button will return to its centre

AxisTouchButton m_PairedWith; // Which button this one is paired with
CrossPlatformInputManager.VirtualAxis m_Axis; // A reference to the virtual axis as it is in the cross platform input

void OnEnable()
{
if (!CrossPlatformInputManager.AxisExists(axisName))
{
// if the axis doesnt exist create a new one in cross platform input
m_Axis = new CrossPlatformInputManager.VirtualAxis(axisName);
CrossPlatformInputManager.RegisterVirtualAxis(m_Axis);
}
else
{
m_Axis = CrossPlatformInputManager.VirtualAxisReference(axisName);
}
FindPairedButton();
}

void FindPairedButton()
{
// find the other button witch which this button should be paired
// (it should have the same axisName)
var otherAxisButtons = FindObjectsOfType(typeof(AxisTouchButton)) as AxisTouchButton[];

if (otherAxisButtons != null)
{
for (int i = 0; i < otherAxisButtons.Length; i++)
{
if (otherAxisButtons[i].axisName == axisName && otherAxisButtons[i] != this)
{
m_PairedWith = otherAxisButtons[i];
}
}
}
}

void OnDisable()
{
// The object is disabled so remove it from the cross platform input system
m_Axis.Remove();
}


public void OnPointerDown(PointerEventData data)
{
if (m_PairedWith == null)
{
FindPairedButton();
}
// update the axis and record that the button has been pressed this frame
m_Axis.Update(Mathf.MoveTowards(m_Axis.GetValue, axisValue, responseSpeed * Time.deltaTime));
}


public void OnPointerUp(PointerEventData data)
{
m_Axis.Update(Mathf.MoveTowards(m_Axis.GetValue, 0, responseSpeed * Time.deltaTime));
}
}
}

DATE: 24-01-2022

- and we are also doing these changes in our "PlayerController" C# Script

void Move(){
    xInput = CrossPlatformInputManager.GetAxis("Horizontal");
    transform.position += Vector3.right * xInput * moveSpeed * Time.deltaTime;

    float xPos = Mathf.Clamp(transform.position.x, -maxPos, maxPos);
    transform.position = new Vector3(xPos, transform.position.y, transform.position.z);
}

- our player movement is working with our On-Screen Buttons

- with that our Porting of our pc game to android is Completed

- Learning Android Touch Controls

- Testing touch controls with this

void Update(){
    Debug.Log(Input.touchCount);
}

- only checking touch count if there is a touch on the android device

Using->

if (Input.touchCount > 0)
{
  Debug.Log(Input.touchCount);
}

- checking the position of single touch at a time in our android device screen

Using->

Debug.Log(Input.GetTouch(0).position);

- check the position of multiple touches at the same time in our android device screen

- Understanding Touch Phases in Unity

- with the touch phase we can check our touch is in what state, if it began or ended or currently working

Using->

if(Input.GetTouch(0).phase == TouchPhase.Began){
  Debug.Log("Touch Began");
}

if (Input.GetTouch(0).phase == TouchPhase.Moved){
Debug.Log("Touch Moved");
}

if (Input.GetTouch(0).phase == TouchPhase.Ended){
  Debug.Log("Touch Ended");
}

DATE:	25-01-2022

- Touch & Destroy Objects with RayCasting in Unity C#

- Understanding RayCasting

	- Creating an ray to be cast from the camera position to the position where our finger touch on the android device
	
	- Ray ray;
	- ray = Camera.main.ScreenPointToRay(Input.GetTouch(0).position);
	
	- casting that ray that we created an checking if it hit something
	
	if (Physics.Raycast(ray, Mathf.Infinity)){
        Debug.Log("hit something");
    }
	
	- adding visual representation of the ray with a colour
	
	Debug.DrawRay(ray.origin, ray.direction * 20, Color.red);
	
	- getting informatin about what we are hitting with the ray
	
	- and destroying it with that ray
	
	RaycastHit hit;
	if (Physics.Raycast(ray, out hit, Mathf.Infinity)){
        Debug.Log("hit something");
        Destroy(hit.transform.gameObject);
    }

DATE:	26-01-2022

- Learning Accelerometer Inputs in Unity C#

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class AccelerometerMovementScript : MonoBehaviour
{
    public float speed;
    private float rotationSpeed = 2f;
    void Update(){
        float temp = Input.acceleration.x;
        float z = Input.acceleration.z;
        //Debug.Log(temp);
        transform.Translate(0, 0, -z * speed * Time.deltaTime);
        transform.Rotate(0, 0, -temp * rotationSpeed);
    }
}

DATE:	27-01-2022

- Learning Touch Swipe Controls in Unity C#

	- Created an C# Script that will tell us if we swipe left or right horizontal or up and down vertical
	
- SwipeTestScrip

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SwipeTestScript : MonoBehaviour
{
    public GameObject player;

    public float maxTime;
    public float minSwipeDistance;

    float startTime;
    float endTime;

    Vector3 startPos;
    Vector3 endPos;

    float swipeDistance;
    float swipeTime;

    void Update(){
        if(Input.touchCount > 0){
            
            Touch touch = Input.GetTouch(0);

            if(touch.phase == TouchPhase.Began){
                
                startTime = Time.time;
                startPos = touch.position;
            }

            else if(touch.phase == TouchPhase.Ended){

                endTime = Time.time;
                endPos = touch.position;

                swipeDistance = (endPos - startPos).magnitude;
                swipeTime = endTime - startTime;

                if(swipeTime < maxTime && swipeDistance > minSwipeDistance){
                    Swipe();
                }
            }
        }
    }

    void Swipe(){

        Vector2 distance = endPos - startPos;
        
        if(Mathf.Abs(distance.x) > Mathf.Abs(distance.y)){

            Debug.Log("Horizontal Swipe");

            if(distance.x > 0){

                Debug.Log("Right Swipe");
            }

            else if(distance.x < 0){

                Debug.Log("Left Swipe");
            }
        }

        else if(Mathf.Abs(distance.x) < Mathf.Abs(distance.y)){

            Debug.Log("Vertical Swipe");

            if (distance.y > 0){

                Debug.Log("UP Swipe");
                player.GetComponent<PlayerJumpScript>().Jump();
            }

            else if (distance.y < 0){

                Debug.Log("Down Swipe");
            }
        }
    }
}

DATE:	28-01-2022

	- Creating an cube player game object that will jump when we swipe vertically in our android device
	
- PlayerJumpScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerJumpScript : MonoBehaviour
{
    public float jumpForce;

    Rigidbody2D rb;

    void Start(){
        rb = GetComponent<Rigidbody2D>();
    }

    public void Jump(){
        rb.AddForce(new Vector2(0, jumpForce));
    }
}

DATE: 29-01-2022

- Creating a joystick controller for our android device

- Created and ball and a joystick controller 

- the ball moves whenever we move our joystick from our android device

- BallScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityStandardAssets.CrossPlatformInput;

public class BallScript : MonoBehaviour
{
  public float speed;

  Rigidbody rb;

  void Awake(){
    rb = GetComponent<Rigidbody>();
  }

  void FixedUpdate(){
    float horizontalInput = CrossPlatformInputManager.GetAxis("Horizontal") * speed;
    float verticalInput = CrossPlatformInputManager.GetAxis("Vertical") * speed;

    rb.AddForce(horizontalInput, 0, verticalInput);
  }
}

DATE:	30-01-2022

- Created Responsive UI in Unity
	
	- Created an UI that will resize automaticaly according to the screen or device resulation

- Creating Zooming In and Out in Unity with C#

	- Created an C# Script called "CameraZoomscript"
	
- CameraZoomscript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CameraZoomScript : MonoBehaviour
{
    public int zoomSpeed2d;
    public int minZoom2d;
    public int maxZoom2d;

    public int zoomSpeed3d;
    public int minZoom3d;
    public int maxZoom3d;

    void Update(){

        // 2D Camera
        if (Camera.main.orthographic){

            if(Input.GetAxis("Mouse ScrollWheel") > 0){
                // Zoom In
                Camera.main.orthographicSize -= zoomSpeed2d * Time.deltaTime;
            }

            else if(Input.GetAxis("Mouse ScrollWheel") < 0){
                // Zoom Out
                Camera.main.orthographicSize += zoomSpeed2d * Time.deltaTime;
            }

            // Restrict the Camera from zooming in or out after an particular value
            Camera.main.orthographicSize = Mathf.Clamp(Camera.main.orthographicSize, minZoom2d, maxZoom2d);
        }

        else{
            // 3D Camera
            if (Input.GetAxis("Mouse ScrollWheel") > 0){
                // Zoom In
                Camera.main.fieldOfView -= zoomSpeed3d * Time.deltaTime;
            }

            else if (Input.GetAxis("Mouse ScrollWheel") < 0){
                // Zoom Out
                Camera.main.fieldOfView += zoomSpeed3d * Time.deltaTime;
            }

            // Restrict the Camera from zooming in or out after an particular value
            Camera.main.fieldOfView = Mathf.Clamp(Camera.main.fieldOfView, minZoom3d, maxZoom3d);
        }
    }
}

DATE: 31-01-2022

- Creating a Camera Shake in Unity

- Created and cube and plane so that we can see the camera shake around the cube

- Created and C# Script called CameraShake

- "CameraShake"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CameraShake : MonoBehaviour
{
  public float shakeTime;
  public float shakeRange;
   
  Transform cameraTransform;

  Vector3 originalPosition;

  void Start(){
     
    cameraTransform = Camera.main.transform;
    originalPosition = cameraTransform.position;
  }

  void Update(){

    if (Input.GetMouseButtonDown(0)){
      StartCoroutine(ShakeCamera());
    }
  }

  IEnumerator ShakeCamera(){

    float elapsedTime = 0;

    while (elapsedTime < shakeTime){

      Vector3 pos = originalPosition + Random.insideUnitSphere * shakeRange;
      pos.z = originalPosition.z;
      cameraTransform.position = pos;

      elapsedTime += Time.deltaTime;

      yield return null;
    }

    cameraTransform.position = originalPosition;
  }
}

DATE:	01-02-2022

- Rotating Objects with Mouse

	- Created an Cube gameobject to make it rotate with mouse
	
	- Created and C# Script called "RotateWithMouseScript"
	
- RotateWithMouseScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RotateWithMouseScript : MonoBehaviour
{
    public float rotationSpeed;

    public void OnMouseDrag(){

        float y = Input.GetAxis("Mouse Y") * rotationSpeed;
        float x = Input.GetAxis("Mouse X") * rotationSpeed;

        transform.Rotate(Vector3.right, y);
        transform.Rotate(Vector3.down, x);
    }
}

DATE: 02-02-2022

- Detecting Button Clicks and Calling Functions

- Created a cube with two buttons one called green and another called red

- the cube change color whenever we press one of the two buttons

- we changed the color of the cube with different methods

- one is by calling OnClick Function from unity Inspector

- and another is from the C# Script itself

- both of these methods are in an C# Script called "ColorChangerScript"

- ColorChangerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;

public class ColorChangerScript : MonoBehaviour
{
  public GameObject cube;

  Button greenButton;

  void Start(){
    greenButton = GameObject.Find("GreenButton").GetComponent<Button>();

    greenButton.onClick.AddListener(() => ChangeToGreen());
  }

  public void ChangeToRed(){
    cube.GetComponent<Renderer>().material.color = Color.red;
  }

  public void ChangeToGreen(){
    cube.GetComponent<Renderer>().material.color = Color.green;
  }
}

DATE: 03-02-2022

- Creating 2D infinite BackGround and a ForeGround

- importing the sprites for the background and foreground

- setting them as texture on a 3d quad

- and setting the wrap mode to repat so that it makes multiple copies of itself

- then creating an C# Script called "BackGroundScript" that will gonna move our background and foreground

- "BackGroundScript"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BackGroundScript : MonoBehaviour
{
  Material material;
  Vector2 offset;

  public int xVelocity;
  public int yVelocity;

  private void Awake(){
    material = GetComponent<Renderer>().material;
  }

  void Update(){

    offset = new Vector2(xVelocity, yVelocity);
    material.mainTextureOffset += offset * Time.deltaTime;
  }
}

- in the C# Script we first get access to the Renderer of the BackGround and ForeGround

- then storing it inside a Material variable called material

- then in the update, we are creating a new offset variable and adding an vector2 to it with the parameters of 
 the xVelocity and yVelocity which are the public int variable that we will gonna change from the Unity inspector
  
- then we are setting the old offset default value to the new offset values

- importing a premade 2d player asset and tweaking its animation speed to matches our background
 and foreground speed
  
- to make it look good we made our background speed half of the foreground speed

- with that, this project is completed

	
DATE: 04-02-2022

- Understanding Navmesh in Unity

- Creating a Monster enemy that will gonna follow our player where ever it goes

- C# Script called "PlayerChaseScript"

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.AI;

public class PlayerChaseScript : MonoBehaviour
{
  public GameObject player;
  NavMeshAgent agent;

  void Start(){
    agent = GetComponent<NavMeshAgent>();
  }

  void Update(){
    agent.SetDestination(player.transform.position);
  }
}

- AI monster learn how to avoid obstacles while chasing the player

- AI monster learn how to use stairs

- AI monster learn how to do jump from one position to another position

	
DATE: 05-02-2022

- Creating a Game called "Little Zig Little Zag"

- Creating a new 3D project in Unity

- Setting the screen Resolution for our game

- Building the Game Level

- Creating a cube and turning it into a platform by changing its scale values to 10 on the x-axis and 10 on the z-axis
 in unity inspector
  
- Creating a 3d Sphere that is gonna be our ball that the player can control 

- adding colors to both of them 

- setting the camera view according to our game view so that it's looking good in the final product

- renaming our cube game object to "PlatformStart" and the sphere to "ball"

- adding physics to our game

- adding rigidbody to our ball

- freezing the ball rotation to the x,y, and z-axis so that it's looks and feel good in our game

- Creating an C# script called "BallController" and adding it to our ball game object

- Creating ball movement so that our ball only move in x and z directions

- and whenever we press the left mouse button our ball should change from x to z and z to x

- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
  [SerializeField]
  private float speed;

  Rigidbody rb;

  private void Awake(){

    rb = GetComponent<Rigidbody>();
  }

void Start(){
rb.rigidbody = new vector3 (speed,0,0);
}

  void Update(){

    if (Input.GetMouseButtonDown(0)){
      SwitchDirection();
    }
  }

  void SwitchDirection(){

    if(rb.velocity.x > 0){
      rb.velocity = new Vector3(0, 0, speed);
    }
    else if(rb.velocity.z > 0){
      rb.velocity = new Vector3(speed, 0, 0);
    }
  }

	
DATE:	06-02-2022

- Moving Ball after the first touch

	- done some changes in our BallController script to achive this functionality
	
- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
    [SerializeField]
    private float speed;

    Rigidbody rb;
	bool started;

    private void Awake(){
        rb = GetComponent<Rigidbody>();
    }

    void Update(){

        if (!started){										
            if (Input.GetMouseButtonDown(0)){				
                rb.velocity = new Vector3(speed, 0, 0);		
                started = true;								
            }												
        }													
		
		if (Input.GetMouseButtonDown(0)){
            SwitchDirection();
        }
    }

    void SwitchDirection(){

        if(rb.velocity.x > 0){
            rb.velocity = new Vector3(0, 0, speed);
        }
        else if(rb.velocity.z > 0){
            rb.velocity = new Vector3(speed, 0, 0);
        }
    }

	
DATE: 07-02-2022

- Checking when the ball falls off the platform

- done some changes in our BallController script to achieve this functionality

- we are using RayCasting to check if our ball is on the platform or not 

- we are casting Ray from our ball downwards to the platform for 1 unit

- and checking if it is colliding with something or not

- if our ball is on the platform then its gonna keep moving because Raycast is gonna return a value
 that shows that it returns from something

- and if it is not on the platform then there is nothing to return by Raycast so it is gonna fall

- also adding some game over logic so that the game stop playing if we fall from the platform

- fixing a bug in which our ball stop for stop time before falling from the platform

- to achieve this we are creating a physics material and setting its friction to 0

- and attaching it to the Material Component of the Ball Sphere Collider 

- also attaching it to the Material Component of the Platform Box Collider

- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
  [SerializeField]
  private float speed;

  Rigidbody rb;
  bool started = false;
  bool gameOver = false;

  private void Awake(){

    rb = GetComponent<Rigidbody>();
  }

  void Update(){

    if (!started){
      if (Input.GetMouseButtonDown(0)){
        rb.velocity = new Vector3(speed, 0, 0);
        started = true;
      }
    }

    Debug.DrawRay(transform.position, Vector3.down, Color.red);

    if(!Physics.Raycast(transform.position, Vector3.down, 1f)){
      gameOver = true;
      rb.velocity = new Vector3(0, -25f, 0);
    }

    if (Input.GetMouseButtonDown(0) && !gameOver){
      SwitchDirection();
    }
  }

  void SwitchDirection(){

    if(rb.velocity.x > 0){
      rb.velocity = new Vector3(0, 0, speed);
    }
    else if(rb.velocity.z > 0){
      rb.velocity = new Vector3(speed, 0, 0);
    }
  }


DATE: 08-02-2022

- Making Camera Follow the Ball

- Created an C# Script called "CameraFollow"

- CameraFollow C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CameraFollow : MonoBehaviour
{
  public GameObject ball;
  public float lerpRate;
  public bool gameOver = false;

  Vector3 offset;

  void Start(){
    offset = ball.transform.position - transform.position;
  }

  void Update(){

    if (!gameOver){
      Follow();
    }
  }

  void Follow(){

    Vector3 pos = transform.position;
    Vector3 targetPos = ball.transform.position - offset;
    pos = Vector3.Lerp(pos, targetPos, lerpRate * Time.deltaTime);
    transform.position = pos;
  }
}


DATE: 09-02-2022

Break

DATE: 10-02-2022

- Making the Platform fall down after the ball goes away

- Creating an empty game object called "TriggerChecker" as a child of Platform game object

- adding box collider2D to it and setting isTrigger property to true

- Creating and adding an C# Script called TriggerCheckerScript to the TriggerChecker game object

- and we are destroying the parent of TriggerChecker game object which is Platform game object
 after the ball goes away from it
  
- TriggerCheckerScript 

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class TriggerCheckerScript : MonoBehaviour
{
  private void OnTriggerExit(Collider other){
     
    if(other.gameObject.tag == "Ball"){
      Invoke("FallDown", 0.1f);
    }
  }

  void FallDown(){
    GetComponentInParent<Rigidbody>().useGravity = true;
    GetComponentInParent<Rigidbody>().isKinematic = false;

    Destroy(transform.parent.gameObject, 2f);
  }
}

	
DATE:	11-02-2022

- Spawning the Platform

	- making the Platform a Prefab so we can use it with the same properties easly
	
	- Creating an empty game object called PlatformSpawner
	
	- Creating an C# Script called PlatformSpawnerScript and attaching it to the PlatformSpawner game object
	
	- Creating an public GameObject variable in the script and adding the Platform prefab to it
	
	- because we want that platform prefab to spawn from that script
	
- PlatformSpawnerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlatFormSpawnerScript : MonoBehaviour
{
    public GameObject platform;

    Vector3 lastPos;
    float size;

    void Start(){

        lastPos = platform.transform.position;
        size = platform.transform.localScale.x;

        for(int i = 0; i < 40; i++){
            SpawnX();
        }
    }  

    void SpawnX(){

        Vector3 pos = lastPos;
        pos.x += size;

        lastPos = pos;
        Instantiate(platform, pos, Quaternion.identity);
    }

    void SpawnZ(){

        Vector3 pos = lastPos;
        pos.z += size;

        lastPos = pos;
        Instantiate(platform, pos, Quaternion.identity);
    }
}

			      
DATE: 12-02-2022

- Creating an AI that will spawn the Platform randomly so that players never get the same level

- Created this AI in the PlatFormSpawnerScript

- PlatFormSpawnerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlatFormSpawnerScript : MonoBehaviour
{
  public GameObject platform;
  public bool gameOver;

  Vector3 lastPos;
  float size;

  void Start(){

    lastPos = platform.transform.position;
    size = platform.transform.localScale.x;

    for(int i = 0; i < 40; i++){
      SpawnPlatfroms();
    }

InvokeRepeating("SpawnPlatfroms", 1f, 0.2f);
  }

void Update(){
if(gameOver){
  CancelInvoke("SpawnPlatfroms");
}
  }

  void SpawnPlatfroms(){

    int random = Random.Range(0, 6);

    if(random < 3){
      SpawnX();
    }
     
    else if( random >= 3){
      SpawnZ();
    }
  }

  void SpawnX(){

    Vector3 pos = lastPos;
    pos.x += size;

    lastPos = pos;
    Instantiate(platform, pos, Quaternion.identity);
  }

  void SpawnZ(){

    Vector3 pos = lastPos;
    pos.z += size;

    lastPos = pos;
    Instantiate(platform, pos, Quaternion.identity);
  }
}

	
DATE: 13-02-2022

- Creating Diamonds and Randomly Spawning

- Created a Diamond game object and gave it a Diamond tag so we can easily call it from scripts

- Created a Material and added it to the Diamond and change its color to pink using that material

- Making Diamonds a Prefab so we can easily instantiate it in the game using C# Script

- added Diamonds in the Game AI so they can spawn randomly

- we achieve this by doing some changes in the PlatFormSpawnerScript

- PlatFormSpawnerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlatFormSpawnerScript : MonoBehaviour
{
  public GameObject platform;
  public GameObject diamonds;
  public bool gameOver;

  Vector3 lastPos;
  float size;

  void Start(){

    lastPos = platform.transform.position;
    size = platform.transform.localScale.x;

    for(int i = 0; i < 40; i++){
      SpawnPlatfroms();
    }
  }

  public void StartSpawningPlatforms(){
    InvokeRepeating("SpawnPlatfroms", 1f, 0.2f);
  }  

  void Update(){
if(gameOver){
  CancelInvoke("SpawnPlatfroms");
}
  }

  void SpawnPlatfroms(){

    int random = Random.Range(0, 6);

    if(random < 3){
      SpawnX();
    }
     
    else if( random >= 3){
      SpawnZ();
    }
  }

  void SpawnX(){

    Vector3 pos = lastPos;
    pos.x += size;

    lastPos = pos;
    Instantiate(platform, pos, Quaternion.identity);

    int randomDimondsX = Random.Range(0, 6);
     
    if(randomDimondsX == 1){
      Instantiate(diamonds, new Vector3(pos.x, pos.y + 1, pos.z), diamonds.transform.rotation);
    }
  }

  void SpawnZ(){

    Vector3 pos = lastPos;
    pos.z += size;

    lastPos = pos;
    Instantiate(platform, pos, Quaternion.identity);

    int randomDimondsY = Random.Range(0, 6);

    if(randomDimondsY == 2){
      Instantiate(diamonds, new Vector3(pos.x, pos.y + 1, pos.z), diamonds.transform.rotation);
    }
  }
}

	
DATE: 14-02-2022

- Destroying Diamonds after the player ball touches them

- Done some changes in the BallController Script

- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
  AudioSource sound;

  public GameObject particle;

  [SerializeField]
  private float speed;

  Rigidbody rb;
  bool started = false;
  bool gameOver = false;

  private void Awake(){

    rb = GetComponent<Rigidbody>();
    sound = GetComponent<AudioSource>();
  }

  void Update(){

    if (!started){
      if (Input.GetMouseButtonDown(0)){
        rb.velocity = new Vector3(speed, 0, 0);
        started = true;

        GameManagerScript.instance.StartGame();
      }
    }

    Debug.DrawRay(transform.position, Vector3.down, Color.red);

    if(!Physics.Raycast(transform.position, Vector3.down, 1f)){
      gameOver = true;
      rb.velocity = new Vector3(0, -25f, 0);

      Camera.main.GetComponent<CameraFollow>().gameOver = true;

      GameManagerScript.instance.GameOver();
    }

    if (Input.GetMouseButtonDown(0) && !gameOver){
      SwitchDirection();
    }
  }

  void SwitchDirection(){

    if(rb.velocity.x > 0){
      rb.velocity = new Vector3(0, 0, speed);
    }
    else if(rb.velocity.z > 0){
      rb.velocity = new Vector3(speed, 0, 0);
    }
  }

  private void OnTriggerEnter(Collider other){
    
    if(other.gameObject.tag == "Diamond"){
      Destroy(other.gameObject);
    }
  }
}

DATE: 15-02-2022

- Creating Some Particle Effects for our game in Unity using Unity Particle System

- Creating a particle for ours diamonds so that when we collect them they show this Particle

- making the particle a prefab so we can use it to instantiate on the diamonds

- added particle system code inside BallController C# Script

- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
  public GameObject particle;

  [SerializeField]
  private float speed;

  Rigidbody rb;
  bool started = false;
  bool gameOver = false;

  private void Awake(){

    rb = GetComponent<Rigidbody>();
    sound = GetComponent<AudioSource>();
  }

  void Update(){

    if (!started){
      if (Input.GetMouseButtonDown(0)){
        rb.velocity = new Vector3(speed, 0, 0);
        started = true;

        GameManagerScript.instance.StartGame();
      }
    }

    Debug.DrawRay(transform.position, Vector3.down, Color.red);

    if(!Physics.Raycast(transform.position, Vector3.down, 1f)){
      gameOver = true;
      rb.velocity = new Vector3(0, -25f, 0);

      Camera.main.GetComponent<CameraFollow>().gameOver = true;

      GameManagerScript.instance.GameOver();
    }

    if (Input.GetMouseButtonDown(0) && !gameOver){
      SwitchDirection();
    }
  }

  void SwitchDirection(){

    if(rb.velocity.x > 0){
      rb.velocity = new Vector3(0, 0, speed);
    }
    else if(rb.velocity.z > 0){
      rb.velocity = new Vector3(speed, 0, 0);
    }
  }

  private void OnTriggerEnter(Collider other){
     
    if(other.gameObject.tag == "Diamond"){

      GameObject particalGameObject = Instantiate(partical, other.gameObject.transform.position, Quaternion.identity) as GameObject;

      Destroy(other.gameObject);
      Destroy(particalGameObject, 0.8f);
    }
  }
}

DATE: 16-02-2022

- Creating UI Manager and Text Animation

	- Creating two empty game object called UIManager and GameManager
	
	- and adding an C# Script called UIManagerScript and GameManagerScript to those empty game objects
	
	- Creating UI for our Game
	
	- Creating an UI for Game title screen
	
	- Creating Your Score and high Score UI
	
	- Creating an UI for Game OverScreen
	
	- and setting UI Scale Mode to Constant Pixel Size so that our game adjets according to player device
	
	- Creating Animations for our Game UI

	
DATE: 17-02-2022

- Scripting the UI of our Game

	- making our title screen and game over screen title animation and button functional
	
- UIManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

public class UIManagerScript : MonoBehaviour
{
    public static UIManagerScript instance;

    public GameObject titlePanel;
    public GameObject gameOverPanel;
    public GameObject tapText;
    public Text score;
    public Text bestScore;

    public Text littleZigText;
    public Text littleZagText;
    public Text highScore;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    public void GameStart(){

        tapText.SetActive(false);
        titlePanel.GetComponent<Animator>().Play("Panel");
        littleZigText.GetComponent<Animator>().Play("LittleZig");
        littleZagText.GetComponent<Animator>().Play("LittleZag");
    }

    public void GameOver(){
        gameOverPanel.SetActive(true);
    }

    public void Restart(){
        SceneManager.LoadScene(0);
    }
}

DATE: 18-02-2022

- Creating Score Manager and HighScore

	- Creating an empty GameObject called ScoreManager
	
	- Creating an C# Script called ScoreManagerScript
	
	- we are doing all the calculation of our game score in this script
	
- ScoreManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ScoreManagerScript : MonoBehaviour
{
    public static ScoreManagerScript instance;

    public int score;
    public int highScore;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    void Start(){
        score = 0;
    }

    void IncrementScore(){
        score++;
        PlayerPrefs.SetInt("scoreKey", score);
    }

    public void StartScore(){
        InvokeRepeating("IncrementScore", 0.1f, 0.5f);
    }

    public void StopScore(){
        CancelInvoke("IncrementScore");
        PlayerPrefs.SetInt("scoreKey", score);

        if (PlayerPrefs.HasKey("highScore")){

            if(score > PlayerPrefs.GetInt("highScore")){
                PlayerPrefs.SetInt("highScore", score);
            }
        }
        
        else{
            PlayerPrefs.SetInt("highScore", score);
        }
    }
}
	

DATE: 19-02-2022

Break

DATE: 20-02-2022

- Creating GameManager and Controlling the whole game

	- Created an empy game object called GameManager
	
	- and attached a C# Script called GameManagerScript to it.
	
- GameManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class GameManagerScript : MonoBehaviour
{
    public static GameManagerScript instance;

    public bool gameOver;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    void Start(){
        gameOver = false;
    }

    public void StartGame(){
        
        UIManagerScript.instance.GameStart();
        ScoreManagerScript.instance.StartScore();

        GameObject.Find("PlatFormSpawner").GetComponent<PlatFormSpawnerScript>().StartSpawningPlatforms();
    }

    public void GameOver(){

        UIManagerScript.instance.GameOver();
        ScoreManagerScript.instance.StopScore();

        gameOver = true;
    }
}

	
DATE: 21-02-2022

	- with some small bug fixes and some code changes here is all the C# Script for this project
	
- BallController C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BallController : MonoBehaviour
{
    AudioSource sound;

    public GameObject partical;

    [SerializeField]
    private float speed;

    Rigidbody rb;
    bool started = false;
    bool gameOver = false;

    private void Awake(){

        rb = GetComponent<Rigidbody>();
        sound = GetComponent<AudioSource>();
    }

    void Update(){

        if (!started){
            if (Input.GetMouseButtonDown(0)){
                rb.velocity = new Vector3(speed, 0, 0);
                started = true;

                GameManagerScript.instance.StartGame();
            }
        }

        Debug.DrawRay(transform.position, Vector3.down, Color.red);

        if(!Physics.Raycast(transform.position, Vector3.down, 1f)){
            gameOver = true;
            rb.velocity = new Vector3(0, -25f, 0);

            Camera.main.GetComponent<CameraFollow>().gameOver = true;

            GameManagerScript.instance.GameOver();
        }

        if (Input.GetMouseButtonDown(0) && !gameOver){
            SwitchDirection();
        }
    }

    void SwitchDirection(){

        if(rb.velocity.x > 0){
            rb.velocity = new Vector3(0, 0, speed);
        }
        else if(rb.velocity.z > 0){
            rb.velocity = new Vector3(speed, 0, 0);
        }
    }

    private void OnTriggerEnter(Collider other){
        
        if(other.gameObject.tag == "Diamond"){

            GameObject particalGameObject = Instantiate(partical, other.gameObject.transform.position, Quaternion.identity) as GameObject;

            Destroy(other.gameObject);
            sound.Play();
            Destroy(particalGameObject, 0.8f);
        }
    }
}


- CameraFollow C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CameraFollow : MonoBehaviour
{
    public GameObject ball;
    public float lerpRate;
    public bool gameOver = false;

    Vector3 offset;

    void Start(){
        offset = ball.transform.position - transform.position;
    }

    void Update(){

        if (!gameOver){
            Follow();
        }
    }

    void Follow(){

        Vector3 pos = transform.position;
        Vector3 targetPos = ball.transform.position - offset;
        pos = Vector3.Lerp(pos, targetPos, lerpRate * Time.deltaTime);
        transform.position = pos;
    }
}

- TriggerCheckerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class TriggerCheckerScript : MonoBehaviour
{
    private void OnTriggerExit(Collider other){
        
        if(other.gameObject.tag == "Ball"){
            Invoke("FallDown", 0.1f);
        }
    }

    void FallDown(){
        GetComponentInParent<Rigidbody>().useGravity = true;
        GetComponentInParent<Rigidbody>().isKinematic = false;

        Destroy(transform.parent.gameObject, 2f);
    }
}

- PlatFormSpawnerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlatFormSpawnerScript : MonoBehaviour
{
    public GameObject platform;
    public GameObject diamonds;
    public bool gameOver;

    Vector3 lastPos;
    float size;

    void Start(){

        lastPos = platform.transform.position;
        size = platform.transform.localScale.x;

        for(int i = 0; i < 40; i++){
            SpawnPlatfroms();
        }
    }

    public void StartSpawningPlatforms(){
        InvokeRepeating("SpawnPlatfroms", 1f, 0.2f);
    }   

    void Update(){

        if (GameManagerScript.instance.gameOver == true){
            CancelInvoke("SpawnPlatfroms");
        }
    }

    void SpawnPlatfroms(){

        int random = Random.Range(0, 6);

        if(random < 3){
            SpawnX();
        }
        
        else if( random >= 3){
            SpawnZ();
        }
    }

    void SpawnX(){

        Vector3 pos = lastPos;
        pos.x += size;

        lastPos = pos;
        Instantiate(platform, pos, Quaternion.identity);

        int randomDimondsX = Random.Range(0, 6);
        
        if(randomDimondsX == 1){
            Instantiate(diamonds, new Vector3(pos.x, pos.y + 1, pos.z), diamonds.transform.rotation);
        }
    }

    void SpawnZ(){

        Vector3 pos = lastPos;
        pos.z += size;

        lastPos = pos;
        Instantiate(platform, pos, Quaternion.identity);

        int randomDimondsY = Random.Range(0, 6);

        if(randomDimondsY == 2){
            Instantiate(diamonds, new Vector3(pos.x, pos.y + 1, pos.z), diamonds.transform.rotation);
        }
    }
}

- GameManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class GameManagerScript : MonoBehaviour
{
    public static GameManagerScript instance;

    public bool gameOver;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    void Start(){
        gameOver = false;
    }

    public void StartGame(){
        
        UIManagerScript.instance.GameStart();
        ScoreManagerScript.instance.StartScore();

        GameObject.Find("PlatFormSpawner").GetComponent<PlatFormSpawnerScript>().StartSpawningPlatforms();
    }

    public void GameOver(){

        UIManagerScript.instance.GameOver();
        ScoreManagerScript.instance.StopScore();

        gameOver = true;
    }
}

- UIManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

public class UIManagerScript : MonoBehaviour
{
    public static UIManagerScript instance;

    public GameObject titlePanel;
    public GameObject gameOverPanel;
    public GameObject tapText;
    public Text score;
    public Text bestScore;

    public Text littleZigText;
    public Text littleZagText;
    public Text highScore;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    void Start(){
        highScore.text = "HighScore: " + PlayerPrefs.GetInt("highScore").ToString();
    }

    public void GameStart(){

        tapText.SetActive(false);
        titlePanel.GetComponent<Animator>().Play("Panel");
        littleZigText.GetComponent<Animator>().Play("LittleZig");
        littleZagText.GetComponent<Animator>().Play("LittleZag");
        highScore.GetComponent<Animator>().Play("HighScore");
    }

    public void GameOver(){

        score.text = PlayerPrefs.GetInt("scoreKey").ToString();
        bestScore.text = PlayerPrefs.GetInt("highScore").ToString();
        gameOverPanel.SetActive(true);
    }

    public void Restart(){
        SceneManager.LoadScene(0);
    }
}

- ScoreManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ScoreManagerScript : MonoBehaviour
{
    public static ScoreManagerScript instance;

    public int score;
    public int highScore;

    private void Awake(){
        if(instance == null){
            instance = this;
        }
    }

    void Start(){
        score = 0;
    }

    void IncrementScore(){
        score++;
        PlayerPrefs.SetInt("scoreKey", score);
    }

    public void StartScore(){
        InvokeRepeating("IncrementScore", 0.1f, 0.5f);
    }

    public void StopScore(){
        CancelInvoke("IncrementScore");
        PlayerPrefs.SetInt("scoreKey", score);

        if (PlayerPrefs.HasKey("highScore")){

            if(score > PlayerPrefs.GetInt("highScore")){
                PlayerPrefs.SetInt("highScore", score);
            }
        }
        
        else{
            PlayerPrefs.SetInt("highScore", score);
        }
    }
}

- now our game "Little Zig Little Zag" is Completed

	

DATE: 22-02-2022

- Creating An Game called "Bricks Breaker"

- Creating Sprites for our Game

- Importing Ball Sprite

- Importing Player Paddel Sprite

- Importing the Bricks Sprites

- Creating four Walls that are the boundaries

- our ball and paddle should not go outside of the screen that is where these boundaries are gonna help us 
 in keeping our ball and player paddle within the screen
  
- Creating a Game Level

- Making our Game functional with C# Scripts

- Making Player Paddle movement

- Created and added an C# Script called "PaddelScript"

- PaddelScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityStandardAssets.CrossPlatformInput;

public class PaddelScript : MonoBehaviour
{
  public float speed;

  private void Update(){
    float movement = CrossPlatformInputManager.GetAxis("Horizontal");
    transform.position += new Vector3(movement, 0, 0) * Time.deltaTime * speed;

    transform.position = new Vector3(Mathf.Clamp(transform.position.x, -8.88f, 8.88f),transform.position.y,transform.position.z);
  }
}

- in PaddelScript we are first Creating Player Paddel Movement

- and then keeping our player paddle within the screen 

- so that our paddle does not go outside of the screen

- we are achieving this using Mathf.Clamp Function

	
DATE: 23-02-2022

- Making our Ball Move

- Created and C# Script called "BallScript"

- and adding it to the Ball GameObject

- BallScript

using UnityEngine;

public class BallScript : MonoBehaviour
{

public float speed;

Rigidbody2D rb;

private void Awake(){
    rb = GetComponent<Rigidbody2D>();
  }

  void Start(){
    Invoke(nameof(BallRandomStart), 1f);
  }

  private void BallRandomStart(){
     
    Vector2 force = Vector2.zero;
    force.x = UnityEngine.Random.Range(-0.5f, 0.5f);
    force.y = -1f;

    rb.AddForce(force.normalized * speed);
  }
}

- in BallScript we are doing these things

- first, we are getting access to the Rigidbody2D Component

- then we are creating a Function called BallRandomStart()

- in this function, we are adding force to the ball game object

- and making its first movement random in the x and y-axis

- which means when the game starts ball can either go to the right or left

- it will go just a little right or left so that our ball be on the player's paddle

- and at the end, we are calling the BallRandomStart() Function in the Start Function using Invoke

- so that our Ball first wait for 1 Second then it starts moving so that the player has some breathing room
 before the game starts

	
DATE: 24-02-2022

Break

DATE: 25-02-2022

- Destroy our Bricks whenever the ball touches them

- so we are destroying the bricks whenever the ball touches them

- to achive this we are using OnCollisionEnter2D funcion

- and adding the "Brick" tag to all the bricks in the game

- then destroying anything that has that brick tag to it

- we added some code in our "BallScript"

- BallScript

using UnityEngine;

public class BallScript : MonoBehaviour
{

public float speed;

Rigidbody2D rb;

private void Awake(){
    rb = GetComponent<Rigidbody2D>();
  }

  void Start(){
    Invoke(nameof(BallRandomStart), 1f);
  }

  private void BallRandomStart(){
     
    Vector2 force = Vector2.zero;
    force.x = UnityEngine.Random.Range(-0.5f, 0.5f);
    force.y = -1f;

    rb.AddForce(force.normalized * speed);
  }
}

private void OnCollisionEnter2D(Collision2D collision){
     
    if (collision.gameObject.tag == "Brick"){
      Destroy(collision.gameObject);
    }
}

- Changing the Color of the walls to some random color whenever our ball touch them

- we have four walls in our game 

- and we are changing the color of the 3 walls. top left and right walls

- and adding a C# Script called "OtherWallScript"

- and keeping the down wall separate from that script

- because we need to destroy the ball whenever the ball touch the down wall 

- which means the player lose the game and we need to end the game

- OtherWallScript

using UnityEngine;

public class OtherWallScript : MonoBehaviour
{
  private void OnCollisionEnter2D(Collision2D collision){

    if (collision.gameObject.tag == "Ball"){

      GetComponent<Renderer>().material.color = Random.ColorHSV(0f, 1f, 1f, 1f, 0.5f, 1f);
    }
  }
}

	
DATE: 26-02-2022

- now making a C# script for the down wall called "WallScript"

- in this script, we are checking if the game object that is colliding with the wall has a tag called "Ball"

- then we are changing the color of the down wall to red

- then we are destroying the ball

- WallScript

using UnityEngine;

public class WallScript : MonoBehaviour
{
  public GameObject gameOverScreen;

  private void OnCollisionEnter2D(Collision2D collision){
     
    if (collision.gameObject.tag == "Ball"){

      GetComponent<Renderer>().material.color = Color.red;
      Destroy(collision.gameObject);

      gameOverScreen.SetActive(true);
    }
  }
}

	
DATE: 27-02-2022

- adding a feature in the game to fix a game bug

- we see in our playtest that sometimes the ball gets stuck in between the left wall and right wall

- so to fix that we are adding ball shooting mechanics

- in this, we are adding two shooting points in our player paddle one in the left and one in the right

- so whenever we press the fire button on the left or right our paddle goona shoot a ball from that side

- so we can aim for the stuck ball and shoot at it so, which will gonna add more force to it because of it
 the ball is gonna start moving again
  
- to achieve this first we created two empty game objects on the paddle on the left and right

- then Created and added a C# script called "ShootScript" in the left empty game object

- and Created and added a C# script called "ShootingFromRightScript" in the right empty game object

- ShootScript

using UnityEngine;

public class ShootingScript : MonoBehaviour
{
  public GameObject bullet;

  GameObject instantiatedObj;

  public void LeftShoot(){

    instantiatedObj = (GameObject)Instantiate(bullet, transform.position, Quaternion.identity);
    Destroy(instantiatedObj, 0.8f);
  }
}

- ShootingFromRightScript

using UnityEngine;

public class ShootingFromRightScript : MonoBehaviour
{
  public GameObject bullet;

  GameObject instantiatedObj;

  public void RightShoot(){

    instantiatedObj = (GameObject)Instantiate(bullet, transform.position, Quaternion.identity);
    Destroy(instantiatedObj, 0.8f);
  }
}

	
DATE: 28-02-2022

- Adding UI in our game

- adding a scoreboard on the top wall in the game

- that shows us in real-time how many bricks we have destroyed

- adding time taken on the top wall in the game

- that shows us in real-time how much time it takes us to win or lose our game

- adding the code of these UI features in our BallScript

- BallScript

using System.Collections;
using System.Collections.Generic;
using System;
using UnityEngine;
using UnityEngine.UI;

public class BallScript : MonoBehaviour
{
  public float speed;

  public Text currentTimeText;
  public Text bricksDestroyedText;

  float currentTime = 0;

  Rigidbody2D rb;

  int bricksCount = 0;
  int bricksDestroyed = 0;

  private void Awake(){
    rb = GetComponent<Rigidbody2D>();
  }

  void Start(){
    Invoke(nameof(BallRandomStart), 1f);
  }

  private void BallRandomStart(){
     
    Vector2 force = Vector2.zero;
    force.x = UnityEngine.Random.Range(-0.5f, 0.5f);
    force.y = -1f;

    rb.AddForce(force.normalized * speed);
  }

  private void OnCollisionEnter2D(Collision2D collision){
     
    if (collision.gameObject.tag == "Brick"){
       
      bricksCount++;
      BricksDestroyedCounter();

      Destroy(collision.gameObject);
    }
  }

  private void FixedUpdate(){

    StopWatch();
  }

  void StopWatch(){
     
    // this is for the gameplay timer and bricks counter

    if (bricksCount != 27){
      currentTime = currentTime + Time.deltaTime;
    }

    else if(bricksCount == 27){
      youWinScreen.SetActive(true);
      Destroy(gameObject);
    }

    TimeSpan time = TimeSpan.FromSeconds(currentTime);
    currentTimeText.text = time.Minutes.ToString() + ":" + time.Seconds.ToString();
  }

  void BricksDestroyedCounter(){

    bricksDestroyed++;
    bricksDestroyedText.text = bricksDestroyed.ToString() + "/27";
  }
}
	

DATE: 01-03-2022

- adding Game Manager in the game

- created an empty gameobject called GameManager

- and added an C# Script called "GameManagerScript" to it

- GameManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class GameManagerScript : MonoBehaviour
{
  public void Restart(){

    SceneManager.LoadScene(SceneManager.GetActiveScene().name);
  }

  public void Exit(){

    Application.Quit();
  }
}

	
DATE: 02-03-2022

- adding YOU WIN and GameOver UI screen in our game

	- Creating You win and Game Over screen 
	
	- and adding Restart and Exit buttons in it
	
	- so we can cantroll it by our GameManagerScript
	
	- added code for these features in our BallScript
	
- BallScript

using System.Collections;
using System.Collections.Generic;
using System;
using UnityEngine;
using UnityEngine.UI;

public class BallScript : MonoBehaviour
{
    public float speed;

    public Text currentTimeText;
    public Text currentTimeMenuText;
    public Text currentTimeYouWinMenuText;

    public Text bricksDestroyedText;
    public Text bricksDestroyedMenuText;
    public Text bricksDestroyedYouWinMenuText;

    public GameObject youWinScreen;

    float currentTime = 0;
    float currentMenuTime = 0;
    float currentYouWinMenuTime = 0;

    Rigidbody2D rb;

    int bricksCount = 0;
    int bricksDestroyed = 0;

    int bricksMenuCount = 0;
    int bricksDestroyedMenu = 0;

    int bricksYouWinMenuCount = 0;
    int bricksDestroyedYouWinMenu = 0;

    private void Awake(){
        rb = GetComponent<Rigidbody2D>();
    }

    void Start(){
        Invoke(nameof(BallRandomStart), 1f);
    }

    private void BallRandomStart(){
        
        Vector2 force = Vector2.zero;
        force.x = UnityEngine.Random.Range(-0.5f, 0.5f);
        force.y = -1f;

        rb.AddForce(force.normalized * speed);
    }

    private void OnCollisionEnter2D(Collision2D collision){
        
        if (collision.gameObject.tag == "Brick"){
            
            bricksCount++;
            bricksMenuCount++;
            bricksYouWinMenuCount++;


            BricksDestroyedCounter();
            BricksDestroyedMenuCounter();
            BricksDestroyedYouWinMenuCounter();

            Destroy(collision.gameObject);
        }
    }

    private void FixedUpdate(){

        StopWatch();
    }

    void StopWatch(){
        
        // this is for the gameplay timer and bricks counter

        if (bricksCount != 27){
            currentTime = currentTime + Time.deltaTime;
        }

        else if(bricksCount == 27){
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan time = TimeSpan.FromSeconds(currentTime);
        currentTimeText.text = time.Minutes.ToString() + ":" + time.Seconds.ToString();

        // this is for the GameOver timer and bricks counter

        if (bricksMenuCount != 27){
            currentMenuTime = currentMenuTime + Time.deltaTime;
        }

        else if (bricksMenuCount == 27){
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan timeMenu = TimeSpan.FromSeconds(currentMenuTime);
        currentTimeMenuText.text = timeMenu.Minutes.ToString() + ":" + timeMenu.Seconds.ToString();

        // this is for the YouWin timer and bricks counter

        if (bricksYouWinMenuCount != 27)
        {
            currentYouWinMenuTime = currentYouWinMenuTime + Time.deltaTime;
        }

        else if (bricksYouWinMenuCount == 27)
        {
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan timeYouWinMenu = TimeSpan.FromSeconds(currentYouWinMenuTime);
        currentTimeYouWinMenuText.text = timeYouWinMenu.Minutes.ToString() + ":" + timeYouWinMenu.Seconds.ToString();
    }

    void BricksDestroyedCounter(){

        bricksDestroyed++;
        bricksDestroyedText.text = bricksDestroyed.ToString() + "/27";
    }

    void BricksDestroyedMenuCounter(){

        bricksDestroyedMenu++;
        bricksDestroyedMenuText.text = bricksDestroyedMenu.ToString() + "/27";
    }

    void BricksDestroyedYouWinMenuCounter(){

        bricksDestroyedYouWinMenu++;
        bricksDestroyedYouWinMenuText.text = bricksDestroyedYouWinMenu.ToString() + "/27";
    }
}

	- with that our game is completed
	
	
DATE: 03-03-2022

	- here is all the C# Script that we used to create this game
	
- ShootingFromRightScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ShootingFromRightScript : MonoBehaviour
{
    public GameObject bullet;

    GameObject instantiatedObj;

    public void RightShoot(){

        instantiatedObj = (GameObject)Instantiate(bullet, transform.position, Quaternion.identity);
        Destroy(instantiatedObj, 0.8f);
    }
}


- ShootingScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ShootingScript : MonoBehaviour
{
    public GameObject bullet;

    GameObject instantiatedObj;

    public void LeftShoot(){

        instantiatedObj = (GameObject)Instantiate(bullet, transform.position, Quaternion.identity);
        Destroy(instantiatedObj, 0.8f);
    }
}

- BulletBallScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BulletBallScript : MonoBehaviour
{
    public float bulletForce;

    Rigidbody2D rb;

    void Awake(){
        rb = GetComponent<Rigidbody2D>();
    }

    void Start(){
        rb.AddForce(Vector2.up * bulletForce);
    }
}


- GameManagerScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class GameManagerScript : MonoBehaviour
{
    public void Restart(){

        SceneManager.LoadScene(SceneManager.GetActiveScene().name);
    }

    public void Exit(){

        Application.Quit();
    }
}


- OtherWallScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class OtherWallScript : MonoBehaviour
{
    private void OnCollisionEnter2D(Collision2D collision){

        if (collision.gameObject.tag == "Ball"){

            GetComponent<Renderer>().material.color = Random.ColorHSV(0f, 1f, 1f, 1f, 0.5f, 1f);
        }
    }
}


- WallScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WallScript : MonoBehaviour
{
    public GameObject gameOverScreen;

    private void OnCollisionEnter2D(Collision2D collision){
        
        if (collision.gameObject.tag == "Ball"){

            GetComponent<Renderer>().material.color = Color.red;
            Destroy(collision.gameObject);

            gameOverScreen.SetActive(true);
        }
    }
}


- BallScript

using System.Collections;
using System.Collections.Generic;
using System;
using UnityEngine;
using UnityEngine.UI;

public class BallScript : MonoBehaviour
{
    public float speed;

    public Text currentTimeText;
    public Text currentTimeMenuText;
    public Text currentTimeYouWinMenuText;

    public Text bricksDestroyedText;
    public Text bricksDestroyedMenuText;
    public Text bricksDestroyedYouWinMenuText;

    public GameObject youWinScreen;

    float currentTime = 0;
    float currentMenuTime = 0;
    float currentYouWinMenuTime = 0;

    Rigidbody2D rb;

    int bricksCount = 0;
    int bricksDestroyed = 0;

    int bricksMenuCount = 0;
    int bricksDestroyedMenu = 0;

    int bricksYouWinMenuCount = 0;
    int bricksDestroyedYouWinMenu = 0;

    private void Awake(){
        rb = GetComponent<Rigidbody2D>();
    }

    void Start(){
        Invoke(nameof(BallRandomStart), 1f);
    }

    private void BallRandomStart(){
        
        Vector2 force = Vector2.zero;
        force.x = UnityEngine.Random.Range(-0.5f, 0.5f);
        force.y = -1f;

        rb.AddForce(force.normalized * speed);
    }

    private void OnCollisionEnter2D(Collision2D collision){
        
        if (collision.gameObject.tag == "Brick"){
            
            bricksCount++;
            bricksMenuCount++;
            bricksYouWinMenuCount++;


            BricksDestroyedCounter();
            BricksDestroyedMenuCounter();
            BricksDestroyedYouWinMenuCounter();

            Destroy(collision.gameObject);
        }
    }

    private void FixedUpdate(){

        StopWatch();
    }

    void StopWatch(){
        
        // this is for the gameplay timer and bricks counter

        if (bricksCount != 27){
            currentTime = currentTime + Time.deltaTime;
        }

        else if(bricksCount == 27){
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan time = TimeSpan.FromSeconds(currentTime);
        currentTimeText.text = time.Minutes.ToString() + ":" + time.Seconds.ToString();

        // this is for the GameOver timer and bricks counter

        if (bricksMenuCount != 27){
            currentMenuTime = currentMenuTime + Time.deltaTime;
        }

        else if (bricksMenuCount == 27){
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan timeMenu = TimeSpan.FromSeconds(currentMenuTime);
        currentTimeMenuText.text = timeMenu.Minutes.ToString() + ":" + timeMenu.Seconds.ToString();

        // this is for the YouWin timer and bricks counter

        if (bricksYouWinMenuCount != 27)
        {
            currentYouWinMenuTime = currentYouWinMenuTime + Time.deltaTime;
        }

        else if (bricksYouWinMenuCount == 27)
        {
            youWinScreen.SetActive(true);
            Destroy(gameObject);
        }

        TimeSpan timeYouWinMenu = TimeSpan.FromSeconds(currentYouWinMenuTime);
        currentTimeYouWinMenuText.text = timeYouWinMenu.Minutes.ToString() + ":" + timeYouWinMenu.Seconds.ToString();
    }

    void BricksDestroyedCounter(){

        bricksDestroyed++;
        bricksDestroyedText.text = bricksDestroyed.ToString() + "/27";
    }

    void BricksDestroyedMenuCounter(){

        bricksDestroyedMenu++;
        bricksDestroyedMenuText.text = bricksDestroyedMenu.ToString() + "/27";
    }

    void BricksDestroyedYouWinMenuCounter(){

        bricksDestroyedYouWinMenu++;
        bricksDestroyedYouWinMenuText.text = bricksDestroyedYouWinMenu.ToString() + "/27";
    }
}


- PaddelScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityStandardAssets.CrossPlatformInput;

public class PaddelScript : MonoBehaviour
{
    public float speed;

    private void Update(){
        float movement = CrossPlatformInputManager.GetAxis("Horizontal");
        transform.position += new Vector3(movement, 0, 0) * Time.deltaTime * speed;

        transform.position = new Vector3(Mathf.Clamp(transform.position.x, -8.88f, 8.88f),transform.position.y,transform.position.z);
    }
}

	
DATE: 04-03-2022

- Creating a new game called "Passing Through"

- Introduction

- in this game player is in 1st person and he has to go through from the coming hollow boxes

- to score a point and stay alive, if he doesn't through from those boxes then he losses the game

- Creating the Level

- Creating the player which is just a cube with a box collider

- to make it the first person we made the main camera it's child

- and set it to the edge of the cube, so we can see through from that cube

- Creating the hollow boxes 

- to create a hollow box we made four cubes and resize them accordingly to make a frame kind of object

- which is our hollow box

- we also made the hollow box a prefab so we can use it to instantiate as many times as we want in the level

- Scripting the game

- adding player movement

- created an C# script called "PlayerMovement"

- PlayerMovement C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
  public float speed;

  public Joystick joystick;

  private void Update(){

    float xInput = joystick.Horizontal;
    float yInput = joystick.Vertical;

    transform.Translate(xInput * speed * Time.deltaTime, yInput * speed * Time.deltaTime, 0);
  }
}

	
DATE: 05-03-2022

- Making Walls(Hollow box) moving

- Created an C# Script called WallsMoving

- added it to the Walls(Hollow box) prefab

- WallsMoving C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WallsMoving : MonoBehaviour
{
  SpawningWallsScript spawningWallsScriptRefrance;

  public float wallSpeed;

  private void Awake(){
    spawningWallsScriptRefrance = GetComponent<SpawningWallsScript>();
  }

  void Update(){

    transform.position += -transform.forward * wallSpeed * Time.deltaTime;
  }

  private void OnTriggerEnter(Collider other){
    if(other.gameObject.tag == "Player"){
      GameManager.instance.IncrementScore();
    }
  }
}

	
DATE: 06-03-2022

- making Walls Spawn in random places

	- Created an C# Script called "SpawningWallsScript"
	
	- and attached it to an empty game object called "SpawningWalls"
	
	- this game object and this C# script handle all the walls spawning stuff
	
- SpawningWallsScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SpawningWallsScript : MonoBehaviour
{
    public static SpawningWallsScript instance;

    public GameObject Walls;
    
    public int xPosition;
    public int yPosition;
    public int zPosition;

    private void Awake(){
        instance = this;
    }

    void Start(){
        StartSpawningWalls();
    }

    void SpawnWalls(){

        int xPos = Random.Range(-xPosition, xPosition);
        int yPos = Random.Range(-yPosition, yPosition);

        Instantiate(Walls, new Vector3(xPos, yPos, transform.position.z), Quaternion.identity);
    }

    IEnumerator WallsSpawn(){

        yield return new WaitForSeconds(1f);

        while (true){
            
            SpawnWalls();

            yield return new WaitForSeconds(2f);
        }
        
    }

    public void StartSpawningWalls(){
        StartCoroutine("WallsSpawn");
    }

    public void StopSpawningWalls(){
        StopCoroutine("WallsSpawn");
    }
}


DATE: 07-03-2022

	- Created and C# script called "CollisionScript"
	
	- and attached it to the Player game object
	
	- this script handle all the collision stuff
	
- CollisionScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CollisionScript : MonoBehaviour
{
    public GameObject Walls;

    private void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "WallCol"){
            transform.DetachChildren();
            Destroy(gameObject);
            FindObjectOfType<SpawningWallsScript>().StopSpawningWalls();
        }
    }
}

- also added some PostProssing to the Walls

	
DATE: 08-03-2022

- Created UI for the game and GameManager to handle all the game Events

- Created UI for the game 

- if a player goes through the wall then the player gets one point 

- and he misses the wall then the player gets destroyed and it's a game over

- Creating Game Manager for the game

- Created an empty game object called GameManager

- and attached an C# script called "GameManager" to it

- GameManager

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

public class GameManager : MonoBehaviour
{
  public static GameManager instance;

  public GameObject gameOverCanvas;

  public Text scoreText;
  public Text menuYourScoreText;
  public Text menuHighScoreText;
  public int score;
  public bool gameOver;

  private void Awake(){
    if (instance == null){
      instance = this;
    }
  }

  private void Start(){
    menuHighScoreText.text = PlayerPrefs.GetInt("HighScore", 0).ToString();
  }

  public void IncrementScore(){
    if (!gameOver){
      score++;
      scoreText.text = score.ToString();
      menuYourScoreText.text = score.ToString();

      if(score > PlayerPrefs.GetInt("HighScore",0)){
        PlayerPrefs.SetInt("HighScore", score);
        menuHighScoreText.text = score.ToString();   
      }
    }
  }

  public void RestartButton(){
    SceneManager.LoadScene(0);
  }

  public void ExitButton(){
    Application.Quit();
  }
}

	
DATE: 09-03-2022

	- here is all the C# Script that we used in this game
	
- PlayerMovement

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed;

    public Joystick joystick;

    private void Update(){

        float xInput = joystick.Horizontal;
        float yInput = joystick.Vertical;

        transform.Translate(xInput * speed * Time.deltaTime, yInput * speed * Time.deltaTime, 0);
    }
}


- WallsMoving

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WallsMoving : MonoBehaviour
{
    SpawningWallsScript spawningWallsScriptRefrance;

    public float wallSpeed;

    private void Awake(){
        spawningWallsScriptRefrance = GetComponent<SpawningWallsScript>();
    }

    void Update(){

        transform.position += -transform.forward * wallSpeed * Time.deltaTime;
    }

    private void OnTriggerEnter(Collider other){
        if(other.gameObject.tag == "Player"){
            GameManager.instance.IncrementScore();
        }
    }
}


- SpawningWallsScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SpawningWallsScript : MonoBehaviour
{
    public static SpawningWallsScript instance;

    public GameObject Walls;
    
    public int xPosition;
    public int yPosition;
    public int zPosition;

    private void Awake(){
        instance = this;
    }

    void Start(){
        StartSpawningWalls();
    }

    void SpawnWalls(){

        int xPos = Random.Range(-xPosition, xPosition);
        int yPos = Random.Range(-yPosition, yPosition);

        Instantiate(Walls, new Vector3(xPos, yPos, transform.position.z), Quaternion.identity);
    }

    IEnumerator WallsSpawn(){

        yield return new WaitForSeconds(1f);

        while (true){
            
            SpawnWalls();

            yield return new WaitForSeconds(2f);
        }
        
    }

    public void StartSpawningWalls(){
        StartCoroutine("WallsSpawn");
    }

    public void StopSpawningWalls(){
        StopCoroutine("WallsSpawn");
    }
}


- CollisionScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CollisionScript : MonoBehaviour
{
    public GameObject Walls;

    private void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "WallCol"){
            transform.DetachChildren();
            Destroy(gameObject);
            FindObjectOfType<SpawningWallsScript>().StopSpawningWalls();
            GameManager.instance.gameOver = true;
            GameManager.instance.gameOverCanvas.SetActive(true);
        }
    }
}


- GameManager

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

public class GameManager : MonoBehaviour
{
    public static GameManager instance;

    public GameObject gameOverCanvas;

    public Text scoreText;
    public Text menuYourScoreText;
    public Text menuHighScoreText;
    public int score;
    public bool gameOver;

    private void Awake(){
        if (instance == null){
            instance = this;
        }
    }

    private void Start(){
        menuHighScoreText.text = PlayerPrefs.GetInt("HighScore", 0).ToString();
    }

    public void IncrementScore(){
        if (!gameOver){
            score++;
            scoreText.text = score.ToString();
            menuYourScoreText.text = score.ToString();

            if(score > PlayerPrefs.GetInt("HighScore",0)){
                PlayerPrefs.SetInt("HighScore", score);
                menuHighScoreText.text = score.ToString();     
            }
        }
    }

    public void RestartButton(){
        SceneManager.LoadScene(0);
    }

    public void ExitButton(){
        Application.Quit();
    }
}

	
DATE: 10-03-2022

- Creating a top-down shooter game called "Can You Shoot them"

- importing Game Assets

- importing player model and enemies model

- and assemble them in the Unity

- adding Box Collider2D and Rigidbody2D to the player and the enemies

- Creating Level for the game using Unity Tile-Map System

- and adding TileMap Collider2D at the corner of the level 

- to keep the player and the enemies from getting out of the level

- to achieve this we also need to add the Rigidbody2D and Composite Collider2D to the Tile-Map
	
	
DATE: 11-03-2022

	- adding movement to the player
	
	- we created an C# Script called "PlayerMovement"
	
- PlayerMovement Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed = 5f;
    public Rigidbody2D rb;

    private Vector2 movement;

    void Update(){

        movement.x = Input.GetAxisRaw("Horizontal");
        movement.y = Input.GetAxisRaw("Vertical");
    }

    private void FixedUpdate(){

        rb.MovePosition(rb.position + movement * moveSpeed * Time.fixedDeltaTime);
    }
}

	
DATE: 12-03-2022

Break

DATE: 13-03-2022

- making the player look wherever the mouse is

	- to achive this we first calculated the distance between the mousePosition and the player
	
	- than we calculated the angle at which the player need to be so it can look at the mouse
	
	- to acive this we used unity built-in function called Mathf.Atan2
	
	- after calculating the angle we just rotate the player at that angle
	
	- we added these lines of code to the PlayerMovement Script
	
- PlayerMovement C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed = 5f;
    public Rigidbody2D rb;
    public Camera cam;

    private Vector2 movement;
    private Vector2 mousePos;

    void Update(){

        movement.x = Input.GetAxisRaw("Horizontal");
        movement.y = Input.GetAxisRaw("Vertical");

        mousePos = cam.ScreenToWorldPoint(Input.mousePosition);
    }

    private void FixedUpdate(){

        rb.MovePosition(rb.position + movement * moveSpeed * Time.fixedDeltaTime);

        Vector2 lookDir = mousePos - rb.position;
        float angle = Mathf.Atan2(lookDir.y, lookDir.x) * Mathf.Rad2Deg - 90f;
        rb.rotation = angle;
    }
}

	
DATE: 14-03-2022

- making Camera Follow the Player Movement

- camera follow the player's movement so that the player always be in the view

- we also made the camera restrict to some area

- so our camera does not show the blank area in the level

- Created an C# Script called "CameraFollow" and added it to the MainCamera Game Object

- CameraFollow C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class CameraFollow : MonoBehaviour
{
  private Transform target;

  public float minX;
  public float maxX;
  public float minY;
  public float maxY;

  private void Awake()
  {
    target = GameObject.FindGameObjectWithTag("Player").transform;
  }

  void FixedUpdate(){

    if (target != null){

      transform.position = new Vector3(target.position.x, target.position.y, transform.position.z);

      transform.position = new Vector3(Mathf.Clamp(target.position.x, minX, maxX), Mathf.Clamp(target.position.y, maxY, minY), transform.position.z);
    }
  }
}

	
after a long break, I am back

DATE: 19-03-2022

- Adding Shooting Mechanics to the Player

- Added two empty game objects to the player's left and right hand

- to set it as a bullet spawn point

- then created and C# Script called "Shooting" to the Player Game Object

- Shooting C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Shooting : MonoBehaviour
{
  public Transform firePointRight;
  public Transform firePointLeft;
  public GameObject bulletPrefab;
  public float bulletForce = 20f;
  public float timeBetweenShots;

  private float shotTime;

  void Update(){
    if (Input.GetMouseButtonDown(0)){
       
      if(Time.time >= shotTime){

        ShootRight();
        ShootLeft();
      }
    }
  }

  void ShootRight(){

    GameObject bullet = Instantiate(bulletPrefab, firePointRight.position, firePointRight.rotation);
    shotTime = Time.time + timeBetweenShots;
    Rigidbody2D rb = bullet.GetComponent<Rigidbody2D>();
    rb.AddForce(firePointRight.up * bulletForce, ForceMode2D.Impulse);
  }

  void ShootLeft(){
    GameObject bullet = Instantiate(bulletPrefab, firePointLeft.position, firePointLeft.rotation);
    shotTime = Time.time + timeBetweenShots;
    Rigidbody2D rb = bullet.GetComponent<Rigidbody2D>();
    rb.AddForce(firePointLeft.up * bulletForce, ForceMode2D.Impulse);
  }
}

	
DATE: 20-03-2022

- Creating Player Bullet that the Player will Shoot with his Guns that are attached to the Player Hand

	- Importing Bullet Sprite and adding Rigidbody2D and Box Collider2D to it
	
	- and making the Box Collider2D "isTrigger"
	
	- and Making it a Prefab
	
	- Creating and Adding an C# Script called "BulletScript" to the Bullet Prefab
	
- BulletScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class BulletScript : MonoBehaviour
{
    public GameObject hitEffect;
    public int damage;

    private void OnTriggerEnter2D(Collider2D collision){

        GameObject effect = Instantiate(hitEffect, transform.position, Quaternion.identity);
        Destroy(effect, 0.2f);
        Destroy(gameObject);

        if(collision.tag == "Enemy"){
            collision.GetComponent<Enemy>().TakeDamage(damage);
        }
    }
}

	
DATE: 21-03-2022

- adding Health Bar to the Player

- Creating and Adding a UI for the Health Bar to the Player

- Creating a C# Script called "HealthBarScript"

- HealthBarScript

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;

public class HealthBarScript : MonoBehaviour
{
  public Slider slider;
  public Gradient gradient;
  public Image fill;

  public void SetMaxHealth(float health){

    slider.maxValue = health;
    slider.value = health;

    fill.color = gradient.Evaluate(1f);
  }

  public void SetHealth(float health){

    slider.value = health;

    fill.color = gradient.Evaluate(slider.normalizedValue);
  }
}

	
DATE: 22-03-2022

	- Creating and Adding an C# Script called "PlayerHealth" to the Player

- PlayerHealth C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerHealth : MonoBehaviour
{
    public static PlayerHealth instance;

    public float maxPlayerHealth;

    [HideInInspector]
    public float currentPlayerHealth;

    public HealthBarScript healthBar;

    private void Awake()
    {

        if (instance == null)
        {
            instance = this;
        }
    }

    void Start()
    {

        currentPlayerHealth = maxPlayerHealth;
        healthBar.SetMaxHealth(maxPlayerHealth);
    }

    public void TakeDamage(float damage)
    {

        currentPlayerHealth -= damage;
        healthBar.SetHealth(currentPlayerHealth);

        if (currentPlayerHealth <= 0)
        {

            Destroy(this.gameObject);
        }
    }

    public void Heal(float healAmount){

        if (currentPlayerHealth + healAmount > maxPlayerHealth){

            currentPlayerHealth = maxPlayerHealth;
            healthBar.SetHealth(currentPlayerHealth);
        }

        else{
            
            currentPlayerHealth += healAmount;
            healthBar.SetHealth(currentPlayerHealth);
        }
    }
}

	
DATE: 23-03-2022

- Creating Enemies

- Created an Enemy C# Class that will be the parent class of all the enemies

- We added in this Script all the code that will gonna be used for all the enemies

- Enemy C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Enemy : MonoBehaviour
{
  public float health;
  public float speed;
  public float timeBetweenAttacks;
  public int healthPickupChance;
  public GameObject healthPickup;

  [HideInInspector]
  public Transform player;

  public virtual void Start(){

    player = GameObject.FindGameObjectWithTag("Player").transform;
  }

  public void TakeDamage(float damageAmount){
     
    health -= damageAmount;

    if(health <= 0){

      int randomHealth = Random.Range(0, 101);
       
      if(randomHealth < healthPickupChance){

        Instantiate(healthPickup, transform.position, Quaternion.identity);
      }

      Destroy(this.gameObject);
    }
  }
}

	
DATE: 24-03-2022

- Creating Melee Enemies

	- Creating Melee Enemies that will chase the player around the level
	
	- and if they touch the player the Health will be Depleted
	
	- imported assests for the Melee Enemies
	
	- there are three type of Melee Enemies with diffrent stats
	
	- added box collider2D and rigidbody2D to the ememies
	
	- and Created and added an C# Script called "EnemyChase"
	
- EnemyChase C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EnemyChase : Enemy
{
    public float stopDistance;
    public float attackSpeed;
    public float damage;

    private Rigidbody2D rb;
    private float attackTime;

    private void Awake(){

        rb = GetComponent<Rigidbody2D>();
    }

    private void Update(){

        if (player != null){

            if(Vector2.Distance(transform.position, player.position) > stopDistance){

                transform.position = Vector2.MoveTowards(transform.position, player.position, speed * Time.deltaTime);

                Vector3 direction = player.position - transform.position;
                float angle = Mathf.Atan2(direction.y, direction.x) * Mathf.Rad2Deg - 90f;
                rb.rotation = angle;
            } else{

                if(Time.time >= attackTime){

                    StartCoroutine(Attack());
                    attackTime = Time.time + timeBetweenAttacks;
                }
            }
        }
    }

    IEnumerator Attack(){

        PlayerHealth.instance.TakeDamage(damage);

        Vector2 originalPosition = transform.position;
        Vector2 tartgetPosition = player.position;

        float percent = 0;
        
        while(percent <= 1){
            
            percent += Time.deltaTime * attackSpeed;
            float animationFormula = (-Mathf.Pow(percent, 2) + percent) * 4;

            transform.position = Vector2.Lerp(originalPosition, tartgetPosition, animationFormula);
            yield return null;
        }
    }
}

			   
DATE: 26-03-2022

- Creating Ranged Enemies

	- Creating ranged enemies that will shoot the bullet to the player
	
	- Imported ranged enemies assets
	
	- added box Collider2D and rigidbody2D
	
	- Created an C# Script called "EnemyChaseShoot"
	
	- this C# Script will cahase and shoot a bullet to the player
	
- EnemyChaseShoot C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EnemyChaseShoot : Enemy
{
    private Rigidbody2D rb;
    private Vector2 movement;

    // shooting variables

    private float timeBtwShots;

    public GameObject bulletPrefab;
    public Transform firePointRight;
    public Transform firePointLeft;

    private void Awake(){

        rb = GetComponent<Rigidbody2D>();
    }

    public override void Start(){

        base.Start();
        timeBtwShots = timeBetweenAttacks;
    }

    void Update(){

        if (timeBtwShots <= 0){

            ShootingFromRight();
            ShootingFromLeft();
        }
        
        else{

            timeBtwShots -= Time.deltaTime;
        }

        if (player != null){

            Vector3 direction = player.position - transform.position;
            float angle = Mathf.Atan2(direction.y, direction.x) * Mathf.Rad2Deg - 90f;
            rb.rotation = angle;

            direction.Normalize();
            movement = direction;
        }
    }

    private void FixedUpdate(){

        moveCharacter(movement);
    }

    void moveCharacter(Vector2 direction){

        rb.MovePosition((Vector2)transform.position + (direction * speed * Time.deltaTime));
    }

    // Shooting Functions

    void ShootingFromRight(){

        Instantiate(bulletPrefab, firePointRight.position, firePointRight.rotation);
        timeBtwShots = timeBetweenAttacks;
    }

    void ShootingFromLeft(){

        Instantiate(bulletPrefab, firePointLeft.position, firePointLeft.rotation);
        timeBtwShots = timeBetweenAttacks;
    }
}

			      
DATE: 27-03-2022

	- Created an C# Script called "EnemyBulletScript"
	
	- this is the script for the Ranged Enemies Bullet
	
	
- EnemyBulletScript 

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EnemyBulletScript : MonoBehaviour
{
    public float speed;
    public float damage;

    private PlayerHealth playerScript;
    private Vector2 targetPosition;

    private void Start(){

        playerScript = GameObject.FindGameObjectWithTag("Player").GetComponent<PlayerHealth>();
        targetPosition = playerScript.transform.position;
    }

    private void Update(){
        
        if(Vector2.Distance(transform.position, targetPosition) > 0.1f){

            transform.position = Vector2.MoveTowards(transform.position, targetPosition, speed * Time.deltaTime);
        } 
        
        else{

            Destroy(gameObject);
        }
    }

    private void OnTriggerEnter2D(Collider2D collision){
        
        if(collision.tag == "Player"){

            playerScript.TakeDamage(damage);
            Destroy(gameObject);
        }
    }
}

	
DATE: 28-03-2022

- Creating an Health Pick Up for the player
	
	- importing the Health Pick Up asset
	
	- adding Box Collider2D and making it isTrigger
	
	- Creating and Adding an C# Script called "HealthPickup"
	
	- also adding an pick up partical effect to game object

	
- HealthPickup C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class HealthPickup : MonoBehaviour
{
    public float healAmount;
    public GameObject pickUpEffect;
    private PlayerHealth playerHealth;

    private void Awake(){

        playerHealth = GameObject.FindGameObjectWithTag("Player").GetComponent<PlayerHealth>();
    }

    private void OnTriggerEnter2D(Collider2D collision){
        
        if(collision.tag == "Player"){

            Instantiate(pickUpEffect, transform.position, Quaternion.identity);

            playerHealth.Heal(healAmount);
            Destroy(gameObject);
        }
        
    }
}

	
DATE: 29-03-2022

- Adding Waves to the Game

	- Created an empty game object called Wave_Spawner
	
	- and Creating and adding an C# script called "WaveSpawner" to that empty game object
	
- WaveSpawner C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WaveSpawner : MonoBehaviour{

    [System.Serializable]
    public class Wave{

        public Enemy[] enemies;
        public int enemyCount;
        public float timeBetweenSpawns;
    }

    public Wave[] waves;
    public Transform[] spawnPoints;
    public float timeBetweenWaves;
    public GameObject boss;
    public Transform bossSpawnPoint;
    public GameObject bossHealthBar;

    private Wave currentWave;
    private int currentWaveIndex;
    private Transform player;
    private bool finishedSpawning;

    private void Start(){

        player = GameObject.FindGameObjectWithTag("Player").transform;
        StartCoroutine(StartNextWave(currentWaveIndex));
    }

    IEnumerator StartNextWave(int index){

        yield return new WaitForSeconds(timeBetweenWaves);
        StartCoroutine(SpawnWave(index));
    }

    IEnumerator SpawnWave(int index){

        currentWave = waves[index];
        yield return null;
        
        for(int i = 0; i < currentWave.enemyCount; i++){

            if (player == null){
                yield break;
            }

            Enemy randomEnemy = currentWave.enemies[Random.Range(0, currentWave.enemies.Length)];
            
            Transform randomSpot = spawnPoints[Random.Range(0, spawnPoints.Length)];
            
            Instantiate(randomEnemy, randomSpot.position, randomSpot.rotation);

            if(i == currentWave.enemyCount - 1){
                finishedSpawning = true;
            }

            else{
                finishedSpawning = false;
            }

            yield return new WaitForSeconds(currentWave.timeBetweenSpawns);
        }
    }

    private void Update(){

        if (finishedSpawning == true && GameObject.FindGameObjectsWithTag("Enemy").Length == 0){

            finishedSpawning = false;

            if(currentWaveIndex + 1 < waves.Length){

                currentWaveIndex++;
                StartCoroutine(StartNextWave(currentWaveIndex));
            } 
            
            else{

                Instantiate(boss, bossSpawnPoint.position, bossSpawnPoint.rotation);
                bossHealthBar.SetActive(true);
            }
        }
    }
}

	
DATE: 30-03-2022

- Adding an Boss in the game
	
	- Imported Boss game Assest named it Boss_Blue
	
	- added an BlueBoss tag to it
	
	- added Box Collider2D and make it isTrigger
	
	- added Rigidbody2D to it
	
	- added an Boss C# Script to it
	
- Boss C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;

public class Boss : MonoBehaviour
{
    public int health;
    public Enemy[] enemies;
    public float spawnOffset;
    public int damage;
    public GameObject bossDeathEffect;

    private int halfHealth;
    private Animator anim;
    private Transform player;
    private Rigidbody2D rb;
    private Slider healthBarSlider;

    private void Start(){

        rb = GetComponent<Rigidbody2D>();
        player = GameObject.FindGameObjectWithTag("Player").transform;
        halfHealth = health / 2;
        anim = GetComponent<Animator>();

        healthBarSlider = GameObject.FindGameObjectWithTag("Slider").GetComponent<Slider>();
        healthBarSlider.maxValue = health;
        healthBarSlider.value = health;
    }

    public void TakeDamage(int damage){

        health -= damage;
        healthBarSlider.value = health;

        if (health <= 0) {

            Instantiate(bossDeathEffect, transform.position, transform.rotation);
            Destroy(this.gameObject);
            healthBarSlider.gameObject.SetActive(false);
        }

        if(health <= halfHealth){

            anim.SetTrigger("Stage2");
        }

        Enemy randomEnemy = enemies[Random.Range(0, enemies.Length)];
        Instantiate(randomEnemy, transform.position + new Vector3(spawnOffset, spawnOffset, 0), transform.rotation);
    }

    private void OnTriggerEnter2D(Collider2D collision){
        
        if(collision.tag == "Player"){

            collision.GetComponent<PlayerHealth>().TakeDamage(damage);
        }
    }

    private void Update(){

        Vector3 direction = player.position - transform.position;
        float angle = Mathf.Atan2(direction.y, direction.x) * Mathf.Rad2Deg - 90f;
        rb.rotation = angle;
    }
}

	
DATE: 31-03-2022

- made the boss patrol around the level and when his health reaches 50% then he starts chasing the player

- added empty game object as a Patrol_Points of the boss

- added animations for the boss

- and managed all the patrol and chase behavior of the boss from animation state machines by creating 2 C# Script

1. Chase_Behaviour
2. Patrol_Behaviour

- Chase_Behaviour C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ChaseBehaviour : StateMachineBehaviour
{
  private GameObject player;
  public float speed;

  override public void OnStateEnter(Animator animator, AnimatorStateInfo stateInfo, int layerIndex){

    player = GameObject.FindGameObjectWithTag("Player");
  }

  override public void OnStateUpdate(Animator animator, AnimatorStateInfo stateInfo, int layerIndex){

    if (player != null){

      animator.transform.position = Vector2.MoveTowards(animator.transform.position, player.transform.position, speed * Time.deltaTime);
    }
  }
}

	
DATE: 02-04-2022

- Patrol_Behaviour C# Script

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PatrolBehaviour : StateMachineBehaviour
{
    public float speed;

    private GameObject[] patrolPoints;
    private int randomPoint;

    override public void OnStateEnter(Animator animator, AnimatorStateInfo stateInfo, int layerIndex){

        patrolPoints = GameObject.FindGameObjectsWithTag("PatrolPoints");
        randomPoint = Random.Range(0, patrolPoints.Length);
    }

    override public void OnStateUpdate(Animator animator, AnimatorStateInfo stateInfo, int layerIndex){

        animator.transform.position = Vector2.MoveTowards(animator.transform.position, patrolPoints[randomPoint].transform.position, speed * Time.deltaTime);

        if(Vector2.Distance(animator.transform.position, patrolPoints[randomPoint].transform.position) < 0.1f){

            randomPoint = Random.Range(0, patrolPoints.Length);
        }
    }
}


DATE: 03-04-2022

- added custom mouse cursor in the game

	- imported custom mouse cursor asset in the game
	
	- Created an C# Script called CursorFollow
	
- CursorFollow C# Script

using UnityEngine;

public class CursorFollow : MonoBehaviour
{
    private void Start(){
        Cursor.visible = false;
    }

    private void Update(){
        transform.position = Input.mousePosition;
    }
}

	- added some more partical effects and sound effect in the game

													       
DATE: 05-04-2022

	- Added main menu in the game
	
	- and created and added an C# script called "LoadNextScene" to an empty game object called Load_Next_Scene
	
- LoadNextScene C# Script

using UnityEngine;
using UnityEngine.SceneManagement;

public class LoadNextScene : MonoBehaviour
{
    public void PlayButton(){
        SceneManager.LoadScene("SampleScene");
    }

    public void ExitButton(){
        Application.Quit();
    }
}

													       
DATE: 06-04-2022

- Added YouWin and YouLose Game Screen

	- added an C# Script called "WinLose" to both of the scenes win and lose
	
- WinLose C# Script

using UnityEngine;
using UnityEngine.SceneManagement;

public class WinLose : MonoBehaviour
{
    public void PlayAgain()
    {
        SceneManager.LoadScene("SampleScene");
    }

    public void Exit()
    {
        Application.Quit();
    }
}

	- also there was a bug where our mouse cursor does not show when win or lose screen displays
	
	- to fix that we created an C# Script called "WinLoseCursor"
	
- WinLoseCursor C# Script

using UnityEngine;

public class WinLoseCursor : MonoBehaviour
{
    private void Start()
    {
        Cursor.visible = true;
    }
}

													       
DATE: 07-04-2022

- Adding Level Music in the game

- Created an Empty game object called "Game_Music"

- and added the level music to it

- also added an C# Script called "RandomGameMusic" to that Game_Music game object

- RandomGameMusic C# Script

using UnityEngine;

public class RandomGameMusic : MonoBehaviour
{
  private void Start()
  {
    DontDestroyOnLoad(gameObject);
  }
}

- we created that C# script so that our game music does not stop when the game scenes change from the main menu to
 the game level
  
- With that our Game "NO ENEMY LEFT" is completed.

													       
DATE: 08-04-2022

- Going in-depth in Unity C# Programming

- Learning about Delegates

- Created an C# Script called "Delegates_Unity" to learn the basics of Delegates

- Delegates_Unity C# Script

using UnityEngine;

public class Delegates_Unity : MonoBehaviour
{
  // declaring delegate Template.
  private delegate void MyDelegate(int n);
  // declaring member variable.
  MyDelegate myDelegate;

  // all the functions must have the same signature as a delegate to be used in the delegate.

  private void Start()
  {
    // assigning the PrintNum Function in myDelegate.
    myDelegate = PrintNum;
    // using myDelegate as a Function.
    myDelegate(50);

    // assigning the DoubleNum Function in myDelegate.
    myDelegate = DoubleNum;
    // using myDelegate as a Function.
    myDelegate(50);
  }

  private void PrintNum(int num)
  {
    Debug.Log("Print Num: " + num);
  }

  private void DoubleNum(int num)
  {
    Debug.Log("Double Num: " + num * 2);
  }

}

- going a little more in-depth in Delegates by seeing different ways of creating Delegates

- Delegates_Code_Monkey C# Script

using UnityEngine;

public class Delegates_Code_Monkey : MonoBehaviour
{
  public delegate bool BoolDelegate(int i);
  BoolDelegate boolDelegate;

  private void Start()
  {
    boolDelegate = BoolFunction;
    Debug.Log(boolDelegate(1));

    // another way of defining the delegate
    // explicitly creating a delegate

    boolDelegate = new BoolDelegate(BoolFunction);
    Debug.Log(boolDelegate(2));
  }

  public bool BoolFunction(int n)
  {
    return n < 5;
  }
}

	
DATE: 10-04-2022

- Multicasting in Delegates

- Multicast_Delegates C# Script


using UnityEngine;

public class Multicast_Delegates : MonoBehaviour
{
  private delegate void MultiDelegate();
  MultiDelegate myMultiDelegate;

  private void Start()
  {
    myMultiDelegate = Sphere;
    // here we are multicasting the delegate using +=
    myMultiDelegate += Sphere_Turning_Red;
    myMultiDelegate();

    // removing an function from delegate using -=
    myMultiDelegate -= Sphere_Turning_Red;
    myMultiDelegate -= Sphere;

    // we should never call a delegate before assigning any function to it
    // otherwise it will gonna have a null value by default which will give us a null value exception.

    // so as a safety mechanism we can check before calling a delegate if it is null or not

    if(myMultiDelegate != null)
    {
      myMultiDelegate();
    }
  }

  private void Sphere()
  {
    print("this is a Sphere");
  }
   
  private void Sphere_Turning_Red()
  {
    GetComponent<Renderer>().material.color = Color.red;
    print("now Sphere is Red");
  }
}

	
DATE: 11-04-2022

	- Lamda Expression and Anonymous Functions in Delegates
	
- Delegates_lambda_and_anonymous C# Script


using UnityEngine;

public class Delegates_lambda_and_anonymous : MonoBehaviour
{
    public delegate void TestDelegate();
    private TestDelegate testDelegate;

    public delegate bool BoolDelegate(int i);
    private BoolDelegate boolDelegate;

    private void Start()
    {
        // creating delegate using Anonymous function.

        testDelegate = delegate () { Debug.Log("Anonymous method"); };
        testDelegate();

        // another way of creating delegate using Anonymous in lamda function.

        testDelegate = () => { Debug.Log("Lamda expression"); };
        testDelegate();

        boolDelegate = (int n) => { return n < 5; };

        // more compact way of writing the single statement lamda expression.

        boolDelegate = (int n) => n < 5;

        Debug.Log(boolDelegate(2));

        // Note -> we can not remove a function from delegate that is created using lamda expression.
        // because we do not have a unique refrance for that function.

        testDelegate = () => { Debug.Log("Lamda expression"); };
        testDelegate += () => { Debug.Log("Second Lamda Expression"); };
        testDelegate();
    }
}

	
DATE: 12-04-2022

- Unity Built-in Delegates Functions

- Built_In_Delegates C# Script


using UnityEngine;
using System;

public class Built_In_Delegates : MonoBehaviour
{
  // there are some built-in delegates in the System namespace in unity.

  // this is a delegate that returns void and takes no parameters.
  private Action action;

  // this is a delegate that takes generic parameters of any kind.
  private Action<int, float> genericAction;

  // this is a delegate that will take generic parameters and return a data type.
  private Func<int, bool> funcDelegate;

  private void Start()
  {
    genericAction = (int i, float f) => { Debug.Log("Generic Delegate Action called by a Lamda Expression"); };
    genericAction(5, 0.2f);

    genericAction = GenericDelegate;
    genericAction(3, 2.4f);

    funcDelegate = (int i) => { return i < 5; };
    Debug.Log("Using Lamda Expression = " + FuncDelegate(3));

    funcDelegate = FuncDelegate;
    Debug.Log(FuncDelegate(2));

  }

  private void GenericDelegate(int i, float f)
  {
    Debug.Log("Generic Delegate Action called by a non-Lamda Expression");
  }

  private bool FuncDelegate(int i)
  {
    return (i < 5);
  }
}
	
	
	
DATE: 13-04-2022

	- Writing Non-Modular Code than converting it to a Modular Code
	
	- First Non-Modular Code Example
	
- Non_Modular_Timer C# Script

using UnityEngine;

public class Non_Modular_Timer : MonoBehaviour
{
    private float timer;
    
    public void SetTimer(float timer)
    {
        this.timer = timer;
    }

    private void Update()
    {
        timer -= Time.deltaTime;
    }

    public bool IsTimerComplete()
    {
        return timer <= 0f;
    }
}


- Non_Modular_Delegate C# Script

using UnityEngine;

public class Non_Modular_Delegate : MonoBehaviour
{
    [SerializeField] private Non_Modular_Timer timer;

    private bool hasTimerElapsed = false;

    private void Start()
    {
        timer.SetTimer(1f);
    }

    private void Update()
    {
        if (!hasTimerElapsed && timer.IsTimerComplete())
        {
            Debug.Log("Timer Complete");
            hasTimerElapsed = true;
        }
    }
}

			  
DATE: 14-04-2022

	- Modular Code Example
	
- Modular_Timer C# Script

using UnityEngine;
using System;

public class Modular_Timer : MonoBehaviour
{
    private Action message;
    private float timer;

    public void SetTimer(float timer, Action message)
    {
        this.timer = timer;
        this.message = message;
    }

    private void Update()
    {
        if(timer > 0f)
        {
            timer -= Time.deltaTime;

            if (IsTimerComplete())
            {
                message();
            }
        }
    }

    public bool IsTimerComplete()
    {
        return timer <= 0f;
    }
}


- Modular_Delegate C# Script

using UnityEngine;

public class Modular_Delegate : MonoBehaviour
{
    [SerializeField] private Modular_Timer modular_Timer;

    private void Start()
    {
        modular_Timer.SetTimer(1f, () => Debug.Log("Timer Completed"));

        modular_Timer.SetTimer(1f, MessageDelegate);
    }

    public void MessageDelegate()
    {
        Debug.Log("Timer is Complete");
    }
}

	
DATE: 15-04-2022

- Going in-depth in Unity C# Programming

	- Learning about Events
	
	- Creating Events in Unity C#
	
- Events_Scripts

using UnityEngine;
using System;

public class Events_Scripts : MonoBehaviour
{
    // template of an Event, in witch EventHandler is a Delegate.
    public event EventHandler OnSpacePressed;

    private void Start()
    {
        // Subscribing to the Event

        OnSpacePressed += Function_OnSpacePressed;
        //OnSpacePressed(this, EventArgs.Empty);
    }

    // In Order to Subscribe to the event first we need to Define a Function that will receive that Event.

    // Function Signature needs to be same as the Event.
    private void Function_OnSpacePressed(object sender, EventArgs e)
    {
        Debug.Log("Space is Pressed");
    }

    private void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            if (OnSpacePressed != null)
            {
                //Event being fired
                //Calling the event Delegate to start the Event

                OnSpacePressed(this, EventArgs.Empty);
            }

            // C# 6.0 Shorthand Version of Checking if not null

            //    Event being fired
            //    Calling the event Delegate to start the Event

            //OnSpacePressed?.Invoke(this, EventArgs.Empty);
        }
    }
}

	
DATE: 16-04-2022

	- Events Subscriber and publisher in diffrent Scripts
	
- Event_Publisher C# Script

using UnityEngine;
using System;

public class Event_Publisher : MonoBehaviour
{
    public event EventHandler OnSpacePressed;
    public event EventHandler OnShiftPressed;

    private void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            if(OnSpacePressed != null)
            {
                OnSpacePressed(this, EventArgs.Empty);
            }
        }

        if (Input.GetKeyDown(KeyCode.LeftShift))
        {
            if(OnShiftPressed != null)
            {
                OnShiftPressed(this, EventArgs.Empty);
            }
        }
    }
}


- Event_Subscriber

using UnityEngine;
using System;

public class Event_Subscriber : MonoBehaviour
{
    private void Start()
    {
        Event_Publisher event_Publisher = GetComponent<Event_Publisher>();

        event_Publisher.OnSpacePressed += Event_Space_Button_Subscriber_Message;
        event_Publisher.OnSpacePressed += Event_Left_Shift_Button_Subscriber_Message;

        event_Publisher.OnShiftPressed += Event_Left_Shift_Button_Subscriber_Message;
    }

    private void Event_Space_Button_Subscriber_Message(object sender, EventArgs eventArgs)
    {
        Debug.Log("Space Button is Pressed");

        // removing an Event Function from a Publisher.
        Event_Publisher event_Publisher = GetComponent<Event_Publisher>();
        event_Publisher.OnSpacePressed -= Event_Left_Shift_Button_Subscriber_Message;
    }

    private void Event_Left_Shift_Button_Subscriber_Message(object sender, EventArgs eventArgs)
    {
        Debug.Log("Left Shift Button is Pressed");
    }
}

	
DATE: 17-04-2022

	- Creating custom Delegate for Events
	
- Event_Custom_Delegate

using UnityEngine;

public class Event_Custom_Delegate : MonoBehaviour
{
    public delegate void EventDelegate(float f);

    public event EventDelegate OnFloatEvent;

    private void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            if(OnFloatEvent != null)
            {
                OnFloatEvent(5.5f);
            }
        }
    }
}


- Event_Custom_Delegate_Subscirber

using UnityEngine;

public class Event_Custom_Delegate_Subscirber : MonoBehaviour
{
    private void Start()
    {
        Event_Custom_Delegate event_Custom_Delegate = GetComponent<Event_Custom_Delegate>();
        event_Custom_Delegate.OnFloatEvent += Event_Custom_Delegate_OnFloatEvent;
    }

    private void Event_Custom_Delegate_OnFloatEvent(float f)
    {
        Debug.Log("float " + f);
    }
}

	
DATE: 18-04-2022

- Passing more informatin in Events using EventArgs

- EventArgs_Publisher

using UnityEngine;
using System;

public class EventArgs_Publisher : MonoBehaviour
{
  // EventHandler has two fields(parameters) one is an object and another is EventArgs
  // EventArgs is a Standard way to pass more information through the event
  // here is an example of that

  // first we create an class that will derive from EventArgs class
  public class OnSpacePressedEventArgs : EventArgs
  {
    // and here we define what fields(parameters) we want
    // so whatever we add there needs to be given as a parameter whenever we call this Event

    public int spaceCount_In_EventArgs_Class;
  }

  // here we need to pass that event class that we created as Generic.

  public event EventHandler<OnSpacePressedEventArgs> OnSpacePressed;

  private int spaceCount;

  // now our Event will contain an object of OnSpacePressedEventArgs type on the second Parameter.

  private void Update()
  {
    if (Input.GetKeyDown(KeyCode.Space))
    {
      spaceCount++;
       
      if(OnSpacePressed != null)
      {
        OnSpacePressed(this, new OnSpacePressedEventArgs { spaceCount_In_EventArgs_Class = spaceCount });
      }
    }
  }
}

- EventArga_Subscriber

using UnityEngine;
using System;

public class EventArga_Subscriber : MonoBehaviour
{
  private void Start()
  {
    EventArgs_Publisher eventArgs_Publisher = GetComponent<EventArgs_Publisher>();
    eventArgs_Publisher.OnSpacePressed += EventArgs_Subscriber_OnSpacePressed;
  }

  private void EventArgs_Subscriber_OnSpacePressed(object sender, EventArgs_Publisher.OnSpacePressedEventArgs e)
  {
    Debug.Log("Space is Pressed " + e.spaceCount_In_EventArgs_Class + " times");
  }
}

	
DATE: 19-04-2022

	- using Unity Built-in Delegate Action in Events
	
- Event_Action_Delegate

using UnityEngine;
using System;

public class Event_Action_Delegate : MonoBehaviour
{
    public event Action<bool, int> OnActionEvent;

    private void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            if(OnActionEvent != null)
            {
                OnActionEvent(true, 50);
            }
        }
    }
}

- Event_Action_Delegate_Subscriber

using UnityEngine;

public class Event_Action_Delegate_Subscriber : MonoBehaviour
{
    private void Start()
    {
        Event_Action_Delegate event_Action_Delegate = GetComponent<Event_Action_Delegate>();
        event_Action_Delegate.OnActionEvent += Event_Action_Delegate_OnActionEvent;
    }

    private void Event_Action_Delegate_OnActionEvent(bool arg1, int arg2)
    {
        Debug.Log(arg1 + " " + arg2);
    }
}

	
DATE: 20-04-2022

	- Built-in Unity Events
	
- UnityEvents

using UnityEngine;
using System;
using UnityEngine.Events;

public class UnityEvents : MonoBehaviour
{
    public UnityEvent OnUnityEvent;

    private void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            OnUnityEvent?.Invoke();
        }
    }
}

- UnityEventsSubscriber

using UnityEngine;

public class UnityEventsSubscriber : MonoBehaviour
{
    public void UnityEvent()
    {
        Debug.Log("Unity Event Function");
    }
}

	
DATE: 21-04-2022

- Creating first multiplayer game using Photon engine

	- Setting the photon for the unity project
	
- Connecting player to the server

	- Creating a loading scene
	
	- Created an empty game object called ConnectToServer
	
	- Created an Folder called Scripts
	
	- and Created and added an C# Script called ConnectToServer and attached it to the empty game object
	
	- in this script we are first connecting the game project to the server
	
	- than after it's connected than we are going into main scene
	
	- creating an main scene
	
- ConnectToServer C# Script

using UnityEngine;
using Photon.Pun;
using UnityEngine.SceneManagement;

public class ConnectToServer : MonoBehaviourPunCallbacks
{
    private void Start()
    {
        PhotonNetwork.ConnectUsingSettings();
    }

    public override void OnConnectedToMaster()
    {
        SceneManager.LoadScene("MainMenu");
    }
}

	
DATE: 22-04-2022

- Creating Joining and Creating Rooms Functionality

- Added a Join and Create Input Fields and Buttons where players can enter the room name and join it.

- Created an C# Script called MainMenu and attached it to an empty game object called MainMenu

- in this script, we are Creating Functions for joining and Creating rooms

- and we also limited the room to only 2 players at the same time because this is a two-player game

- also creating a Game scene whenever a player creates or join a room then the player will move to the game scene

- MainMenu C# Script

using UnityEngine;
using Photon.Pun;
using Photon.Realtime;
using TMPro;

public class MainMenu : MonoBehaviourPunCallbacks
{
  public TMP_InputField createInput;
  public TMP_InputField joinInput;

  public void CreateRoom()
  {
    RoomOptions roomOptions = new RoomOptions();
    roomOptions.MaxPlayers = 2;

    PhotonNetwork.CreateRoom(createInput.text, roomOptions);
  }

  public void JoinRoom()
  {
    PhotonNetwork.JoinRoom(joinInput.text);
  }

  public override void OnJoinedRoom()
  {
    PhotonNetwork.LoadLevel("Game");
  }
}

	
DATE: 23-04-2022

- Spawning the player on both devices

- Created a Player character and added Photon View Component to it

- because the player needs to be on the network to show on both player's screen

- Created a folder called Resources

- added the player in this folder to make it a prefab

- In-game scene created an empty game object called "SpawnPlayers"

- and added an C# Script called "SpawnPlayers" to that object

- SpawnPlayers C# Script

using UnityEngine;
using Photon.Pun;

public class SpawnPlayers : MonoBehaviour
{
  public GameObject player;
  public float minX, minY, maxX, maxY;

  private void Start()
  {
    Vector2 randomPosition = new Vector2(Random.Range(minX, maxX), Random.Range(minY, maxY));

    PhotonNetwork.Instantiate(player.name, randomPosition, Quaternion.identity);
  }
}

	
DATE: 24-04-2022

- Creating Player Controller for the players

- Created an C# Script called "PlayerController"

- and added it to the player prefab game object


- PlayerController C# Script

using UnityEngine;
using Photon.Pun;
using System.Collections;

public class PlayerController : MonoBehaviour
{
  public float speed;

  private PhotonView photonView;

  private void Start()
  {
    photonView = GetComponent<PhotonView>();
  }

  private void Update()
  {
    if (photonView.IsMine)
    {
      Vector2 moveInput = new Vector2(Input.GetAxisRaw("Horizontal"), Input.GetAxisRaw("Vertical"));
      Vector2 moveAmount = moveInput.normalized * speed * Time.deltaTime;

      transform.position += (Vector3)moveAmount;
}
  }


- now that player movement done

- now we need to sync the player movement on both player's screen

- for that, we are adding a Photon Component called "Photon Transform view classic" to the player prefab

- and checking the Synchronize Position box in that component
	

	
DATE: 25-04-2022

- Spawning Enemies

- Created a Cube as the enemy and gave it a blue color

- and added photon view component to it

- and made emeny a prefab by dragging and dropping him in the Resources folder

- Created and added an C# Script called "Enemy" to the enemy prefab game object

- Enemy C# Script

using UnityEngine;
using Photon.Pun;

public class Enemy : MonoBehaviour
{
  public float speed;

  private PlayerController[] players;
  private PlayerController nearestPlayer;

  private void Start()
  {
    players = FindObjectsOfType<PlayerController>();
  }

  private void Update()
  {
    float distanceOne = Vector2.Distance(transform.position, players[0].transform.position);
    float distanceTwo = Vector2.Distance(transform.position, players[1].transform.position);

    if(distanceOne < distanceTwo)
    {
      nearestPlayer = players[0];
    }
    else
    {
      nearestPlayer = players[1];
    }

    if(nearestPlayer != null)
    {
      transform.position = Vector2.MoveTowards(transform.position, nearestPlayer.transform.position, speed * Time.deltaTime);
    }
  }

				 
DATE: 26-04-2022

- Creating enemies Spawn points
		
		- Created some empty game objects and set them where we want the ememies to spawn from
		
		- than Created an parrent game object for these Spawn points called "EnemySpawnPoints"
		
		- and made all the spawn points children of this parent object
		
		- also created an empty game object called "Spawner"
		
		- and attached an C# Script called "Spawner" to that empty game object
		

- Spawner C# Script

using UnityEngine;
using Photon.Pun;

public class Spawner : MonoBehaviour
{
    public Transform[] spawnPoints;
    public GameObject enemy;
    public float startTimeBetweenSpawns;

    private float timeBetweenSpawns;

    private void Start()
    {
        timeBetweenSpawns = startTimeBetweenSpawns;
    }

    private void Update()
    {
        if(PhotonNetwork.IsMasterClient == false || PhotonNetwork.CurrentRoom.PlayerCount != 2)
        {
            return;
        }

        if(timeBetweenSpawns <= 0)
        {
            // Spawn Enemies

            Vector3 spawnPosition = spawnPoints[Random.Range(0, spawnPoints.Length)].position;

            PhotonNetwork.Instantiate(enemy.name, spawnPosition, Quaternion.identity);
            timeBetweenSpawns = startTimeBetweenSpawns;
        }
        else
        {
            timeBetweenSpawns -= Time.deltaTime;
        }
    }
}

	
DATE: 27-04-2022

- Creating Health Points for the player

- Creating a UI for the health points name "Health" and giving it a default value of 10 points

- Creating and C# Script called Health and adding it to the Health game object

- Adding box Collider 2d to the enemy and the player and setting them as isTrigger

- also add rigidbody2D to the enemy and set it to Kinematic

- and adding an Enemy tag to the enemy prefab

- added a photon view component to the health game object


- Health C# Script

using UnityEngine;
using UnityEngine.UI;
using Photon.Pun;
using TMPro;

public class Health : MonoBehaviour
{
  public int health;
  public TextMeshProUGUI healthDisplay;

  private PhotonView photonView;

  private void Start()
  {
    photonView = GetComponent<PhotonView>();
  }

  public void TakeDamage()
  {
    photonView.RPC("TakeDamageRPC", RpcTarget.All);
  }

  [PunRPC]
  private void TakeDamageRPC()
  {
    health--;

    if(health <= 0)
    {
      health = 0;
    }

    healthDisplay.text = health.ToString();
  }
}

- we also done some changes in the PlayerController Script

- PlayerController Script

using UnityEngine;
using Photon.Pun;
using System.Collections;

public class PlayerController : MonoBehaviour
{
  public float speed;

  private PhotonView photonView;
  private Health healthScript;

  private void Start()
  {
    photonView = GetComponent<PhotonView>();
    healthScript = FindObjectOfType<Health>();
  }

  private void Update()
  {
    if (photonView.IsMine)
    {
      Vector2 moveInput = new Vector2(Input.GetAxisRaw("Horizontal"), Input.GetAxisRaw("Vertical"));
      Vector2 moveAmount = moveInput.normalized * speed * Time.deltaTime;

      transform.position += (Vector3)moveAmount;
    }
  }

  private void OnTriggerEnter2D(Collider2D collision)
  {
    if (photonView.IsMine)
    {
      if (collision.tag == "Enemy")
      {
        healthScript.TakeDamage();
      }
    }
  }
}

	
DATE: 28-04-2022		

- Creating a line using unity Line Renderer that will work as our game main mechanics to kill enemies

	- Setting up the Line Renderer properties according to our game
	
	- Adding Line Renderer Functionalities in the PlayerController Script
	
- PlayerController Script

using UnityEngine;
using Photon.Pun;
using System.Collections;

public class PlayerController : MonoBehaviour
{
    public float speed;

    private PhotonView photonView;
    private Health healthScript;
	private LineRenderer lineRenderer;

    private void Start()
    {
        photonView = GetComponent<PhotonView>();
        healthScript = FindObjectOfType<Health>();
		lineRenderer = FindObjectOfType<LineRenderer>();
    }

    private void Update()
    {
        if (photonView.IsMine)
        {
            Vector2 moveInput = new Vector2(Input.GetAxisRaw("Horizontal"), Input.GetAxisRaw("Vertical"));
            Vector2 moveAmount = moveInput.normalized * speed * Time.deltaTime;

            transform.position += (Vector3)moveAmount;
			
			lineRenderer.SetPosition(0, transform.position);
        }
		else
        {
            lineRenderer.SetPosition(1, transform.position);
        }
    }

    private void OnTriggerEnter2D(Collider2D collision)
    {
        if (photonView.IsMine)
        {
            if (collision.tag == "Enemy")
            {
                healthScript.TakeDamage();
            }
        }
    }
}
		
	- adding an EdgeCollider2D to our Line Renderer game object
	
	- and checking the isTrigger property to ture
	
	- Creating a new C# Script called "GoldenRay" and attaching it to our Line Renderer game object
	

- GoldenRay Script

using UnityEngine;
using System.Collections.Generic;

public class GoldenRay : MonoBehaviour
{
    public List<Vector2> linePoints = new List<Vector2>();

    private LineRenderer lineRenderer;
    private EdgeCollider2D edgeCollider2d;

    private void Start()
    {
        lineRenderer = GetComponent<LineRenderer>();
        edgeCollider2d = GetComponent<EdgeCollider2D>();
    }

    private void Update()
    {
        linePoints[0] = lineRenderer.GetPosition(0);
        linePoints[1] = lineRenderer.GetPosition(1);

        edgeCollider2d.SetPoints(linePoints.ConvertAll(p => (Vector2)transform.InverseTransformPoint(p)));
    }
}


	- adding an tag called "GoldenRay" to the LineRenderer

	
DATE: 29-04-2022
	
- done some changes in Enemy Script so that our LineRenderer can kill enemies

- Enemy Script

using UnityEngine;
using Photon.Pun;

public class Enemy : MonoBehaviour
{
    public float speed;

    private PlayerController[] players;
    private PlayerController nearestPlayer;

    private void Start()
    {
        players = FindObjectsOfType<PlayerController>();
    }

    private void Update()
    {
        float distanceOne = Vector2.Distance(transform.position, players[0].transform.position);
        float distanceTwo = Vector2.Distance(transform.position, players[1].transform.position);

        if(distanceOne < distanceTwo)
        {
            nearestPlayer = players[0];
        }
        else
        {
            nearestPlayer = players[1];
        }

        if(nearestPlayer != null)
        {
            transform.position = Vector2.MoveTowards(transform.position, nearestPlayer.transform.position, speed * Time.deltaTime);
        }
    }
	
	private void OnTriggerEnter2D(Collider2D collision)
    {
        if (PhotonNetwork.IsMasterClient)
        {
            if (collision.tag == "GoldenRay")
            {
                PhotonNetwork.Destroy(this.gameObject);
            }
        }
    }
}


- Creating a Score System for our game
	
	- Creating Score UI in the Canvas
	
	- and naming it to Score
	
	- and setting it to the top left of the screen
	
	- Creating an empty game object called "Score"
	
	- and Creating and attaching an C# Script called "Score" to that empty game object

	- also adding an Photon view component to it because we need to call an RPC function from this script
	  (we call an RPC Function to sync it between all the players or to the network)
	  

- Score Script

using UnityEngine;
using Photon.Pun;
using TMPro;

public class Score : MonoBehaviour
{
    public TextMeshProUGUI scoreDisplay;

    public int score = 0;
    private PhotonView photonView;

    private void Start()
    {
        photonView = GetComponent<PhotonView>();
    }

    public void AddScore()
    {
        photonView.RPC("AddScoreRPC", RpcTarget.All);
    }

    [PunRPC]
    private void AddScoreRPC()
    {
        score++;
        scoreDisplay.text = score.ToString();
    }
}

	
DATE: 30-04-2022

	- done some changes to the enemy script so that when ever an enemy dies a score get incremented

- Enemy Script

using UnityEngine;
using Photon.Pun;

public class Enemy : MonoBehaviour
{
    public float speed;

    private PlayerController[] players;
    private PlayerController nearestPlayer;
	private Score score;

    private void Start()
    {
        players = FindObjectsOfType<PlayerController>();
		score = FindObjectOfType<Score>();
    }

    private void Update()
    {
        float distanceOne = Vector2.Distance(transform.position, players[0].transform.position);
        float distanceTwo = Vector2.Distance(transform.position, players[1].transform.position);

        if(distanceOne < distanceTwo)
        {
            nearestPlayer = players[0];
        }
        else
        {
            nearestPlayer = players[1];
        }

        if(nearestPlayer != null)
        {
            transform.position = Vector2.MoveTowards(transform.position, nearestPlayer.transform.position, speed * Time.deltaTime);
        }
    }
	
	private void OnTriggerEnter2D(Collider2D collision)
    {
        if (PhotonNetwork.IsMasterClient)
        {
            if (collision.tag == "GoldenRay")
            {
				score.AddScore();
                PhotonNetwork.Destroy(this.gameObject);
            }
        }
    }
}

	- drag and drop Score Text into the Score Script


	- Adding Dash Functionality in the game


- PlayerController Script

using UnityEngine;
using Photon.Pun;
using System.Collections;

public class PlayerController : MonoBehaviour
{
    public float speed;
	public float dashSpeed;
    public float dashTime;

    private PhotonView photonView;
    private Health healthScript;
	private LineRenderer lineRenderer;
	private float resetSpeed;

    private void Start()
    {
        photonView = GetComponent<PhotonView>();
        healthScript = FindObjectOfType<Health>();
		lineRenderer = FindObjectOfType<LineRenderer>();
		
		resetSpeed = speed;
    }

    private void Update()
    {
        if (photonView.IsMine)
        {
            Vector2 moveInput = new Vector2(Input.GetAxisRaw("Horizontal"), Input.GetAxisRaw("Vertical"));
            Vector2 moveAmount = moveInput.normalized * speed * Time.deltaTime;

            transform.position += (Vector3)moveAmount;
			
			lineRenderer.SetPosition(0, transform.position);
			
			if (Input.GetKeyDown(KeyCode.Space) && moveInput != Vector2.zero)
            {
                StartCoroutine("Dash");
            }
        }
		else
        {
            lineRenderer.SetPosition(1, transform.position);
        }
    }
	
	IEnumerator Dash()
    {
        speed = dashSpeed;
        yield return new WaitForSeconds(dashTime);
        speed = resetSpeed;
    }

    private void OnTriggerEnter2D(Collider2D collision)
    {
        if (photonView.IsMine)
        {
            if (collision.tag == "Enemy")
            {
                healthScript.TakeDamage();
            }
        }
    }
}
