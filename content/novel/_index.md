---
title: "连载小说"
description: "原创小说连载"
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
  <div class="subpage-title">连载小说</div>
  <button class="subpage-theme-btn" onclick="toggleTheme()">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


{{< inpage-search placeholder="🔍 输入章节名搜索..." listId="article-list" resultId="no-result" >}}

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接1" title="第1章：街角的琴声" date="2026-09-28" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接2" title="第2章：陌生人的吉他" date="2026-09-29" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接3" title="第3章：旧乐谱" date="2026-09-30" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关章节，试试其他关键词
</p>

---

## 🔒 付费章节

{{< paywall_notice title="第4章及以后为付费章节" >}}
后续章节为付费连载内容，购买后可解锁全部。
{{< /paywall_notice >}}

{{< buy_button url="https://mbd.pub/o/替换成你的小说合集链接" text="👉 购买完整版小说合集" >}}
