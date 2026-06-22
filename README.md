# 🚀 AI Omni-Search | 主流 AI 划词搜索配置集

一套专为浏览器划词搜索扩展（如 Edge 划词搜索、Selection Search、PopClip 等）定制的 AI 快捷搜索配置串。一键导入，无缝切换当前最顶尖的 AI 助手。

---

## 📦 核心配置 (JSON)

请复制以下代码直接粘贴到你的划词扩展「自定义搜索引擎」或「JSON 导入」中：

```json
[
  { "name": "DeepSeek 划词搜", "keyword": "ds", "url": "[https://chat.deepseek.com/?q=%s](https://chat.deepseek.com/?q=%s)" },
  { "name": "通义千问 划词搜", "keyword": "qw", "url": "[https://tongyi.aliyun.com/qianwen/?q=%s](https://tongyi.aliyun.com/qianwen/?q=%s)" },
  { "name": "豆包 AI 划词搜", "keyword": "db", "url": "[https://www.doubao.com/chat/?q=%s](https://www.doubao.com/chat/?q=%s)" },
  { "name": "ChatGPT 划词搜", "keyword": "gpt", "url": "[https://chatgpt.com/?q=%s](https://chatgpt.com/?q=%s)" },
  { "name": "Gemini 划词搜", "keyword": "ge", "url": "[https://gemini.google.com/app?q=%s](https://gemini.google.com/app?q=%s)" }
]
