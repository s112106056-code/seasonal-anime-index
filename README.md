# 季番誌｜日本動畫季度資料庫

清爽淺色風格的靜態網站，使用 AniList GraphQL API 顯示日本電視動畫與網路動畫。

## 功能
- 冬、春、夏、秋季度與年份切換
- 中、英、日文名稱搜尋
- 依播出形式、作品狀態、類型篩選
- 海報卡片、評分、首播日期
- 詳細資料視窗：簡介、集數、單集長度、製作公司、類型與 AniList 連結
- 瀏覽器本地收藏（localStorage）
- 手機響應式版面
- API 失敗時使用介面範例資料

## 本機執行
建議在此資料夾執行：
```bash
python -m http.server 8000
```
開啟 http://localhost:8000

## GitHub Pages 部署
1. 將所有檔案上傳到 Repository 根目錄。
2. 開啟 Settings → Pages。
3. Source 選擇 Deploy from a branch。
4. Branch 選 main、資料夾選 /(root)，按 Save。
5. 等待部署完成後，從 Pages 頁面開啟網站。

## API
- Endpoint: https://graphql.anilist.co
- 文件: https://docs.anilist.co/guide/graphql/
- 本版查詢日本來源、非成人向動畫，格式為 TV、TV_SHORT、ONA。

## 資料限制
- 清單依 AniList 的季度與年份分類，完整度取決於資料庫。
- ONA 是網路動畫格式，不代表所有串流平台上架作品。
- 播出日期、集數、製作公司、評分及簡介可能缺漏或變動。
- 尚未整合台灣合法串流平台、台灣上架日期與精確播出時間。
- API 限流或連線失敗時會顯示範例資料，範例不是實際季度名單。
- 海報與作品資料屬 AniList／各權利人所有，使用前應確認相關政策；本網站不是 AniList 官方產品。
- 收藏只存在目前瀏覽器，不會跨裝置同步。
