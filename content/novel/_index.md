---
title: "连载小说"
description: "原创小说连载"
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
  <div class="subpage-title">连载小说</div>
  <button class="subpage-theme-btn" onclick="var h=document.documentElement;var c=h.getAttribute('data-theme')==='dark'?'light':'dark';h.setAttribute('data-theme',c);localStorage.setItem('theme',c)">☀</button>
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
