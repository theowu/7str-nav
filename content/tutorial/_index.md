---
title: "魔法教程"
description: "各类创作教程分享"
disableHeader: true
---

<style>
.subpage-header-wrap {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  width: 100%;
  margin: 0.4rem 0 0.8rem;
}
.subpage-title {
  grid-column: 2;
  font-size: 1.4rem;
  font-weight: bold;
  text-align: center;
}
.subpage-home-btn {
  grid-column: 3;
  justify-self: end;
}
.subpage-home-btn a {
  font-size: 1.1rem;
}
</style>

<div class="subpage-header-wrap">
  <div class="subpage-title">魔法教程</div>
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
