---
title: "连载小说"
description: "原创小说连载"
---

<div style="position: sticky; top: 0; background: var(--entry); padding: 12px 0; z-index: 10;">
  <input id="search-input" type="text" placeholder="🔍 输入章节名搜索..."
    style="width: 100%; padding: 12px 16px; font-size: 1rem; border: 2px solid var(--primary); border-radius: 10px; outline: none; box-sizing: border-box;" />
</div>

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
