## GAME PROJECT
 #### GAME ENGINE PROGRAMING AND DEVELOPMENT 
 #### KURANAGE SENITH MADUSHAN PEREREA 
 #### 2412587

# VELOCITY RUSH
- ### Game URL: https://sendev2001.itch.io/velocity-rush
- ### GitHub URL: https://github.com/SenDev2001/Game-Project.git
- ### Gameplay Video: https://youtu.be/yvwEWiiB-iQ?si=t5gZ_OtTzPvNIoCR

## INTRODUCTION
Velocity Rush is a 3D endless runner game designed for android and webgl and it’s made for the winter season environment and player have run through road while snow falling and avoid obstacles and collecting coins also velocity rush has leaderboard system so players can see names and score what they got and whose got high score. And the highest score show in top in the leaderboard. 
## RESEARCH 
- I have done research subway surface case study to better understand its gaming mechanics and design components, which may inspire and lead the development of my own game. I looked at key elements including endless runner gameplay the necessity of user input, and the usage dynamic challenges. This case study helped me grasp the fundamental features of a successful mobile game, such as level design, coins, player movements and obstacles which I want to include to my project.
  - References - Subway Surfers case study (s.d.) At: https://unity.com/case-study/subway-surfers (Accessed 03/12/2024).
    
- Also, I have done research Temple Run Documentation to get ideas for my velocity rush game, The documentation game details on gaming mechanics, design aspects, and user engagement methods. This study helped me in better understanding basic aspects such as obstacle design, powerups and level design same as subway surfers.
  - References - Template documentation (2024) At: https://templerun.fandom.com/wiki/Category:Template_documentation (Accessed 03/12/2024).

- I looked at documentation in unity input systems for mobile. The unity input system literature version 1.11.2 provided a detailed description of how to configure and implement touch controllers, multi touch gestures and swipe recognition on mobile devices.
  -  References - Input System | Input System | 1.11.2 (s.d.) At: https://docs.unity3d.com/Packages/com.unity.inputsystem@1.11/manual/index.html (Accessed 03/12/2024).

- I followed YouTube videos to understand swipe detection for my first mobile game velocity rush. These tutorials demonstrated how to create swipe detection for touch and mouse inputs in unity’s new input system. I learnt how to detect directional swipes, analyse input data and combine swipe actions into game mechanism. In addition, I learnt visual upgrades such as trail effects to improve the user experience. This understanding allowed me to develop responsive and accurate swipe controls, resulting in intuitive gameplay. First I used old unity input system after I change it to new unity input system because its good for cross platform controls and also it has smooth swipe detection. These elements are essential for mobile games, since they increase play interest and correspond with the main dynamics of and endless runner game.
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
  - Menu Scene

  <img src="Screenshot 2025-01-19 225658.png" alt="Alt text" width="800" height="350">
 
  - Game Scene

   <img src="Screenshot 2025-01-19 225738.png" alt="Alt text" width="800" height="350">

- #### Mobile & WEBGL/PC Controls: 
  - I used unity’s new input System to build touch and swipe detection for seamless player interactions. 
  #### [Player Input Action Map Screenshot]
  <img src="Screenshot 2025-01-19 225907.png" alt="Alt text" width="500" height="300">


  #### [Mobile Game Screenshots]
  - Menu
  
  <img src="Screenshot_20250108-085525.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250108-085533.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250108-085538.png" alt="Alt text" width="250" >
  
  - Game

  <img src="Screenshot_20250120-153116.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250120-153155.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250120-153322.png" alt="Alt text" width="250" >

  - Pause & Audio

  <img src="Screenshot_20250108-085606.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250108-085610.png" alt="Alt text" width="250" >

  - Game Over And Leaderboard

  <img src="Screenshot_20250108-114339.png" alt="Alt text" width="250" >
  <img src="Screenshot_20250120-153131.png" alt="Alt text" width="250" >



- #### Testing and Feedbacks:
   - I did user tests to identify areas for upgrades, such as Swipe detection difficulties and leaderboard access. Whe n i game my game to play Students in uca they said Improve swipe system so before I use old input system after i change to unity new input system and its work nicely. Also i sent my game to my friends in Sri Lanka they Said add pause button and volume Mixer so after the feed back i fixed everything.
  #### [User Testing Video]
  https://youtu.be/7UuQ2rcpN-A
  #### [LeaderBoard Testing Video]
  https://www.youtube.com/watch?v=HpXlYbRmdug

### Main Code Snippets 
- #### RoadManager 
  - Road Spawning 
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
 - Spawning Snow
```csharp
 private void SpawnSnowAboveRoad(GameObject road)
{
    Vector3 snowPosition = road.transform.position + new Vector3(0, 10, 0);
    GameObject snow = Instantiate(snowPrefab, snowPosition, Quaternion.identity);

    snow.transform.SetParent(road.transform);
}
```
 - Cheching Roads and spawn
```csharp
 private void CheckRoadsAndSpawnNew()
{
    if (activeRoads.Count > 1)
    {
        GameObject secondRoad = activeRoads.ToArray()[1];
        if (playerTransform.position.z > secondRoad.transform.position.z + roadLength)
        {
            DestroyFirstRoadAndSpawnNew();
        }
    }
}

```
- Delete old Roads and generate new roads
```csharp
private void DestroyFirstRoadAndSpawnNew()
{
    GameObject firstRoad = activeRoads.Dequeue();
    Destroy(firstRoad);
    SpawnRoad();
}

```
The roads and snow are spawned in an Endless Runner game plays a very important role in keeping the player on a continuous journey and creating a lively environment. Spawning roads helps to keep the player on a continuous journey, and adding elements like snow makes the environment look lively and attractive. Together, these two processes help to maintain the great experience in my velocity rush game. Accordingly, the way roads are spawned is a key component of the Endless Runner game, making the game seem like a long and continuous journey.

- #### Score and Leaderboard manager
  
 ```csharp
using System.Collections;
using UnityEngine;
using UnityEngine.Networking;
using TMPro;

public class M_ScoreManager : MonoBehaviour
{
    public int Score { get; private set; }
    public TMP_Text scoreText;
    public TMP_Text leaderboardText;

    private string addScoreUrl = "https://sendev2001.pythonanywhere.com/addscore";
    private string leaderboardUrl = "https://sendev2001.pythonanywhere.com/leaderboard";

    private string playerName;

    private void Start()
    {
        playerName = PlayerPrefs.GetString("PlayerName", "Guest");
        ResetScore();
    }

    public void ResetScore()
    {
        Score = 0;
        UpdateScoreText();
    }

    public void AddScore(int amount)
    {
        Score += amount;
        UpdateScoreText();
    }

    private void UpdateScoreText()
    {
        if (scoreText != null)
        {
            scoreText.text = "Score: " + Score.ToString();
        }
    }

    public void SubmitScore()
    {
        StartCoroutine(AddScoreToAPI(playerName, Score));
    }

    private IEnumerator AddScoreToAPI(string name, int score)
    {
        string json = BuildScoreJson(name, score);
        UnityWebRequest request = CreateWebRequest(json);
        yield return request.SendWebRequest();

        HandleAddScoreResponse(request);
    }

    private string BuildScoreJson(string name, int score)
    {
        return "{\"name\": \"" + name + "\", \"score\": " + score + "}";
    }

    private UnityWebRequest CreateWebRequest(string json)
    {
        UnityWebRequest request = new UnityWebRequest(addScoreUrl + "?timestamp=" + Time.time, "POST"); // Added timestamp for cache busting
        byte[] jsonToSend = new System.Text.UTF8Encoding().GetBytes(json);
        request.uploadHandler = new UploadHandlerRaw(jsonToSend);
        request.downloadHandler = new DownloadHandlerBuffer();
        request.SetRequestHeader("Content-Type", "application/json");

        return request;
    }

    private void HandleAddScoreResponse(UnityWebRequest request)
    {
        if (request.result != UnityWebRequest.Result.Success)
        {
            LogError(request);
            return;
        }

        Debug.Log("Score added successfully!");
        StartCoroutine(GetLeaderboard());
    }

    private void LogError(UnityWebRequest request)
    {
        Debug.LogError("Failed to add score: " + request.error);
        Debug.LogError("Response: " + request.downloadHandler.text);

        if (leaderboardText != null)
        {
            leaderboardText.text = "\nTry Again!\nNo Coins Collected";
        }
    }

    private IEnumerator GetLeaderboard()
    {
        UnityWebRequest request = UnityWebRequest.Get(leaderboardUrl + "?timestamp=" + Time.time);  // Added timestamp for cache busting
        yield return request.SendWebRequest();

        HandleGetLeaderboardResponse(request);
    }

    private void HandleGetLeaderboardResponse(UnityWebRequest request)
    {
        if (request.result != UnityWebRequest.Result.Success)
        {
            HandleLeaderboardError(request);
            return;
        }

        DisplayLeaderboard(request.downloadHandler.text);
    }

    private void HandleLeaderboardError(UnityWebRequest request)
    {
        if (leaderboardText != null)
        {
            leaderboardText.text = "Error fetching leaderboard: " + request.error;
        }
    }

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

    private string FormatLeaderboardResponse(string jsonResponse)
    {
        if (jsonResponse.StartsWith("["))
        {
            jsonResponse = "{\"leaderboardEntries\":" + jsonResponse + "}";
        }

        return jsonResponse;
    }

    private string BuildLeaderboardDisplay(LeaderboardResponse leaderboardResponse)
    {
        string leaderboardDisplay = "\n";
        foreach (LeaderboardEntry entry in leaderboardResponse.leaderboardEntries)
        {
            leaderboardDisplay += entry.name + ": " + entry.score + "\n";
        }

        return leaderboardDisplay;
    }

    public void RestartGame()
    {
        SubmitScore();
        UnityEngine.SceneManagement.SceneManager.LoadScene("GameScene");
    }
}

[System.Serializable]
public class LeaderboardEntry
{
    public string name;
    public int score;
}

[System.Serializable]
public class LeaderboardResponse
{
    public LeaderboardEntry[] leaderboardEntries;
}


  ``` 
  In this code snippet I use my full code of the ScoreManager. Because this is the hardest part I done. ScoreMAnager is a method designed to implement a player score management and leaderboard system in Unity. Its main function is to control the player's score and send it to the server via API and retrieve the leaderboard. It makes it easy to send and receive data via JSON using UnityWebRequest. This class establishes a live and efficient interaction between the game and the web service, thereby providing the player with a user-friendly experience of manipulating the score and leaderboard system data. And I used chatgpt to create these code comments is its help to understand my code.

- #### Flask Api
     
 ```python
from flask import Flask, jsonify, request
from flask_cors import CORS

app = Flask(__name__)

# Enable CORS for all routes to allow cross-origin requests (e.g., from WebGL/Android)
CORS(app)

# Sample leaderboard (You can replace this with a database)
leaderboard = []

# Disable caching on the server side (add Cache-Control headers)
@app.after_request
def add_cache_control(response):
    response.cache_control.no_cache = True
    response.cache_control.no_store = True
    response.cache_control.must_revalidate = True
    response.headers['Pragma'] = 'no-cache'
    response.headers['Expires'] = '0'
    return response

# Route to add a score to the leaderboard
@app.route('/addscore', methods=['POST'])
def add_score():
    data = request.get_json()  # Get the JSON data from the request

    player_name = data.get('name')  # Get player name
    player_score = data.get('score')  # Get player score

    # Check if name and score are provided
    if not player_name or not player_score:
        return jsonify({"error": "Name and score are required"}), 400

    # Add the score to the leaderboard
    leaderboard.append({"name": player_name, "score": player_score})

    # Optionally, return the updated leaderboard along with a success message
    return jsonify({
        "message": "Score added successfully!",
        "player": player_name,
        "score": player_score,
        "leaderboard": leaderboard  # Return the current leaderboard
    })

# Route to get the leaderboard
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

- #### Keyboard and Swipe Control
  - Swipe Handeling 
```csharp
private void DetectSwipe(bool enable = true)
{
    if (!enable)
    {
        swipeAction.Disable();
        return;
    }

    swipeAction.Enable(); 

    if (Time.time - lastSwipeTime < swipeCooldown) return;

    swipeDelta = swipeAction.ReadValue<Vector2>();

    if (swipeDelta.magnitude >= minimumSwipeDistance)
    {
        ProcessSwipe(swipeDelta);
        swipeDelta = Vector2.zero;
        lastSwipeTime = Time.time;
    }
}

private void ProcessSwipe(Vector2 delta)
{
    if (Mathf.Abs(delta.x) > Mathf.Abs(delta.y))
    {
        if (delta.x > 0) MoveRight();
        else MoveLeft();
    }
    else if (delta.y > 0) 
    {
        Jump();
    }
}

```
  - Keyboard Handeling 
```csharp
private void HandleKeyboardInput(bool enable = true)
{
    if (!enable)
    {
        keyboardAction.Disable(); 
        return;
    }

    keyboardAction.Enable(); 

    if (Time.time - lastKeyboardTime < keyboardCooldown) return;

    Vector2 input = keyboardAction.ReadValue<Vector2>();

    if (input.y > 0) Jump(); 
    if (input.x < 0) MoveLeft(); 
    if (input.x > 0) MoveRight(); 

    lastKeyboardTime = Time.time; 
}

```

    
### Future Improvements

Future Improments ideas for my velocity rush game are as follows:

- #### Adding Enemies
  To increase the challenge of the game, enemies can be added. This makes it more challenging and competitive for the player.

- #### Changeable Environment and Levels
  By changing the environment and levels of the game, the player can have a new experience. Adding options such as new environments, mountains, and fire ascents makes the game more attractive.

- #### New Equipment and Power-ups
  By giving the player new powers or equipment, it helps in passing the challenges. This further increases the appeal and challenge of the game.

- #### New Multiplayer and Online Competitions
  As a new feature of the game, by adding a competition between online players, Sri Lankan and international players can play together.

- #### New Sound and Music Themes
  Adding new music and sound effects to game elements can provide an engaging experience for the player.

- #### Leaderboard Development
  Adding leaderboards can help players further hone their game skills. By giving the highest ranked players and rewards according to the leaderboard, more challenges and series can be added to the game.

## Import Assets 
- City Props Pack! | 3D Props | Unity Asset Store (s.d.) At: https://assetstore.unity.com/packages/3d/props/city-props-pack-153581 (Accessed  22/01/2025).
- Metal and Concrete Barriers | 3D Exterior | Unity Asset Store (s.d.) At: https://assetstore.unity.com/packages/3d/props/exterior/metal-and-concrete-barriers-231794 (Accessed  22/01/2025).
- Mobile Tree Package | 3D Trees | Unity Asset Store (s.d.) At: https://assetstore.unity.com/packages/3d/vegetation/trees/mobile-tree-package-18866 (Accessed  22/01/2025).
- POLYGON office building | 3D Urban | Unity Asset Store (s.d.) At: https://assetstore.unity.com/packages/3d/environments/urban/polygon-office-building-82282 (Accessed  22/01/2025).
- Mixamo (s.d.) At: https://www.mixamo.com/#/?page=1&type=Character (Accessed  22/01/2025).
- Russian buildings pack | 3D Urban | Unity Asset Store (s.d.) At: https://assetstore.unity.com/packages/3d/environments/urban/russian-buildings-pack-113375 (Accessed  22/01/2025).
   


## Bibliography 
- Subway Surfers Case Study (s.d.) At: Unity Case Study - Subway Surfers (Accessed 03/12/2024).
- Temple Run Template Documentation (2024) At: [Temple Run Wiki] (https://templerun.fandom.com/wiki/Category:Template_documentation) (Accessed 03/12/2024).
- Unity Input System 1.11.2 (s.d.) At: Unity Input System Documentation (Accessed 03/12/2024).
- Detect Swipe NEW Input System (Touch/Mouse) At: YouTube - Swipe Detection Tutorial (Accessed 03/12/2024).
- Flask Documentation (3.1.x) (s.d.) At: Flask Official Documentation (Accessed 03/12/2024).
- High Score Table with Saving and Loading (Unity Tutorial for Beginners) At: YouTube - Unity High Score Tutorial (Accessed 03/12/2024).
- How to Send a Request from a Unity Game to a Flask Application Server At: YouTube Tutorial (Accessed 03/12/2024).











 
  

 
  
