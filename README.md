joyboy ..le respect ne se demande pas 

<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>ZETSU CLAN • Réseau Privé</title>
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

        /* Conteneur principal */
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
            position: relative;
        }

        /* Header */
        .tg-header {
            background: #1e2a36;
            padding: 16px 20px;
            border-bottom: 1px solid #2b3b47;
            text-align: center;
        }

        .tg-header h1 {
            font-size: 1.6rem;
            font-weight: 700;
            background: linear-gradient(135deg, #ffd966, #ffb347);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .tg-header p {
            font-size: 0.7rem;
            color: #7e9aab;
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

        /* Zone de scroll */
        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        /* Bulle de message */
        .bubble {
            max-width: 90%;
            padding: 10px 14px;
            border-radius: 18px;
            font-size: 0.9rem;
            line-height: 1.4;
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
            margin-top: 6px;
        }

        .comment strong {
            color: #ffb347;
        }

        /* Input zone */
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
        }

        /* Auth panel */
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
            flex-wrap: wrap;
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

        .admin-section {
            background: #1e2a36;
            margin: 16px;
            padding: 16px;
            border-radius: 24px;
            border-left: 4px solid #ffb347;
        }

        .pending-user {
            background: #0f1a22;
            padding: 10px;
            border-radius: 16px;
            margin: 8px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .approve-btn {
            background: #2b8c5e;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.75rem;
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

        .code-input {
            background: #0f1a22;
            border: 1px solid #ffb347;
        }

        small {
            color: #ffb347;
        }
    </style>
</head>
<body>
<div class="telegram-app">
    <div class="tg-header">
        <h1>⚔️ 𝐙𝐄𝐓𝐒𝐔 𝐂𝐋𝐀𝐍 ⚔️</h1>
        <p>○ Réseau privé — Approuvé par le Chef ○</p>
        <div class="leaders-tg">
            <span>👑 BLACK TOBI ZETSU</span>
            <span>🌸 Hinata ZETSU</span>
            <span>👸 QUEEN ZETSU</span>
        </div>
    </div>

    <!-- Barre utilisateur connecté -->
    <div id="userStatusArea" class="user-status hide">
        <span>🐦 <strong id="displayUser"></strong> <span id="chefBadge" style="display:none;" class="badge-chef">👑 CHEF</span></span>
        <button id="logoutBtnTelegram" style="background:#2b3b47; padding:6px 12px; border-radius:20px;">🚪 Quitter</button>
    </div>

    <!-- Zone d'authentification -->
    <div id="authContainer" class="auth-panel">
        <input type="text" id="regName" placeholder="Pseudo ZETSU">
        <input type="password" id="regPass" placeholder="Mot de passe">
        <input type="text" id="regCode" placeholder="Code d'invitation (optionnel si tu es le chef)" class="code-input">
        <div class="auth-buttons">
            <button onclick="registerUser()">📝 Demander adhésion</button>
        </div>
        <hr style="margin: 12px 0; border-color:#2b3b47;">
        <input type="text" id="loginName" placeholder="Pseudo">
        <input type="password" id="loginPass" placeholder="Mot de passe">
        <div class="auth-buttons">
            <button onclick="loginUser()">🔓 Connexion</button>
        </div>
        <small>🔐 Code unique chef : ZETSUCHEF2025</small>
    </div>

    <!-- Zone admin (approbation) -->
    <div id="adminPanel" class="admin-section hide">
        <h4 style="color:#ffd966;">👑 Espace Chef — Approbations</h4>
        <div id="pendingList">Chargement...</div>
    </div>

    <!-- Mur des messages -->
    <div class="chat-messages" id="feedTelegram">
        <div style="text-align:center; opacity:0.6; padding:20px;">🐦 Connectez-vous pour voir les messages du clan</div>
    </div>

    <!-- Zone pour publier -->
    <div id="newPostArea" class="tg-input-area hide">
        <textarea id="postContent" rows="2" placeholder="Message public au clan ZETSU..."></textarea>
        <button onclick="publishPost()">📨 Envoyer au mur</button>
    </div>
</div>

<script>
    // ---------- STRUCTURE ----------
    let users = JSON.parse(localStorage.getItem('zetsu_approved_users')) || [];
    let pendingUsers = JSON.parse(localStorage.getItem('zetsu_pending_users')) || [];
    let posts = JSON.parse(localStorage.getItem('zetsu_global_posts')) || [];
    let currentUser = localStorage.getItem('zetsu_current_session') || null;

    const CHEF_CODE = "ZETSUCHEF2025";
    const CHEF_NAME = "BLACK TOBI ZETSU";

    function saveAll() {
        localStorage.setItem('zetsu_approved_users', JSON.stringify(users));
        localStorage.setItem('zetsu_pending_users', JSON.stringify(pendingUsers));
        localStorage.setItem('zetsu_global_posts', JSON.stringify(posts));
    }

    // Vérifier si un user est chef
    function isChef(username) {
        return username === CHEF_NAME;
    }

    // Inscription avec demande d'approbation
    window.registerUser = function() {
        const pseudo = document.getElementById('regName').value.trim();
        const mdp = document.getElementById('regPass').value.trim();
        const code = document.getElementById('regCode').value.trim();

        if(!pseudo || !mdp) return alert("Remplis pseudo et mot de passe");

        // Vérifier si déjà approuvé ou en attente
        if(users.find(u => u.pseudo === pseudo)) return alert("Ce pseudo est déjà membre actif.");
        if(pendingUsers.find(u => u.pseudo === pseudo)) return alert("Demande déjà envoyée, attends l'approbation du chef.");

        // Si c'est le chef avec le bon code
        if(code === CHEF_CODE && pseudo === CHEF_NAME) {
            // Chef direct
            if(!users.find(u => u.pseudo === CHEF_NAME)) {
                users.push({ pseudo: CHEF_NAME, mdp: mdp, role: "chef", approved: true });
                saveAll();
                alert("✅ Chef enregistré avec succès !");
                return;
            } else {
                alert("Le chef existe déjà.");
                return;
            }
        } 
        else if(code === CHEF_CODE) {
            alert("❌ Ce code est réservé uniquement au chef BLACK TOBI ZETSU.");
            return;
        }
        else {
            // Demande normale
            pendingUsers.push({ pseudo, mdp, requestedAt: new Date().toLocaleString() });
            saveAll();
            alert(`🙏 Demande envoyée ! Le chef approuvera ton inscription bientôt.`);
            document.getElementById('regName').value = '';
            document.getElementById('regPass').value = '';
            document.getElementById('regCode').value = '';
        }
    };

    // Connexion (seulement membres approuvés)
    window.loginUser = function() {
        const pseudo = document.getElementById('loginName').value.trim();
        const mdp = document.getElementById('loginPass').value.trim();
        const user = users.find(u => u.pseudo === pseudo && u.mdp === mdp && u.approved === true);
        if(user) {
            currentUser = pseudo;
            localStorage.setItem('zetsu_current_session', currentUser);
            refreshUI();
            renderFeed();
        } else {
            alert("Accès refusé. Soit mot de passe incorrect, soit ton compte n'est pas encore approuvé par le chef.");
        }
    };

    function logout() {
        currentUser = null;
        localStorage.removeItem('zetsu_current_session');
        refreshUI();
        renderFeed();
    }

    // Approuver un membre (chef seulement)
    window.approveMember = function(index) {
        if(!isChef(currentUser)) return alert("Seul le chef peut approuver");
        const pending = pendingUsers[index];
        if(pending) {
            users.push({ pseudo: pending.pseudo, mdp: pending.mdp, role: "member", approved: true });
            pendingUsers.splice(index,1);
            saveAll();
            renderAdminPanel();
            alert(`✅ ${pending.pseudo} est maintenant membre ZETSU !`);
        }
    };

    // Refuser / supprimer une demande
    window.denyMember = function(index) {
        if(!isChef(currentUser)) return;
        pendingUsers.splice(index,1);
        saveAll();
        renderAdminPanel();
    };

    // Afficher le panneau admin (uniquement pour chef)
    function renderAdminPanel() {
        const panel = document.getElementById('adminPanel');
        const pendingDiv = document.getElementById('pendingList');
        if(!isChef(currentUser)) {
            panel.classList.add('hide');
            return;
        }
        panel.classList.remove('hide');
        if(pendingUsers.length === 0) {
            pendingDiv.innerHTML = "<p>Aucune demande en attente.</p>";
            return;
        }
        pendingDiv.innerHTML = "";
        pendingUsers.forEach((u, idx) => {
            const div = document.createElement('div');
            div.className = 'pending-user';
            div.innerHTML = `
                <span>🐦 ${u.pseudo} — demande le ${u.requestedAt}</span>
                <div>
                    <button class="approve-btn" onclick="approveMember(${idx})">✅ Approuver</button>
                    <button style="background:#5c3a2e;" onclick="denyMember(${idx})">❌ Refuser</button>
                </div>
            `;
            pendingDiv.appendChild(div);
        });
    }

    // Publier un message
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

    window.toggleComments = function(postId) {
        const div = document.getElementById(`commentsBox_${postId}`);
        if(div.style.display === 'none' || !div.style.display) div.style.display = 'flex';
        else div.style.display = 'none';
    };

    window.addComment = function(postId) {
        if(!currentUser) return alert("Connecte-toi pour commenter");
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
            container.innerHTML = `<div style="text-align:center; padding:20px;">🐦 Aucun message. Sois le premier ZETSU à écrire !</div>`;
            return;
        }
        container.innerHTML = '';
        posts.forEach(post => {
            const isLiked = currentUser && post.likes.includes(currentUser);
            const isAuthorChef = (post.author === CHEF_NAME);
            const bubble = document.createElement('div');
            bubble.className = 'bubble';
            bubble.innerHTML = `
                <div class="bubble-meta">
                    <span class="bubble-name">🎩 ${escapeHtml(post.author)} ${isAuthorChef ? '<span class="badge-chef">👑 CHEF</span>' : ''}</span>
                    <span>${post.date}</span>
                </div>
                <div>${escapeHtml(post.content)}</div>
                <div class="bubble-actions">
                    <button class="like-button ${isLiked ? 'liked' : ''}" onclick="likePost(${post.id})">❤️ ${post.likes.length}</button>
                    <button class="comment-button" onclick="toggleComments(${post.id})">💬 ${post.comments.length}</button>
                </div>
                <div id="commentsBox_${post.id}" class="comment-section" style="display:none;">
                    <div id="commentsList_${post.id}">
                        ${post.comments.map(c => `<div class="comment"><strong>🐦 ${escapeHtml(c.author)}</strong> <span style="font-size:0.65rem;">${c.date}</span><br>${escapeHtml(c.text)}</div>`).join('')}
                    </div>
                    <div class="comment-input-area" style="display:flex; gap:8px; margin-top:8px;">
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
            if(isChef(currentUser)) {
                chefBadgeSpan.style.display = 'inline';
                renderAdminPanel();
            } else {
                chefBadgeSpan.style.display = 'none';
                document.getElementById('adminPanel').classList.add('hide');
            }
            logoutBtn.onclick = () => logout();
        } else {
            authDiv.classList.remove('hide');
            userStatus.classList.add('hide');
            newPostDiv.classList.add('hide');
            document.getElementById('adminPanel').classList.add('hide');
        }
    }

    // Initialisation avec chef par défaut si nécessaire
    function initDefault() {
        if(!users.find(u => u.pseudo === CHEF_NAME)) {
            users.push({ pseudo: CHEF_NAME, mdp: "chef123", role: "chef", approved: true });
            saveAll();
        }
        if(posts.length === 0) {
            posts = [
                { id: 1, author: CHEF_NAME, content: "Bienvenue dans le clan ZETSU ! Seuls les membres approuvés peuvent parler ici. Respect et honneur 🔥", date: new Date().toLocaleString(), likes: [], comments: [] },
                { id: 2, author: "QUEEN ZETSU", content: "Que la force du chapeau de paille nous unisse. Postez vos exploits !", date: new Date().toLocaleString(), likes: [], comments: [] }
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
