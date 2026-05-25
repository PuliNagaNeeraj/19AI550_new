# Ex.No: 10  Implementation of 2D/3D game 
### DATE:  25-05-2026                                                                     
### REGISTER NUMBER : 212223240130
### AIM: 
To develop a game “2D Maze Runner Game” in Unity.
### Algorithm:
```
1.Open Unity Hub and create a new 2D project.
2.Design the maze environment using tiles and sprites.
3.Add a player object to the scene.
4.Create movement controls using C# scripting.
5.Add walls and obstacles inside the maze.
6.Implement collision detection to prevent the player from crossing walls.
7.Add a goal point to complete the game.
8.Test and run the game successfully in Unity.
```  
### Program:

### PLAYER MOVEMENT 
```
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed = 3f;
    private Rigidbody2D rb;
    private Vector2 movement;

    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        movement.x = Input.GetAxisRaw("Horizontal");
        movement.y = Input.GetAxisRaw("Vertical");
    }

    void FixedUpdate()
    {
        rb.MovePosition(rb.position + movement * speed * Time.fixedDeltaTime);
    }
}
```
### GOAL
```
using UnityEngine;

public class Goal : MonoBehaviour
{
    private void OnTriggerEnter2D(Collider2D other)
    {
        Debug.Log("Something touched Goal");

        if (other.CompareTag("Player"))
        {
            Debug.Log("Game Completed!");
        }
    }
}
```

### Output:
### BEFORE 
<img width="1918" height="958" alt="image" src="https://github.com/user-attachments/assets/933c217b-c8b8-4ef1-95c0-28d8da8695ca" />


### AFTER 
<img width="1918" height="995" alt="image" src="https://github.com/user-attachments/assets/f776d183-3208-4827-8170-447354b25505" />

### Result:
Thus the game “2D Maze Runner Game” was developed using Unity and adopted Artificial Intelligence technology.
