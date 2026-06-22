# 🚀 AI Omni-Search | 浏览器地址栏 & 划词 AI 搜索 V1.0

通过地址栏通过输入简写（如 `qw+空格+内容`）或者鼠标划词选中网页文本 ，快速呼叫 AI。

祝大家用的愉快，玩的开心(^o^)，帮我点一下右边的★， 让更多人看到。

>Quickly summon AI by typing shortcuts in the address bar (e.g., qw + Space + Content) or by selecting text on a webpage with your mouse.
Have fun and enjoy using it! (^o^) If you find this helpful, please drop a ★ (Star) on the top right to make it visible to more people.

---

## 📦 核心配置数据

### 方案 A：浏览器设置直达 Direct Browser Settings
（注：千问、豆包免扩展，ds+油猴、哈吉米+油猴、GPT+油猴 支持一键直达结果；gpt免扩展仅支持搜索内容填充对话框）
>(Note: Qianwen and Doubao natively support auto-sending without extensions. DeepSeek + Tampermonkey, Gemini + Tampermonkey, and ChatGPT + Tampermonkey all support one-click direct access to results. Without extensions, ChatGPT only supports pre-filling the search content into the dialogue box).

 Chrome  `设置` -> `搜索引擎` -> `管理搜索引擎和网站搜索` 中，点击 **「网站搜索」** 旁的 **添加**，将以下表格中的内容逐一填入：
 >Go to Chrome `Settings` -> `Search engine` -> `Manage search engines and site search`. Under the **"Site search"** section, click the **Add** button and fill in the fields one by one.

| 搜索引擎名称(Name) | 快捷字词 (Keyword) | 网址格式（用 `%s` 代替搜索字词） |
| :--- | :---: | :--- |
| 通义千问  | `qw` | `https://qianwen.com/?q=%s` |
| 豆包 | `db` | `https://www.doubao.com/chat/url-action?action={"pluginId":"Send_Message","payload":{"text":"%s"}}` |
| DeepSeek  | `ds` | `https://chat.deepseek.com/?q=%s` |
| Gemini | `ge` | `https://gemini.google.com/app?q=%s` |
| ChatGPT | `gpt` | `https://chatgpt.com/?q=%s` |


### 方案 B：第三方划词扩展导入 (JSON 数组格式) Third-Party Extension Import (JSON Array)

如果你使用的是支持 JSON 批量导入的 Chrome 划词扩展（如 *Selection Search*、*沙拉查词*、*Glance Search* 等），可以直接复制以下代码：
>If you are using a Chrome selection search extension that supports batch JSON importing (such as *Selection Search*, *Saladict*, *Glance Search*, etc.), you can directly copy the code block below:
```json
  { "name": "通义千问 ", "keyword": "qw", "url": "[https://qianwen.com/?q=%s](https://qianwen.com/?q=%s" },
  { "name": "豆包 ", "keyword": "gpt", "url": "[https://www.doubao.com/chat/url-action?action={"pluginId":"Send_Message","payload":{"text":"%s"}}](https://www.doubao.com/chat/url-action?action={"pluginId":"Send_Message","payload":{"text":"%s"}})" },
  { "name": "DeepSeek ", "keyword": "ds", "url": "[https://chat.deepseek.com/?q=%s](https://chat.deepseek.com/?q=%s)" },
  { "name": "Gemini ", "keyword": "ge", "url": "[https://gemini.google.com/app?q=%s](https://gemini.google.com/app?q=%s)" }
  { "name": "ChatGPT ", "keyword": "gpt", "url": "[https://chatgpt.com/?q=%s](https://chatgpt.com/?q=%s)" },



