joyboy ..le respect ne se demande pas 
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>ZETSU CLAN • Médias & Réseau</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: #0a0e12;
            color: #e4e6eb;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .telegram-app {
            width: 100%;
            max-width: 550px;
            height: 95vh;
            background: #17212b;
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
            display: flex;
            flex-direction: column;
        }

        .tg-header {
            background: #1e2a36;
            padding: 14px 20px;
            border-bottom: 1px solid #2b3b47;
            text-align: center;
        }

        .tg-header h1 {
            font-size: 1.5rem;
            background: linear-gradient(135deg, #ffd966, #ffb347);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .leaders-tg {
            display: flex;
            justify-content: center;
            gap: 6px;
            flex-wrap: wrap;
            margin-top: 6px;
            font-size: 0.65rem;
        }

        .leaders-tg span {
            background: #2b3b47;
            padding: 3px 8px;
            border-radius: 30px;
            color: #ffd966;
        }

        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .bubble {
            max-width: 92%;
            padding: 10px 14px;
            border-radius: 18px;
            background: #1e2a36;
            align-self: flex-start;
            border-bottom-left-radius: 4px;
        }

        .bubble-meta {
            font-size: 0.7rem;
            color: #7e9aab;
            margin-bottom: 5px;
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }

        .bubble-name {
            font-weight: bold;
            color: #ffd966;
        }

        .badge-chef {
            background: #b85c1a;
            font-size: 0.6rem;
            padding: 2px 8px;
            border-radius: 20px;
            color: gold;
        }

        .media-content {
            margin: 8px 0;
            max-width: 100%;
            border-radius: 16px;
            overflow: hidden;
        }

        .media-content img, .media-content video {
            max-width: 100%;
            max-height: 300px;
            border-radius: 16px;
            cursor: pointer;
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
        }

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

        .media-buttons {
            display: flex;
            gap: 10px;
        }

        .media-buttons button {
            background: #2b5270;
            border: none;
            padding: 6px 12px;
            border-radius: 25px;
            font-size: 0.75rem;
            color: white;
            cursor: pointer;
        }

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
            cursor: pointer;
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

        small {
            color: #ffb347;
            display: block;
            text-align: center;
            margin-top: 8px;
        }
    </style>
</head>
<body>
<div class="telegram-app">
    <div class="tg-header">
        <h1>⚔️ 𝐙𝐄𝐓𝐒𝐔 𝐂𝐋𝐀𝐍 ⚔️</h1>
        <div class="leaders-tg">
            <span>👑 BLACK TOBI ZETSU</span>
            <span>🌸 Hinata ZETSU</span>
            <span>👸 QUEEN ZETSU</span>
        </div>
    </div>

    <div id="userStatusArea" class="user-status hide">
        <span>🐦 <strong id="displayUser"></strong> <span id="chefBadge" style="display:none;" class="badge-chef">👑 CHEF</span></span>
        <button id="logoutBtnTelegram" style="background:#2b3b47; padding:6px 12px; border-radius:20px;">🚪 Quitter</button>
    </div>

    <div id="authContainer" class="auth-panel">
        <input type="text" id="regName" placeholder="Pseudo ZETSU">
        <input type="password" id="regPass" placeholder="Mot de passe">
        <input type="text" id="regCode" placeholder="Code d'invitation (ZETSU2025)">
        <div class="auth-buttons">
            <button onclick="registerUser()">📝 S'inscrire</button>
        </div>
        <hr style="margin: 12px 0; border-color:#2b3b47;">
        <input type="text" id="loginName" placeholder="Pseudo">
        <input type="password" id="loginPass" placeholder="Mot de passe">
        <div class="auth-buttons">
            <button onclick="loginUser()">🔓 Connexion</button>
        </div>
        <small>🔑 Code unique : ZETSU2025</small>
    </div>

    <div class="chat-messages" id="feedTelegram">
        <div style="text-align:center; opacity:0.6; padding:20px;">🐦 Connecte-toi avec le code ZETSU2025</div>
    </div>

    <div id="newPostArea" class="tg-input-area hide">
        <textarea id="postContent" rows="2" placeholder="Message textuel..."></textarea>
        <div class="media-buttons">
            <button onclick="addImagePrompt()">🖼️ Ajouter une image (URL)</button>
            <button onclick="addVideoPrompt()">🎬 Ajouter une vidéo (URL)</button>
        </div>
        <button onclick="publishPost()">📨 Publier sur le mur</button>
    </div>
</div>

<script>
    // === DONNÉES ===
    let users = JSON.parse(localStorage.getItem('zetsu_media_users')) || [];
    let posts = JSON.parse(localStorage.getItem('zetsu_media_posts')) || [];
    let currentUser = localStorage.getItem('zetsu_media_session') || null;

    const INVITE_CODE = "ZETSU2025";
    const CHEF_NAME = "BLACK TOBI ZETSU";

    function saveAll() {
        localStorage.setItem('zetsu_media_users', JSON.stringify(users));
        localStorage.setItem('zetsu_media_posts', JSON.stringify(posts));
    }

    function isChef(username) {
        return username === CHEF_NAME;
    }

    // Inscription avec code unique
    window.registerUser = function() {
        const pseudo = document.getElementById('regName').value.trim();
        const mdp = document.getElementById('regPass').value.trim();
        const code = document.getElementById('regCode').value.trim();

        if(!pseudo || !mdp) return alert("Remplis pseudo et mot de passe");
        if(code !== INVITE_CODE) return alert("❌ Code d'invitation incorrect ! Il faut ZETSU2025 pour rejoindre le clan.");
        if(users.find(u => u.pseudo === pseudo)) return alert("Ce pseudo existe déjà");

        const role = (pseudo === CHEF_NAME) ? "chef" : "member";
        users.push({ pseudo, mdp, role, joined: new Date().toLocaleString() });
        saveAll();
        alert(`✅ Bienvenue ${pseudo} ! Tu es maintenant membre du clan ZETSU. Connecte-toi.`);
        document.getElementById('regName').value = '';
        document.getElementById('regPass').value = '';
        document.getElementById('regCode').value = '';
    };

    window.loginUser = function() {
        const pseudo = document.getElementById('loginName').value.trim();
        const mdp = document.getElementById('loginPass').value.trim();
        const user = users.find(u => u.pseudo === pseudo && u.mdp === mdp);
        if(user) {
            currentUser = pseudo;
            localStorage.setItem('zetsu_media_session', currentUser);
            refreshUI();
            renderFeed();
        } else {
            alert("Pseudo ou mot de passe incorrect");
        }
    };

    function logout() {
        currentUser = null;
        localStorage.removeItem('zetsu_media_session');
        refreshUI();
        renderFeed();
    }

    let pendingMediaURL = null;
    let pendingMediaType = null;

    window.addImagePrompt = function() {
        let url = prompt("Colle l'URL de l'image (jpg, png, gif, etc.) :");
        if(url && url.trim()) {
            pendingMediaURL = url.trim();
            pendingMediaType = 'image';
            alert("✅ Image ajoutée ! Tu peux encore écrire du texte avant de publier.");
        }
    };

    window.addVideoPrompt = function() {
        let url = prompt("Colle l'URL de la vidéo (mp4, webm, YouTube n'est pas supporté directement, préfère un lien direct .mp4) :");
        if(url && url.trim()) {
            pendingMediaURL = url.trim();
            pendingMediaType = 'video';
            alert("✅ Vidéo ajoutée !");
        }
    };

    window.publishPost = function() {
        if(!currentUser) return alert("Connecte-toi d'abord");
        let textContent = document.getElementById('postContent').value.trim();
        if(!textContent && !pendingMediaURL) return alert("Ajoute du texte ou un média");

        const newPost = {
            id: Date.now(),
            author: currentUser,
            text: textContent || "",
            mediaURL: pendingMediaURL || null,
            mediaType: pendingMediaType || null,
            date: new Date().toLocaleString(),
            likes: [],
            comments: []
        };

        posts.unshift(newPost);
        saveAll();
        document.getElementById('postContent').value = '';
        pendingMediaURL = null;
        pendingMediaType = null;
        renderFeed();
    };

    window.likePost = function(postId) {
        if(!currentUser) return alert("Connecte-toi");
        const post = posts.find(p => p.id === postId);
        if(post) {
            const idx = post.likes.indexOf(currentUser);
            idx === -1 ? post.likes.push(currentUser) : post.likes.splice(idx,1);
            saveAll();
            renderFeed();
        }
    };

    window.toggleComments = function(postId) {
        const div = document.getElementById(`commentsBox_${postId}`);
        if(div.style.display === 'none' || !div.style.display) div.style.display = 'flex';
        else div.style.display = 'none';
    };

    window.addComment = function(postId) {
        if(!currentUser) return alert("Connecte-toi");
        const inputField = document.getElementById(`commentInput_${postId}`);
        const text = inputField.value.trim();
        if(!text) return;
        const post = posts.find(p => p.id === postId);
        if(post) {
            post.comments.push({ author: currentUser, text: text, date: new Date().toLocaleString() });
            saveAll();
            inputField.value = '';
            renderFeed();
        }
    };

    function escapeHtml(str) {
        if(!str) return '';
        return str.replace(/[&<>]/g, function(m) {
            if(m === '&') return '&amp;';
            if(m === '<') return '&lt;';
            if(m === '>') return '&gt;';
            return m;
        });
    }

    function renderFeed() {
        const container = document.getElementById('feedTelegram');
        if(!container) return;
        if(posts.length === 0) {
            container.innerHTML = `<div style="text-align:center; padding:20px;">🐦 Aucun message. Publie quelque chose !</div>`;
            return;
        }
        container.innerHTML = '';
        posts.forEach(post => {
            const isLiked = currentUser && post.likes.includes(currentUser);
            const isAuthorChef = (post.author === CHEF_NAME);
            let mediaHTML = '';
            if(post.mediaURL && post.mediaType === 'image') {
                mediaHTML = `<div class="media-content"><img src="${escapeHtml(post.mediaURL)}" alt="image" loading="lazy" onclick="window.open(this.src)"></div>`;
            } else if(post.mediaURL && post.mediaType === 'video') {
                mediaHTML = `<div class="media-content"><video controls src="${escapeHtml(post.mediaURL)}" onclick="this.paused ? this.play() : this.pause()"></video></div>`;
            }
            const bubble = document.createElement('div');
            bubble.className = 'bubble';
            bubble.innerHTML = `
                <div class="bubble-meta">
                    <span class="bubble-name">🎩 ${escapeHtml(post.author)} ${isAuthorChef ? '<span class="badge-chef">👑 CHEF</span>' : ''}</span>
                    <span>${post.date}</span>
                </div>
                ${post.text ? `<div>${escapeHtml(post.text)}</div>` : ''}
                ${mediaHTML}
                <div class="bubble-actions">
                    <button class="like-button ${isLiked ? 'liked' : ''}" onclick="likePost(${post.id})">❤️ ${post.likes.length}</button>
                    <button class="comment-button" onclick="toggleComments(${post.id})">💬 ${post.comments.length}</button>
                </div>
                <div id="commentsBox_${post.id}" class="comment-section" style="display:none;">
                    <div id="commentsList_${post.id}">
                        ${post.comments.map(c => `<div class="comment"><strong>🐦 ${escapeHtml(c.author)}</strong> <span style="font-size:0.65rem;">${c.date}</span><br>${escapeHtml(c.text)}</div>`).join('')}
                    </div>
                    <div style="display:flex; gap:8px; margin-top:8px;">
                        <input type="text" id="commentInput_${post.id}" placeholder="Écrire un commentaire..." style="flex:1; background:#0f1a22; border:none; padding:8px; border-radius:20px; color:white;">
                        <button onclick="addComment(${post.id})" style="background:#2b5270; border:none; border-radius:20px; padding:6px 12px;">➤</button>
                    </div>
                </div>
            `;
            container.appendChild(bubble);
        });
        container.scrollTop = container.scrollHeight;
    }

    function refreshUI() {
        const authDiv = document.getElementById('authContainer');
        const userStatus = document.getElementById('userStatusArea');
        const newPostDiv = document.getElementById('newPostArea');
        const displaySpan = document.getElementById('displayUser');
        const chefBadgeSpan = document.getElementById('chefBadge');
        const logoutBtn = document.getElementById('logoutBtnTelegram');

        if(currentUser) {
            authDiv.classList.add('hide');
            userStatus.classList.remove('hide');
            newPostDiv.classList.remove('hide');
            displaySpan.innerText = currentUser;
            if(isChef(currentUser)) chefBadgeSpan.style.display = 'inline';
            else chefBadgeSpan.style.display = 'none';
            logoutBtn.onclick = () => logout();
        } else {
            authDiv.classList.remove('hide');
            userStatus.classList.add('hide');
            newPostDiv.classList.add('hide');
        }
    }

    function initDefault() {
        if(!users.find(u => u.pseudo === CHEF_NAME)) {
            users.push({ pseudo: CHEF_NAME, mdp: "chef123", role: "chef" });
            saveAll();
        }
        if(posts.length === 0) {
            posts = [
                { id: 1, author: CHEF_NAME, text: "Bienvenue dans le clan ZETSU ! Ici vous pouvez envoyer des messages, images et vidéos. Code : ZETSU2025", mediaURL: null, date: new Date().toLocaleString(), likes: [], comments: [] },
                { id: 2, author: "QUEEN ZETSU", text: "N'hésitez pas à partager vos exploits en image 🔥", mediaURL: "https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExamZhbmdlcnNob3J0c2NlbmUycmFuZG9ta2V5d29yZHMmY2lkPTc5MGI3NjExeWZ6d3NvMnJ2aHpmeXN6bGZna2R1cW1vbTJ0aGQ5Y2NnN3ZucGtxcw&ep=v1_gifs_search&rid=200w.gif&ct=g", mediaType: "image", date: new Date().toLocaleString(), likes: [], comments: [] }
            ];
            saveAll();
        }
    }

    initDefault();
    refreshUI();
    renderFeed();
</script>
</body>
</html>
