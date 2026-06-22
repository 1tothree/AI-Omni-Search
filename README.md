# 🚀 AI Omni-Search | Chrome 浏览器地址栏 & 划词 AI 搜索 V1.0

桌面浏览器AI 模型网页版搜索配置串：
通过浏览器地址栏通过输入简写（如 `qw`）快速呼叫 AI，或者鼠标划词一键搜索选中文本。

祝大家用的愉快，玩的开心(^o^)
---

## 📦 核心配置数据

### 方案 A：浏览器设置直达
（注：千问、豆包免扩展，原生支持；ds、哈吉米需要油猴脚本辅助；gpt仅支持搜索内容填充对话框）

 Chrome  `设置` -> `搜索引擎` -> `管理搜索引擎和网站搜索` 中，点击 **「网站搜索」** 旁的 **添加**，将以下表格中的内容逐一填入：

| 搜索引擎名称 | 快捷字词 (Keyword) | 网址格式（用 `%s` 代替搜索字词） |
| :--- | :---: | :--- |
| 通义千问  | `qw` | `https://tongyi.aliyun.com/qianwen/?q=%s` |
| 豆包 | `db` | `https://www.doubao.com/chat/url-action?action={"pluginId":"Send_Message","payload":{"text":"%s"}}` |
| DeepSeek  | `ds` | `https://chat.deepseek.com/?q=%s` |
| ChatGPT | `gpt` | `https://chatgpt.com/?q=%s` |
| Gemini | `ge` | `https://gemini.google.com/app?q=%s` |

### 方案 B：第三方划词扩展导入 (JSON 数组格式)

如果你使用的是支持 JSON 批量导入的 Chrome 划词扩展（如 *Selection Search*、*沙拉查词*、*Glance Search* 等），可以直接复制以下代码块：

```json
  { "name": "通义千问 划词搜", "keyword": "qw", "url": "[https://tongyi.aliyun.com/qianwen/?q=%s](https://tongyi.aliyun.com/qianwen/?q=%s)" },
  { "name": "豆包 AI 划词搜", "keyword": "db", "url": "[https://www.doubao.com/chat/?q=%s](https://www.doubao.com/chat/?q=%s)" }](https://www.doubao.com/chat/url-action?action={"pluginId":"Send_Message","payload":{"text":"%s"}}),
  { "name": "DeepSeek 划词搜", "keyword": "ds", "url": "[https://chat.deepseek.com/?q=%s](https://chat.deepseek.com/?q=%s)" },
  { "name": "ChatGPT 划词搜", "keyword": "gpt", "url": "[https://chatgpt.com/?q=%s](https://chatgpt.com/?q=%s)" },
  { "name": "Gemini 划词搜", "keyword": "ge", "url": "[https://gemini.google.com/app?q=%s](https://gemini.google.com/app?q=%s)" }


