# Exp.No:7 Redirecting the scene
## Aim:
To Redirecting the scene in the unity engine.


## Algorithm:
### Step 1:

Open the unity engine.

### Step 2:

Create a new plane and create a cube and give color for the cube.

### Step 3:

Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:

Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:

Create the C# script file in the Assets and write the Coding for the Redirecting.

### Step 6:

Next Create a another new scene named as page2.

### Step 7:

In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

### Step 8:

Click the Build and run button in the Build settings and run the scene.

### Step 9:

The Sphere after touching the cube it will disappeared and Press the key [space] for redircting to the new scene that is page2.



## Program:
Developed By: **Nithishkumar P**
</br>
Register No.: **212221230070**
```python
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class PlayerController : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            SceneManager.LoadScene("level2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "cube")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Output:
![beforeplay exp 7](https://github.com/NITHISHKUMAR-P/Redirecting-the-scene/assets/93427017/48074c64-b571-4741-8cce-e218916a0cd0)
### After the Ball hit the cube:
![game](https://github.com/NITHISHKUMAR-P/Redirecting-the-scene/assets/93427017/d585f457-82bf-4c70-86d7-cef353b1fdf1)
### Redirected scene:
![image](https://github.com/NITHISHKUMAR-P/Redirecting-the-scene/assets/93427017/59e77659-76a3-4fe4-b288-4f6086114235)


## Result:
Thus the above C# coding is successfully redirecting the scene in the unity engine.
