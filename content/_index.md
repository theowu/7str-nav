---
title: "七弦万事屋地图"
layout: "home"
---

<style>
/* 头部容器：整行居中，减少上下边距 */
.header-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 100%;
  margin: 0.4rem 0 0.8rem !important;
  flex-wrap: wrap;
}
.site-title-text {
  font-size: 1.8rem;
  font-weight: bold;
}
.theme-toggle-btn {
  background: transparent;
  border: none;
  font-size:1.4rem;
  cursor:pointer;
  color:#fff;
}
.home-link-btn a{
  font-size:1.2rem;
}

/* 全局板块容器，减少板块之间的间距 */
.section-block{
  margin:1.2rem auto;
  text-align:center;
}
.section-title{
  font-size:1.2rem;
  margin-bottom:0.6rem;
}

/* Grid容器，桌面端；移动端媒体查询在下方 */
.section-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, 160px);
  justify-content: center;
  gap:12px;
}

/* 卡片统一尺寸 */
.grid-card {
  width: 160px;
  height: 90px;
  box-sizing: border-box;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  background:#2b2b2b;
  border-radius:14px;
  cursor:grab;
  transition: all 0.15s ease;
  user-select:none;
}
.grid-card:active{
  cursor:grabbing;
}
.grid-card:hover{
  background:#383838;
}
.grid-card-icon{
  font-size:1.6rem;
  margin-bottom:4px;
}
.grid-card-name{
  font-size:0.9rem;
}

/* 首页搜索框样式 */
.home-search-wrap{
  max-width:600px;
  margin:0 auto 1.2rem !important;
}
#home-search-input{
  width:100%;
  padding:12px 16px;
  border-radius:12px;
  border:none;
  background:#333;
  color:#fff;
  font-size:1rem;
  outline:none;
}
#home-search-input:focus{
  box-shadow:0 0 0 2px #555;
}
.no-match-tip{
  text-align:center;
  margin-top:0.6rem;
  opacity:0.7;
  display:none;
}

/* ===== 移动端：屏幕宽度小于768px，一行最多5张卡片 ===== */
@media (max-width:768px) {
  .section-grid {
    grid-template-columns: repeat(5, 1fr) !important;
    padding:0 8px;
  }
  .grid-card {
    width:100% !important;
    height:80px !important;
  }
  .site-title-text {
    font-size:1.4rem;
  }
}
</style>

<div class="header-wrap">
  <div class="site-title-text">七弦万事屋地图</div>
  <button class="theme-toggle-btn" onclick="document.documentElement.classList.toggle('dark')">☀</button>
  <div class="home-link-btn"><a href="/">🏠首页</a></div>
</div>

<div class="home-search-wrap">
  <input id="home-search-input" placeholder="🔍搜索栏目，长按拖拽可排序">
  <div class="no-match-tip" id="no-result">未找到匹配栏目</div>
</div>

<!-- 娱乐专栏 -->
<div class="section-block">
  <div class="section-title">🎮 娱乐专栏</div>
  <div class="section-grid" id="group-ent">
    <div class="grid-card" data-id="ent-music" data-keywords="AIGC音乐,ai音乐,音乐">
      <div class="grid-card-icon">🤖</div>
      <div class="grid-card-name">AIGC音乐</div>
      <a href="/aigc-music/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="ent-video" data-keywords="AIGC视频,ai视频,视频">
      <div class="grid-card-icon">🎬</div>
      <div class="grid-card-name">AIGC视频</div>
      <a href="/aigc-video/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="ent-game" data-keywords="精品游戏,游戏">
      <div class="grid-card-icon">🎮</div>
      <div class="grid-card-name">精品游戏</div>
      <a href="/game/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="ent-novel" data-keywords="连载小说,小说,故事">
      <div class="grid-card-icon">📖</div>
      <div class="grid-card-name">连载小说</div>
      <a href="/novel/" style="position:absolute;width:100%;height:100%"></a>
    </div>
  </div>
</div>

<!-- 学习空间 -->
<div class="section-block">
  <div class="section-title">📚 学习空间</div>
  <div class="section-grid" id="group-study">
    <div class="grid-card" data-id="study-tutorial" data-keywords="魔法教程,教程">
      <div class="grid-card-icon">📝</div>
      <div class="grid-card-name">魔法教程</div>
      <a href="/tutorial/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="study-fr" data-keywords="法语资讯,法语,fr">
      <div class="grid-card-icon">🇫🇷</div>
      <div class="grid-card-name">法语资讯</div>
      <a href="/french/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="study-fin" data-keywords="财经故事,财经">
      <div class="grid-card-icon">💰</div>
      <div class="grid-card-name">财经故事</div>
      <a href="/finance/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="study-think" data-keywords="认知提升,认知">
      <div class="grid-card-icon">🧠</div>
      <div class="grid-card-name">认知提升</div>
      <a href="/cognition/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="study-guitar" data-keywords="指弹吉他,吉他,曲谱">
      <div class="grid-card-icon">🎸</div>
      <div class="grid-card-name">指弹吉他</div>
      <a href="/guitar/" style="position:absolute;width:100%;height:100%"></a>
    </div>
  </div>
</div>

<!-- 魔法工具 -->
<div class="section-block">
  <div class="section-title">🔧 魔法工具</div>
  <div class="section-grid" id="group-tool">
    <div class="grid-card" data-id="tool-open" data-keywords="开源神器,开源,软件">
      <div class="grid-card-icon">🛠️</div>
      <div class="grid-card-name">开源神器</div>
      <a href="/opensource/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="tool-self" data-keywords="自制神器,自制">
      <div class="grid-card-icon">🔨</div>
      <div class="grid-card-name">自制神器</div>
      <a href="/self-made/" style="position:absolute;width:100%;height:100%"></a>
    </div>
    <div class="grid-card" data-id="tool-mail" data-keywords="魔法信箱,信箱">
      <div class="grid-card-icon">📮</div>
      <div class="grid-card-name">魔法信箱</div>
      <a href="/mailbox/" style="position:absolute;width:100%;height:100%"></a>
    </div>
  </div>
</div>

<p style="text-align:center; margin-top:2rem; opacity:0.6; font-size:0.9rem;">© 2026 七弦万事屋地图 · Powered by Hugo & PaperMod</p>

<script src="https://cdn.jsdelivr.net/npm/sortablejs@1.15.0/Sortable.min.js"></script>
<script>
// 分组ID列表
const groups = ["group-ent","group-study","group-tool"];
// 初始化拖拽+读取本地存储
groups.forEach(gid=>{
  const el = document.getElementById(gid);
  const storageKey = `sort_${gid}`;
  let savedOrder = localStorage.getItem(storageKey);
  if(savedOrder){
    savedOrder = JSON.parse(savedOrder);
    const frag = document.createDocumentFragment();
    savedOrder.forEach(id=>{
      const item = el.querySelector(`[data-id="${id}"]`);
      if(item) frag.appendChild(item);
    })
    el.appendChild(frag);
  }
  new Sortable(el, {
    animation:150,
    delay:200, //长按200ms触发拖拽，防止误触点击
    touchStartThreshold:5,
    ghostClass:"sort-ghost",
    onEnd(evt){
      const order = Array.from(el.querySelectorAll('.grid-card')).map(item=>item.dataset.id);
      localStorage.setItem(storageKey, JSON.stringify(order));
    }
  })
})

// 首页搜索过滤
const searchInput = document.getElementById("home-search-input");
const noResult = document.getElementById("no-result");
searchInput.oninput = function(){
  const kw = this.value.trim().toLowerCase();
  let hasAny = false;
  document.querySelectorAll('.grid-card').forEach(card=>{
    const keys = card.dataset.keywords.toLowerCase();
    const match = keys.includes(kw);
    card.style.display = kw ? (match ? "flex":"none") : "flex";
    if(match) hasAny=true;
  })
  noResult.style.display = (kw && !hasAny) ? "block":"none";
}
</script>
