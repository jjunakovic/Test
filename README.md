<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Support Forum</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f4f4f4; }
        header { background: #0073e6; color: white; padding: 15px; text-align: center; }
        nav { display: flex; justify-content: center; background: #005bb5; padding: 10px; }
        nav a { color: white; padding: 10px 20px; text-decoration: none; }
        nav a:hover { background: #003f80; }
        .container { width: 80%; margin: auto; padding: 20px; background: white; }
        .post { background: #e6f2ff; padding: 15px; margin: 10px 0; border-radius: 5px; }
        .form-group { margin-bottom: 15px; }
        .form-group label { display: block; font-weight: bold; }
        .form-group textarea { width: 100%; height: 100px; padding: 10px; }
        .btn { background: #0073e6; color: white; padding: 10px 15px; border: none; cursor: pointer; }
        .btn:hover { background: #005bb5; }
    </style>
</head>
<body>
    <header>
        <h1>Student Support Forum</h1>
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#forum">Forum</a>
        <a href="#resources">Resources</a>
        <a href="#contact">Contact</a>
    </nav>
    <div class="container" id="forum">
        <h2>Anonymous Forum</h2>
        <div class="form-group">
            <label for="postContent">Share your thoughts or concerns:</label>
            <textarea id="postContent"></textarea>
        </div>
        <button class="btn" onclick="postMessage()">Post Anonymously</button>
        <div id="forumPosts"></div>
    </div>
    <script>
        function postMessage() {
            let content = document.getElementById("postContent").value;
            if (content.trim() !== "") {
                let post = document.createElement("div");
                post.className = "post";
                post.textContent = content;
                document.getElementById("forumPosts").prepend(post);
                document.getElementById("postContent").value = "";
            }
        }
    </script>
</body>
</html>
