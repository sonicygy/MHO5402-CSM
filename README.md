# Kano Lab · 雙語卡諾模型課堂遊戲

## 課堂入口

- 學生：https://sonicygy.github.io/MHO5402-CSM/
- 投影／二維碼：https://sonicygy.github.io/MHO5402-CSM/classroom.html
- 教師成績后台：https://kano-csm-teacher.sonic-acc.chatgpt.site

學生掃碼後輸入名字，選擇中文、英文或雙語，完成10題，再按「提交給老師」。無需學生帳號、班級或班級代碼。原有學生網址及二維碼保持不變。

教師使用指定 ChatGPT 帳號登入后台，查看名字、分數、提交時間、每題答案和文字理由。后台每15秒更新，可匯出CSV。其他帳號與未登入訪客不能讀取成績。

## 課件用詞

卡諾模型 / Kano Model：M 必備 / Must-be；O 一維 / One-dimensional；A 魅力 / Attractive；I 無差異 / Indifferent；R 反向 / Reverse。

用詞依 MHO5302 第四講中文與英文課件。Q 是待澄清的問卷結果，不是第六種需要。

## 成績與保存

- 每題只計首次確認的分類答案，滿分10分。服務分類依題中顧客、承諾和情境判讀。
- 題目回饋和討論在學生頁顯示；文字理由不自動評分。
- 學生練習進度暫存在瀏覽器，名字與成績保存在獨立的 Sites D1 数据库；學生資料不存放在此公開倉庫。
- 網頁收到服务器確認後才顯示提交成功。網絡失敗時可重試同一份答案，不會新增重複提交；已提交的首次結果不能被改寫。
- 點「換人／再玩一次」可開始一份新紀錄；同名者的不同嘗試會分別列出。
- 登記僅填名字，不驗證學生身份，適用於課堂遊戲。
- 線上名字登記及提交需要網絡；原有本地單檔HTML另行保留，用於離線練習。

## 檔案

`index.html` 是學生入口；`classroom.html` 是投影入口。`assets/Kano_Classroom_QR.png` 和 `.svg` 可放入PPT；`assets/Kano_Classroom_Poster.png` 是課堂海報。

教師后台源码在課程目錄 `output/interactive/Kano_Teacher_Backend`，由 Sites 發布；此 GitHub 倉庫只保存公開學生頁和投影資源。

## References and licenses

Kano evaluation matrix: Atlason & Giacalone (2018), Table 1, https://pmc.ncbi.nlm.nih.gov/articles/PMC6263047/ . Scenarios and conceptual curves are teaching examples, not empirical findings.

QR library: davidshimjs/qrcodejs (MIT); see `assets/qrcodejs-LICENSE.txt`.
