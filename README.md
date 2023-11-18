using UnityEngine;

public class Kogel : MonoBehaviour
{
    public float snelheid = 10f;
    public float levensduur = 2f;

    void Start()
    {
        Destroy(gameObject, levensduur);
    }

    void Update()
    {
        BeweegKogel();
    }

    void BeweegKogel()
    {
        transform.Translate(Vector3.forward * snelheid * Time.deltaTime);
    }
}

