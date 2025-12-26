using UnityEngine;

public class PlayerMove : MonoBehaviour
{
    public float speed = 5f; // سرعة حركة الشخصية

    void Update()
    {
        // قراءة مفاتيح الحركة
        float x = Input.GetAxis("Horizontal"); // ← → / A D
        float y = Input.GetAxis("Vertical");   // ↑ ↓ / W S

        // تحريك الشخصية
        transform.Translate(new Vector2(x, y) * speed * Time.deltaTime);
    }
}
