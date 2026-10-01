---
title: "认知提升"
description: "思维方法和认知升级"
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
  <div class="subpage-title">认知提升</div>
  <button class="subpage-theme-btn" onclick="var h=document.documentElement;var c=h.getAttribute('data-theme')==='dark'?'light':'dark';h.setAttribute('data-theme',c);localStorage.setItem('theme',c)">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


{{< inpage-search placeholder="🔍 输入关键词搜索..." listId="article-list" resultId="no-result" >}}

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接1" title="费曼学习法实操指南" date="2026-09-21" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接2" title="如何建立自己的知识体系" date="2026-09-08" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接3" title="第一性原理思维应用" date="2026-08-30" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关内容，试试其他关键词
</p>
