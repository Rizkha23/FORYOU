<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday! ✨</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      background: #0f172a;
      padding: 40px 20px;
      overflow-x: hidden;
      position: relative;
      color: #f8fafc;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    /* Ambient Glow Background */
    .light-glow {
      position: fixed;
      border-radius: 50%;
      filter: blur(90px);
      opacity: 0.5;
      pointer-events: none;
      z-index: 1;
    }

    .glow-1 {
      width: 350px;
      height: 350px;
      background: radial-gradient(circle, #f43f5e 0%, rgba(244, 63, 94, 0) 70%);
      top: -10%;
      left: -10%;
    }

    .glow-2 {
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, #8b5cf6 0%, rgba(139, 92, 246, 0) 70%);
      bottom: -10%;
      right: -10%;
    }

    /* Header Section */
    .header-title {
      text-align: center;
      margin-bottom: 30px;
      z-index: 2;
    }

    .header-title h1 {
      font-size: 2rem;
      font-weight: 800;
      background: linear-gradient(135deg, #ffffff 0%, #fb7185 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 6px;
    }

    .header-title p {
      color: #94a3b8;
      font-size: 0.95rem;
    }

    /* Cards Container */
    .cards-container {
      display: flex;
      flex-direction: column;
      gap: 24px;
      max-width: 390px;
      width: 100%;
      z-index: 2;
    }

    /* Individual Card Glassmorphism */
    .card {
      background: rgba(30, 41, 59, 0.65);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border-radius: 24px;
      padding: 24px;
      text-align: center;
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3),
                  inset 0 1px 1px rgba(255, 255, 255, 0.15);
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: transform 0.3s ease;
    }

    .card-step {
      display: inline-block;
      background: rgba(244, 63, 94, 0.15);
      color: #fb7185;
      border: 1px solid rgba(244, 63, 94, 0.3);
      font-size: 0.75rem;
      font-weight: 700;
      padding: 4px 14px;
      border-radius: 20px;
      margin-bottom: 14px;
      letter-spacing: 0.8px;
      text-transform: uppercase;
    }

    /* Card Photo */
    .photo-frame {
      width: 100%;
      height: 180px;
      border-radius: 16px;
      overflow: hidden;
      margin-bottom: 16px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
    }

    .photo-frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .card h2 {
      font-size: 1.3rem;
      color: #f8fafc;
      margin-bottom: 12px;
    }

    /* Collapsible Message Box */
    .message-box {
      max-height: 0;
      overflow: hidden;
      transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
      opacity: 0;
      background: rgba(15, 23, 42, 0.5);
      border-radius: 14px;
      padding: 0 14px;
      text-align: left;
      border: 1px solid rgba(255, 255, 255, 0.05);
    }

    .message-box.open {
      max-height: 250px;
      opacity: 1;
      padding: 16px 14px;
      margin-bottom: 16px;
    }

    .message-box p {
      color: #cbd5e1;
      font-size: 0.9rem;
      line-height: 1.6;
    }

    /* Buttons */
    .btn {
      background: linear-gradient(135deg, #f43f5e 0%, #e11d48 100%);
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 50px;
      font-weight: 600;
      font-size: 0.88rem;
      cursor: pointer;
      box-shadow: 0 6px 20px rgba(244, 63, 94, 0.35);
      transition: all 0.2s ease;
      width: 100%;
    }

    .btn:active {
      transform: scale(0.97);
    }

    /* Light Particles */
    .light-particle {
      position: absolute;
      background: #ffffff;
      border-radius: 50%;
      pointer-events: none;
      box-shadow: 0 0 10px #ffffff, 0 0 20px #fb7185;
      animation: floatUp 2s ease-out forwards;
    }

    @keyframes floatUp {
      0% { opacity: 1; transform: translateY(0) scale(1); }
      100% { opacity: 0; transform: translateY(-100px) scale(0.2); }
    }
  </style>
</head>
<body>

  <!-- Background Glows -->
  <div class="light-glow glow-1"></div>
  <div class="light-glow glow-2"></div>

  <!-- Header -->
  <div class="header-title">
    <h1>Happy Birthday! 🎉</h1>
    <p>Scroll ke bawah untuk melihat pesan ✨</p>
  </div>

  <!-- Cards Container -->
  <div class="cards-container">

    <!-- Card 1 -->
    <div class="card">
      <span class="card-step">Card 01</span>
      <div class="photo-frame">
        <!-- Ganti tautan gambar di bawah ini -->
        <img src="https://images.unsplash.com/photo-1513151233558-d860c5398176?w=500" alt="Momen 1">
      </div>
      <h2>Kenangan Pertama 📸</h2>
      <div class="message-box" id="msg1">
        <p>
          Terima kasih sudah menjadi sosok yang selalu membawa keceriaan. Setiap momen yang dihabiskan bersamamu selalu terasa seru dan berkesan! ✨
        </p>
      </div>
      <button class="btn" onclick="toggleCard(this, 'msg1', event)">Buka Pesan 💌</button>
    </div>

    <!-- Card 2 -->
    <div class="card">
      <span class="card-step">Card 02</span>
      <div class="photo-frame">
        <!-- Ganti tautan gambar di bawah ini -->
        <img src="https://images.unsplash.com/photo-1464349095431-e9a21285b5f3?w=500" alt="Momen 2">
      </div>
      <h2>Doa & Harapan 🌟</h2>
      <div class="message-box" id="msg2">
        <p>
          Semoga di usiamu yang baru ini, kamu semakin dekat dengan semua impianmu, selalu dikelilingi orang-orang baik, dan sehat selalu. 🤲🎂
        </p>
      </div>
      <button class="btn" onclick="toggleCard(this, 'msg2', event)">Buka Pesan 💌</button>
    </div>

    <!-- Card 3 -->
    <div class="card">
      <span class="card-step">Card 03</span>
      <div class="photo-frame">
        <!-- Ganti tautan gambar di bawah ini -->
        <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?w=500" alt="Momen 3">
      </div>
      <h2>Pesan Spesial 💖</h2>
      <div class="message-box" id="msg3">
        <p>
          <i>"Tetaplah tumbuh dan bersinar dengan caramu sendiri."</i><br><br>
          Sekali lagi, Selamat Ulang Tahun! Bahagia selalu ya! 🎉✨
        </p>
      </div>
      <button class="btn" onclick="toggleCard(this, 'msg3', event)">Buka Pesan 💌</button>
    </div>

  </div>

  <script>
    function toggleCard(btn, msgId, e) {
      const msg = document.getElementById(msgId);
      
      if (!msg.classList.contains('open')) {
        msg.classList.add('open');
        btn.innerText = 'Tutup Pesan ✨';
        createLightParticles(e);
      } else {
        msg.classList.remove('open');
        btn.innerText = 'Buka Pesan 💌';
      }
    }

    function createLightParticles(e) {
      for (let i = 0; i < 12; i++) {
        const particle = document.createElement('div');
        particle.classList.add('light-particle');
        
        const size = Math.random() * 5 + 4 + 'px';
        particle.style.width = size;
        particle.style.height = size;
        
        particle.style.left = (e.clientX + (Math.random() * 100 - 50)) + 'px';
        particle.style.top = (e.clientY + (Math.random() * 20 - 10)) + 'px';
        
        document.body.appendChild(particle);

        setTimeout(() => {
          particle.remove();
        }, 2000);
      }
    }
  </script>
</body>
</html>
