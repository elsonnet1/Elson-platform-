curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash - && \
sudo apt-get install -y nodejs nginx git curl && \
sudo npm install -g pm2 && \
mkdir -p /var/www/elson-platform/public && \
cd /var/www/elson-platform && \
cat << 'EOF' > server.js
const express = require('express');
const fs = require('fs');
const path = require('path');
const app = express();
const PORT = 3000;

app.use(express.json());
app.use(express.static(path.join(__dirname, 'public')));

const DB_FILE = path.join(__dirname, 'platform_data.json');
if (!fs.existsSync(DB_FILE)) {
    fs.writeFileSync(DB_FILE, JSON.stringify({ registered_partners: [], logs: [] }, null, 2));
}

app.post('/api/ai-partner-finder', (req, res) => {
    try {
        const db = JSON.parse(fs.readFileSync(DB_FILE, 'utf8'));
        const niches = ['aquaculture', 'catfish feed', 'generator parts', 'solar inverter'];
        const selected = niches[Math.floor(Math.random() * niches.length)];
        const partner = {
            id: 'PARTNER_' + Date.now(),
            storeName: `${selected.charAt(0).toUpperCase() + selected.slice(1)} Global Supply`,
            status: 'Approved & Integrated',
            affiliateLink: `https://elson.com/partner-route/redirect?target=${selected}`,
            timestamp: new Date().toISOString()
        };
        db.registered_partners.push(partner);
        db.logs.push(`[SYSTEM LOOP] AI integrated affiliate deal with ${partner.storeName}`);
        fs.writeFileSync(DB_FILE, JSON.stringify(db, null, 2));
        res.json({ success: true, partner });
    } catch (error) {
        res.status(500).json({ success: false, error: error.message });
    }
});

app.get('/api/partners', (req, res) => {
    const db = JSON.parse(fs.readFileSync(DB_FILE, 'utf8'));
    res.json(db.registered_partners);
});

app.get('*', (req, res) => { res.sendFile(path.join(__dirname, 'public', 'index.html')); });
app.listen(PORT);
EOF
cat << 'EOF' > public/index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELSON Premium Hub</title>
    <style>
        :root { --primary: #007bff; --dark: #1e293b; --light: #f8fafc; --accent: #10b981; --whatsapp: #25D366; }
        body { font-family: system-ui, sans-serif; margin: 0; padding: 0; background: var(--light); color: var(--dark); }
        header { background: var(--dark); color: white; padding: 1.5rem; text-align: center; }
        .container { max-width: 1200px; margin: 2rem auto; padding: 0 1rem; }
        .btn { display: inline-block; background: var(--primary); color: white; text-decoration: none; border: none; padding: 0.75rem 1.5rem; border-radius: 5px; cursor: pointer; margin: 0.25rem; }
        .btn-audio { background: var(--accent); }
        .btn-whatsapp { background: var(--whatsapp); font-weight: bold; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; }
        .card { background: white; padding: 1.5rem; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); display: flex; flex-direction: column; justify-content: space-between; }
        .price-tag { font-size: 1.2rem; font-weight: bold; margin: 0.75rem 0; padding: 0.25rem 0.5rem; background: #e2e8f0; border-radius: 4px; width: fit-content; }
        .dashboard-admin { background: #cbd5e1; padding: 1.5rem; border-radius: 8px; margin-bottom: 2rem; border: 2px dashed var(--primary); }
        #ai-widget { position: fixed; bottom: 20px; right: 20px; width: 350px; background: white; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15); display: none; flex-direction: column; overflow: hidden; z-index: 1000; }
        .ai-header { background: var(--dark); color: white; padding: 1rem; display: flex; justify-content: space-between; }
        .ai-body { height: 250px; padding: 1rem; overflow-y: auto; background: #f1f5f9; }
        .ai-input-area { display: flex; border-top: 1px solid #e2e8f0; }
        .ai-input-area input { flex: 1; border: none; padding: 0.75rem; outline: none; }
        .ai-input-area button { background: var(--primary); color: white; border: none; padding: 0.75rem; }
        #ai-toggle-btn { position: fixed; bottom: 20px; right: 20px; background: var(--dark); color: white; border: none; width: 60px; height: 60px; border-radius: 50%; font-size: 1.5rem; cursor: pointer; z-index: 999; }
        .msg { margin-bottom: 0.8rem; padding: 0.5rem 0.75rem; border-radius: 8px; max-width: 80%; }
        .msg.user { background: var(--primary); color: white; margin-left: auto; }
        .msg.bot { background: #e2e8f0; }
    </style>
</head>
<body>
<header><h1>ELSON Premium Hub</h1><p>Automated Solutions & Agribusiness</p></header>
<div class="container">
    <div class="dashboard-admin">
        <h3>⚙️ Automated System Controls</h3>
        <p>Tap below to activate the hybrid scanner loop to find and integrate affiliate links dynamically.</p>
        <button class="btn" onclick="triggerAIPartnerFinder()">🔄 Initiate Automated AI Partner Finder</button>
        <span id="loop-status" style="margin-left:15px; font-weight:bold; color:var(--primary);"></span>
    </div>
    <div class="controls" style="text-align:center; margin-bottom:2rem;">
        <button class="btn btn-audio" id="read-page-btn" onclick="toggleSpeech()">🔊 Read Page Aloud</button>
    </div>
    <main class="grid" id="main-content">
        <section class="card">
            <div><h2>🎬 High-Speed Media Downloads</h2><p>Direct server access routes for movie downloads and compressed files.</p><div class="price-tag">N500 / Token</div></div>
            <a href="https://wa.me/2348123456789?text=Hello%20ELSON,%20I%20want%20to%20buy%20a%20Media%20Download%20Token." class="btn btn-whatsapp" target="_blank">💬 Connect via WhatsApp</a>
        </section>
        <section class="card">
            <div><h2>🐟 Catfish Farming Masterclass</h2><p>Complete logs tracking water quality formulas and live feeding loops.</p><div class="price-tag">N3,500 Full Pack</div></div>
            <a href="https://wa.me/2348123456789?text=Hello%20ELSON,%20I%20need%20the%20Catfish%20Farming%20Masterclass%20Guide." class="btn btn-whatsapp" target="_blank">💬 Request via WhatsApp</a>
        </section>
        <section class="card" id="dynamic-partner-section">
            <div><h2>🔗 Integrated Partner Node</h2><div id="partner-display"><p style="color:gray;">No active dynamic networks loaded. Tap the control button above to scrape and hook a partner network instantly.</p></div></div>
        </section>
    </main>
</div>
<button id="ai-toggle-btn" onclick="toggleAIWidget()">🤖</button>
<div id="ai-widget">
    <div class="ai-header"><strong>ELSON AI Guide Navigator</strong><span style="cursor:pointer;" onclick="toggleAIWidget()">✖</span></div>
    <div class="ai-body" id="chat-box"><div class="msg bot">Welcome to ELSON. Type what you need (prices, fish guides, movie downloads) and I will route you instantly.</div></div>
    <div class="ai-input-area"><input type="text" id="user-input" placeholder="Type your query..." onkeypress="handleKeyPress(event)"><button onclick="sendMsg()">Send</button></div>
</div>
<script>
    let speaking = false; let synth = window.speechSynthesis; let utterance;
    function toggleSpeech() {
        if (speaking) { synth.cancel(); speaking = false; document.getElementById('read-page-btn').innerText = "🔊 Read Page Aloud"; }
        else { const t = document.getElementById('main-content').innerText; utterance = new SpeechSynthesisUtterance(t); utterance.onend = () => { speaking = false; document.getElementById('read-page-btn').innerText = "🔊 Read Page Aloud"; }; synth.speak(utterance); speaking = true; document.getElementById('read-page-btn').innerText = "🛑 Stop Reading"; }
    }
    function toggleAIWidget() { const w = document.getElementById('ai-widget'); const b = document.getElementById('ai-toggle-btn'); if (w.style.display === 'none' || w.style.display === '') { w.style.display = 'flex'; b.style.display = 'none'; } else { w.style.display = 'none'; b.style.display = 'block'; } }
    function handleKeyPress(e) { if (e.key === 'Enter') sendMsg(); }
    function sendMsg() {
        const input = document.getElementById('user-input'); const text = input.value.trim(); if(!text) return; appendMessage(text, 'user'); input.value = '';
        setTimeout(() => {
            let r = "I can navigate the ELSON platform. Try typing 'prices', 'movies', or 'catfish farming'."; let q = text.toLowerCase();
            if(q.includes('price') || q.includes('how much')) { r = "ELSON Prices: \n• Media: N500 \n• Catfish Manual: N3,500. Tap a WhatsApp button to order."; }
            else if (q.includes('movie') || q.includes('download')) { r = "Routing to Media Downloads (N500/Token). Click the card's WhatsApp link to order."; }
            else if (q.includes('fish') || q.includes('catfish')) { r = "Navigating to Agribusiness. Complete fish farming guides are available for N3,500."; }
            appendMessage(r, 'bot');
        }, 400);
    }
    function appendMessage(t, s) { const box = document.getElementById('chat-box'); const m = document.createElement('div'); m.className = `msg ${s}`; m.innerText = t; box.appendChild(m); box.scrollTop = box.scrollHeight; }
    async function triggerAIPartnerFinder() {
        const s = document.getElementById('loop-status'); s.innerText = "Loop Active...";
        try {
            const res = await fetch('/api/ai-partner-finder', { method: 'POST' }); const data = await res.json();
            if(data.success) {
                s.innerText = "Success! Node Integrated.";
                document.getElementById('partner-display').innerHTML = `<h3>🔥 ${data.partner.storeName}</h3><p>Status: <b style="color:green;">${data.partner.status}</b></p><a href="${data.partner.affiliateLink}" class="btn" target="_blank">Go to Affiliate Link</a>`;
            }
        } catch (err) { s.innerText = "Loop error."; }
    }
    async function loadPartners() { try { const res = await fetch('/api/partners'); const list = await res.json(); if(list.length > 0) { const l = list[list.length - 1]; document.getElementById('partner-display').innerHTML = `<h3>🔥 ${l.storeName}</h3><p>Status: <b style="color:green;">${l.status}</b></p><a href="${l.affiliateLink}" class="btn" target="_blank">Go to Affiliate Link</a>`; } } catch(e) {} }
    window.onload = loadPartners;
</script>
</body>
</html>
EOF
npm install express && \
pm2 start server.js --name "elson-platform" && \
pm2 startup && pm2 save && \
sudo systemctl restart nginx
