<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My House - Belajar Bahasa Inggris Kelas 4</title>
<link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;500;600;700&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #FF6B6B;
    --secondary: #4ECDC4;
    --accent: #FFE66D;
    --purple: #A78BFA;
    --blue: #60A5FA;
    --green: #34D399;
    --orange: #FB923C;
    --pink: #F472B6;
    --dark: #1E293B;
    --light: #F8FAFC;
    --shadow: 0 10px 25px rgba(0,0,0,0.15);
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Nunito', sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
    min-height: 100vh;
    overflow-x: hidden;
    color: var(--dark);
  }

  /* Floating decorations */
  .floating {
    position: fixed;
    pointer-events: none;
    z-index: 0;
    opacity: 0.3;
    animation: float 6s ease-in-out infinite;
  }
  .floating:nth-child(2) { animation-delay: 1s; }
  .floating:nth-child(3) { animation-delay: 2s; }
  .floating:nth-child(4) { animation-delay: 3s; }
  @keyframes float {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(5deg); }
  }

  .screen {
    display: none;
    min-height: 100vh;
    padding: 20px;
    position: relative;
    z-index: 1;
  }
  .screen.active {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  /* ===== WELCOME SCREEN ===== */
  #welcome {
    background: linear-gradient(160deg, #a8edea 0%, #fed6e3 50%, #d4fc79 100%);
  }
  .welcome-card {
    background: white;
    border-radius: 30px;
    padding: 40px 50px;
    box-shadow: var(--shadow);
    text-align: center;
    max-width: 520px;
    width: 100%;
    position: relative;
    animation: bounceIn 0.8s ease;
  }
  @keyframes bounceIn {
    0% { transform: scale(0.5); opacity: 0; }
    60% { transform: scale(1.05); }
    100% { transform: scale(1); opacity: 1; }
  }
  .mascot-container {
    width: 180px;
    height: 180px;
    margin: 0 auto 20px;
    border-radius: 50%;
    background: linear-gradient(145deg, #FFE66D, #FF9F43);
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 8px 20px rgba(255,159,67,0.4);
    overflow: hidden;
    border: 5px solid white;
  }
  .mascot-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  <img src="nama-file-mr-ken.png"> {
    font-size: 80px;
    line-height: 1;
  }
  h1 {
    font-family: 'Fredoka', sans-serif;
    font-size: 2.2rem;
    color: var(--primary);
    margin-bottom: 8px;
  }
  .subtitle {
    color: #64748b;
    font-size: 1.1rem;
    margin-bottom: 25px;
  }
  .input-group {
    margin-bottom: 18px;
    text-align: left;
  }
  .input-group label {
    display: block;
    font-weight: 700;
    margin-bottom: 6px;
    color: var(--dark);
    font-size: 0.95rem;
  }
  .input-group input, .input-group select {
    width: 100%;
    padding: 14px 18px;
    border: 3px solid #e2e8f0;
    border-radius: 16px;
    font-size: 1.1rem;
    font-family: 'Nunito', sans-serif;
    transition: all 0.3s;
    background: #f8fafc;
  }
  .input-group input:focus, .input-group select:focus {
    outline: none;
    border-color: var(--secondary);
    background: white;
    box-shadow: 0 0 0 4px rgba(78,205,196,0.2);
  }
  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 16px 36px;
    border: none;
    border-radius: 50px;
    font-family: 'Fredoka', sans-serif;
    font-size: 1.2rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 6px 0 rgba(0,0,0,0.15);
    position: relative;
    top: 0;
  }
  .btn:active {
    top: 4px;
    box-shadow: 0 2px 0 rgba(0,0,0,0.15);
  }
  .btn-primary {
    background: linear-gradient(135deg, #FF6B6B, #FF8E53);
    color: white;
  }
  .btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 0 rgba(0,0,0,0.15);
  }
  .btn-secondary {
    background: linear-gradient(135deg, #4ECDC4, #44A08D);
    color: white;
  }
  .btn-purple {
    background: linear-gradient(135deg, #A78BFA, #8B5CF6);
    color: white;
  }
  .btn-blue {
    background: linear-gradient(135deg, #60A5FA, #3B82F6);
    color: white;
  }
  .btn-green {
    background: linear-gradient(135deg, #34D399, #10B981);
    color: white;
  }
  .btn-orange {
    background: linear-gradient(135deg, #FB923C, #F97316);
    color: white;
  }
  .btn-sm {
    padding: 10px 22px;
    font-size: 1rem;
  }

  /* ===== HEADER ===== */
  .header {
    width: 100%;
    max-width: 900px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    background: white;
    padding: 12px 24px;
    border-radius: 20px;
    box-shadow: var(--shadow);
  }
  .student-info {
    font-weight: 700;
    color: var(--primary);
    font-size: 1.05rem;
  }
  .nav-btns {
    display: flex;
    gap: 10px;
  }

  /* ===== MENU SCREEN ===== */
  #menu {
    background: linear-gradient(160deg, #ffecd2 0%, #fcb69f 100%);
  }
  .menu-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    max-width: 800px;
    width: 100%;
  }
  .menu-card {
    background: white;
    border-radius: 24px;
    padding: 30px 20px;
    text-align: center;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: var(--shadow);
    border: 4px solid transparent;
  }
  .menu-card:hover {
    transform: translateY(-8px) scale(1.03);
    border-color: var(--accent);
  }
  .menu-icon {
    font-size: 3.5rem;
    margin-bottom: 12px;
  }
  .menu-card h3 {
    font-family: 'Fredoka', sans-serif;
    font-size: 1.3rem;
    margin-bottom: 6px;
  }
  .menu-card p {
    color: #64748b;
    font-size: 0.9rem;
  }

  /* ===== MATERI SCREEN ===== */
  #materi {
    background: linear-gradient(160deg, #e0c3fc 0%, #8ec5fc 100%);
  }
  .content-box {
    background: white;
    border-radius: 24px;
    padding: 30px;
    max-width: 900px;
    width: 100%;
    box-shadow: var(--shadow);
    max-height: 80vh;
    overflow-y: auto;
  }
  .section-title {
    font-family: 'Fredoka', sans-serif;
    font-size: 1.8rem;
    color: var(--primary);
    text-align: center;
    margin-bottom: 20px;
  }
  .rooms-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 16px;
    margin-bottom: 30px;
  }
  .room-card {
    background: linear-gradient(145deg, #f0f9ff, #e0f2fe);
    border-radius: 18px;
    padding: 18px 12px;
    text-align: center;
    border: 3px solid #bae6fd;
    transition: all 0.3s;
    cursor: pointer;
  }
  .room-card:hover {
    transform: scale(1.05);
    border-color: var(--blue);
    box-shadow: 0 8px 20px rgba(96,165,250,0.3);
  }
  .room-emoji {
    font-size: 2.8rem;
    margin-bottom: 8px;
  }
  .room-name {
    font-weight: 800;
    font-size: 1.05rem;
    color: var(--dark);
  }
  .room-indo {
    font-size: 0.85rem;
    color: #64748b;
  }

  .prep-section {
    background: linear-gradient(145deg, #fef3c7, #fde68a);
    border-radius: 20px;
    padding: 24px;
    margin-bottom: 24px;
  }
  .prep-title {
    font-family: 'Fredoka', sans-serif;
    font-size: 1.4rem;
    color: #b45309;
    margin-bottom: 16px;
    text-align: center;
  }
  .prep-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
  }
  .prep-item {
    background: white;
    border-radius: 14px;
    padding: 14px;
    display: flex;
    align-items: center;
    gap: 12px;
    border: 2px solid #fcd34d;
  }
  .prep-icon {
    font-size: 1.8rem;
    min-width: 40px;
    text-align: center;
  }
  .prep-text strong {
    color: #b45309;
    font-size: 1.05rem;
  }
  .prep-text span {
    display: block;
    font-size: 0.85rem;
    color: #78716c;
  }

  .example-box {
    background: linear-gradient(145deg, #d1fae5, #a7f3d0);
    border-radius: 20px;
    padding: 24px;
    margin-bottom: 20px;
  }
  .example-title {
    font-family: 'Fredoka', sans-serif;
    font-size: 1.3rem;
    color: #047857;
    margin-bottom: 14px;
    text-align: center;
  }
  .example-item {
    background: white;
    border-radius: 12px;
    padding: 12px 16px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 12px;
    border-left: 5px solid var(--green);
  }
  .example-item .en {
    font-weight: 700;
    color: var(--dark);
  }
  .example-item .id {
    font-size: 0.9rem;
    color: #64748b;
  }

  /* ===== GAME SCREEN ===== */
  #game {
    background: linear-gradient(160deg, #ff9a9e 0%, #fecfef 50%, #f6d365 100%);
  }
  .game-area {
    background: white;
    border-radius: 24px;
    padding: 30px;
    max-width: 800px;
    width: 100%;
    box-shadow: var(--shadow);
    text-align: center;
  }
  .game-question {
    font-family: 'Fredoka', sans-serif;
    font-size: 1.5rem;
    margin-bottom: 20px;
    color: var(--dark);
  }
  .game-image-box {
    background: linear-gradient(145deg, #e0f2fe, #bae6fd);
    border-radius: 20px;
    padding: 30px;
    margin-bottom: 24px;
    min-height: 180px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 4px dashed #38bdf8;
  }
  .game-scene {
    font-size: 3.2rem;
    margin-bottom: 10px;
    white-space: pre-line;
    line-height: 1.3;
    letter-spacing: 2px;
  }
  .game-options {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    max-width: 500px;
    margin: 0 auto;
  }
  .option-btn {
    padding: 16px;
    border: 3px solid #e2e8f0;
    border-radius: 16px;
    background: #f8fafc;
    font-family: 'Nunito', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.25s;
  }
  .option-btn:hover {
    border-color: var(--secondary);
    background: #e0f7f5;
    transform: scale(1.03);
  }
  .option-btn.correct {
    background: #d1fae5 !important;
    border-color: #10b981 !important;
    color: #065f46;
  }
  .option-btn.wrong {
    background: #fee2e2 !important;
    border-color: #ef4444 !important;
    color: #991b1b;
  }
  .score-badge {
    display: inline-block;
    background: var(--accent);
    color: var(--dark);
    padding: 8px 20px;
    border-radius: 50px;
    font-weight: 800;
    font-size: 1.1rem;
    margin-bottom: 16px;
  }
  .feedback {
    margin-top: 18px;
    font-size: 1.2rem;
    font-weight: 700;
    min-height: 30px;
  }
  .feedback.correct { color: #059669; }
  .feedback.wrong { color: #dc2626; }

  /* ===== QUIZ SCREEN ===== */
  #quiz {
    background: linear-gradient(160deg, #c3cfe2 0%, #f5f7fa 100%);
  }
  .quiz-progress {
    width: 100%;
    height: 12px;
    background: #e2e8f0;
    border-radius: 10px;
    margin-bottom: 20px;
    overflow: hidden;
  }
  .quiz-progress-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--secondary), var(--green));
    border-radius: 10px;
    transition: width 0.4s ease;
  }
  .quiz-number {
    font-weight: 700;
    color: #64748b;
    margin-bottom: 10px;
  }

  /* ===== RESULT SCREEN ===== */
  #result {
    background: linear-gradient(160deg, #f093fb 0%, #f5576c 100%);
  }
  .result-card {
    background: white;
    border-radius: 30px;
    padding: 40px;
    text-align: center;
    max-width: 500px;
    width: 100%;
    box-shadow: var(--shadow);
  }
  .result-emoji {
    font-size: 5rem;
    margin-bottom: 10px;
  }
  .result-score {
    font-family: 'Fredoka', sans-serif;
    font-size: 3rem;
    color: var(--primary);
  }
  .stars {
    font-size: 2.5rem;
    margin: 15px 0;
  }

  /* ===== HOUSE MAP GAME ===== */
  .house-map {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin: 20px 0;
  }
  .room-drop {
    background: #f1f5f9;
    border: 3px dashed #94a3b8;
    border-radius: 16px;
    padding: 20px;
    min-height: 100px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: all 0.3s;
  }
  .room-drop.highlight {
    border-color: var(--secondary);
    background: #ccfbf1;
  }
  .room-drop.correct-drop {
    border-color: #10b981;
    background: #d1fae5;
  }
  .drag-item {
    display: inline-block;
    background: white;
    border: 3px solid var(--purple);
    border-radius: 12px;
    padding: 10px 16px;
    margin: 6px;
    cursor: grab;
    font-weight: 700;
    transition: all 0.2s;
    user-select: none;
  }
  .drag-item:active {
    cursor: grabbing;
  }
  .drag-item.dragging {
    opacity: 0.5;
    transform: scale(1.1);
  }

  /* ===== SPEAK BUTTON ===== */
  .speak-btn {
    background: var(--blue);
    color: white;
    border: none;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    font-size: 1.2rem;
    cursor: pointer;
    margin-left: 8px;
    transition: all 0.2s;
  }
  .speak-btn:hover {
    transform: scale(1.1);
  }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 600px) {
    .welcome-card { padding: 30px 20px; }
    h1 { font-size: 1.7rem; }
    .menu-grid { grid-template-columns: 1fr 1fr; }
    .game-options { grid-template-columns: 1fr; }
    .rooms-grid { grid-template-columns: 1fr 1fr; }
    .header { flex-direction: column; gap: 10px; }
  }

  /* Confetti */
  .confetti {
    position: fixed;
    width: 10px;
    height: 10px;
    top: -10px;
    z-index: 9999;
    animation: confetti-fall 3s linear forwards;
  }
  @keyframes confetti-fall {
    to {
      transform: translateY(100vh) rotate(720deg);
      opacity: 0;
    }
  }
</style>
</head>
<body>

<!-- Floating decorations -->
<div class="floating" style="top:10%;left:5%;font-size:40px;">🏠</div>
<div class="floating" style="top:20%;right:8%;font-size:35px;">📚</div>
<div class="floating" style="bottom:15%;left:10%;font-size:30px;">✏️</div>
<div class="floating" style="bottom:25%;right:5%;font-size:38px;">🌟</div>

<!-- ===== WELCOME SCREEN ===== -->
<div id="welcome" class="screen active">
  <div class="welcome-card">
    <div class="mascot-container" id="mascotBox">
      <div class="mascot-placeholder">🧒</div>
    </div>
    <h1>🏠 My House Adventure</h1>
    <p class="subtitle">Belajar Bagian Rumah & Preposisi Bahasa Inggris<br>Kelas 4 • Kurikulum Merdeka • Semester 1</p>
    
    <div class="input-group">
      <label>👤 Nama Siswa</label>
      <input type="text" id="studentName" placeholder="Ketik namamu di sini..." maxlength="30">
    </div>
    <div class="input-group">
      <label>🏫 Kelas</label>
      <select id="studentClass">
        <option value="">Pilih Kelas</option>
        <option value="4 A">4 A</option>
        <option value="4 B">4 B</option>
      </select>
    </div>
    <button class="btn btn-primary" onclick="startLearning()" style="margin-top:10px;width:100%;">
      🚀 Mulai Belajar!
    </button>
    <p style="margin-top:18px;font-size:0.9rem;color:#94a3b8;">Bersama Mr. Ken 🧒</p>
  </div>
</div>

<!-- ===== MENU SCREEN ===== -->
<div id="menu" class="screen">
  <div class="header">
    <div class="student-info">👋 Halo, <span id="displayName">Siswa</span>!</div>
    <div class="nav-btns">
      <button class="btn btn-sm btn-orange" onclick="showScreen('welcome')">🏠 Beranda</button>
    </div>
  </div>
  <h2 class="section-title" style="color:white;text-shadow:2px 2px 4px rgba(0,0,0,0.2);">Pilih Kegiatan Belajar</h2>
  <div class="menu-grid">
    <div class="menu-card" onclick="showScreen('materi')">
      <div class="menu-icon">📖</div>
      <h3>Materi</h3>
      <p>Belajar bagian rumah & preposisi</p>
    </div>
    <div class="menu-card" onclick="startGame1()">
      <div class="menu-icon">🎮</div>
      <h3>Game 1</h3>
      <p>Pilih preposisi yang tepat</p>
    </div>
    <div class="menu-card" onclick="startGame2()">
      <div class="menu-icon">🧩</div>
      <h3>Game 2</h3>
      <p>Pasangkan benda ke ruangan</p>
    </div>
    <div class="menu-card" onclick="startQuiz()">
      <div class="menu-icon">📝</div>
      <h3>Kuis</h3>
      <p>Uji kemampuanmu!</p>
    </div>
  </div>
</div>

<!-- ===== MATERI SCREEN ===== -->
<div id="materi" class="screen">
  <div class="header">
    <div class="student-info">📖 Materi Belajar</div>
    <div class="nav-btns">
      <button class="btn btn-sm btn-secondary" onclick="showScreen('menu')">⬅️ Menu</button>
    </div>
  </div>
  <div class="content-box">
    <h2 class="section-title">🏠 Parts of the House</h2>
    <p style="text-align:center;margin-bottom:20px;color:#64748b;">Klik kartu untuk mendengar pengucapan!</p>
    
    <div class="rooms-grid" id="roomsGrid">
      <!-- filled by JS -->
    </div>

    <div class="prep-section">
      <h3 class="prep-title">📍 Prepositions of Place (Kata Keterangan Tempat)</h3>
      <div class="prep-grid">
        <div class="prep-item">
          <div class="prep-icon">📦</div>
          <div class="prep-text"><strong>in</strong><span>di dalam</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">🔝</div>
          <div class="prep-text"><strong>on</strong><span>di atas (menempel)</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">⬇️</div>
          <div class="prep-text"><strong>under</strong><span>di bawah</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">➡️</div>
          <div class="prep-text"><strong>next to / beside</strong><span>di samping</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">⬅️</div>
          <div class="prep-text"><strong>behind</strong><span>di belakang</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">👤</div>
          <div class="prep-text"><strong>in front of</strong><span>di depan</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">↔️</div>
          <div class="prep-text"><strong>between</strong><span>di antara</span></div>
        </div>
        <div class="prep-item">
          <div class="prep-icon">⬆️</div>
          <div class="prep-text"><strong>above</strong><span>di atas (tidak menempel)</span></div>
        </div>
      </div>
    </div>

    <div class="example-box">
      <h3 class="example-title">💬 Contoh Kalimat</h3>
      <div class="example-item">
        <span style="font-size:1.5rem;">🛏️</span>
        <div>
          <div class="en">The bed is <strong>in</strong> the bedroom.</div>
          <div class="id">Tempat tidur ada di dalam kamar tidur.</div>
        </div>
      </div>
      <div class="example-item">
        <span style="font-size:1.5rem;">🪴</span>
        <div>
          <div class="en">The flower is <strong>on</strong> the table.</div>
          <div class="id">Bunga ada di atas meja.</div>
        </div>
      </div>
      <div class="example-item">
        <span style="font-size:1.5rem;">🐱</span>
        <div>
          <div class="en">The cat is <strong>under</strong> the chair.</div>
          <div class="id">Kucing ada di bawah kursi.</div>
        </div>
      </div>
      <div class="example-item">
        <span style="font-size:1.5rem;">📺</span>
        <div>
          <div class="en">The TV is <strong>next to</strong> the sofa.</div>
          <div class="id">TV ada di samping sofa.</div>
        </div>
      </div>
      <div class="example-item">
        <span style="font-size:1.5rem;">🌳</span>
        <div>
          <div class="en">The tree is <strong>behind</strong> the house.</div>
          <div class="id">Pohon ada di belakang rumah.</div>
        </div>
      </div>
      <div class="example-item">
        <span style="font-size:1.5rem;">🚪</span>
        <div>
          <div class="en">The car is <strong>in front of</strong> the garage.</div>
          <div class="id">Mobil ada di depan garasi.</div>
        </div>
      </div>
    </div>

    <div style="text-align:center;margin-top:20px;">
      <button class="btn btn-green" onclick="startGame1()">🎮 Main Game Sekarang!</button>
    </div>
  </div>
</div>

<!-- ===== GAME 1 SCREEN ===== -->
<div id="game" class="screen">
  <div class="header">
    <div class="student-info">🎮 Game Preposisi</div>
    <div class="nav-btns">
      <button class="btn btn-sm btn-secondary" onclick="showScreen('menu')">⬅️ Menu</button>
    </div>
  </div>
  <div class="game-area">
    <div class="score-badge">⭐ Skor: <span id="gameScore">0</span> / <span id="gameTotal">0</span></div>
    <div class="game-question" id="gameQuestion">Pilih preposisi yang tepat!</div>
    <div class="game-image-box">
      <div class="game-scene" id="gameScene">🏠</div>
      <div id="gameDesc" style="font-size:1.1rem;font-weight:600;color:#0369a1;"></div>
    </div>
    <div class="game-options" id="gameOptions"></div>
    <div class="feedback" id="gameFeedback"></div>
    <div style="margin-top:20px;">
      <button class="btn btn-primary btn-sm" id="nextGameBtn" onclick="nextGameQuestion()" style="display:none;">Soal Berikutnya ➡️</button>
    </div>
  </div>
</div>

<!-- ===== GAME 2 SCREEN ===== -->
<div id="game2" class="screen">
  <div class="header">
    <div class="student-info">🧩 Pasangkan Benda</div>
    <div class="nav-btns">
      <button class="btn btn-sm btn-secondary" onclick="showScreen('menu')">⬅️ Menu</button>
    </div>
  </div>
  <div class="game-area">
    <div class="score-badge">⭐ Benar: <span id="matchScore">0</span></div>
    <div class="game-question">Seret benda ke ruangan yang tepat!</div>
    <div id="dragItems" style="margin:15px 0;min-height:50px;"></div>
    <div class="house-map" id="houseMap"></div>
    <div class="feedback" id="matchFeedback"></div>
    <div style="margin-top:15px;">
      <button class="btn btn-green btn-sm" onclick="checkMatching()">✅ Cek Jawaban</button>
      <button class="btn btn-orange btn-sm" onclick="resetMatching()" style="margin-left:8px;">🔄 Ulangi</button>
    </div>
  </div>
</div>

<!-- ===== QUIZ SCREEN ===== -->
<div id="quiz" class="screen">
  <div class="header">
    <div class="student-info">📝 Kuis</div>
    <div class="nav-btns">
      <button class="btn btn-sm btn-secondary" onclick="showScreen('menu')">⬅️ Menu</button>
    </div>
  </div>
  <div class="game-area">
    <div class="quiz-progress"><div class="quiz-progress-bar" id="quizBar" style="width:0%"></div></div>
    <div class="quiz-number" id="quizNumber">Soal 1 dari 8</div>
    <div class="score-badge">⭐ Skor: <span id="quizScore">0</span></div>
    <div class="game-question" id="quizQuestion">...</div>
    <div class="game-image-box" id="quizImageBox">
      <div class="game-scene" id="quizScene">🏠</div>
    </div>
    <div class="game-options" id="quizOptions"></div>
    <div class="feedback" id="quizFeedback"></div>
    <div style="margin-top:20px;">
      <button class="btn btn-primary btn-sm" id="nextQuizBtn" onclick="nextQuizQuestion()" style="display:none;">Soal Berikutnya ➡️</button>
    </div>
  </div>
</div>

<!-- ===== RESULT SCREEN ===== -->
<div id="result" class="screen">
  <div class="result-card">
    <div class="result-emoji" id="resultEmoji">🎉</div>
    <h2 class="section-title" id="resultTitle">Hebat!</h2>
    <div class="result-score" id="resultScore">0/8</div>
    <div class="stars" id="resultStars">⭐⭐⭐</div>
    <p id="resultMessage" style="margin:15px 0;color:#64748b;font-size:1.1rem;"></p>
    <button class="btn btn-primary" onclick="showScreen('menu')" style="margin-top:10px;">🏠 Kembali ke Menu</button>
    <button class="btn btn-green" onclick="startQuiz()" style="margin-top:12px;margin-left:8px;">🔄 Coba Lagi</button>
  </div>
</div>

<script>
// ===== DATA =====
const rooms = [
  { name: "Living Room", indo: "Ruang Tamu", emoji: "🛋️", speak: "living room" },
  { name: "Bedroom", indo: "Kamar Tidur", emoji: "🛏️", speak: "bedroom" },
  { name: "Kitchen", indo: "Dapur", emoji: "🍳", speak: "kitchen" },
  { name: "Bathroom", indo: "Kamar Mandi", emoji: "🚿", speak: "bathroom" },
  { name: "Dining Room", indo: "Ruang Makan", emoji: "🍽️", speak: "dining room" },
  { name: "Garage", indo: "Garasi", emoji: "🚗", speak: "garage" },
  { name: "Garden", indo: "Taman", emoji: "🌳", speak: "garden" },
  { name: "Study Room", indo: "Ruang Belajar", emoji: "📚", speak: "study room" }
];

const game1Questions = [
  {
    scene: "🐱  ⬇️  🪑",
    desc: "The cat is _____ the chair.",
    options: ["on", "under", "behind", "between"],
    answer: "under",
    explain: "Kucing ada di bawah kursi → under"
  },
  {
    scene: "🌺\ndi atas\n🪑",
    desc: "The flower is _____ the table.",
    options: ["in", "on", "under", "behind"],
    answer: "on",
    explain: "Bunga ada di atas meja → on"
  },
  {
    scene: "📺   ↔️   🛋️",
    desc: "The TV is _____ the sofa.",
    options: ["in", "under", "next to", "above"],
    answer: "next to",
    explain: "TV ada di samping sofa → next to"
  },
  {
    scene: "🛏️   di dalam   🚪",
    desc: "The bed is _____ the bedroom.",
    options: ["on", "in", "under", "behind"],
    answer: "in",
    explain: "Tempat tidur ada di dalam kamar tidur → in"
  },
  {
    scene: "🏠   🌳 di belakang",
    desc: "The tree is _____ the house.",
    options: ["in front of", "behind", "on", "under"],
    answer: "behind",
    explain: "Pohon ada di belakang rumah → behind"
  },
  {
    scene: "🚗   di depan   🏠",
    desc: "The car is _____ the garage.",
    options: ["behind", "under", "in front of", "between"],
    answer: "in front of",
    explain: "Mobil ada di depan garasi → in front of"
  },
  {
    scene: "📚   🪑   📚",
    desc: "The chair is _____ the two bookshelves.",
    options: ["on", "under", "between", "behind"],
    answer: "between",
    explain: "Kursi ada di antara dua rak buku → between"
  },
  {
    scene: "💡   ⬆️   🛏️",
    desc: "The lamp is _____ the bed.",
    options: ["under", "above", "in", "behind"],
    answer: "above",
    explain: "Lampu ada di atas tempat tidur → above"
  }
];

const quizQuestions = [
  {
    q: "What room is this?",
    options: ["Bedroom", "Kitchen", "Bathroom", "Garage"],
    answer: "Kitchen",
    scene: "🍳 🍲 🥘"
  },
  {
    q: "The sofa is usually in the _____.",
    options: ["Bathroom", "Kitchen", "Living Room", "Garage"],
    answer: "Living Room",
    scene: "🛋️ 📺 🪴"
  },
  {
    q: "Look at the picture. Choose the correct sentence.",
    options: [
      "The book is on the table.",
      "The book is in the table.",
      "The book is under the table.",
      "The book is behind the table."
    ],
    answer: "The book is on the table.",
    scene: "📖\ndi atas\n🪑"
  },
  {
    q: "Where do we take a bath?",
    options: ["Kitchen", "Bedroom", "Bathroom", "Garden"],
    answer: "Bathroom",
    scene: "🚿 🛁 🧼"
  },
  {
    q: "The cat is _____ the table. (di bawah meja)",
    options: ["on", "in", "under", "next to"],
    answer: "under",
    scene: "🐱  ⬇️  🪑"
  },
  {
    q: "Which preposition means 'di samping'?",
    options: ["behind", "next to", "under", "above"],
    answer: "next to",
    scene: "📺  ↔️  🛋️"
  },
  {
    q: "The car is in the _____.",
    options: ["Kitchen", "Bedroom", "Garage", "Bathroom"],
    answer: "Garage",
    scene: "🚗  🏠🚪"
  },
  {
    q: "The picture is _____ the wall. (menempel di dinding)",
    options: ["under", "in", "on", "between"],
    answer: "on",
    scene: "🖼️  ⬇️  🧱"
  }
];

const matchItems = [
  { id: "bed", emoji: "🛏️", name: "Bed", room: "bedroom" },
  { id: "sofa", emoji: "🛋️", name: "Sofa", room: "living" },
  { id: "stove", emoji: "🍳", name: "Stove", room: "kitchen" },
  { id: "toilet", emoji: "🚽", name: "Toilet", room: "bathroom" },
  { id: "car", emoji: "🚗", name: "Car", room: "garage" },
  { id: "tree", emoji: "🌳", name: "Tree", room: "garden" }
];

const matchRooms = [
  { id: "living", name: "Living Room", emoji: "🛋️" },
  { id: "bedroom", name: "Bedroom", emoji: "🛏️" },
  { id: "kitchen", name: "Kitchen", emoji: "🍳" },
  { id: "bathroom", name: "Bathroom", emoji: "🚿" },
  { id: "garage", name: "Garage", emoji: "🚗" },
  { id: "garden", name: "Garden", emoji: "🌳" }
];

// ===== STATE =====
let studentName = "";
let studentClass = "";
let game1Index = 0;
let game1Score = 0;
let quizIndex = 0;
let quizScore = 0;
let answered = false;

// ===== AUDIO =====
const audioCtx = new (window.AudioContext || window.webkitAudioContext)();

function playCorrect() {
  // Happy ascending tones
  [523.25, 659.25, 783.99].forEach((freq, i) => {
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.connect(gain);
    gain.connect(audioCtx.destination);
    osc.frequency.value = freq;
    osc.type = "sine";
    gain.gain.setValueAtTime(0.3, audioCtx.currentTime + i * 0.12);
    gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + i * 0.12 + 0.3);
    osc.start(audioCtx.currentTime + i * 0.12);
    osc.stop(audioCtx.currentTime + i * 0.12 + 0.3);
  });
}

function playWrong() {
  // Descending buzz
  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.connect(gain);
  gain.connect(audioCtx.destination);
  osc.frequency.setValueAtTime(300, audioCtx.currentTime);
  osc.frequency.exponentialRampToValueAtTime(100, audioCtx.currentTime + 0.4);
  osc.type = "sawtooth";
  gain.gain.setValueAtTime(0.2, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.4);
  osc.start();
  osc.stop(audioCtx.currentTime + 0.4);
}

function playClick() {
  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.connect(gain);
  gain.connect(audioCtx.destination);
  osc.frequency.value = 800;
  osc.type = "sine";
  gain.gain.setValueAtTime(0.15, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.08);
  osc.start();
  osc.stop(audioCtx.currentTime + 0.08);
}

function speak(text) {
  if ('speechSynthesis' in window) {
    const u = new SpeechSynthesisUtterance(text);
    u.lang = 'en-US';
    u.rate = 0.85;
    speechSynthesis.cancel();
    speechSynthesis.speak(u);
  }
}

// ===== NAVIGATION =====
function showScreen(id) {
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  playClick();
}

function startLearning() {
  const name = document.getElementById('studentName').value.trim();
  const cls = document.getElementById('studentClass').value;
  if (!name) {
    alert('Masukkan namamu dulu ya! 😊');
    return;
  }
  if (!cls) {
    alert('Pilih kelasmu dulu ya! 🏫');
    return;
  }
  studentName = name;
  studentClass = cls;
  document.getElementById('displayName').textContent = name + ' (' + cls + ')';
  showScreen('menu');
}

// ===== MATERI =====
function renderRooms() {
  const grid = document.getElementById('roomsGrid');
  grid.innerHTML = rooms.map(r => `
    <div class="room-card" onclick="speak('${r.speak}')">
      <div class="room-emoji">${r.emoji}</div>
      <div class="room-name">${r.name}</div>
      <div class="room-indo">${r.indo}</div>
    </div>
  `).join('');
}

// ===== GAME 1 =====
function startGame1() {
  game1Index = 0;
  game1Score = 0;
  answered = false;
  document.getElementById('gameScore').textContent = '0';
  document.getElementById('gameTotal').textContent = game1Questions.length;
  showScreen('game');
  loadGame1Question();
}

function loadGame1Question() {
  answered = false;
  const q = game1Questions[game1Index];
  document.getElementById('gameQuestion').textContent = 'Pilih preposisi yang tepat!';
  document.getElementById('gameScene').textContent = q.scene;
  document.getElementById('gameDesc').textContent = q.desc;
  document.getElementById('gameFeedback').textContent = '';
  document.getElementById('gameFeedback').className = 'feedback';
  document.getElementById('nextGameBtn').style.display = 'none';
  
  const opts = document.getElementById('gameOptions');
  opts.innerHTML = q.options.map(o => 
    `<button class="option-btn" onclick="checkGame1('${o}')">${o}</button>`
  ).join('');
}

function checkGame1(selected) {
  if (answered) return;
  answered = true;
  const q = game1Questions[game1Index];
  const btns = document.querySelectorAll('#gameOptions .option-btn');
  btns.forEach(b => {
    b.disabled = true;
    if (b.textContent === q.answer) b.classList.add('correct');
    if (b.textContent === selected && selected !== q.answer) b.classList.add('wrong');
  });
  
  const fb = document.getElementById('gameFeedback');
  if (selected === q.answer) {
    game1Score++;
    document.getElementById('gameScore').textContent = game1Score;
    fb.textContent = '✅ Benar! ' + q.explain;
    fb.className = 'feedback correct';
    playCorrect();
  } else {
    fb.textContent = '❌ Salah. Jawaban: ' + q.answer + '. ' + q.explain;
    fb.className = 'feedback wrong';
    playWrong();
  }
  document.getElementById('nextGameBtn').style.display = 'inline-flex';
}

function nextGameQuestion() {
  game1Index++;
  if (game1Index >= game1Questions.length) {
    // Show mini result
    alert(`🎉 Game selesai!\nSkor kamu: ${game1Score}/${game1Questions.length}\nHebat, ${studentName}!`);
    showScreen('menu');
  } else {
    loadGame1Question();
  }
}

// ===== GAME 2: MATCHING =====
function startGame2() {
  document.getElementById('matchScore').textContent = '0';
  document.getElementById('matchFeedback').textContent = '';
  showScreen('game2');
  renderMatching();
}

function renderMatching() {
  // Shuffle items
  const items = [...matchItems].sort(() => Math.random() - 0.5);
  const dragArea = document.getElementById('dragItems');
  dragArea.innerHTML = items.map(item => 
    `<div class="drag-item" draggable="true" data-id="${item.id}" data-room="${item.room}" id="drag-${item.id}">
      ${item.emoji} ${item.name}
    </div>`
  ).join('');

  const map = document.getElementById('houseMap');
  map.innerHTML = matchRooms.map(r => 
    `<div class="room-drop" data-room="${r.id}" id="drop-${r.id}" ondragover="allowDrop(event)" ondrop="dropItem(event)" ondragleave="dragLeave(event)">
      <div style="font-size:1.8rem">${r.emoji}</div>
      <div style="font-weight:700;font-size:0.9rem">${r.name}</div>
    </div>`
  ).join('');

  // Drag events
  document.querySelectorAll('.drag-item').forEach(el => {
    el.addEventListener('dragstart', e => {
      e.dataTransfer.setData('text/plain', el.dataset.id);
      el.classList.add('dragging');
    });
    el.addEventListener('dragend', e => el.classList.remove('dragging'));
  });
}

function allowDrop(e) {
  e.preventDefault();
  e.currentTarget.classList.add('highlight');
}
function dragLeave(e) {
  e.currentTarget.classList.remove('highlight');
}
function dropItem(e) {
  e.preventDefault();
  e.currentTarget.classList.remove('highlight');
  const id = e.dataTransfer.getData('text/plain');
  const item = document.getElementById('drag-' + id);
  if (item && !e.currentTarget.querySelector('.drag-item')) {
    e.currentTarget.appendChild(item);
  }
}

function checkMatching() {
  let correct = 0;
  matchRooms.forEach(r => {
    const drop = document.getElementById('drop-' + r.id);
    const item = drop.querySelector('.drag-item');
    if (item && item.dataset.room === r.id) {
      correct++;
      drop.classList.add('correct-drop');
    } else {
      drop.classList.remove('correct-drop');
    }
  });
  document.getElementById('matchScore').textContent = correct;
  const fb = document.getElementById('matchFeedback');
  if (correct === matchItems.length) {
    fb.textContent = '🎉 Sempurna! Semua benar!';
    fb.className = 'feedback correct';
    playCorrect();
    confetti();
  } else {
    fb.textContent = `Kamu benar ${correct} dari ${matchItems.length}. Coba lagi ya!`;
    fb.className = 'feedback wrong';
    playWrong();
  }
}

function resetMatching() {
  renderMatching();
  document.getElementById('matchScore').textContent = '0';
  document.getElementById('matchFeedback').textContent = '';
}

// ===== QUIZ =====
function startQuiz() {
  quizIndex = 0;
  quizScore = 0;
  answered = false;
  document.getElementById('quizScore').textContent = '0';
  showScreen('quiz');
  loadQuizQuestion();
}

function loadQuizQuestion() {
  answered = false;
  const q = quizQuestions[quizIndex];
  document.getElementById('quizNumber').textContent = `Soal ${quizIndex + 1} dari ${quizQuestions.length}`;
  document.getElementById('quizBar').style.width = ((quizIndex) / quizQuestions.length * 100) + '%';
  document.getElementById('quizQuestion').textContent = q.q;
  document.getElementById('quizScene').textContent = q.scene;
  document.getElementById('quizFeedback').textContent = '';
  document.getElementById('quizFeedback').className = 'feedback';
  document.getElementById('nextQuizBtn').style.display = 'none';
  
  const opts = document.getElementById('quizOptions');
  // Shuffle options
  const shuffled = [...q.options].sort(() => Math.random() - 0.5);
  opts.innerHTML = shuffled.map(o => 
    `<button class="option-btn" onclick="checkQuiz('${o.replace(/'/g, "\\'")}')">${o}</button>`
  ).join('');
}

function checkQuiz(selected) {
  if (answered) return;
  answered = true;
  const q = quizQuestions[quizIndex];
  const btns = document.querySelectorAll('#quizOptions .option-btn');
  btns.forEach(b => {
    b.disabled = true;
    if (b.textContent === q.answer) b.classList.add('correct');
    if (b.textContent === selected && selected !== q.answer) b.classList.add('wrong');
  });
  
  const fb = document.getElementById('quizFeedback');
  if (selected === q.answer) {
    quizScore++;
    document.getElementById('quizScore').textContent = quizScore;
    fb.textContent = '✅ Benar sekali!';
    fb.className = 'feedback correct';
    playCorrect();
  } else {
    fb.textContent = '❌ Salah. Jawaban yang benar: ' + q.answer;
    fb.className = 'feedback wrong';
    playWrong();
  }
  document.getElementById('nextQuizBtn').style.display = 'inline-flex';
  document.getElementById('quizBar').style.width = ((quizIndex + 1) / quizQuestions.length * 100) + '%';
}

function nextQuizQuestion() {
  quizIndex++;
  if (quizIndex >= quizQuestions.length) {
    showResult();
  } else {
    loadQuizQuestion();
  }
}

function showResult() {
  const total = quizQuestions.length;
  const pct = Math.round(quizScore / total * 100);
  document.getElementById('resultScore').textContent = `${quizScore}/${total}`;
  
  let emoji, title, stars, msg;
  if (pct >= 90) {
    emoji = '🏆'; title = 'Luar Biasa!'; stars = '⭐⭐⭐';
    msg = `Hebat ${studentName}! Kamu menguasai materi dengan sangat baik!`;
  } else if (pct >= 70) {
    emoji = '🎉'; title = 'Bagus!'; stars = '⭐⭐';
    msg = `Bagus ${studentName}! Terus berlatih ya!`;
  } else if (pct >= 50) {
    emoji = '💪'; title = 'Cukup Baik!'; stars = '⭐';
    msg = `Semangat ${studentName}! Pelajari lagi materinya ya!`;
  } else {
    emoji = '📚'; title = 'Ayo Belajar Lagi!'; stars = '🌱';
    msg = `Jangan menyerah ${studentName}! Coba ulangi materinya dulu.`;
  }
  document.getElementById('resultEmoji').textContent = emoji;
  document.getElementById('resultTitle').textContent = title;
  document.getElementById('resultStars').textContent = stars;
  document.getElementById('resultMessage').textContent = msg;
  
  if (pct >= 70) confetti();
  showScreen('result');
}

// ===== CONFETTI =====
function confetti() {
  const colors = ['#FF6B6B', '#4ECDC4', '#FFE66D', '#A78BFA', '#60A5FA', '#F472B6'];
  for (let i = 0; i < 50; i++) {
    setTimeout(() => {
      const el = document.createElement('div');
      el.className = 'confetti';
      el.style.left = Math.random() * 100 + 'vw';
      el.style.background = colors[Math.floor(Math.random() * colors.length)];
      el.style.borderRadius = Math.random() > 0.5 ? '50%' : '0';
      el.style.width = (Math.random() * 12 + 6) + 'px';
      el.style.height = el.style.width;
      document.body.appendChild(el);
      setTimeout(() => el.remove(), 3000);
    }, i * 40);
  }
}

// ===== INIT =====
renderRooms();
</script>
</body>
</html>

