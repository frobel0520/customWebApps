# customWebApps

幾個單檔 HTML 小工具，各自一個資料夾，透過 GitHub Pages 發布。沒有 build、沒有後端，資料存在瀏覽器 localStorage。

## 工具

| 工具 | 網址 | 內容 |
|---|---|---|
| 計時器 | [CustomTimer/](https://frobel0520.github.io/customWebApps/CustomTimer/) | 輸入分、秒倒數，可暫停與重設 |
| 台股自選清單 | [stock/](https://frobel0520.github.io/customWebApps/stock/) | 輸入股票代號加入清單，顯示最近收盤價與漲跌；清單存在 localStorage，股價來自 [FinMind API](https://finmindtrade.com/)（需要 FinMind token） |
| 蘑菇戰情室（單機版） | [pikmin/](https://frobel0520.github.io/customWebApps/pikmin/) | 皮克敏蘑菇重生倒數，只存在自己的瀏覽器 |

蘑菇戰情室後來獨立成 [pikmin-mushroom-room](https://github.com/frobel0520/pikmin-mushroom-room)，改用 Supabase 讓家人即時同步；這裡的 `pikmin/` 是早期的單機版。

根目錄沒有首頁，直接開各工具的網址。

## Harbor 整合

三個頁面的 `<head>` 都載入 Harbor 的維護腳本（`data-project="custom-web-apps"`，2026-09-15 起）：

- Harbor 開啟維護模式時顯示全螢幕維護畫面；有公告時顯示可關閉的底部公告列。
- Harbor 連不上或逾時 800 ms 時頁面照常顯示。

## 結構

```text
CustomTimer/index.html
stock/index.html
pikmin/index.html   # 附兩張背景圖 Pikmin.jpg、Pikmin2.jpg
```

## 修改與部署

直接改對應的 `index.html`，push 到 `main` 後 GitHub Pages 自動更新。
