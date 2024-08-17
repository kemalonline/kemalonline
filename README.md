using UnityEngine;
using UnityEngine.UI;

public class TouchScore : MonoBehaviour
{
    public Text scoreText; // Puanı gösterecek UI Text bileşeni
    private int score = 0;

    void Start()
    {
        UpdateScoreText();
    }

    void Update()
    {
        // Eğer ekrana dokunulduysa
        if (Input.GetMouseButtonDown(0)) // Mobilde dokunuş, bilgisayarda mouse tıklaması olarak çalışır
        {
            AddScore();
        }
    }

    void AddScore()
    {
        score++; // Puanı artır
        UpdateScoreText();
    }

    void UpdateScoreText()
    {
        scoreText.text = "Score: " + score.ToString();
    }
}
