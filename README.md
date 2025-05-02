<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A free platform for Hindi audio stories. 18+ only.">
  <meta name="keywords" content="Hindi audio stories, adult audio, user-submitted audio">
  <title>हिंदी ऑडियो कहानियाँ</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+Devanagari:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Noto Serif Devanagari', serif;
    }

    body {
      background-color: #f0f0f0;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #1a2a44;
      color: #fff;
      padding: 1.5rem;
      text-align: center;
    }

    header h1 {
      font-size: 2.2rem;
      margin-bottom: 0.5rem;
    }

    nav {
      background-color: #2a3b55;
      padding: 1rem;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 0 1.2rem;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-size: 1.1rem;
    }

    nav ul li a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    .audio-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.5rem;
    }

    .audio-card {
      background-color: #fff;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    .audio-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }

    .audio-card audio {
      width: 100%;
      margin-top: 0.5rem;
    }

    .submission-form {
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      margin-top: 2rem;
    }

    .submission-form h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .submission-form label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: bold;
    }

    .submission-form input,
    .submission-form textarea,
    .submission-form select,
    .submission-form input[type="file"] {
      width: 100%;
      padding: 0.5rem;
      margin-bottom: 1rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
    }

    .submission-form button {
      background-color: #1a2a44;
      color: #fff;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1rem;
    }

    .submission-form button:hover {
      background-color: #2a3b55;
    }

    footer {
      background-color: #1a2a44;
      color: #fff;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }

    #age-verification {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      z-index: 1000;
      justify-content: center;
      align-items: center;
    }

    .age-popup {
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      text-align: center;
      max-width: 400px;
    }

    .age-popup h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .age-popup p {
      margin-bottom: 1.5rem;
    }

    .age-popup button {
      background-color: #1a2a44;
      color: #fff;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      margin: 0 0.5rem;
    }

    .age-popup button:hover {
      background-color: #2a3b55;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 1.6rem;
      }

      nav ul li {
        margin: 0.5rem;
      }

      .audio-list {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- Age Verification Popup -->
  <div id="age-verification">
    <div class="age-popup">
      <h2>18+ केवल</h2>
      <p>इस वेबसाइट में वयस्क सामग्री है। आगे बढ़ने के लिए आपकी आयु 18 वर्ष या अधिक होनी चाहिए।</p>
      <button onclick="verifyAge(true)">मैं 18+ हूँ</button>
      <button onclick="verifyAge(false)">मैं 18 से कम हूँ</button>
    </div>
  </div>

  <!-- Header -->
  <header>
    <h1>हिंदी ऑडियो कहानियाँ</h1>
    <p>18+ के लिए मुफ्त हिंदी ऑडियो कहानियाँ</p>
  </header>

  <!-- Navigation -->
  <nav>
    <ul>
      <li><a href="#home">होम</a></li>
      <li><a href="#popular">लोकप्रिय</a></li>
      <li><a href="#romance">रोमांस</a></li>
      <li><a href="#humor">हास्य</a></li>
      <li><a href="#submit">ऑडियो जमा करें</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <div class="container">
    <section id="home">
      <h2>स्वागत है!</h2>
      <p>यहाँ आपको हिंदी में रोमांचक ऑडियो कहानियाँ मिलेंगी। अपनी कहानी साझा करें और समुदाय के साथ जुड़ें।</p>
    </section>

    <section id="popular">
      <h2>लोकप्रिय ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>प्यार की रात</h3>
          <p>एक रोमांटिक कहानी जो दिल को छू लेगी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
        <div class="audio-card">
          <h3>रहस्यमयी आवाज़</h3>
          <p>एक रहस्य से भरी कहानी जो आपको सोचने पर मजबूर कर देगी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="romance">
      <h2>रोमांस ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>पहली मुलाकात</h3>
          <p>दो अजनबियों की प्रेम कहानी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="humor">
      <h2>हास्य ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>मजेदार भूल</h3>
          <p>एक छोटी सी गलती जो हंसी का कारण बन जाती है।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="submit" class="submission-form">
      <h2>अपनी ऑडियो कहानी जमा करें</h2>
      <form id="audio-form">
        <label for="title">कहानी का शीर्षक:</label>
        <input type="text" id="title" name="title" required>

        <label for="category">श्रेणी:</label>
        <select id="category" name="category" required>
          <option value="popular">लोकप्रिय</option>
          <option value="romance">रोमांस</option>
          <option value="humor">हास्य</option>
        </select>

        <label for="description">विवरण:</label>
        <textarea id="description" name="description" rows="4" required></textarea>

        <label for="audio-file">ऑडियो फ़ाइल (MP3):</label>
        <input type="file" id="audio-file" name="audio-file" accept="audio/mpeg" required>

        <button type="submit">जमा करें</button>
      </form>
    </section>
  </div>

  <!-- Footer -->
  <footer>
    <p>© 2025 हिंदी ऑडियो कहानियाँ। सभी अधिकार सुरक्षित। 18+ केवल।</p>
    <p><a href="#privacy" style="color: #fff;">गोपनीयता नीति</a> | <a href="#terms" style="color: #fff;">उपयोग की शर्तें</a></p>
  </footer>

  <script>
    // Age Verification
    window.onload = function() {
      document.getElementById('age-verification').style.display = 'flex';
    };

    function verifyAge(isAdult) {
      if (isAdult) {
        document.getElementById('age-verification').style.display = 'none';
      } else {
        window.location.href = 'https://www.google.com'; // Redirect if under 18
      }
    }

    // Form Submission (Basic Alert for Demo)
    document.getElementById('audio-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const title = document.getElementById('title').value;
      const category = document.getElementById('category').value;
      const description = document.getElementById('description').value;
      const audioFile = document.getElementById('audio-file').files[0]?.name || 'No file selected';

      alert(`ऑडियो जमा हो गया!\nशीर्षक: ${title}\nश्रेणी: ${category}\nविवरण: ${description.substring(0, 50)}...\nफ़ाइल: ${audioFile}`);
      this.reset(); // Reset form
    });

    // Smooth Scroll for Navigation
    document.querySelectorAll('nav a').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const sectionId = this.getAttribute('href');
        document.querySelector(sectionId).scrollIntoView({ behavior: 'smooth' });
      });
    });
  </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A free platform for Hindi audio stories. 18+ only.">
  <meta name="keywords" content="Hindi audio stories, adult audio, user-submitted audio">
  <title>हिंदी ऑडियो कहानियाँ</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+Devanagari:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Noto Serif Devanagari', serif;
    }

    body {
      background-color: #f0f0f0;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #1a2a44;
      color: #fff;
      padding: 1.5rem;
      text-align: center;
    }

    header h1 {
      font-size: 2.2rem;
      margin-bottom: 0.5rem;
    }

    nav {
      background-color: #2a3b55;
      padding: 1rem;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 0 1.2rem;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-size: 1.1rem;
    }

    nav ul li a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    .audio-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.5rem;
    }

    .audio-card {
      background-color: #fff;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    .audio-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }

    .audio-card audio {
      width: 100%;
      margin-top: 0.5rem;
    }

    .submission-form {
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      margin-top: 2rem;
    }

    .submission-form h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .submission-form label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: bold;
    }

    .submission-form input,
    .submission-form textarea,
    .submission-form select,
    .submission-form input[type="file"] {
      width: 100%;
      padding: 0.5rem;
      margin-bottom: 1rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
    }

    .submission-form button {
      background-color: #1a2a44;
      color: #fff;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1rem;
    }

    .submission-form button:hover {
      background-color: #2a3b55;
    }

    footer {
      background-color: #1a2a44;
      color: #fff;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }

    #age-verification {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      z-index: 1000;
      justify-content: center;
      align-items: center;
    }

    .age-popup {
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      text-align: center;
      max-width: 400px;
    }

    .age-popup h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .age-popup p {
      margin-bottom: 1.5rem;
    }

    .age-popup button {
      background-color: #1a2a44;
      color: #fff;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      margin: 0 0.5rem;
    }

    .age-popup button:hover {
      background-color: #2a3b55;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 1.6rem;
      }

      nav ul li {
        margin: 0.5rem;
      }

      .audio-list {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- Age Verification Popup -->
  <div id="age-verification">
    <div class="age-popup">
      <h2>18+ केवल</h2>
      <p>इस वेबसाइट में वयस्क सामग्री है। आगे बढ़ने के लिए आपकी आयु 18 वर्ष या अधिक होनी चाहिए।</p>
      <button onclick="verifyAge(true)">मैं 18+ हूँ</button>
      <button onclick="verifyAge(false)">मैं 18 से कम हूँ</button>
    </div>
  </div>

  <!-- Header -->
  <header>
    <h1>हिंदी ऑडियो कहानियाँ</h1>
    <p>18+ के लिए मुफ्त हिंदी ऑडियो कहानियाँ</p>
  </header>

  <!-- Navigation -->
  <nav>
    <ul>
      <li><a href="#home">होम</a></li>
      <li><a href="#popular">लोकप्रिय</a></li>
      <li><a href="#romance">रोमांस</a></li>
      <li><a href="#humor">हास्य</a></li>
      <li><a href="#submit">ऑडियो जमा करें</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <div class="container">
    <section id="home">
      <h2>स्वागत है!</h2>
      <p>यहाँ आपको हिंदी में रोमांचक ऑडियो कहानियाँ मिलेंगी। अपनी कहानी साझा करें और समुदाय के साथ जुड़ें।</p>
    </section>

    <section id="popular">
      <h2>लोकप्रिय ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>प्यार की रात</h3>
          <p>एक रोमांटिक कहानी जो दिल को छू लेगी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
        <div class="audio-card">
          <h3>रहस्यमयी आवाज़</h3>
          <p>एक रहस्य से भरी कहानी जो आपको सोचने पर मजबूर कर देगी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="romance">
      <h2>रोमांस ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>पहली मुलाकात</h3>
          <p>दो अजनबियों की प्रेम कहानी।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="humor">
      <h2>हास्य ऑडियो कहानियाँ</h2>
      <div class="audio-list">
        <div class="audio-card">
          <h3>मजेदार भूल</h3>
          <p>एक छोटी सी गलती जो हंसी का कारण बन जाती है।</p>
          <audio controls>
            <source src="https://www.example.com/sample-audio.mp3" type="audio/mpeg">
            आपका ब्राउज़र ऑडियो तत्व का समर्थन नहीं करता।
          </audio>
        </div>
      </div>
    </section>

    <section id="submit" class="submission-form">
      <h2>अपनी ऑडियो कहानी जमा करें</h2>
      <form id="audio-form">
        <label for="title">कहानी का शीर्षक:</label>
        <input type="text" id="title" name="title" required>

        <label for="category">श्रेणी:</label>
        <select id="category" name="category" required>
          <option value="popular">लोकप्रिय</option>
          <option value="romance">रोमांस</option>
          <option value="humor">हास्य</option>
        </select>

        <label for="description">विवरण:</label>
        <textarea id="description" name="description" rows="4" required></textarea>

        <label for="audio-file">ऑडियो फ़ाइल (MP3):</label>
        <input type="file" id="audio-file" name="audio-file" accept="audio/mpeg" required>

        <button type="submit">जमा करें</button>
      </form>
    </section>
  </div>

  <!-- Footer -->
  <footer>
    <p>© 2025 हिंदी ऑडियो कहानियाँ। सभी अधिकार सुरक्षित। 18+ केवल।</p>
    <p><a href="#privacy" style="color: #fff;">गोपनीयता नीति</a> | <a href="#terms" style="color: #fff;">उपयोग की शर्तें</a></p>
  </footer>

  <script>
    // Age Verification
    window.onload = function() {
      document.getElementById('age-verification').style.display = 'flex';
    };

    function verifyAge(isAdult) {
      if (isAdult) {
        document.getElementById('age-verification').style.display = 'none';
      } else {
        window.location.href = 'https://www.google.com'; // Redirect if under 18
      }
    }

    // Form Submission (Basic Alert for Demo)
    document.getElementById('audio-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const title = document.getElementById('title').value;
      const category = document.getElementById('category').value;
      const description = document.getElementById('description').value;
      const audioFile = document.getElementById('audio-file').files[0]?.name || 'No file selected';

      alert(`ऑडियो जमा हो गया!\nशीर्षक: ${title}\nश्रेणी: ${category}\nविवरण: ${description.substring(0, 50)}...\nफ़ाइल: ${audioFile}`);
      this.reset(); // Reset form
    });

    // Smooth Scroll for Navigation
    document.querySelectorAll('nav a').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const sectionId = this.getAttribute('href');
        document.querySelector(sectionId).scrollIntoView({ behavior: 'smooth' });
      });
    });
  </script>
</body>
</html>
