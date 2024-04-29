<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lonely Chat</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
        }
        .chat-area {
            height: 300px;
            overflow-y: auto;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        .input-area {
            display: flex;
        }
        .input-area input[type="text"] {
            flex: 1;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
        .input-area button, .input-area input[type="file"] {
            padding: 8px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .video-call-btn, .photo-sharing-btn {
            display: block;
            margin: 10px auto;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-align: center;
            text-decoration: none;
            width: 200px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Lonely Chat</h1>
        <div class="chat-area" id="chatArea">
            <!-- Chat messages will appear here -->
        </div>
        <div class="input-area">
            <input type="text" id="messageInput" placeholder="Type your message...">
            <input type="file" accept="audio/*" id="audioInput">
            <button onclick="sendMessage()">Send</button>
            <button onclick="sendVoiceMessage()">Send Voice Message</button>
        </div>
        <a href="#" class="video-call-btn">Start Video Call</a>
        <a href="#" class="photo-sharing-btn">Share Photos</a>
    </div>

    <script>
        function sendMessage() {
            var messageInput = document.getElementById("messageInput");
            var message = messageInput.value.trim();
            if (message !== "") {
                var chatArea = document.getElementById("chatArea");
                var messageElement = document.createElement("div");
                messageElement.textContent = message;
                chatArea.appendChild(messageElement);
                chatArea.scrollTop = chatArea.scrollHeight;
                messageInput.value = "";
            }
        }

        function sendVoiceMessage() {
            var audioInput = document.getElementById("audioInput");
            var audioFile = audioInput.files[0];
            if (audioFile) {
                var chatArea = document.getElementById("chatArea");
                var messageElement = document.createElement("div");
                var audioElement = document.createElement("audio");
                audioElement.controls = true;
                var source = document.createElement("source");
                source.src = URL.createObjectURL(audioFile);
                audioElement.appendChild(source);
                messageElement.appendChild(audioElement);
                chatArea.appendChild(messageElement);
                chatArea.scrollTop = chatArea.scrollHeight;
                audioInput.value = "";
            }
        }
    </script>
</body>
</html>
