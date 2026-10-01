---
title: "七弦万事屋藏宝图"
---

<style>
/* 隐藏PaperMod原生头部，消除重复标题 */
header.site-header,
#site-header,
.header {
  display: none !important;
}

/* 头部容器：整行居中，和grid对齐宽度 */
.header-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 100%;
  max-width: 1200px;
  margin: 0.4rem auto 0.8rem;
  flex-wrap: wrap;
  padding: 0 8px;
  box-sizing: border-box;
}
.site-title-text {
  font-size: 1.8rem;
  font-weight: bold;
}
.theme-toggle-btn {
  background: transparent;
  border: none;
  font-size: 1.3rem;
  cursor: pointer;
}
.home-link-btn a {
  font-size: 1.1rem;
}

/* 板块容器：和搜索框同宽对齐 */
.section-block {
  margin: 1.2rem auto;
  text-align: center;
  max-width: 1200px;
  padding: 0 8px;
  box-sizing: border-box;
}
.section-title {
  font-size: 1.1rem;
  margin-bottom: 0.6rem;
}

/* 桌面端：一行固定5列，卡片自动伸缩填充 */
.section-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  justify-content: center;
  gap: 12px;
}

/* 卡片：修复文字溢出 */
.grid-card {
  width: 100%;
  height: 90px;
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
  padding-top: 8px;
}
.grid-card:active { cursor: grabbing; }
.grid-card:hover { background: var(--border); }
.grid-card-icon { font-size: 1.5rem; margin-bottom: 6px; margin-top: 4px; line-height: 1; }
.grid-card-name { font-size: 0.85rem; text-align: center; white-space: nowrap; }

/* 搜索框：和grid对齐宽度 */
.home-search-wrap {
  width: 100%;
  max-width: 1200px;
  margin: 0.4rem auto 1.2rem;
  padding: 0 8px;
  box-sizing: border-box;
}
#home-search-input {
  width: 100%;
  padding: 12px 16px;
  border-radius: 12px;
  border: 1.5px solid var(--border);
  background: var(--tertiary);
  color: var(--primary);
  font-size: 1rem;
  outline: none;
  box-sizing: border-box;
}
#home-search-input:focus {
  border-color: var(--primary);
}
.no-match-tip {
  text-align: center;
  margin-top: 0.6rem;
  opacity: 0.7;
  display: none;
}

/* 移动端：一行5张卡片 */
@media (max-width: 768px) {
  .section-grid {
    grid-template-columns: repeat(5, 1fr);
    padding: 0 8px;
    gap: 8px;
  }
  .grid-card {
    width: 100%;
    height: 80px;
  }
  .site-title-text { font-size: 1.3rem; }
  .grid-card-icon { font-size: 1.2rem; margin-bottom: 5px; }
  .grid-card-name { font-size: 0.65rem; white-space: nowrap; }
}
</style>

<div class="header-wrap">
  <div class="site-title-text">七弦万事屋藏宝图</div>
  <button class="theme-toggle-btn" onclick="var h=document.documentElement;var c=h.getAttribute('data-theme')==='dark'?'light':'dark';h.setAttribute('data-theme',c);localStorage.setItem('theme',c)">☀</button>
  <div class="home-link-btn"><a href="/">🏠首页</a></div>
</div>

<div class="home-search-wrap">
  <input id="home-search-input" placeholder="🔍 搜索栏目，长按拖拽可排序">
  <div class="no-match-tip" id="no-result">未找到匹配栏目</div>
</div>

<!-- 娱乐专栏 -->
<div class="section-block">
  <div class="section-title">🎮 娱乐专栏</div>
  <div class="section-grid" id="group-ent">
    <div class="grid-card" data-id="ent-music" data-keywords="AIGC音乐 ai音乐 音乐" onclick="location.href='/aigc-music/'">
      <div class="grid-card-icon">🤖</div>
      <div class="grid-card-name">AIGC音乐</div>
    </div>
    <div class="grid-card" data-id="ent-video" data-keywords="AIGC视频 ai视频 视频" onclick="location.href='/aigc-video/'">
      <div class="grid-card-icon">🎬</div>
      <div class="grid-card-name">AIGC视频</div>
    </div>
    <div class="grid-card" data-id="ent-game" data-keywords="精品游戏 游戏" onclick="location.href='/game/'">
      <div class="grid-card-icon">🎮</div>
      <div class="grid-card-name">精品游戏</div>
    </div>
    <div class="grid-card" data-id="ent-novel" data-keywords="连载小说 小说 故事" onclick="location.href='/novel/'">
      <div class="grid-card-icon">📖</div>
      <div class="grid-card-name">连载小说</div>
    </div>
  </div>
</div>

<!-- 学习空间 -->
<div class="section-block">
  <div class="section-title">📚 学习空间</div>
  <div class="section-grid" id="group-study">
    <div class="grid-card" data-id="study-tutorial" data-keywords="魔法教程 教程" onclick="location.href='/tutorial/'">
      <div class="grid-card-icon">📝</div>
      <div class="grid-card-name">魔法教程</div>
    </div>
    <div class="grid-card" data-id="study-fr" data-keywords="法语资讯 法语" onclick="location.href='/french/'">
      <div class="grid-card-icon">🇫🇷</div>
      <div class="grid-card-name">法语资讯</div>
    </div>
    <div class="grid-card" data-id="study-fin" data-keywords="财经故事 财经" onclick="location.href='/finance/'">
      <div class="grid-card-icon">💰</div>
      <div class="grid-card-name">财经故事</div>
    </div>
    <div class="grid-card" data-id="study-think" data-keywords="认知提升 认知" onclick="location.href='/cognition/'">
      <div class="grid-card-icon">🧠</div>
      <div class="grid-card-name">认知提升</div>
    </div>
    <div class="grid-card" data-id="study-guitar" data-keywords="指弹吉他 吉他 曲谱" onclick="location.href='/guitar/'">
      <div class="grid-card-icon">🎸</div>
      <div class="grid-card-name">指弹吉他</div>
    </div>
  </div>
</div>

<!-- 魔法工具 -->
<div class="section-block">
  <div class="section-title">🔧 魔法工具</div>
  <div class="section-grid" id="group-tool">
    <div class="grid-card" data-id="tool-open" data-keywords="开源神器 开源 软件" onclick="location.href='/opensource/'">
      <div class="grid-card-icon">🛠️</div>
      <div class="grid-card-name">开源神器</div>
    </div>
    <div class="grid-card" data-id="tool-self" data-keywords="自制神器 自制" onclick="location.href='/homemade/'">
      <div class="grid-card-icon">🔨</div>
      <div class="grid-card-name">自制神器</div>
    </div>
    <div class="grid-card" data-id="tool-mail" data-keywords="魔法信箱 信箱" onclick="location.href='/mailbox/'">
      <div class="grid-card-icon">📮</div>
      <div class="grid-card-name">魔法信箱</div>
    </div>
  </div>
</div>

<p style="text-align:center; margin-top:2rem; opacity:0.6; font-size:0.85rem;">© 2026 七弦万事屋藏宝图</p>

<script src="https://cdn.jsdelivr.net/npm/sortablejs@1.15.0/Sortable.min.js"></script>
<script>
function toggleTheme() {
  const t = document.getElementById("dark-mode-toggle");
  if (t) { t.click(); return; }
  const html = document.documentElement;
  html.classList.toggle("dark");
  localStorage.setItem("theme", html.classList.contains("dark") ? "dark" : "light");
}

const groups = ["group-ent", "group-study", "group-tool"];
groups.forEach(function(gid) {
  const el = document.getElementById(gid);
  const storageKey = "sort_" + gid;
  const savedOrder = localStorage.getItem(storageKey);
  if (savedOrder) {
    const ids = JSON.parse(savedOrder);
    const frag = document.createDocumentFragment();
    ids.forEach(function(id) {
      const item = el.querySelector('[data-id="' + id + '"]');
      if (item) frag.appendChild(item);
    });
    el.appendChild(frag);
  }
  new Sortable(el, {
    animation: 150,
    delay: 200,
    touchStartThreshold: 5,
    forceFallback: true,
    fallbackOnBody: true,
    ghostClass: "sort-ghost",
    onEnd: function() {
      const order = Array.from(el.querySelectorAll('.grid-card')).map(function(c) { return c.dataset.id; });
      localStorage.setItem(storageKey, JSON.stringify(order));
    }
  });
});

const searchInput = document.getElementById("home-search-input");
const noResult = document.getElementById("no-result");
searchInput.oninput = function() {
  const kw = this.value.trim().toLowerCase();
  let hasAny = false;
  document.querySelectorAll('.grid-card').forEach(function(card) {
    const keys = card.dataset.keywords.toLowerCase();
    const match = keys.includes(kw);
    card.style.display = kw ? (match ? "flex" : "none") : "flex";
    if (match) hasAny = true;
  });
  noResult.style.display = (kw && !hasAny) ? "block" : "none";
};
</script>
