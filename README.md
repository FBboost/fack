<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Video Categories</title>
  <style>
    body {
      background: #000;
      font-family: Arial, sans-serif;
      color: #00ffc8;
      padding: 40px;
      text-align: center;
    }

    .btn-group {
      margin-bottom: 30px;
    }

    .btn-group button {
      background-color: black;
      color: #00ffc8;
      border: 2px solid #00ffc8;
      padding: 10px 20px;
      margin: 5px;
      cursor: pointer;
      box-shadow: 0 0 10px #00ffc8;
      transition: all 0.3s ease;
    }

    .btn-group button:hover,
    .btn-group button.active {
      background-color: #00ffc8;
      color: black;
      font-weight: bold;
      box-shadow: 0 0 25px #00ffc8;
    }

    .video-card-box {
      background: black;
      border: 2px solid #00ffc8;
      box-shadow: 0 0 15px #00ffc8;
      padding: 20px;
      animation: shadowPulse 2s infinite ease-in-out;
      max-width: 1200px;
      margin: auto;
    }

    @keyframes shadowPulse {
      0% { box-shadow: 0 0 10px #00ffc8; }
      50% { box-shadow: 0 0 25px #00ffc8; }
      100% { box-shadow: 0 0 10px #00ffc8; }
    }

    .category {
      display: none;
    }

    .category.active {
      display: block;
    }

    .category h2 {
      border-bottom: 1px solid #00ffc8;
      padding-bottom: 5px;
      margin-bottom: 15px;
      font-size: 24px;
    }

    .videos {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .video {
      flex: 1 1 calc(33.333% - 20px);
      background: #111;
      padding: 10px;
      border: 1px solid #00ffc8;
      border-radius: 10px;
      box-shadow: 0 0 10px #00ffc8;
    }

    .video video {
      width: 100%;
      height: auto;
      border-radius: 50px;
      width: 400px;
      height: 500px;
      border: 2px solid #00ffc8;
    }

    @media (max-width: 768px) {
      .video {
        flex: 1 1 100%;
      }
    }
  </style>
</head>
<body>

  <div class="btn-group">
    <button class="tab-btn active" onclick="showCategory('cat1', this)">Category 1</button>
    <button class="tab-btn" onclick="showCategory('cat2', this)">Category 2</button>
    <button class="tab-btn" onclick="showCategory('cat3', this)">Category 3</button>
    <button class="tab-btn" onclick="showCategory('cat4', this)">Category 4</button>
    <button class="tab-btn" onclick="showCategory('cat5', this)">Category 5</button>
  </div>

  <div class="video-card-box">

    <div id="cat1" class="category active">
      <h2>Category 1</h2>
      <div class="videos">
        <div class="video"><video src="health1.mp4" controls></video></div>
        <div class="video"><video src="videoplayback (6) (13).mp4" controls></video></div>
        <div class="video"><video src="video3.mp4" controls></video></div>
      </div>
    </div>

    <div id="cat2" class="category">
      <h2>Category 2</h2>
      <div class="videos">
        <div class="video"><video src="video4.mp4" controls></video></div>
        <div class="video"><video src="video5.mp4" controls></video></div>
        <div class="video"><video src="video6.mp4" controls></video></div>
      </div>
    </div>

    <div id="cat3" class="category">
      <h2>Category 3</h2>
      <div class="videos">
        <div class="video"><video src="video7.mp4" controls></video></div>
        <div class="video"><video src="video8.mp4" controls></video></div>
        <div class="video"><video src="video9.mp4" controls></video></div>
      </div>
    </div>

    <div id="cat4" class="category">
      <h2>Category 4</h2>
      <div class="videos">
        <div class="video"><video src="video10.mp4" controls></video></div>
        <div class="video"><video src="video11.mp4" controls></video></div>
        <div class="video"><video src="video12.mp4" controls></video></div>
      </div>
    </div>

    <div id="cat5" class="category">
      <h2>Category 5</h2>
      <div class="videos">
        <div class="video"><video src="video13.mp4" controls></video></div>
        <div class="video"><video src="video14.mp4" controls></video></div>
        <div class="video"><video src="video15.mp4" controls></video></div>
      </div>
    </div>

  </div>

  <script>
    function showCategory(catId, btn) {
      document.querySelectorAll('.category').forEach(c => c.classList.remove('active'));
      document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
      document.getElementById(catId).classList.add('active');
      btn.classList.add('active');
    }
  </script>

</body>
</html>
