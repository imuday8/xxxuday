<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XXX WEBSITE OF UDAY SAHA</title>
    <u><h1 style="color:red;background-color: #2629f5",><CENter>WELCOME TO THE UDAY'S PORN SITE</CENter></h1></u>

    <marquee behavior=scroll direction="left" scrollamount="18"><h1 style="color:rgb(255, 2, 150);background-color: #26ff09",><CENter>UDAY SAHA AND HIS TEAM</CENter></h1></marquee>
    <CENTER><B><U><pre>YOU CAN SEARCH HERE</pre></U></B></CENTER>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: #ff3535;
            padding: 1em;
        }

        .search-box {
            display: flex;
            align-items: center;
            justify-content: center; /* Add this line to center horizontally */
            height: 3vh;
            
        }

        .search-input {
            padding: 8px;
            margin-right: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .search-button {
            background-color: #2629f5;
            color: #ffffff;
            padding: 8px 12px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        main {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 20px;
        }

        .video-item {
            position: relative;
            overflow: hidden;
            border-radius: 5px;
        }

        .video-item img {
            width: 100%;
            height: auto;
            border-radius: 5px;
            transition: transform 0.3s;
        }

        .video-item:hover img {
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .video-grid {
                grid-template-columns: repeat(1, 1fr);
            }
        }

        #upload-container {
            text-align: center;
            max-width: 400px;
            width: 100%;
            margin: 20px auto;
        }

        #upload-form {
            border: 2px solid #eeff03;
            padding: 20px;
            border-radius: 19px;
        }

        #file-input {
            margin-bottom: 10px;
        }
        pre {
            font-size: 25px; /* Adjust the size as needed */
            color: rgb(123, 255, 0);
        }
        body {
            background-color: #0e00d4; /* Set the background color to a light gray shade */
            /* You can replace #f0f0f0 with any valid CSS color value */
            /* For example: red, #00ff00, rgb(255, 0, 0), etc. */
        }
    </style>
</head>
<body>

    <header>
        <div class="search-box">
            <input type="text" class="search-input" placeholder="Search...">
            <button class="search-button">Search</button>
        </div>
    </header>

    <main>
        <div class="video-grid">
            <div class="video-item">
                <!-- Replace the URL with the thumbnail of your video -->
                <img src="hairstyle 1.jpg" alt="Video 1" width="60">
            </div>

            <div class="video-item">
                <img src="WhatsApp Image 2023-11-11 at 00.47.32_ed76ca05.jpg" alt="Video 2">
            </div>

            <div class="video-item">
                <img src="20221113_154945.jpg" alt="Video 3">
            </div>

            <!-- Add more video items as needed -->
        </div>
        <b><u><center><pre>IF YOU WANT TO JOIN WITH US YOU CAN UPLOAD SOME VIDEOS IN THIS WEBSITE TO IMPROVE US</pre></center></u></b>
        <div id="upload-container">
            <form id="upload-form" enctype="multipart/form-data">
                <label for="file-input">Select Video:</label>
                <input type="file" id="file-input" name="video" accept="video/*" required>
                <br>
                <button type="button" onclick="uploadVideo()">Upload</button>
                <progress id="upload-progress" value="0" max="100" style="display: none;"></progress>
                <div id="upload-message"></div>
            </form>
        </div>
    </main>

    <script>
        function uploadVideo() {
            var fileInput = document.getElementById('file-input');
            var file = fileInput.files[0];

            if (file) {
                var formData = new FormData();
                formData.append('video', file);

                var xhr = new XMLHttpRequest();
                xhr.open('POST', 'your_upload_endpoint.php', true);

                xhr.upload.onprogress = function (e) {
                    if (e.lengthComputable) {
                        var percentComplete = (e.loaded / e.total) * 100;
                        document.getElementById('upload-progress').style.display = 'block';
                        document.getElementById('upload-progress').value = percentComplete;
                    }
                };

                xhr.onload = function () {
                    if (xhr.status === 200) {
                        document.getElementById('upload-message').innerHTML = 'Upload successful!';
                    } else {
                        document.getElementById('upload-message').innerHTML = 'Upload failed. Please try again.';
                    }
                };

                xhr.send(formData);
            } else {
                document.getElementById('upload-message').innerHTML = 'Please select a video file.';
            }
        }
    </script>
    
</body>
</html>
