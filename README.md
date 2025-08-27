<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Ratthew – Brand Creator Coin</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f2f5;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    .card {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      display: inline-block;
      padding: 24px;
      max-width: 680px;
      margin-top: 40px;
      text-align: left;
    }
    .avatar {
      width: 120px;
      border-radius: 50%;
      display: block;
      margin: 0 auto;
    }
    h1, h2 {
      text-align: center;
      margin: 16px 0 8px;
    }
    .tagline {
      font-style: italic;
      color: #555;
      text-align: center;
      margin-bottom: 16px;
    }
    .stats {
      background: #fafafa;
      border-radius: 8px;
      padding: 16px;
      margin: 20px 0;
      font-size: 14px;
    }
    .stats div {
      margin-bottom: 8px;
    }
    .links {
      text-align: center;
      margin: 20px 0;
    }
    .links a {
      color: #007bff;
      margin: 0 8px;
      text-decoration: none;
    }
    .links a:hover {
      text-decoration: underline;
    }
    .about, .roadmap {
      margin: 24px 0;
    }
    .roadmap ul {
      list-style: none;
      padding: 0;
    }
    .roadmap li {
      background: #f9f9f9;
      margin: 8px 0;
      padding: 10px;
      border-left: 4px solid #007bff;
      border-radius: 6px;
    }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://zora.co/_next/image?url=%2Fratthew.png&w=128&q=75" alt="Ratthew Avatar" class="avatar">
    <h1>Ratthew</h1>
    <p class="tagline">“little rat big city swag life”</p>

    <!-- Live Stats -->
    <div class="stats" id="stats">
      <div><strong>Price:</strong> Loading...</div>
      <div><strong>24h Volume:</strong> Loading...</div>
      <div><strong>Liquidity:</strong> Loading...</div>
      <div><strong>Holders:</strong> Loading...</div>
    </div>

    <!-- Social Links -->
    <div class="links">
      <a href="https://zora.co/@ratthew" target="_blank">Zora Profile</a>
      <a href="https://t.me/ratthewportal" target="_blank">Telegram</a>
      <a href="https://x.com/zora" target="_blank">Twitter</a>
    </div>

    <!-- About Section -->
    <div class="about">
      <h2>About Ratthew</h2>
      <p>
        <strong>Ratthew</strong> is the first creator coin launched on 
        <a href="https://zora.co" target="_blank">Zora</a>. 
        More than just a token, Ratthew represents creativity, community, and culture. 
        With the tagline <em>“little rat big city swag life”</em>, the project blends humor, 
        art, and decentralized finance to build a unique creator economy on the 
        <strong>Base Network</strong>.
      </p>
    </div>

    <!-- Roadmap Section -->
    <div class="roadmap">
      <h2>Roadmap</h2>
      <ul>
        <li><strong>Phase 1 – Launch:</strong> Token creation, Zora profile, community building on Telegram.</li>
        <li><strong>Phase 2 – Growth:</strong> Listings on DEX tools (DexScreener, GeckoTerminal), expanding holders & liquidity.</li>
        <li><strong>Phase 3 – Ecosystem:</strong> Launch of Ratthew-inspired digital art, memes, and collaborations with creators.</li>
        <li><strong>Phase 4 – Utility:</strong> Integration into creator economy tools, staking features, and possible mini-games.</li>
        <li><strong>Phase 5 – Expansion:</strong> Partnerships, wider exposure, and development of Ratthew-branded experiences.</li>
      </ul>
    </div>
  </div>

  <script>
    async function fetchStats() {
      const statsEl = document.getElementById('stats');
      try {
        // DexScreener API for Ratthew token on Base
        const url = "https://api.dexscreener.com/latest/dex/tokens/0xCcB00Cb269a62dc0c2021c3D699A564e8A868f48";
        const res = await fetch(url);
        const data = await res.json();
        const pair = data.pairs[0]; // main trading pair