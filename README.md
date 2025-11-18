# project-karim1 sex balls
using UnityEngine;
using UnityEngine.Rendering;

public class cube_movement : MonoBehaviour
{
    public Rigidbody rb;
    // Start is called once before the first execution of Update after the MonoBehaviour is created


    public float forwardforce = 50f;
    public float sidewaysforce = 50f;


    // Update is called once per frame
    void FixedUpdate()
    {
        rb.AddForce(0, 0, forwardforce * Time.deltaTime);
        //add force and reduces frame for poor computers 
        if (Input.GetKey("d"))
        {
            rb.AddForce(sidewaysforce * Time.deltaTime, 0, 0,ForceMode.VelocityChange);
        }
        if (Input.GetKey("a"))
        {
            rb.AddForce(-sidewaysforce * Time.deltaTime, 0, 0,ForceMode.VelocityChange);
        }
    }
}
