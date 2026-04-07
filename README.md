joyboy ..le respect ne se demande pas 
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>ZETSU CLAN • Telegram</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: #0f0f0f;
            color: #e4e6eb;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Conteneur principal style Telegram */
        .telegram-app {
            width: 100%;
            max-width: 500px;
            height: 95vh;
            background: #17212b;
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
            display: flex;
            flex-direction: column;
            position: relative;
        }

        /* Header style Telegram */
        .tg-header {
            background: #1e2a36;
            padding: 16px 20px;
            border-bottom: 1px solid #2b3b47;
            text-align: center;
        }

        .tg-header h1 {
            font-size: 1.5rem;
            font-weight: 600;
            background: linear-gradient(135deg, #ffd966, #ffb347);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }

        .tg-header p {
            font-size: 0.7rem;
            color: #7e9aab;
            margin-top: 4px;
        }

        .leaders-tg {
            display: flex;
            justify-content: center;
            gap: 8px;
            flex-wrap: wrap;
            margin-top: 8px;
            font-size: 0.7rem;
        }

        .leaders-tg span {
            background: #2b3b47;
            padding: 4px 10px;
            border-radius: 30px;
            color: #ffd966;
        }

        /* Zone de scroll (messages & posts) */
        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        /* Bulle de message façon Telegram */
        .bubble {
            max-width: 85%;
            padding: 10px 14px;
            border-radius: 18px;
            font-size: 0.9rem;
            line-height: 1.4;
            word-wrap: break-word;
            background: #1e2a36;
            align-self: flex-start;
            border-bottom-left-radius: 4px;
        }

        .bubble-meta {
            font-size: 0.7rem;
            color: #7e9aab;
            margin-bottom: 4px;
            display: flex;
            gap: 8px;
        }

        .bubble-name {
            font-weight: bold;
            color: #ffd966;
        }

        .bubble-date {
            font-size: 0.65rem;
        }

        .bubble-actions {
            margin-top: 8px;
            display: flex;
            gap: 12px;
        }

        .like-button, .comment-button {
            background: transparent;
            border: none;
            color: #7e9aab;
            font-size: 0.75rem;
            cursor: pointer;
            padding: 4px 8px;
            border-radius: 20px;
            transition: 0.2s;
        }

        .like-button.liked {
            color: #ff5e5e;
        }

        .comment-section {
            margin-top: 10px;
            display: none;
            flex-direction: column;
            gap: 8px;
        }

        .comment {
            background: #0f1a22;
            padding: 8px 12px;
            border-radius: 16px;
            font-size: 0.8rem;
            margin-top: 6px;
        }

        .comment strong {
            color: #ffb347;
        }

        .comment-input-area {
            display: flex;
            gap: 8px;
            margin-top: 8px;
        }

        .comment-input-area input {
            flex: 1;
            background: #0f1a22;
            border: none;
            padding: 8px 12px;
            border-radius: 25px;
            color: white;
            font-size: 0.8rem;
        }

        .comment-input-area button {
            background: #2b5270;
            border: none;
            border-radius: 25px;
            padding: 6px 14px;
            color: white;
            cursor: pointer;
        }

        /* Zone d'écriture (nouveau post) */
        .tg-input-area {
            background: #1e2a36;
            padding: 12px;
            border-top: 1px solid #2b3b47;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .tg-input-area textarea {
            background: #0f1a22;
            border: none;
            border-radius: 22px;
            padding: 10px 16px;
            color: white;
            font-family: inherit;
            resize: none;
            font-size: 0.9rem;
        }

        .tg-input-area button {
            background: #2b5270;
            border: none;
            border-radius: 30px;
            padding: 10px;
            font-weight: bold;
            color: white;
            cursor: pointer;
            transition: 0.2s;
        }

        .tg-input-area button:hover {
            background: #3e6d91;
        }

        /* Auth panel style Telegram */
        .auth-panel {
            background: #1e2a36;
            margin: 16px;
            padding: 18px;
            border-radius: 24px;
        }

        .auth-panel input {
            width: 100%;
            background: #0f1a22;
            border: none;
            padding: 12px;
            border-radius: 28px;
            margin-bottom: 10px;
            color: white;
        }

        .auth-buttons {
            display: flex;
            gap: 10px;
            margin-top: 8px;
        }

        .auth-buttons button {
            flex: 1;
            background: #2b5270;
            border: none;
            padding: 10px;
            border-radius: 30px;
            color: white;
            font-weight: bold;
        }

        .logout-btn {
            background: #5c3a2e !important;
        }

        .user-status {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #1e2a36;
            padding: 10px 16px;
            border-bottom: 1px solid #2b3b47;
        }

        .hide {
            display: none;
        }
    </style>
</head>
<body>
<div class="telegram-app">
    <!-- Header Telegram -->
    <div class="tg-header">
        <h1>⚡ 𝐙𝐄𝐓𝐒𝐔 ＣＬＡＮ</h1>
        <p>○ Telegram du Chapeau de Paille ○</p>
        <div class="leaders-tg">
            <span>👑 BLACK TOBI ZETSU</span>
            <span>🌸 Hinata ZETSU</span>
            <span>👸 QUEEN ZETSU</span>
        </div>
    </div>

    <!-- Zone utilisateur connecté -->
    <div id="userStatusArea" class="user-status hide">
        <span>🐦 <strong id="displayUser"></strong></span>
        <button id="logoutBtnTelegram" class="logout-btn" style="background:#2b3b47; padding:6px 12px;">🚪 Quitter</button>
    </div>

    <!-- Zone d'authentification -->
    <div id="authContainer" class="auth-panel">
        <input type="text" id="regName" placeholder="Nouveau pseudo ZETSU">
        <input type="password" id="regPass" placeholder="Mot de passe">
        <div class="auth-buttons">
            <button onclick="registerUser()">📝 S'inscrire</button>
        </div>
        <hr style="margin: 12px 0; border-color:#2b3b47;">
        <input type="text" id="loginName" placeholder="Pseudo">
        <input type="password" id="loginPass" placeholder="Mot de passe">
        <div class="auth-buttons">
            <button onclick="loginUser()">🔓 Connexion</button>
        </div>
    </div>

    <!-- Zone des messages (feed) -->
    <div class="chat-messages" id="feedTelegram">
        <!-- Les posts apparaîtront ici comme des bulles -->
        <div style="text-align:center; opacity:0.6; padding:20px;">🐦 Connectez-vous pour voir les messages du clan</div>
    </div>

    <!-- Zone pour écrire un nouveau post -->
    <div id="newPostArea" class="tg-input-area hide">
        <textarea id="postContent" rows="2" placeholder="Écrire un message au clan..."></textarea>
        <button onclick="publishPost()">📨 Envoyer</button>
    </div>
</div>

<script>
    // ---------- DATA ----------
    let users = JSON.parse(localStorage.getItem('zetsu_telegram_users')) || [];
    let posts = JSON.parse(localStorage.getItem('zetsu_telegram_posts')) || [];
    let currentUser = localStorage.getItem('zetsu_telegram_current') || null;

    function saveAll() {
        localStorage.setItem('zetsu_telegram_users', JSON.stringify(users));
        localStorage.setItem('zetsu_telegram_posts', JSON.stringify(posts));
    }

    // Inscription
    window.registerUser = function() {
        const pseudo = document.getElementById('regName').value.trim();
        const mdp = document.getElementById('regPass').value.trim();
        if(!pseudo || !mdp) return alert("Remplis pseudo et mot de passe");
        if(users.find(u => u.pseudo === pseudo)) return alert("Ce pseudo existe déjà");
        users.push({ pseudo, mdp, joined: new Date().toISOString() });
        saveAll();
        alert(`✅ Inscription réussie ${pseudo} ! Connecte-toi.`);
        document.getElementById('regName').value = '';
        document.getElementById('regPass').value = '';
    };

    // Connexion
    window.loginUser = function() {
        const pseudo = document.getElementById('loginName').value.trim();
        const mdp = document.getElementById('loginPass').value.trim();
        const user = users.find(u => u.pseudo === pseudo && u.mdp === mdp);
        if(user) {
            currentUser = pseudo;
            localStorage.setItem('zetsu_telegram_current', currentUser);
            refreshUI();
            renderFeed();
        } else {
            alert("Pseudo ou mot de passe incorrect");
        }
    };

    // Déconnexion
    function logout() {
        currentUser = null;
        localStorage.removeItem('zetsu_telegram_current');
        refreshUI();
        renderFeed();
    }

    // Rafraîchir l'affichage selon connexion
    function refreshUI() {
        const authDiv = document.getElementById('authContainer');
        const userStatus = document.getElementById('userStatusArea');
        const newPostDiv = document.getElementById('newPostArea');
        const displaySpan = document.getElementById('displayUser');
        const logoutBtn = document.getElementById('logoutBtnTelegram');

        if(currentUser) {
            authDiv.classList.add('hide');
            userStatus.classList.remove('hide');
            newPostDiv.classList.remove('hide');
            displaySpan.innerText = currentUser;
            if(logoutBtn) logoutBtn.onclick = () => logout();
        } else {
            authDiv.classList.remove('hide');
            userStatus.classList.add('hide');
            newPostDiv.classList.add('hide');
        }
    }

    // Publier un nouveau message (post)
    window.publishPost = function() {
        if(!currentUser) return alert("Connecte-toi d'abord");
        const content = document.getElementById('postContent').value.trim();
        if(!content) return alert("Écris quelque chose !");
        const newPost = {
            id: Date.now(),
            author: currentUser,
            content: content,
            date: new Date().toLocaleString(),
            likes: [],
            comments: []
        };
        posts.unshift(newPost);
        saveAll();
        document.getElementById('postContent').value = '';
        renderFeed();
    };

    // Like un post
    window.likePost = function(postId) {
        if(!currentUser) return alert("Connecte-toi pour liker");
        const post = posts.find(p => p.id === postId);
        if(post) {
            const idx = post.likes.indexOf(currentUser);
            idx === -1 ? post.likes.push(currentUser) : post.likes.splice(idx,1);
            saveAll();
            renderFeed();
        }
    };

    // Afficher/masquer comments
    window.toggleCommentsTelegram = function(postId) {
        const div = document.getElementById(`commentsBox_${postId}`);
        if(div.style.display === 'none' || !div.style.display) div.style.display = 'flex';
        else div.style.display = 'none';
    };

    // Ajouter commentaire
    window.addCommentTelegram = function(postId) {
        if(!currentUser) return alert("Connecte-toi pour commenter");
        const inputField = document.getElementById(`commentInput_${postId}`);
        const text = inputField.value.trim();
        if(!text) return;
        const post = posts.find(p => p.id === postId);
        if(post) {
            post.comments.push({
                author: currentUser,
                text: text,
                date: new Date().toLocaleString()
            });
            saveAll();
            inputField.value = '';
            renderFeed();
        }
    };

    // Rendu du feed façon Telegram (bulles)
    function renderFeed() {
        const container = document.getElementById('feedTelegram');
        if(!container) return;
        if(posts.length === 0) {
            container.innerHTML = `<div style="text-align:center; padding:20px; opacity:0.6;">🐦 Aucun message. Sois le premier ZETSU à parler !</div>`;
            return;
        }

        container.innerHTML = '';
        posts.forEach(post => {
            const isLiked = currentUser && post.likes.includes(currentUser);
            const bubbleDiv = document.createElement('div');
            bubbleDiv.className = 'bubble';
            bubbleDiv.innerHTML = `
                <div class="bubble-meta">
                    <span class="bubble-name">🎩 ${post.author}</span>
                    <span class="bubble-date">${post.date}</span>
                </div>
                <div>${escapeHtml(post.content)}</div>
                <div class="bubble-actions">
                    <button class="like-button ${isLiked ? 'liked' : ''}" onclick="likePost(${post.id})">❤️ ${post.likes.length}</button>
                    <button class="comment-button" onclick="toggleCommentsTelegram(${post.id})">💬 ${post.comments.length}</button>
                </div>
                <div id="commentsBox_${post.id}" class="comment-section" style="display:none;">
                    <div id="commentsList_${post.id}">
                        ${post.comments.map(c => `<div class="comment"><strong>🐦 ${escapeHtml(c.author)}</strong> <span style="font-size:0.65rem;">${c.date}</span><br>${escapeHtml(c.text)}</div>`).join('')}
                    </div>
                    <div class="comment-input-area">
                        <input type="text" id="commentInput_${post.id}" placeholder="Écrire un commentaire...">
                        <button onclick="addCommentTelegram(${post.id})">➤</button>
                    </div>
                </div>
            `;
            container.appendChild(bubbleDiv);
        });
        container.scrollTop = container.scrollHeight;
    }

    function escapeHtml(str) {
        if(!str) return '';
        return str.replace(/[&<>]/g, function(m) {
            if(m === '&') return '&amp;';
            if(m === '<') return '&lt;';
            if(m === '>') return '&gt;';
            return m;
        }).replace(/[\uD800-\uDBFF][\uDC00-\uDFFF]/g, function(c) {
            return c;
        });
    }

    // initialisation avec exemples
    function initDemoPosts() {
        if(posts.length === 0) {
            posts = [
                { id: 1001, author: "BLACK TOBI ZETSU", content: "Bienvenue dans le clan ZETSU version Telegram ! Ici on parle stratégie et respect. 🎩🐦", date: new Date().toLocaleString(), likes: [], comments: [] },
                { id: 1002, author: "QUEEN ZETSU", content: "Que la plume et le sabre guident nos pas. Postez vos pensées 🔥", date: new Date().toLocaleString(), likes: [], comments: [] }
            ];
            saveAll();
        }
    }

    initDemoPosts();
    refreshUI();
    renderFeed();
</script>
</body>
</html>
