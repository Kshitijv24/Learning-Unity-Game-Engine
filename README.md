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
