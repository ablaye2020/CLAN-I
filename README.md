joyboy ..le respect ne se demande pas 
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZETSU CLAN - Le Village des Oiseaux</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', 'Segoe UI', sans-serif;
            min-height: 100vh;
            color: #2c1a0c;
            overflow-x: hidden;
        }

        /* Vidéo de fond */
        #bgVideo {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -2;
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.55);
            z-index: -1;
        }

        /* Conteneur principal */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 2;
        }

        /* ========= CHAPEAU DE PAILLE + OISEAUX (entrée animée) ========= */
        .straw-hat-banner {
            background: linear-gradient(135deg, #f7e05e, #d4a017);
            border-radius: 60px 60px 30px 30px;
            padding: 25px 20px;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            box-shadow: 0 15px 25px rgba(0,0,0,0.3), inset 0 1px 4px rgba(255,255,200,0.8);
            border-bottom: 6px solid #8b5a2b;
            transition: all 0.3s ease;
            animation: floatHat 3s infinite ease-in-out;
        }

        @keyframes floatHat {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-8px); }
            100% { transform: translateY(0px); }
        }

        .straw-hat-banner h2 {
            font-size: 2.2rem;
            font-weight: bold;
            text-shadow: 3px 3px 0 #ffb347;
            color: #3b2a1f;
            letter-spacing: 2px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .straw-hat-banner h2 span {
            background: #8b5a2b;
            padding: 0 15px;
            border-radius: 50px;
            color: #ffec80;
            font-size: 1.8rem;
        }

        /* Le chapeau en emoji / dessin */
        .hat-icon {
            font-size: 3rem;
            filter: drop-shadow(2px 4px 6px rgba(0,0,0,0.3));
            display: inline-block;
            animation: tiltHat 2s infinite;
        }

        @keyframes tiltHat {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
        }

        /* Oiseaux volants */
        .bird {
            position: absolute;
            font-size: 1.8rem;
            pointer-events: none;
            z-index: 10;
            animation: flyBird linear infinite;
        }

        @keyframes flyBird {
            0% {
                transform: translateX(-10%) translateY(0px) rotate(0deg);
                opacity: 0;
            }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% {
                transform: translateX(110vw) translateY(-30px) rotate(10deg);
                opacity: 0;
            }
        }

        /* Header clan */
        .clan-header {
            text-align: center;
            padding: 30px;
            background: rgba(245, 222, 179, 0.85);
            border-radius: 50px;
            margin-bottom: 30px;
            backdrop-filter: blur(8px);
            border: 2px solid #ffd966;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .clan-header h1 {
            font-size: 3em;
            letter-spacing: 4px;
            color: #5c3a1a;
            text-shadow: 2px 2px 0 #ffcd7e;
        }

        .leaders {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .leaders span {
            background: #6b3e1c;
            padding: 8px 18px;
            border-radius: 40px;
            color: #ffeaac;
            font-weight: bold;
            box-shadow: inset 0 -1px 0 #ffcd7e, 0 4px 8px rgba(0,0,0,0.2);
        }

        /* Sections stylisées */
        .auth-section, .post-section, .video-section, .feed {
            background: rgba(255, 248, 225, 0.9);
            border-radius: 35px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid #ffd58c;
            box-shadow: 0 8px 18px rgba(0,0,0,0.15);
            transition: transform 0.2s;
        }

        input, textarea {
            background: #fffef5;
            border: 2px solid #e2b87a;
            padding: 10px 15px;
            border-radius: 50px;
            font-size: 1rem;
            width: 220px;
            margin: 5px;
        }

        button {
            background: #f5bc70;
            border: none;
            padding: 10px 20px;
            border-radius: 40px;
            font-weight: bold;
            color: #3e2a1b;
            cursor: pointer;
            transition: 0.2s;
            box-shadow: 0 3px 6px rgba(0,0,0,0.2);
        }

        button:hover {
            background: #ffcf8a;
            transform: scale(1.02);
        }

        .logout-btn {
            background: #c97e3a;
            color: white;
        }

        .post {
            background: #fff3e0;
            border-radius: 28px;
            padding: 18px;
            margin-bottom: 20px;
            border-left: 8px solid #f7b32b;
        }

        .post-author {
            font-weight: bold;
            color: #b45f1b;
            font-size: 1.1rem;
        }

        .like-btn.liked {
            background: #f7b32b;
            color: #2c1a0c;
        }

        .comment {
            background: #faeec2;
            border-radius: 20px;
        }

        @media (max-width: 700px) {
            .clan-header h1 { font-size: 2rem; }
            .straw-hat-banner h2 { font-size: 1.4rem; }
        }
    </style>
</head>
<body>
    <video autoplay loop muted id="bgVideo">
        <source src="https://ia800504.us.archive.org/10/items/youtube-embed-Q1WMof5utos/Q1WMof5utos.mp4" type="video/mp4">
    </video>
    <div class="overlay"></div>

    <!-- Création des oiseaux dynamiques -->
    <div id="birdsArea"></div>

    <div class="container">
        <!-- Bannière Chapeau de Paille + accueil chaleureux -->
        <div class="straw-hat-banner">
            <div class="hat-icon">🎩🍂</div>
            <h2>
                <span>🍃</span> L'ENTRÉE DES LÉGENDES <span>🍃</span>
            </h2>
            <div style="font-size:1.2rem; margin-top:8px;">~ Chapeau de Paille & Oiseaux de liberté ~</div>
            <div class="hat-icon" style="font-size:2rem;">🐦🌾</div>
        </div>

        <!-- Header Clan -->
        <div class="clan-header">
            <h1>⚔️ 𝐙𝐄𝐓𝐒𝐔 𝐂𝐋𝐀𝐍 ⚔️</h1>
            <div class="leaders">
                <span>👑 Chef: 𝐁𝐋𝐀𝐂𝐊 𝐓𝐎𝐁𝐈 𝐙𝐄𝐓𝐒𝐔</span>
                <span>🌸 Sous-chef: Hinata 𝐙𝐄𝐓𝐒𝐔</span>
                <span>👸 Reine: 𝙌𝙐𝙀𝙀𝙉 𝐙𝐄𝐓𝐒𝐔</span>
            </div>
        </div>

        <!-- Zone Authentification -->
        <div id="authSection" class="auth-section">
            <h3>🔐 Portail 𝐙𝐄𝐓𝐒𝐔 — Entre Amis</h3>
            <div id="authForms">
                <input type="text" id="regPseudo" placeholder="Pseudo ZETSU">
                <input type="password" id="regMdp" placeholder="Mot de passe">
                <button onclick="register()">📜 S'inscrire</button>
                <hr style="margin: 15px 0; background:#e2b87a;">
                <input type="text" id="loginPseudo" placeholder="Pseudo">
                <input type="password" id="loginMdp" placeholder="Mot de passe">
                <button onclick="login()">🍂 Entrer dans le clan</button>
            </div>
            <div id="userInfo" style="display:none;">
                <div style="display: flex; justify-content: space-between; align-items:center;">
                    <span>🐦 Connecté : <strong id="currentUser"></strong></span>
                    <button class="logout-btn" onclick="logout()">🚪 Quitter</button>
                </div>
            </div>
        </div>

        <!-- Vidéo officielle -->
        <div class="video-section">
            <h3>📺 La Vidéo Sacrée des 𝐙𝐄𝐓𝐒𝐔</h3>
            <div style="position:relative; padding-bottom:56.25%; height:0; border-radius:25px; overflow:hidden;">
                <iframe src="https://www.youtube.com/embed/Q1WMof5utos?autoplay=1&mute=0&loop=1&playlist=Q1WMof5utos" style="position:absolute; top:0; left:0; width:100%; height:100%;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
        </div>

        <!-- Publier (connecté) -->
        <div id="postSection" class="post-section" style="display:none;">
            <h3>🌾 Partager une pensée, un exploit 𝐙𝐄𝐓𝐒𝐔</h3>
            <textarea id="newPostContent" rows="3" placeholder="Exprime la force du clan..." style="width:100%; border-radius:25px; background:#fff9ef;"></textarea>
            <button onclick="createPost()">➕ Lâcher l'oiseau 🕊️</button>
        </div>

        <!-- Mur des posts -->
        <div class="feed">
            <h3>💬 Mur des 𝐙𝐄𝐓𝐒𝐔 — Où volent les paroles</h3>
            <div id="feedContainer"></div>
        </div>
    </div>

    <script>
        // === Données ===
        let users = JSON.parse(localStorage.getItem('zetsu_users')) || [];
        let posts = JSON.parse(localStorage.getItem('zetsu_posts')) || [];
        let currentUser = localStorage.getItem('zetsu_currentUser') || null;

        function saveData() {
            localStorage.setItem('zetsu_users', JSON.stringify(users));
            localStorage.setItem('zetsu_posts', JSON.stringify(posts));
        }

        // === OISEAUX EN VOL ===
        function createFlyingBirds() {
            const birdsArea = document.getElementById('birdsArea');
            if(!birdsArea) return;
            setInterval(() => {
                const bird = document.createElement('div');
                bird.className = 'bird';
                const birdEmojis = ['🐦', '🐧', '🕊️', '🐤', '🐦‍⬛', '🌾'];
                bird.innerHTML = birdEmojis[Math.floor(Math.random() * birdEmojis.length)];
                bird.style.left = '-5%';
                bird.style.top = Math.random() * 80 + '%';
                bird.style.fontSize = (1.5 + Math.random() * 1.5) + 'rem';
                bird.style.animationDuration = (6 + Math.random() * 5) + 's';
                bird.style.animationDelay = '0s';
                birdsArea.appendChild(bird);
                setTimeout(() => { if(bird && bird.remove) bird.remove(); }, 11000);
            }, 4000);
        }

        // === AUTH ===
        function register() {
            const pseudo = document.getElementById('regPseudo').value.trim();
            const mdp = document.getElementById('regMdp').value.trim();
            if (!pseudo || !mdp) return alert("Remplis tout !");
            if (users.find(u => u.pseudo === pseudo)) return alert("Ce pseudo existe déjà !");
            users.push({ pseudo, mdp, date: new Date().toISOString() });
            saveData();
            alert("Inscription réussie " + pseudo + " ! Connecte-toi.");
            document.getElementById('regPseudo').value = '';
            document.getElementById('regMdp').value = '';
        }

        function login() {
            const pseudo = document.getElementById('loginPseudo').value.trim();
            const mdp = document.getElementById('loginMdp').value.trim();
            const user = users.find(u => u.pseudo === pseudo && u.mdp === mdp);
            if (user) {
                currentUser = pseudo;
                localStorage.setItem('zetsu_currentUser', currentUser);
                updateUI();
                loadFeed();
                alert("Bienvenue dans le nid, " + pseudo + " ! 🐦");
            } else {
                alert("Mauvais pseudo/mot de passe, 𝐙𝐄𝐓𝐒𝐔.");
            }
        }

        function logout() {
            currentUser = null;
            localStorage.removeItem('zetsu_currentUser');
            updateUI();
            loadFeed();
        }

        function updateUI() {
            const authForms = document.getElementById('authForms');
            const userInfoDiv = document.getElementById('userInfo');
            const postSection = document.getElementById('postSection');
            const currentUserSpan = document.getElementById('currentUser');
            if (currentUser) {
                authForms.style.display = 'none';
                userInfoDiv.style.display = 'block';
                postSection.style.display = 'block';
                currentUserSpan.innerText = currentUser;
            } else {
                authForms.style.display = 'block';
                userInfoDiv.style.display = 'none';
                postSection.style.display = 'none';
            }
        }

        function createPost() {
            if (!currentUser) return alert("Connecte-toi pour poster !");
            const content = document.getElementById('newPostContent').value.trim();
            if (!content) return alert("Écris quelque chose !");
            const newPost = {
                id: Date.now(),
                author: currentUser,
                content: content,
                date: new Date().toLocaleString(),
                likes: [],
                comments: []
            };
            posts.unshift(newPost);
            saveData();
            document.getElementById('newPostContent').value = '';
            loadFeed();
        }

        function likePost(postId) {
            if (!currentUser) return alert("Connecte-toi pour liker !");
            const post = posts.find(p => p.id === postId);
            if (post) {
                const idx = post.likes.indexOf(currentUser);
                idx === -1 ? post.likes.push(currentUser) : post.likes.splice(idx, 1);
                saveData();
                loadFeed();
            }
        }

        function addComment(postId) {
            if (!currentUser) return alert("Connecte-toi pour commenter !");
            const inputId = `commentInput_${postId}`;
            const txt = document.getElementById(inputId).value.trim();
            if (!txt) return;
            const post = posts.find(p => p.id === postId);
            if (post) {
                post.comments.push({ author: currentUser, text: txt, date: new Date().toLocaleString() });
                saveData();
                document.getElementById(inputId).value = '';
                loadFeed();
            }
        }

        function toggleComments(postId) {
            const div = document.getElementById(`comments_${postId}`);
            if (div.style.display === 'none' || !div.style.display) div.style.display = 'block';
            else div.style.display = 'none';
        }

        function loadFeed() {
            const container = document.getElementById('feedContainer');
            if (!container) return;
            if (posts.length === 0) {
                container.innerHTML = '<p style="text-align:center; padding:20px;">🐦 Aucun message... Sois le premier ZETSU à s’exprimer ! 🌾</p>';
                return;
            }
            container.innerHTML = '';
            posts.forEach(post => {
                const div = document.createElement('div');
                div.className = 'post';
                const isLiked = currentUser && post.likes.includes(currentUser);
                div.innerHTML = `
                    <div style="display:flex; justify-content:space-between; flex-wrap:wrap;">
                        <span class="post-author">🪶 ${post.author}</span>
                        <span style="font-size:0.8rem; opacity:0.7;">📅 ${post.date}</span>
                    </div>
                    <div style="margin:12px 0;">🌾 ${post.content.replace(/</g, '&lt;').replace(/>/g, '&gt;')}</div>
                    <div style="display:flex; gap:15px;">
                        <button class="like-btn ${isLiked ? 'liked' : ''}" onclick="likePost(${post.id})">❤️ ${post.likes.length}</button>
                        <button class="comment-btn" onclick="toggleComments(${post.id})">💬 ${post.comments.length}</button>
                    </div>
                    <div class="comments-section" id="comments_${post.id}" style="display:none; margin-top:12px;">
                        <div id="commentsList_${post.id}">
                            ${post.comments.map(c => `<div class="comment"><strong>🐦 ${c.author}</strong> (${c.date}) : ${c.text.replace(/</g, '&lt;')}</div>`).join('')}
                        </div>
                        <div style="display:flex; gap:5px; margin-top:10px;">
                            <input type="text" id="commentInput_${post.id}" placeholder="Ajoute un commentaire..." style="flex:1;">
                            <button onclick="addComment(${post.id})">Envoyer 🌾</button>
                        </div>
                    </div>
                `;
                container.appendChild(div);
            });
        }

        function initDemo() {
            if(posts.length === 0) {
                posts = [
                    { id: 100, author: "𝐁𝐋𝐀𝐂𝐊 𝐓𝐎𝐁𝐈 𝐙𝐄𝐓𝐒𝐔", content: "Sous le chapeau de paille, nous sommes invincibles ! Bienvenue à tous les oiseaux du clan 🎩🐦", date: new Date().toLocaleString(), likes: [], comments: [] },
                    { id: 101, author: "𝙌𝙐𝙀𝙀𝙉 𝐙𝐄𝐓𝐒𝐔", content: "Que nos plumes brillent comme l’or. Postez vos exploits, ZETSU ! 👑✨", date: new Date().toLocaleString(), likes: [], comments: [] }
                ];
                saveData();
            }
        }

        // LANCEMENT
        createFlyingBirds();
        initDemo();
        updateUI();
        loadFeed();
    </script>
</body>
</html>
