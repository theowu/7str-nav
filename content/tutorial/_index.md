---
title: "魔法教程"
description: "各类创作教程分享"
disableHeader: true
---

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
  <div class="subpage-title">魔法教程</div>
  <button class="subpage-theme-btn" onclick="var h=document.documentElement;var c=h.getAttribute('data-theme')==='dark'?'light':'dark';h.setAttribute('data-theme',c);localStorage.setItem('theme',c)">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


{{< inpage-search placeholder="🔍 输入教程名搜索..." listId="article-list" resultId="no-result" >}}

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接1" title="如何用AI生成一首完整的歌曲" date="2026-09-22" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接2" title="AI视频制作完整流程" date="2026-09-10" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接3" title="本地部署Ollama完整指南" date="2026-09-01" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关教程，试试其他关键词
</p>
