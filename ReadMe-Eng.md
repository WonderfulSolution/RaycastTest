# RaycastTest

using UnityEngine; using System.Collections;

public class RaycastTest : MonoBehaviour {

void Update () {
        Ray ray = Camera.main.ScreenPointToRay(Input.mousePosition);
        RaycastHit hit;
        if (Input.GetMouseButton(0) && Physics.Raycast(ray, out hit))
        {
            Debug.DrawLine(Camera.main.transform.position, hit.transform.position, Color.red, 0.1f, true);
            Debug.Log(hit.transform.name);
           }
        }
}

How to use 3D Ray (novice)

# RaycastTest2D

using UnityEngine; using System.Collections;

public class RaycastTest2 : MonoBehaviour {

void Update () {
    Ray ray = Camera.main.ScreenPointToRay(Input.mousePosition);
    if (Input.GetMouseButton(0))
    {
        RaycastHit2D hit = Physics2D.Raycast(ray.origin, ray.direction, 10);
        if (hit.collider)
        {
            Debug.DrawLine(ray.origin, hit.transform.position, Color.blue, 0.1f, true);
            Debug.Log(hit.transform.name);
        }
    }
}
}

How to use 2D Ray (novice)
