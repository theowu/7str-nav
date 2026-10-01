---
title: "七弦万事屋藏宝图"
---

<script>
// 页面加载前立即读取主题，避免闪烁
(function(){
  var t = localStorage.getItem('theme');
  if(t === 'dark'){
    document.documentElement.setAttribute('data-theme','dark');
    document.documentElement.classList.add('dark');
  }
})();
</script>

<style>
body { padding-top: 0 !important; }
.main, .post, .page { padding-top: 0 !important; }

header.site-header, #site-header, .header { display: none !important; }

.header-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 100%;
  max-width: 1200px;
  margin: 0.2rem auto 0.5rem;
  flex-wrap: wrap;
  padding: 0 8px;
  box-sizing: border-box;
}
.site-title-text { font-size: 1.8rem; font-weight: bold; }
.theme-toggle-btn { background: transparent; border: none; font-size: 1.3rem; cursor: pointer; }
.home-link-btn a { font-size: 1.1rem; }

.section-block {
  margin: 0.8rem auto;
  text-align: center;
  max-width: 1200px;
  padding: 0 8px;
  box-sizing: border-box;
}
.section-title { font-size: 1.1rem; margin-bottom: 0.4rem; }

.section-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 12px;
}

.grid-card {
  width: 100%;
  height: 80px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: var(--tertiary);
  border-radius: 14px;
  cursor: grab;
  transition: all 0.15s ease;
  user-select: none;
  overflow: hidden;
  padding-top: 6px;
  touch-action: none;
}
.grid-card:active { cursor: grabbing; }
.grid-card:hover { background: var(--border); }
.grid-card.dragging { opacity: 0.5; }
.grid-card-icon { font-size: 1.4rem; margin-bottom: 3px; line-height: 1; }
.grid-card-name { font-size: 0.85rem; text-align: center; white-space: nowrap; }

.drag-ghost {
  position: fixed;
  z-index: 9999;
  pointer-events: none;
  opacity: 0.9;
  transform: rotate(3deg);
  box-shadow: 0 8px 24px rgba(0,0,0,0.3);
  border-radius: 14px;
}

.home-search-wrap {
  width: 100%;
  max-width: 1200px;
  margin: 0.3rem auto 0.6rem;
  padding: 0 8px;
  box-sizing: border-box;
}
#home-search-input {
  width: 100%;
  padding: 10px 16px;
  border-radius: 12px;
  border: 1.5px solid var(--border);
  background: var(--tertiary);
  color: var(--primary);
  font-size: 1rem;
  outline: none;
  box-sizing: border-box;
}
.no-match-tip { text-align: center; margin-top: 0.4rem; opacity: 0.7; display: none; }

@media (max-width: 768px) {
  .section-grid { grid-template-columns: repeat(5, 1fr); gap: 8px; }
  .grid-card { height: 68px; }
  .site-title-text { font-size: 1.3rem; }
  .grid-card-icon { font-size: 1.15rem; margin-bottom: 2px; }
  .grid-card-name { font-size: 0.63rem; white-space: nowrap; }
  .header-wrap { gap: 0.6rem; margin: 0.15rem auto 0.3rem; }
  .home-link-btn a { font-size: 0.95rem; }
}
</style>

<div class="header-wrap">
  <div class="site-title-text">七弦万事屋藏宝图</div>
  <button class="theme-toggle-btn" onclick="toggleTheme()">☀</button>
  <div class="home-link-btn"><a href="/">🏠首页</a></div>
</div>

<div class="home-search-wrap">
  <input id="home-search-input" placeholder="🔍 搜索栏目，长按拖拽可排序">
  <div class="no-match-tip" id="no-result">未找到匹配栏目</div>
</div>

<div class="section-block">
  <div class="section-title">🎮 娱乐专栏</div>
  <div class="section-grid" id="group-ent">
    <div class="grid-card" data-id="ent-music" data-keywords="AIGC音乐 ai音乐 音乐" data-link="/aigc-music/">
      <div class="grid-card-icon">🤖</div>
      <div class="grid-card-name">AIGC音乐</div>
    </div>
    <div class="grid-card" data-id="ent-video" data-keywords="AIGC视频 ai视频 视频" data-link="/aigc-video/">
      <div class="grid-card-icon">🎬</div>
      <div class="grid-card-name">AIGC视频</div>
    </div>
    <div class="grid-card" data-id="ent-game" data-keywords="精品游戏 游戏" data-link="/game/">
      <div class="grid-card-icon">🎮</div>
      <div class="grid-card-name">精品游戏</div>
    </div>
    <div class="grid-card" data-id="ent-novel" data-keywords="连载小说 小说 故事" data-link="/novel/">
      <div class="grid-card-icon">📖</div>
      <div class="grid-card-name">连载小说</div>
    </div>
  </div>
</div>

<div class="section-block">
  <div class="section-title">📚 学习空间</div>
  <div class="section-grid" id="group-study">
    <div class="grid-card" data-id="study-tutorial" data-keywords="魔法教程 教程" data-link="/tutorial/">
      <div class="grid-card-icon">📝</div>
      <div class="grid-card-name">魔法教程</div>
    </div>
    <div class="grid-card" data-id="study-fr" data-keywords="法语资讯 法语" data-link="/french/">
      <div class="grid-card-icon">🇫🇷</div>
      <div class="grid-card-name">法语资讯</div>
    </div>
    <div class="grid-card" data-id="study-fin" data-keywords="财经故事 财经" data-link="/finance/">
      <div class="grid-card-icon">💰</div>
      <div class="grid-card-name">财经故事</div>
    </div>
    <div class="grid-card" data-id="study-think" data-keywords="认知提升 认知" data-link="/cognition/">
      <div class="grid-card-icon">🧠</div>
      <div class="grid-card-name">认知提升</div>
    </div>
    <div class="grid-card" data-id="study-guitar" data-keywords="指弹吉他 吉他 曲谱" data-link="/guitar/">
      <div class="grid-card-icon">🎸</div>
      <div class="grid-card-name">指弹吉他</div>
    </div>
  </div>
</div>

<div class="section-block">
  <div class="section-title">🔧 魔法工具</div>
  <div class="section-grid" id="group-tool">
    <div class="grid-card" data-id="tool-open" data-keywords="开源神器 开源 软件" data-link="/opensource/">
      <div class="grid-card-icon">🛠️</div>
      <div class="grid-card-name">开源神器</div>
    </div>
    <div class="grid-card" data-id="tool-self" data-keywords="自制神器 自制" data-link="/homemade/">
      <div class="grid-card-icon">🔨</div>
      <div class="grid-card-name">自制神器</div>
    </div>
    <div class="grid-card" data-id="tool-mail" data-keywords="魔法信箱 信箱" data-link="/mailbox/">
      <div class="grid-card-icon">📮</div>
      <div class="grid-card-name">魔法信箱</div>
    </div>
  </div>
</div>

<p style="text-align:center; margin-top:0.8rem; opacity:0.5; font-size:0.78rem;">© 2026 七弦万事屋藏宝图</p>

<script>
// 主题切换函数（全局，所有页面共享逻辑）
function toggleTheme() {
  var h = document.documentElement;
  var isDark = h.getAttribute('data-theme') === 'dark';
  var newTheme = isDark ? 'light' : 'dark';
  h.setAttribute('data-theme', newTheme);
  h.classList.toggle('dark', !isDark);
  localStorage.setItem('theme', newTheme);
}

// 原生拖拽实现（touch + mouse统一用Pointer Events）
function setupDrag(el, storageKey) {
  var dragEl = null, ghost = null, startX = 0, startY = 0, moved = false, longPressTimer = null, isTouch = false;

  // 恢复保存的顺序
  var saved = localStorage.getItem(storageKey);
  if (saved) {
    var ids = JSON.parse(saved);
    var frag = document.createDocumentFragment();
    ids.forEach(function(id) {
      var item = el.querySelector('[data-id="' + id + '"]');
      if (item) frag.appendChild(item);
    });
    el.appendChild(frag);
  }

  function createGhost(card) {
    var rect = card.getBoundingClientRect();
    ghost = card.cloneNode(true);
    ghost.className = 'grid-card drag-ghost';
    ghost.style.width = rect.width + 'px';
    ghost.style.height = rect.height + 'px';
    ghost.style.left = rect.left + 'px';
    ghost.style.top = rect.top + 'px';
    document.body.appendChild(ghost);
    card.classList.add('dragging');
  }

  function moveGhost(x, y) {
    if (!ghost) return;
    ghost.style.left = (x - ghost.offsetWidth / 2) + 'px';
    ghost.style.top = (y - ghost.offsetHeight / 2) + 'px';
    var under = document.elementFromPoint(x, y);
    var underCard = under ? under.closest('.grid-card') : null;
    if (underCard && underCard !== dragEl && !underCard.classList.contains('dragging')) {
      var rect = underCard.getBoundingClientRect();
      var cx = rect.left + rect.width / 2;
      if (x < cx) el.insertBefore(dragEl, underCard);
      else el.insertBefore(dragEl, underCard.nextSibling);
    }
  }

  function endDrag() {
    clearTimeout(longPressTimer);
    if (ghost) {
      ghost.remove();
      ghost = null;
      dragEl.classList.remove('dragging');
      var order = Array.from(el.querySelectorAll('.grid-card')).map(function(c) { return c.dataset.id; });
      localStorage.setItem(storageKey, JSON.stringify(order));
    }
    var wasMoved = moved;
    var card = dragEl;
    dragEl = null;
    ghost = null;
    moved = false;
    return { wasMoved: wasMoved, card: card };
  }

  el.addEventListener('pointerdown', function(e) {
    var card = e.target.closest('.grid-card');
    if (!card) return;
    isTouch = (e.pointerType === 'touch');
    startX = e.clientX;
    startY = e.clientY;
    moved = false;
    dragEl = card;

    if (isTouch) {
      longPressTimer = setTimeout(function() {
        createGhost(dragEl);
        if (e.cancelable) e.preventDefault();
      }, 200);
    }
    // PC端不立即创建ghost，等pointermove移动后才创建
  });

  el.addEventListener('pointermove', function(e) {
    if (!dragEl) return;
    var dx = e.clientX - startX;
    var dy = e.clientY - startY;

    // PC端：移动超过5px后创建ghost开始拖拽
    if (!ghost && !isTouch && (Math.abs(dx) > 5 || Math.abs(dy) > 5)) {
      createGhost(dragEl);
      moved = true;
    }

    if (!ghost && Math.abs(dx) < 5 && Math.abs(dy) < 5) return;

    if (isTouch && !ghost) {
      clearTimeout(longPressTimer);
      return;
    }

    if (ghost) {
      moved = true;
      moveGhost(e.clientX, e.clientY);
      if (e.cancelable) e.preventDefault();
    }
  });

  el.addEventListener('pointerup', function(e) {
    var result = endDrag();
    if (!result.wasMoved && result.card) {
      var link = result.card.getAttribute('data-link');
      if (link) location.href = link;
    }
  });

  el.addEventListener('pointercancel', function() { endDrag(); });
}

// 初始化三个分组
setupDrag(document.getElementById('group-ent'), 'sort_group-ent');
setupDrag(document.getElementById('group-study'), 'sort_group-study');
setupDrag(document.getElementById('group-tool'), 'sort_group-tool');

// 搜索
var searchInput = document.getElementById('home-search-input');
var noResult = document.getElementById('no-result');
searchInput.oninput = function() {
  var kw = this.value.trim().toLowerCase();
  var hasAny = false;
  document.querySelectorAll('.grid-card').forEach(function(card) {
    var keys = card.dataset.keywords.toLowerCase();
    var match = keys.includes(kw);
    card.style.display = kw ? (match ? 'flex' : 'none') : 'flex';
    if (match) hasAny = true;
  });
  noResult.style.display = (kw && !hasAny) ? 'block' : 'none';
};
</script>
