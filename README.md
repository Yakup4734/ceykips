<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CEYKIP Blog</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap');
        body {
            background-color: #111;
            color: white;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background: linear-gradient(to right, red, black, yellow);
            padding: 20px;
            text-align: center;
            font-size: 36px;
            font-weight: bold;
            font-family: 'Permanent Marker', cursive;
            text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.7);
            letter-spacing: 2px;
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 15px;
            background-color: black;
            padding: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }
        .container {
            max-width: 800px;
            margin: auto;
            padding: 20px;
        }
        .comment-section {
            margin-top: 20px;
            background: #222;
            padding: 10px;
            border-radius: 5px;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: black;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>CEYKIP Blog</header>
    <nav>
        <a href="#">Ana Sayfa</a>
        <a href="#">Hakkında</a>
        <a href="#">İletişim</a>
    </nav>
    <div class="container">
        <h2>Günün Konusu</h2>
        <p>Buraya günlüğünü yazabilirsin...</p>
        
        <div class="comment-section">
            <h3>Yorumlar</h3>
            <textarea id="comment" rows="3" style="width: 100%;"></textarea>
            <button onclick="addComment()">Gönder</button>
            <ul id="commentList"></ul>
        </div>
    </div>
    <footer>
        <p>CEYKIP Blog &copy; 2025</p>
        <p>
            <a href="#">Instagram</a> |
            <a href="#">Twitter</a> |
            <a href="#">Facebook</a>
        </p>
    </footer>
    <script>
        function addComment() {
            let commentText = document.getElementById("comment").value;
            if(commentText.trim() !== "") {
                let li = document.createElement("li");
                li.textContent = commentText;
                document.getElementById("commentList").appendChild(li);
                document.getElementById("comment").value = "";
            }
        }
    </script>
</body>
</html>
