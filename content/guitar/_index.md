---
title: "指弹吉他"
description: "指弹吉他曲谱目录，支持搜索"
---

<div style="position: sticky; top: 0; background: var(--entry); padding: 12px 0; z-index: 10;">
  <input
    id="song-search"
    type="text"
    placeholder="🔍 输入歌曲名搜索..."
    style="width: 100%; padding: 12px 16px; font-size: 1rem; border: 2px solid var(--primary); border-radius: 10px; outline: none; box-sizing: border-box;"
  />
</div>

<div id="song-list" style="margin-top: 1rem;">

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

<script>
const input = document.getElementById('song-search');
const list = document.getElementById('song-list');
const noResult = document.getElementById('no-result');
const cards = list.querySelectorAll('.sheet-card');

input.addEventListener('input', function() {
  const keyword = this.value.trim().toLowerCase();
  let count = 0;

  cards.forEach(card => {
    const title = card.querySelector('.sheet-title').textContent.toLowerCase();
    if (title.includes(keyword)) {
      card.style.display = '';
      count++;
    } else {
      card.style.display = 'none';
    }
  });

  noResult.style.display = count === 0 ? '' : 'none';
});
</script>
