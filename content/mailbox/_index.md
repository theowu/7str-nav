---
title: "魔法信箱"
description: "留言和联系我"
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
  <div class="subpage-title">魔法信箱</div>
  <button class="subpage-theme-btn" onclick="toggleTheme()">☀</button>
  <div class="subpage-home-btn"><a href="/">🏠首页</a></div>
</div>


## 📮 联系我

有问题、建议或合作意向，欢迎通过以下方式联系：

- **公众号后台留言**：直接在公众号对话框发消息
- **邮件**：你的邮箱地址（替换成你自己的）

---

💡 也可以直接在公众号回复关键词获取对应内容：
- 回复「曲谱」→ 获取全部曲谱目录
- 回复「法语」→ 获取法语学习资料合集
- 回复「小说」→ 获取小说最新章节
