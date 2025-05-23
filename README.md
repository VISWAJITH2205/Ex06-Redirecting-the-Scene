# NAME : VISWAJITH LALITHRAM R.V
# REG.NO: 212224240187
---
# Ex06-Redirecting-the-Scene
---
## Aim:

To Redirecting the scene in the unity engine.

---

## Algorithm:

Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

---


## Program:

## PLAYERCONTROLLER

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
---

## Output:

![Alt text](Assets/1.png)

![Alt text](Assets/2.png)

![Alt text](Assets/3.png)

---

## Result:

The above C# coding is successfully redirecting the scene in the unity engine.
