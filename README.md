# 日本語練習（Japanese daily practice）

每日日文練習嘅網頁版，可以**朗讀短文**。

## 功能

- 📅 **首頁係月曆**（星期一至五），有 🌸 嘅日子撳入去就係嗰日嘅練習；下面仲有全部練習清單
- 每日頁有「← 月曆」同前一日／後一日
- 櫻花＋日本城背景（深色模式會變夜景）
- 🔊 **讀全篇**：用瀏覽器內置嘅日文語音（Web Speech API）朗讀短文，讀緊嗰句會 highlight
- 撳任何一句 → 由嗰句開始讀
- 速度調校（0.5×–1.3×）
- 詞彙、文法例句、答案都有 🔊 掣
- 振假名開／關
- 🇬🇧 **英式英文版**：每日同一個題材有英文版（日文標題下面有英文標題），撳「🇬🇧 English」就轉，用英式英文語音（en-GB）朗讀，預設揀英國女聲；英文頁有「聲音」選單可以自己揀，會記住
- 🗣 **跟讀模式（shadowing）**：開咗之後每句讀完會停一停，等你跟住講，日文英文都用得
- 網址加 `#2026-11-02` 可以直接開嗰日，`#2026-11-02/en` 開嗰日嘅英文版，`#m-2026-10` 開嗰個月

朗讀用括號入面嘅讀音代替漢字，所以就算語音引擎讀錯漢字，都會照住課文嘅讀音讀。

## 點樣開

- **本機**：直接雙擊 `index.html`（唔使 server）
- **GitHub Pages**：Settings → Pages → Branch 揀 `main`、資料夾 `/ (root)` → Save，之後喺 `https://<username>.github.io/japanesslearning/` 打開

> 語音要有日文同英文 voice（英文會優先揀英國女聲）。最自然嘅英國女聲：Edge 嘅 Sonia／Libby（Natural）、Chrome 嘅 Google UK English Female、iPhone／Mac 下載 Serena 或 Martha（Enhanced）。Chrome / Edge / Safari（iPhone、Mac）一般都有；Windows 冇嘅話：設定 → 時間與語言 → 語音 → 加日文。

## 新增一日

喺 `data/lessons.js` 嘅陣列最頂加一個物件（同現有嗰日一樣嘅格式）。漢字讀音用全形括號寫，例如 `花火（はなび）`。

英文版喺同一個物件加 `en`：

```js
"en": {
  "title": "First Snow in Sapporo",
  "intro": "（廣東話簡介）",
  "passage": "同一個故事嘅英式英文版，一句對一句，方便跟讀。",
  "vocab": [["slippery", "跣、滑"]],
  "phrase": { "point": "When / If + 現在式", "explain": ["…"], "examples": [["When it snows, …", "一落雪…"]] },
  "questions": [["When does Sapporo get its first snow?", "Around the end of October."]]
}
```

冇 `en` 嘅日子就只有日文版。
