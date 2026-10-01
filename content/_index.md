---
title: "首页"
---

<div style="position: sticky; top: 0; background: var(--entry); padding: 16px 0; z-index: 10; margin: -8px -0 0;">
  <input id="home-search" type="text" placeholder="🔍 搜索栏目或内容，如：吉他、小说、AI..."
    style="width: 100%; padding: 14px 18px; font-size: 1.05rem; border: 2px solid var(--primary); border-radius: 12px; outline: none; box-sizing: border-box;" />
</div>

<div id="category-list" style="margin-top: 1.5rem;">

## 🎮 娱乐专栏

<div class="cat-card" data-keywords="AI 音乐 歌曲 aigc-music">
<a class="sheet-card" href="/aigc-music/">
  <div class="sheet-title">🤖 AIGC音乐</div>
  <div class="sheet-meta">AI生成的音乐作品</div>
</a>
</div>

<div class="cat-card" data-keywords="AI 视频 aigc-video">
<a class="sheet-card" href="/aigc-video/">
  <div class="sheet-title">🎬 AIGC视频</div>
  <div class="sheet-meta">AI生成的视频作品</div>
</a>
</div>

<div class="cat-card" data-keywords="游戏 game 推荐">
<a class="sheet-card" href="/game/">
  <div class="sheet-title">🎮 精品游戏</div>
  <div class="sheet-meta">游戏推荐和体验分享</div>
</a>
</div>

<div class="cat-card" data-keywords="小说 连载 novel 故事">
<a class="sheet-card" href="/novel/">
  <div class="sheet-title">📖 连载小说</div>
  <div class="sheet-meta">原创小说连载</div>
</a>
</div>

## 📚 学习空间

<div class="cat-card" data-keywords="吉他 指弹 曲谱 guitar">
<a class="sheet-card" href="/guitar/">
  <div class="sheet-title">🎸 指弹吉他</div>
  <div class="sheet-meta">指弹曲谱分享</div>
</a>
</div>

<div class="cat-card" data-keywords="教程 教学 魔法 tutorial">
<a class="sheet-card" href="/tutorial/">
  <div class="sheet-title">📝 魔法教程</div>
  <div class="sheet-meta">各类创作教程</div>
</a>
</div>

<div class="cat-card" data-keywords="法语 french 语言 学习">
<a class="sheet-card" href="/french/">
  <div class="sheet-title">🇫🇷 法语资讯</div>
  <div class="sheet-meta">法语学习素材</div>
</a>
</div>

<div class="cat-card" data-keywords="财经 基金 股票 理财 finance">
<a class="sheet-card" href="/finance/">
  <div class="sheet-title">💰 财经故事</div>
  <div class="sheet-meta">财经知识和故事</div>
</a>
</div>

<div class="cat-card" data-keywords="认知 思维 学习方法 cognition">
<a class="sheet-card" href="/cognition/">
  <div class="sheet-title">🧠 认知提升</div>
  <div class="sheet-meta">思维方法和认知升级</div>
</a>
</div>

## 🔧 魔法工具

<div class="cat-card" data-keywords="开源 软件 工具 opensource">
<a class="sheet-card" href="/opensource/">
  <div class="sheet-title">🛠️ 开源神器</div>
  <div class="sheet-meta">推荐好用的开源软件</div>
</a>
</div>

<div class="cat-card" data-keywords="自制 自己开发 homemade 工具">
<a class="sheet-card" href="/homemade/">
  <div class="sheet-title">🔨 自制神器</div>
  <div class="sheet-meta">自己开发的工具</div>
</a>
</div>

<div class="cat-card" data-keywords="联系 留言 信箱 邮箱 mailbox">
<a class="sheet-card" href="/mailbox/">
  <div class="sheet-title">📮 魔法信箱</div>
  <div class="sheet-meta">留言和联系我</div>
</a>
</div>

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关栏目，试试其他关键词
</p>

<script>
const input = document.getElementById('home-search');
const list = document.getElementById('category-list');
const noResult = document.getElementById('no-result');
const cards = list.querySelectorAll('.cat-card');

input.addEventListener('input', function() {
  const kw = this.value.trim().toLowerCase();
  let count = 0;
  cards.forEach(card => {
    const keywords = (card.dataset.keywords + ' ' + card.textContent).toLowerCase();
    if (keywords.includes(kw)) {
      card.style.display = '';
      count++;
    } else {
      card.style.display = 'none';
    }
  });
  noResult.style.display = count === 0 ? '' : 'none';
});
</script>
