# Wiki Log

> Chronological, append-only history. 新事件加在最上方或最下方皆可，但不得刪除舊紀錄。

## [2026-11-22] initialize | 建立 Motorcycle LLM Wiki 初始版本

- 操作：initialize
- 建立三層架構：`raw/`、`wiki/`、`AGENTS.md`。
- 建立知識頁：engine-four-stroke、transmission-overview、g7-facts、maintenance-basics、sources。
- 建立索引與本日誌。
- 初始來源：S1–S5。
- 檢查發現：G7 官方頁列示 PTM 鏈條傳動；一般 CVT 教材不得錯套到 G7。
- 範圍限制：S2 為 X-TOWN ST 手冊，不可直接套用到 G7。
- 人工審閱：待逐篇與使用者討論。
- 待辦：補齊 G7 專屬手冊、煞車原理來源，並逐篇完成 ingest 審閱。

## [2026-11-22] ingest | S1 KYMCO G7 官方規格頁

- 操作：ingest / integrate / lint
- 討論：先向使用者呈現 S1 摘要、影響頁面與限制；使用者明確同意後才整合。
- 核對來源：KYMCO 官方 G7 產品規格頁（https://www.kymco.com.tw/motor/g7）。
- 整合內容：補入 17.3 PS / 8,000 rpm 引擎最大馬力、17.8 PS 綜效馬力、1.7 kg-m / 6,000 rpm 最大扭力；保留 175.1 c.c.、水冷四閥四行程 ISG、PTM 鍊條、前後固定碟及機油容量等原有規格。
- 更新頁面：`g7-facts.md`、`transmission-overview.md`、`index.md`。
- Raw 原則：未改寫 `raw/S1-kymco-g7-official.md`，保留原始來源紀錄；本次依官方網頁再次核對並將可支持的規格整合至 Wiki。
- Lint 結果：S1 引用可追溯；G7 PTM 鍊條與一般 CVT 教材已區分；沒有將 X-TOWN ST 的保養數值套用到 G7；內部連結指向既有頁面。
- 審閱狀態：使用者已同意本次整理方向；S1 本次整合完成。
- 限制／待辦：官方產品頁不是完整維修手冊；PTM 內部構造及 G7 專屬保養週期仍待原廠技術資料支持。

## [2026-11-22] batch ingest | S2–S5

- 操作：batch ingest / integrate / lint
- 使用者指示：S2–S5 一次完成；因此本輪不再逐篇停下等待確認，依既有來源紀錄與可直接檢視的原始網頁／PDF內容完成整合。
- S2（KYMCO X-TOWN ST 使用說明書）：核對手冊中的騎乘前檢查章節、機油檢查、煞車、輪胎、燈光與定期檢查章節；只作 X-TOWN ST 案例。明確禁止將其機油容量、換油里程、CVT 或其他保養數字套用到 G7。
- S3（ARTC 技術文章）：核對四行程四個階段與氣閥機構作動概念；整合至 `engine-four-stroke.md`。
- S4（歸仁國中動力機械群教材）：核對四行程曲軸轉兩圈完成循環、離合器功能、齒輪變速概念及 V 型無段自動變速構成；整合至 `engine-four-stroke.md`、`transmission-overview.md`。
- S5（第 55 屆中小學科學展覽會「可更換式蹄片離合器」作品）：核對曲軸、離合器、變速齒輪至車輪的動力傳遞敘述及離心式離合器概念；以教育案例整合至 `transmission-overview.md`，不視為所有車款通用規格。
- 更新頁面：`engine-four-stroke.md`、`transmission-overview.md`、`maintenance-basics.md`、`sources.md`、`index.md`。
- Raw 原則：未覆寫 `raw/S2`–`raw/S5`，保留原始來源紀錄。
- Lint 結果：來源 ID 可追溯；X-TOWN ST 與 G7 的適用範圍已區分；一般 CVT 教材與 G7 PTM 鏈條已區分；S5 標示為學生研究作品；相關內部連結均指向既有頁面。
- 審閱狀態：S2–S5 已依使用者要求完成批次整合；此狀態代表 Wiki 整合完成，不代表所有來源均為原廠維修規格。
- 待辦：補齊 G7 專屬保養手冊、煞車／ABS 原理、SAE 黏度分類及 PTM 詳細機構來源。

## [2026-11-22] generate | HTML teaching slides

- 操作：query / organize / generate / check
- 知識來源：以 `wiki/index.md` 為入口，使用 `engine-four-stroke.md`、`transmission-overview.md`、`g7-facts.md`、`maintenance-basics.md` 與 `sources.md`。
- 產出：`slides/index.html`，共 12 張投影片，包含學習路線、引擎、四行程、氣閥機構、傳動、離合器、CVT/PTM 區別、G7 規格、保養觀念、小測驗與來源。
- 教學順序：先引擎、再傳動、再 G7 案例，最後回到保養手冊判讀。
- 互動：上一頁／下一頁按鈕、鍵盤方向鍵、頁碼與進度條、三題即時回饋小測驗。
- 來源標記：各主題投影片標示 [S1]–[S5]；末頁列出原始來源連結。
- 檢查：HTML 為單檔、無外部 JS/CSS 依賴；投影片數量 12；所有投影片均含來源標記或屬課程導覽／測驗頁；保養頁清楚標示 S2 僅為 X-TOWN ST 範例，不將數值套用到 G7。
- 限制：本投影片只根據現有 Wiki，不補寫 G7 專屬保養週期、SAE 黏度或 PTM 內部維修細節。
