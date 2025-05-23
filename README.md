# Ex06-Redirecting-the-Scene

## Aim:
To Redirect the scene in the unity engine.

## Algorithm:
### Step 1 :

To open the unity engine.

### Step 2 :

Create a new 3D project.

### Step 3 :

Create plane and name it as ground and create cube and name it as player.

### Step 4 :

Add WinText in Hierarchy.

### Step 5 :

Create a C# Script and name it as playercontroller and add the script to player.

### Step 6 :

Use the R button to change the level 2

### Step 7 :

Print the Output and end the program.

## Program:

### DEVELOPED BY: MANIKANDAN K
### REGISTER NUMBER : 212224230150

~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coading : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created\
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
       rb = GetComponent<Rigidbody>(); 
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level 2");
        }
    }
    private void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
~~~
## Output:
![image](https://github.com/user-attachments/assets/14edda78-d020-4254-8bbd-c6cf4df7f502)


## Result:
The redirecting of the scene in the unity engine is done successfully.
