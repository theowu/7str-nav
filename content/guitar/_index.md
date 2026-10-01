---
title: "指弹吉他"
description: "指弹吉他曲谱目录，支持搜索"
disableHeader: true
---


<script>
(function(){
  var t = localStorage.getItem('theme');
  if(t === 'dark'){
    document.documentElement.classList.add('dark');
    document.documentElement.setAttribute('data-theme','dark');
  } else {
    document.documentElement.classList.remove('dark');
    document.documentElement.setAttribute('data-theme','light');
  }
})();
function toggleTheme() {
  var h = document.documentElement;
  var isDark = h.classList.contains('dark');
  h.classList.toggle('dark', !isDark);
  h.setAttribute('data-theme', !isDark ? 'dark' : 'light');
  localStorage.setItem('theme', !isDark ? 'dark' : 'light');
}
</script>
<style>
body { padding-top: 0 !important; }
.main, .post, .page { padding-top: 0 !important; }

.subpage-header-wrap {
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
.subpage-title { font-size: 1.8rem; font-weight: bold; }
.subpage-theme-btn { background: transparent; border: none; font-size: 1.3rem; cursor: pointer; }
.subpage-home-btn a { font-size: 1.1rem; }

.sub-search-wrap {
  width: 100%;
  max-width: 1200px;
  margin: 0.3rem auto 0.6rem;
  padding: 0 8px;
  box-sizing: border-box;
}
.sub-search-wrap input {
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

.search-wrap {
  width: 100% !important;
  max-width: 1200px !important;
  margin: 0.3rem auto 0.6rem !important;
  padding: 0 8px !important;
  box-sizing: border-box !important;
}
.search-wrap input {
  width: 100% !important;
  padding: 10px 16px !important;
  border-radius: 12px !important;
  border: 1.5px solid var(--border) !important;
  background: var(--tertiary) !important;
  color: var(--primary) !important;
  font-size: 1rem !important;
  outline: none !important;
  box-sizing: border-box !important;
}
</style>

<div class="subpage-header-wrap">
  <div class="subpage-title">指弹吉他</div>
  <button class="subpage-theme-btn" onclick="toggleTheme()">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


{{< inpage-search placeholder="🔍 输入歌曲名搜索..." listId="article-list" resultId="no-result" >}}

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换成你的文章链接1" title="《枫叶城》指弹谱" difficulty="★★★" date="2026-10-01" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换成你的文章链接2" title="《流行的云》指弹谱" difficulty="★★☆" date="2026-09-15" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换成你的文章链接3" title="《花》指弹谱" difficulty="★★☆" date="2026-09-10" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换成你的文章链接4" title="《黄昏》指弹谱" difficulty="★★★" date="2026-09-01" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换成你的文章链接5" title="《风之诗》指弹谱" difficulty="★★☆" date="2026-08-25" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关曲谱，试试其他关键词
</p>

---

## 🔒 完整版获取

部分曲谱提供免费预览，完整版PDF可通过下方按钮购买：

{{< buy_button url="https://mbd.pub/o/替换成你的曲谱合集链接" text="👉 查看全部曲谱合集" >}}
