# KANO LAB · 顧客需要與卡諾模型課堂活動

## 課堂入口

- 學生：https://sonicygy.github.io/MHO5402-CSM/
- 投影／二維碼：https://sonicygy.github.io/MHO5402-CSM/classroom.html
- 教師成績後台：https://kano-csm-teacher.sonic-acc.chatgpt.site

本資料夾是2026-10-14修訂來源；本地修改不等於已發布，線上版本須以整體驗證及發布紀錄為準。

學生輸入名字後，以繁體中文（預設）或英文進行活動。頁首課程名稱為繁中「KANO LAB / MHO5302K 顧客服務管理」及英文「KANO LAB / MHO5302 Customer Service Management」。不設簡體中文或雙語顯示模式。

學習順序：01 概念圖解 → 02 情境練習 → 03 顧客問卷 → 04 學習紀錄。先看概念，再完成10題情境分類和全部4組顧客問卷，最後按「提交給老師」並等候確認。不需輸入文字作答，不提供換人、重玩或重新開始按鈕。

## 情境題與顧客問卷

- 情境分類只計首次確認，滿分10分；確認後不能改寫分類。參考解釋與討論問題保留。
- 顧客問卷包括免費 Wi-Fi、免費提早入住、自助入住選項，以及入住後每日推廣通知。每項屬性均須選擇「提供」和「不提供」時的反應，4組共8個選項全部必填。
- 問卷是顧客喜好，不計對錯，也不計入10分制情境分數。M／O／A／I／R／Q 均可由矩陣得出；Q 是待澄清結果，不是第六種顧客需要。
- 轉換屬性或語言、重新整理同一頁籤時，已選反應保留。問卷與情境進度按同一次練習保存；只有實際練習識別碼改變時才重設。
- 學習紀錄顯示問卷完成數（0/4至4/4），可直接前往第一組未完成問卷。10題情境及4組問卷全部完成後才可提交。
- 成功提交後，本次情境結果與問卷均鎖定。學生頁只在收到伺服器確認後顯示成功；網絡失敗可重試同一次提交。

## 儲存與資料格式

課堂期間請保留原頁籤。情境與問卷進度保存在目前瀏覽器；本次練習憑證沿用頁籤的工作階段儲存方式。登記只填名字，不驗證學生身份，無需學生帳號、班級或班級代碼。網址及二維碼保持不變。

`POST /api/start` 傳送 `name` 與目前介面語言 `language`（`zh` 或 `en`）。`POST /api/submit` 傳送原有 `id`、`token`、情境 `answers`（只含 `choice`），並加入：

```json
{
  "language": "zh",
  "surveyVersion": 2,
  "surveyAnswers": [
    { "featureId": "wifi", "functional": 0, "dysfunctional": 4 },
    { "featureId": "early-check-in", "functional": 0, "dysfunctional": 2 },
    { "featureId": "self-check-in", "functional": 2, "dysfunctional": 2 },
    { "featureId": "promotions", "functional": 4, "dysfunctional": 0 }
  ]
}
```

`functional`、`dysfunctional` 必須是0–4的整數，依序代表喜歡、本來就應該、沒有特別感受、可以接受、不喜歡。前端不傳送問卷分類；後台須重新驗證四個固定屬性、反應值及分類，並按屬性彙整教師結果。情境分數同樣由後台重新計算。

姓名和提交資料不放在此公開倉庫。教師後台的授權、資料儲存與彙整由獨立後台來源負責；本次前端修訂必須與配套後台一同驗證後發布。

## 檔案

`index.html` 是學生入口；`classroom.html` 是投影入口。`assets/Kano_Classroom_QR.png` 和 `.svg` 可放入課件。二維碼連結未變；既有 `assets/Kano_Classroom_Poster.png` 是先前海報，不因修改投影網頁而自動更新，不應作為本次新流程的說明。

教師後台來源在課程目錄 `output/interactive/Kano_Teacher_Backend`；此公開倉庫只保存學生頁、投影頁和公開資源。離線單檔練習是另一個用途版本，不自動由此修訂取代。

## References and licenses

Kano evaluation matrix: Atlason & Giacalone (2018), Table 1, https://pmc.ncbi.nlm.nih.gov/articles/PMC6263047/ . Scenarios and conceptual curves are teaching examples, not empirical findings.

QR library: davidshimjs/qrcodejs (MIT); see `assets/qrcodejs-LICENSE.txt`.
