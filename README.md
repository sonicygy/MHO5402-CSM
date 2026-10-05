# Kano Lab · 雙語 Kano 分類練習

中英雙語的課堂練習。學生不需帳戶，手機或電腦瀏覽器皆可使用。

上傳目標：[sonicygy/MHO5402-CSM](https://github.com/sonicygy/MHO5402-CSM)。2026-10-05 準備時已確認倉庫使用 `main`，根目錄只有 README。

預計學生網址：`https://sonicygy.github.io/MHO5402-CSM/`。

預計教師入口：`https://sonicygy.github.io/MHO5402-CSM/classroom.html`。

二維碼已指向上述預計學生網址；完成上傳並啟用 Pages 後才能使用。尚未聲稱網站已發布。

## 上傳到 GitHub Pages

1. 開啟你已建立的倉庫 [sonicygy/MHO5402-CSM](https://github.com/sonicygy/MHO5402-CSM)。倉庫為 Public。
2. 解壓 `Kano_GitHub_Pages_upload.zip`。
3. 在倉庫選 **Add file → Upload files**，將解壓後的 `index.html`、`classroom.html`、`assets` 資料夾、`.nojekyll` 和 `README.md` 上傳到倉庫根目錄，然後 Commit。
4. 不要上傳 ZIP 檔本身，也不要把檔案再放入 `Kano_GitHub_Pages` 子資料夾。根目錄應直接看到 `index.html`。
5. 開啟 **Settings → Pages**。
6. 在 **Build and deployment → Source** 選 **Deploy from a branch**。
7. Branch 選 `main`；Folder 選 `/(root)`；按 **Save**。
8. 等待發布完成。官方文件說明更新可能需要最多 10 分鐘；可查看倉庫 Actions 的部署狀態。
9. 從 Settings → Pages 複製實際網站網址。預計為 `https://sonicygy.github.io/MHO5402-CSM/`。若日後設定自訂域名或更換路徑，請更新二維碼。
10. 用手機先開一次網址，確認能看見練習，再分享給學生。

`.nojekyll` 是空檔案，用於停用 Jekyll。若網頁上傳介面沒有選到這個隱藏檔，這個簡單靜態網站仍可發布；亦可在 GitHub 用 Add file → Create new file 補建 `.nojekyll`。重點是 HTML 與 assets 保持上述相對位置。

## 課堂網址與二維碼

- **學生入口：** 網站根網址，或同一網址下的 `index.html`。
- **教師投影入口：** 同一網址下的 `classroom.html`。
- 學生網址預計為 `https://sonicygy.github.io/MHO5402-CSM/`，教師入口就是 `https://sonicygy.github.io/MHO5402-CSM/classroom.html`。
- 線上開啟 `classroom.html` 時，會自動生成同目錄學生入口的二維碼。
- 本機開啟 `classroom.html` 時會使用上述預計網址。若實際發布網址不同，貼上正確 HTTPS 網址再按「生成二維碼」。
- 可下載有白邊的 PNG／SVG 二維碼，插入 PPT；或用「全螢幕投影」「列印海報」。
- **生成二維碼不會發布網站或核實網址是否上線。** 上課前請以手機掃碼測試。不要用倉庫 `github.com/...` 的網址替代 Pages 網站網址。

## 課堂安排

1. 掃碼後選繁中、English 或雙語。
2. 個別完成 10 題並寫下理由，約 8 分鐘。
3. 小組比較分類與理由，約 5 分鐘。
4. 使用問卷實驗，討論客群、情境和承諾如何影響分類，約 5 分鐘。
5. 需要收集結果時，學生在「學習紀錄」下載文字紀錄，再提交 Moodle 作業。

## 分數與資料

- 答案依虛構教學情境中的顧客反應判斷。文字理由不會自動評分。
- 首次提交計分；答案與解釋存在網頁原始碼中，適合形成性練習。
- 練習進度只保存在各學生的瀏覽器，不會自動傳給教師或 Moodle。
- 不收集姓名、不設登入、不使用分析追蹤或外部 AI API。網站託管服務仍會按其政策處理一般網站請求。
- 本地 HTML 與線上網頁是不同來源，練習進度不會互通。

## Files / 檔案

```text
index.html                 Student bilingual activity / 學生雙語練習
classroom.html             Classroom QR poster / 教師掃碼與投影入口
assets/qrcode.min.js       Bundled QR generator / 隨附 QR 程式
assets/qrcodejs-LICENSE.txt Third-party MIT licence / 第三方授權
.nojekyll                  Static Pages marker / 靜態網頁標記
README.md                  This guide / 本說明
assets/Kano_Classroom_QR.png  Ready-to-use QR PNG / 二維碼圖片
assets/Kano_Classroom_QR.svg  Scalable QR SVG / 二維碼向量圖
```

## Reference / 參考

- Kano concepts and evaluation matrix: Atlason & Giacalone (2018), Table 1, [Rapid computation and visualization of data from Kano surveys in R](https://pmc.ncbi.nlm.nih.gov/articles/PMC6263047/). The activity adds original bilingual scenarios and illustrative curves.
- QR library: [davidshimjs/qrcodejs](https://github.com/davidshimjs/qrcodejs), MIT, bundled from commit `06c7a5e134f116402699f03cda5819e10a0e5787`. Preserve the bundled licence when redistributing.
- [GitHub: creating a Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).
- [GitHub: configuring a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Quick English deployment guide

Create a public repository, upload these files directly to its root, then choose **Settings → Pages → Deploy from a branch → main → /(root) → Save**. Open the actual URL shown by GitHub after deployment. Students use the root URL; the teacher opens `classroom.html` at the same site to generate, project or download the QR code. Test it on a phone before class. No build tools or package installation are required.
