---
title: "AIGC音乐"
description: "AI生成的音乐作品"
disableHeader: true
---

<style>
.subpage-header-wrap {
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
.subpage-title {
  font-size: 1.8rem;
  font-weight: bold;
}
.subpage-theme-btn {
  background: transparent;
  border: none;
  font-size: 1.3rem;
  cursor: pointer;
}
.subpage-home-btn a {
  font-size: 1.1rem;
}
</style>

<div class="subpage-header-wrap">
  <div class="subpage-title">AIGC音乐</div>
  <button class="subpage-theme-btn" onclick="var h=document.documentElement;var c=h.getAttribute('data-theme')==='dark'?'light':'dark';h.setAttribute('data-theme',c);localStorage.setItem('theme',c)">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


{{< inpage-search placeholder="🔍 输入歌名搜索..." listId="article-list" resultId="no-result" >}}

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接1" title="AI生成指弹风格纯音乐《黄昏》" date="2026-10-01" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接2" title="AI生成Lo-fi放松音乐合集" date="2026-09-20" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接3" title="AI生成钢琴曲《月光》" date="2026-09-10" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关内容，试试其他关键词
</p>
