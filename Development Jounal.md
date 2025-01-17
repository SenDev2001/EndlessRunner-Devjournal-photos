# GAME PROJECT (VELOCITY RUSH 3D)
 #### GAME ENGINE PROGRAMING AND DEVELOPMENT 
 #### KURANAGE SENITH MADUSHAN PEREREA 
 #### 2412587

## INTRODUCTION
Velocity Rush is a 3D endless runner game designed for android and webgl and it’s made for the winter season environment and player have run through road while snow falling and avoid obstacles and collecting coins also velocity rush has leaderboard system so players can see names and score what they got and whose got high score.
## RESEARCH 
- I have done research subway surface case study to better understand its gaming mechanics and design components, which may inspire and lead the development of my own game. I looked at key elements including endless runner gameplay the necessity of user input, and the usage dynamic challenges. This case study helped me grasp the fundamental features of a successful mobile game, such as level design, coins, player movements and obstacles which I want to include to my project.
  - References - Subway Surfers case study (s.d.) At: https://unity.com/case-study/subway-surfers (Accessed 03/12/2024).
    
- Also, I have done research Temple Run Documentation to get ideas for my velocity rush game, The documentation game details on gaming mechanics, design aspects, and user engagement methods. This study helped me in better understanding basic aspects such as obstacle design, powerups and level design same as subway surfers.
  - References - Template documentation (2024) At: https://templerun.fandom.com/wiki/Category:Template_documentation (Accessed 03/12/2024).

- I looked at documentation in unity input systems for mobile. The unity input system literature version 1.11.2 provided a detailed description of how to configure and implement touch controllers, multi touch gestures and swipe recognition on mobile devices.
  -  References - Input System | Input System | 1.11.2 (s.d.) At: https://docs.unity3d.com/Packages/com.unity.inputsystem@1.11/manual/index.html (Accessed 03/12/2024).

- I followed YouTube videos to understand swipe detection for my first mobile game velocity rush. These tutorials demonstrated how to create swipe detection for touch and mouse inputs in unity’s new input system. I learnt how to detect directional swipes, analyse input data and combine swipe actions into game mechanism. In addition, I learnt visual upgrades such as trail effects to improve the user experience. This understanding allowed me to develop responsive and accurate swipe controls, resulting in intuitive gameplay. These elements are essential for mobile games, since they increase play interest and correspond with the main dynamics of and endless runner game.
  - References - detect Swipe NEW Input system (touch / mouse) | how to detect swipe in unity with New Input system (2022) At: https://www.youtube.com/watch?v=Xm9_rcmv3UU (Accessed 03/12/2024). Swipe Detection + Trail Effect w/ New Input System - Unity Tutorial (2021) At: https://www.youtube.com/watch?v=XUx_QlJpd0M (Accessed 03/12/2024).Swipe Detection + Trail Effect w/ New Input System - Unity Tutorial - YouTube (s.d.) At: https://www.youtube.com/watch?v=XUx_QlJpd0M (Accessed  12/12/2024).


- I have done research flask documentation to learn how to build a leaderboard system with Flask. I learnt Flask’s lightweight and flexible characteristics, as well as how to configure routes for receiving request and dynamically handle data with templates. I also looked at flask SQL Alchemy for database interaction and learnt how to create Restful APIs for leaderboard functions, Additionally I learnt how to deploy flask apps and secure routs, this study game me the groundwork to create a practical and user-friendly leaderboard system. 
  - References - Welcome to Flask — Flask Documentation (3.1.x) (s.d.) At: https://flask.palletsprojects.com/en/stable/ (Accessed  12/12/2024).


- I studied the Flask-CORS guide and it helped me to allow cross-origin requests in my Flask backend. If the Unity game front-end and Flask backend are maintained in separate domains, cross-origin requests are naturally blocked in browsers. Using CORS(app) helped me get better performance between my game and the backend server.
  - References - Flask-CORS — Flask-Cors 3.0.10 documentation (s.d.) At: https://flask-cors.readthedocs.io/en/latest/ (Accessed 12/12/2024).

- I have done research on how to deploy a flask in pythonanywhere. This guide give detailed information on how to setting up with a flask backend server. I've been taught how to configure WSGI, define environments, and manage database connections. That's all I need to deploy a Flask app, as well as instructions for running the app with ease Deployed the leaderboard server and provided the technical principles necessary to facilitate easy access and interaction with my game. 
  - References - PythonAnywere (2015) Setting up Flask applications on PythonAnywhere. At: https://help.pythonanywhere.com/pages/Flask/ (Accessed  12/12/2024).


- I did research about how to integrate UnityWebRequest with Flask server by watching YouTube video tutorials. The purpose of this study is to understand the methods required to create connections between a game and a Flask-backend server, specifically the requirements for sending and receiving data efficiently. 
  - References - High Score Table with Saving and Loading (Unity Tutorial for Beginners) - YouTube (s.d.) At: https://www.youtube.com/watch?v=iAbaqGYdnyI&t=150s (Accessed 03/12/2024). How to send a request from a Unity game to a Flask application server - YouTube (s.d.) At: https://www.youtube.com/watch?v=6JXYiGWGG-Y (Accessed 03/12/2024). Unity3d - UnityWebRequest Get async tutorial - YouTube (s.d.) At: https://www.youtube.com/watch?v=Yp8uPxEn6Vg&t=136s (Accessed 03/12/2024).

## Game Development Process
### Process Of Completing The task 
- #### Gameplay Design: 
  - I started by researching current endless runner games to learn about effective game mechanism. I concentrated on creating important gameplay elements such as player movement, swipe gestures, obstacle avoidance (add road barriers and busses), and snow partials.
  #### [Game Scene Screenshots] 
- #### Mobile Controls: 
  - I used unity’s new input System to build touch and swipe detection for seamless player interactions. 
#### [Mobile Game Screenshots]

- #### Testing and Feedbacks:
   - I did user tests to identify areas for upgrades, such as Swipe detection difficulties and leaderboard access.
#### [User Testing Videos]
https://youtu.be/7UuQ2rcpN-A
  
### Code Snippets 
- Spawning Roads
```csharp
 private void SpawnRoad()
 {
     int prefabIndex = prefabOrder[currentPrefabIndex];
     GameObject road = Instantiate(roadPrefabs[prefabIndex]);

     road.transform.SetParent(transform);
     road.transform.position = new Vector3(0, 0, spawnZ);

     SpawnSnowAboveRoad(road);

     activeRoads.Enqueue(road);

     spawnZ += roadLength;
     currentPrefabIndex = (currentPrefabIndex + 1) % prefabOrder.Length;
```
The roads and snow are spawned in an Endless Runner game plays a very important role in keeping the player on a continuous journey and creating a lively environment. Spawning roads helps to keep the player on a continuous journey, and adding elements like snow makes the environment look lively and attractive. Together, these two processes help to maintain the great experience in my velocity rush game. Accordingly, the way roads are spawned is a key component of the Endless Runner game, making the game seem like a long and continuous journey.

- Score and Leaderboard manager
  
  ```csharp
  public class ScoreManager : MonoBehaviour
  {
    // The current player's score
    public int Score { get; private set; }

    // UI elements for displaying the score and leaderboard
    public TMP_Text scoreText;
    public TMP_Text leaderboardText;

    // URLs for interacting with the backend API
    private string addScoreUrl = "https://sendev2001.pythonanywhere.com/addscore";
    private string leaderboardUrl = "https://sendev2001.pythonanywhere.com/leaderboard";

    // Player's name (loaded from PlayerPrefs)
    private string playerName;

    // Initialize the manager and set up player data
    private void Start()
    {
        // Load player name or default to "Guest"
        playerName = PlayerPrefs.GetString("PlayerName", "Guest");
        // Reset the score to start the game fresh
        ResetScore();
    }

    // Reset the score to zero and update the display
    public void ResetScore()
    {
        Score = 0;
        UpdateScoreText();
    }

    // Add a specified amount to the score and update the display
    public void AddScore(int amount)
    {
        Score += amount;
        UpdateScoreText();
    }

    // Update the score displayed in the UI
    private void UpdateScoreText()
    {
        if (scoreText != null)
        {
            scoreText.text = "Score: " + Score.ToString();
        }
    }

    // Submit the player's score to the backend API
    public void SubmitScore()
    {
        // Start the coroutine to submit the score to the server
        StartCoroutine(AddScoreToAPI(playerName, Score));
    }

    // Coroutine to send the score to the backend API
    private IEnumerator AddScoreToAPI(string name, int score)
    {
        string json = BuildScoreJson(name, score);
        Debug.Log("Sending JSON: " + json);

        UnityWebRequest request = CreateWebRequest(json);
        yield return request.SendWebRequest();

        // Handle the response from the server after submitting the score
        HandleAddScoreResponse(request);
    }

    // Create a JSON string for the score submission
    private string BuildScoreJson(string name, int score)
    {
        return "{\"name\": \"" + name + "\", \"score\": " + score + "}";
    }

    // Create the UnityWebRequest for submitting the score
    private UnityWebRequest CreateWebRequest(string json)
    {
        UnityWebRequest request = new UnityWebRequest(addScoreUrl, "POST");
        byte[] jsonToSend = new System.Text.UTF8Encoding().GetBytes(json);
        request.uploadHandler = new UploadHandlerRaw(jsonToSend);
        request.downloadHandler = new DownloadHandlerBuffer();
        request.SetRequestHeader("Content-Type", "application/json");

        return request;
    }

    // Handle the response after submitting the score
    private void HandleAddScoreResponse(UnityWebRequest request)
    {
        if (request.result != UnityWebRequest.Result.Success)
        {
            LogError(request);
            return;
        }

        Debug.Log("Score added successfully!");
        // After adding the score, fetch the leaderboard
        StartCoroutine(GetLeaderboard());
    }

    // Log errors if the score submission fails
    private void LogError(UnityWebRequest request)
    {
        Debug.LogError("Failed to add score: " + request.error);
        Debug.LogError("Response: " + request.downloadHandler.text);

        if (leaderboardText != null)
        {
            leaderboardText.text = "Error submitting score: " + request.error;
        }
    }

    // Coroutine to fetch the leaderboard data
    private IEnumerator GetLeaderboard()
    {
        UnityWebRequest request = UnityWebRequest.Get(leaderboardUrl);
        yield return request.SendWebRequest();

        // Handle the response for the leaderboard data
        HandleGetLeaderboardResponse(request);
    }

    // Handle the response after fetching the leaderboard data
    private void HandleGetLeaderboardResponse(UnityWebRequest request)
    {
        if (request.result != UnityWebRequest.Result.Success)
        {
            HandleLeaderboardError(request);
            return;
        }

        // Display the leaderboard if the data was successfully fetched
        DisplayLeaderboard(request.downloadHandler.text);
    }

    // Handle any errors that occur while fetching the leaderboard
    private void HandleLeaderboardError(UnityWebRequest request)
    {
        if (leaderboardText != null)
        {
            leaderboardText.text = "Error fetching leaderboard: " + request.error;
        }
    }

    // Parse and display the leaderboard from the JSON response
    private void DisplayLeaderboard(string jsonResponse)
    {
        string formattedResponse = FormatLeaderboardResponse(jsonResponse);
        LeaderboardResponse leaderboardResponse = JsonUtility.FromJson<LeaderboardResponse>(formattedResponse);
        string leaderboardDisplay = BuildLeaderboardDisplay(leaderboardResponse);

        if (leaderboardText != null)
        {
            leaderboardText.text = leaderboardDisplay;
        }
    }

    // Ensure the JSON response is in the correct format
    private string FormatLeaderboardResponse(string jsonResponse)
    {
        if (jsonResponse.StartsWith("["))
        {
            jsonResponse = "{\"leaderboardEntries\":" + jsonResponse + "}";
        }

        return jsonResponse;
    }

    // Build a string to display the leaderboard
    private string BuildLeaderboardDisplay(LeaderboardResponse leaderboardResponse)
    {
        string leaderboardDisplay = "\n";
        foreach (LeaderboardEntry entry in leaderboardResponse.leaderboardEntries)
        {
            leaderboardDisplay += entry.name + ": " + entry.score + "\n";
        }

        return leaderboardDisplay;
    }
  ``` 
  In this code snippet I use my full code of the ScoreManager. Because this is the hardest part I done. ScoreMAnager is a method designed to implement a player score management and leaderboard system in Unity. Its main function is to control the player's score and send it to the server via API and retrieve the leaderboard. It makes it easy to send and receive data via JSON using UnityWebRequest. This class establishes a live and efficient interaction between the game and the web service, thereby providing the player with a user-friendly experience of manipulating the score and leaderboard system data. And I used chatgpt to create these code comments is its help to understand my code.Also I used chatgpt for get idea for made this.
  - flask api
     
    ```python
    from flask import Flask, jsonify, request
    from flask_cors import CORS
    app = Flask(__name__)
    CORS(app)
    leaderboard = []
    @app.route('/addscore', methods=['POST'])
    def add_score():
    data = request.get_json()  # Get the JSON data from the request

    player_name = data.get('name')  # Get player name from the data
    player_score = data.get('score')  # Get player score from the data

    if not player_name or not player_score:
        return jsonify({"error": "Name and score are required"}), 400

    # Add the score to the leaderboard
    leaderboard.append({"name": player_name, "score": player_score})

    # Optionally return the updated leaderboard with a success message
    return jsonify({
        "message": "Score added successfully!",
        "player": player_name,
        "score": player_score,
        "leaderboard": leaderboard  # Return the current leaderboard
    })
    @app.route('/leaderboard', methods=['GET'])
    def get_leaderboard():
    # Sort the leaderboard by score in descending order
    sorted_leaderboard = sorted(leaderboard, key=lambda x: x['score'], reverse=True)

    # Return the sorted leaderboard as JSON
    return jsonify(sorted_leaderboard)
    if __name__ == '__main__':
    # Run the Flask app
    app.run(debug=True, host='0.0.0.0', port=5003)
    ```
    
    This is my Flask API, and I created it for the Endless Runner game in Unity. The main function of this API is to get the player name and score and post it to the API. In the Endless Runner game in Unity, this API is used to transmit the player name and score. In this Flask API, the /addscore method is implemented. Here, Unity sends the player name and score to the API using the POST method in JSON format. The API then receives that data and adds it to the scoreboard. Also, after the player name and score are successfully added by the API, the API returns a message in JSON format with the new score. The /leaderboard method in the API uses the GET method to get the current scoreboard of the game. This method shows the players who have the highest score after seeing their latest score. Here, the scoreboard data is sorted from top to bottom, giving Unity players details about their highest scores and latest standings. This Flask API is designed to be a system that can record the names and scores of players in the Unity Endless Runner game. Also, using the API, Unity players can easily adjust their scores and check the leaderboard.
    
### Future Improvements

## Bibliography 
- Subway Surfers Case Study (s.d.) At: Unity Case Study - Subway Surfers (Accessed 03/12/2024).
- Temple Run Template Documentation (2024) At: [Temple Run Wiki] (https://templerun.fandom.com/wiki/Category:Template_documentation) (Accessed 03/12/2024).
- Unity Input System 1.11.2 (s.d.) At: Unity Input System Documentation (Accessed 03/12/2024).
- Detect Swipe NEW Input System (Touch/Mouse) At: YouTube - Swipe Detection Tutorial (Accessed 03/12/2024).
- Flask Documentation (3.1.x) (s.d.) At: Flask Official Documentation (Accessed 03/12/2024).
- High Score Table with Saving and Loading (Unity Tutorial for Beginners) At: YouTube - Unity High Score Tutorial (Accessed 03/12/2024).
- How to Send a Request from a Unity Game to a Flask Application Server At: YouTube Tutorial (Accessed 03/12/2024).











 
  
