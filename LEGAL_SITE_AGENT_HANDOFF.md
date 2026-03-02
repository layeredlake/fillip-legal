# Fillip 法務靜態網站交接文件（給新專案 Agent）

## 目標
建立一個超低成本、可公開存取、可直接提供給 App Store Connect 的法務網站，包含：
- `privacy.html`（隱私權政策，必填）
- `support.html`（支援頁，必填）
- `terms.html`（服務條款，建議）
- `index.html`（簡單入口頁）

網站用途：
- App Store Connect 的「隱私權政策 URL」
- App Store Connect 的「支援 URL」
-（可選）條款 URL

---

## 建議架構
建立**新 GitHub repo**（建議名稱：`fillip-legal`），避免和 App 主程式耦合。

建議檔案結構：

```text
fillip-legal/
  index.html
  privacy.html
  support.html
  terms.html
  assets/
    logo.png   (可選)
  README.md
```

---

## 技術要求
- 純靜態 HTML/CSS（不要框架、不要後端）
- 手機與桌面都可讀（RWD）
- 全站 UTF-8
- 文字語言：繁體中文
- 可加上更新日期欄位（例如：`最後更新：2026-03-02`）

---

## GitHub Pages 部署要求
1. 專案 push 到 GitHub（分支 `main`）
2. `Settings -> Pages`
3. Source 選 `Deploy from a branch`
4. Branch 選 `main` + `/ (root)`
5. 成功後應產生網址：
   - `https://<github-user>.github.io/fillip-legal/`
   - `https://<github-user>.github.io/fillip-legal/privacy.html`
   - `https://<github-user>.github.io/fillip-legal/support.html`
   - `https://<github-user>.github.io/fillip-legal/terms.html`

---

## 內容最低需求（務必有）

### privacy.html
- 收集哪些資料（例如：帳號識別、學習進度、診斷資訊）
- 收集目的（登入、同步、改善服務）
- 第三方服務（Firebase、RevenueCat、Google AdMob）
- 使用者權利（刪除帳號/聯絡方式）
- 聯絡信箱

### support.html
- 常見聯絡方式（email）
- 回覆時間說明（例如：3-5 工作天）
- FAQ 簡版（登入、同步、訂閱、還原購買）

### terms.html
- 使用規範
- 訂閱與自動續訂基本說明（以 App Store 條款為準）
- 責任限制與服務調整聲明

---

## App Store Connect 對接
完成後請提供這三個 URL 給主專案：
- Privacy Policy URL -> `privacy.html`
- Support URL -> `support.html`
- Terms URL（可選）-> `terms.html`

---

## 完成驗收條件
- [ ] 三個網址均可匿名開啟（無登入、無 404）
- [ ] 手機 Safari 可正常閱讀
- [ ] HTTPS 正常（無憑證錯誤）
- [ ] 頁面內容為繁中且不含模板佔位字（如 `TODO`）
- [ ] 提供最終 URL 清單

---

## 補充說明
- 若使用同一 GitHub 帳號，建議 repo 設為 Public（Pages 最簡單）
- 本站僅作法務與支援資訊，不放任何私密資料
