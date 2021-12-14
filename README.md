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
