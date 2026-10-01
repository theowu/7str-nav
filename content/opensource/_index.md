---
title: "开源神器"
description: "推荐好用的开源软件和工具"
---

<div style="position: sticky; top: 0; background: var(--entry); padding: 12px 0; z-index: 10;">
  <input id="search-input" type="text" placeholder="🔍 输入工具名搜索..."
    style="width: 100%; padding: 12px 16px; font-size: 1rem; border: 2px solid var(--primary); border-radius: 10px; outline: none; box-sizing: border-box;" />
</div>

<div id="article-list" style="margin-top: 1rem;">

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接1" title="5个必装的开源效率工具" date="2026-09-23" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接2" title="免费开源的本地AI部署方案" date="2026-09-11" >}}

{{< wx_article url="https://mp.weixin.qq.com/s/替换链接3" title="开源笔记软件推荐" date="2026-09-01" >}}

</div>

<p id="no-result" style="display:none; text-align:center; padding:2rem; color:var(--secondary);">
  未找到相关工具，试试其他关键词
</p>

<script>
const input = document.getElementById('search-input');
const list = document.getElementById('article-list');
const noResult = document.getElementById('no-result');
const cards = list.querySelectorAll('.sheet-card');
input.addEventListener('input', function() {
  const kw = this.value.trim().toLowerCase();
  let count = 0;
  cards.forEach(c => {
    const t = c.querySelector('.sheet-title').textContent.toLowerCase();
    c.style.display = t.includes(kw) ? '' : 'none';
    if (t.includes(kw)) count++;
  });
  noResult.style.display = count === 0 ? '' : 'none';
});
</script>
