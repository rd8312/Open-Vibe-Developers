# 統整報告：AI Coding 在專案進行中如何運作良好

---
## 🗂️ 一、講者觀點整理

### 1.1 高見龍：你說得對！AI Coding如何融入專案中

- **核心分享**：  
  講述近期與 AI 協作開發「線上購物系統」的經驗，從需求拆解、程式碼撰寫、錯誤修正到維護，完整展現 AI 在專案中的角色定位。  

- **觀點重點**：  
  - **AI 的助力**：  
    - 能快速生成雛形程式碼，縮短開發初期的嘗試時間。  
    - 在重複性高或模式明確的程式任務中，能顯著提升效率。  
  - **AI 的挑戰**：  
    - 有時會「自信地犯錯」，生成看似合理卻邏輯錯誤的程式碼。  
    - 在專案規模擴大後，AI 無法理解長期維護與團隊協作的隱性成本。  
  - **工程師的責任**：  
    - 工程師必須扮演品質守門人，檢查 AI 的程式是否符合專案需求與效能標準。  
    - 人類工程師仍需負責架構性決策與專案治理，AI 無法替代這些判斷。  

- **案例補充**：  
  - 在開發購物車模組時，AI 自動生成了可運行的程式碼，但忽略了「交易一致性」與「例外狀況處理」的需求。  
  - 經過人工檢視後，團隊重新設計了交易流程，確保資料完整性與安全性。  

- **結論**：  
  AI 更像是一個可靠的「副駕駛」：它能加速開發、提出靈感，但在落地專案與長期維護上，人類工程師才是最後的決策者與責任承擔者。  

---

### 1.2 Migu：把問題變成流程 — Vibe Coding 工作流的 6 個迭代圈

- **核心分享**：  
  將「問題拆解」視為 Vibe Coding 的核心，並提出一個可循環的工作流，協助團隊持續與 AI 協作。  

- **六個迭代圈**：  
  1. **問題定義**  
     - 釐清需求與目標，避免直接下模糊指令，例如「做一個留言功能」。  
     - 轉化成「使用者能新增留言、可刪除留言、留言需與使用者帳號綁定」等明確條件。  
  2. **輸入設計**  
     - 將需求整理成提示詞或規格書（spec），確保 AI 能理解背景脈絡。  
     - 避免單句提問，而是提供「資料結構、限制條件、測試案例」。  
  3. **AI 輸出**  
     - 獲得程式碼或設計草稿，作為初始版本。  
     - 不期待一次到位，而是把 AI 的輸出視為「起點」。  
  4. **檢驗與修正**  
     - 透過測試驗證程式正確性，並標記偏差或漏洞。  
     - 記錄錯誤案例，作為下一輪輸入設計的依據。  
  5. **優化迭代**  
     - 調整提示詞、補充需求，重新生成程式。  
     - 在每一次迭代中，逐步逼近專案的真正需求。  
  6. **沉澱流程**  
     - 將成功的提示與輸入方式整理成模板，歸納為「團隊知識庫」。  
     - 長期下來能形成標準化工作流，降低重複試錯成本。  

- **觀點重點**：  
  - Vibe Coding 的核心不在「一次生成完美程式碼」，而是透過循環檢驗與修正，逐步收斂到可靠的結果。  
  - 建立「迭代圈」能讓 AI 成為真正的合作夥伴，而非單純的工具。  

- **案例補充**：  
  - 在開發 API 時，第一輪 AI 生成的程式碼缺乏完整的錯誤處理機制。  
  - 經過多輪輸入修正，最終不僅補上了錯誤處理，還沉澱出「API 開發流程模板」，可供未來專案快速套用。  

- **結論**：  
  Vibe Coding 是一種「以流程驅動」的開發模式。透過明確需求、迭代檢驗與知識沉澱，團隊可以持續優化 AI 的價值，並建立穩定的工作流。  


## 💬 二、Discord 精華與觀點

### 2.1 影片與資源

 - [Better Than Vibe Coding: Agile AI Driven Development for Complex Apps](https://www.youtube.com/watch?v=JbhiLUY_V2U&t=4s&ab_channel=BMadCode) · [FB 介紹](https://www.facebook.com/story.php?story_fbid=24505590792369050&id=100000344080732&rdid=ifinU9pGXJVRduiv#)  
   - 主張「敏捷 AI 驅動開發（Agile-AI）」比 Vibe Coding 更能避免失控與技術債。  
   - 特色：以 AI 分飾 **BA、PM、Architect、PO、Scrum Master** 五種角色，先行完成需求澄清、研究、架構設計、任務拆解與驗收條件。  
   - **落地方式**：  
     - 將產物（需求、設計、任務）以 Markdown 形式放入專案目錄。  
     - 每個 Story = 一次獨立對話，透過測試驗收降低跨 Story 依賴。  
     - 測試覆蓋率 80–90%，測試即契約。  
   - **效益**：  
     - 成本可控、上下文乾淨、避免 Vibe Coding 中「修一處壞一片」。  
   - GitHub: [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD)  

 - [From Vibe Coding To Vibe Engineering](https://thenewstack.io/from-vibe-coding-to-vibe-engineering-its-time-to-stop-riffing-with-ai/)  
   - 提出「Vibe Engineering」：在生成式 AI 的基礎上加入 **結構（structure）、意圖（intent）、約束（constraints）**。  
   - **實踐要點**：  
     1. 系統思維（Think Beyond the Task）  
     2. 規範與約束（命名、目錄、抽象邊界、安全區域）  
     3. 重用與改善（避免 legacy，強調現代化重構）  
     4. 測試驅動開發（TDD，測試即規格與契約）  
     5. 保持同步（PR 摘要與架構追蹤，避免人類落後於 AI）
- 敏捷 AI 驅動開發 vs Vibe Engineering 對照表:

| 面向        | **敏捷 AI 驅動開發 (AAI)**                                                                                                         | **Vibe Engineering**                                                |
| --------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **核心理念**  | 將 AI 代理分為五種敏捷角色（BA/PM/Architect/PO/Scrum Master），在寫程式前先完成需求澄清、研究、架構、任務拆解與驗收規範。                                               | 從「即興 vibe coding」進化為「有結構、意圖與約束的 orchestrating」，工程師轉型為 orchestrator。 |
| **適用場景**  | 建立**可持續成長**的應用程式，避免一次性 demo 變成技術債。                                                                                           | 任何需要避免「快但脆弱」的專案，特別是進入 **production 階段**時。                           |
| **前期規劃**  | - **BA**：需求澄清<br> - **PM**：市場研究、PRD、MVP 規劃<br> - **Architect**：技術架構設計<br> - **PO**：任務拆解<br> - **Scrum Master**：建立 Story/Epic | - **Think Beyond the Task**：系統思維，不只解 ticket，要看全局抽象與架構層級。            |
| **規範與約束** | 架構文件與 Story 中清楚定義：檔案結構、技術選型、驗收條件、人工步驟。                                                                                       | **Codify the Rules**：將命名規範、目錄結構、邊界條件變成 AI 必須遵守的約束。                  |
| **重用與品質** | 每個 Story 都**明確標註依賴與測試條件**，避免 AI 隨意發揮。                                                                                        | **Reuse & Improvement**：明確指示 AI 使用乾淨元件，並主動改善舊邏輯、消除 duplication。     |
| **測試策略**  | 每個 Story 都附測試，追求 **80–90% 覆蓋率**（單元/整合/E2E）。                                                                                  | **TDD 驅動**：先生成測試，再實作，讓測試成為需求契約。                                     |
| **開發循環**  | - 每個 Story 在全新對話執行 → 上下文乾淨、節省 token<br> - 完成後 commit/PR，持續迭代                                                                 | - **Stay in Sync**：透過 AI 工具追蹤 PR 摘要與程式演進，維持人類與 AI 一致性。              |
| **角色定位**  | AI 擔任敏捷五角色，工程師在不同階段切換對應 AI 角色。                                                                                               | 工程師 = **Orchestrator**：定義邊界、制定規則、編排 AI，而非單純產碼者。                     |
| **核心差異**  | **更像敏捷專案流程的分工演繹**：每步驟角色明確、輸出文件化。                                                                                             | **更像工程思維的提升**：聚焦在持續演進、規範化與架構導向。                                     |


 - [A Guide to Gen AI / LLM Vibecoding for Expert Programmers](https://www.stochasticlifestyle.com/a-guide-to-gen-ai-llm-vibecoding-for-expert-programmers/)  
   - 作者 Rackauckas（MIT 合作者）認為：**只有專家才能正確使用 Vibe Coding**，因為能管控風險與品質。  
   - **方法論**：  
     - 把 LLM 當「程式二年級實習生」。  
     - 任務分解與 sandbox 測試。  
     - 週期性監督與審查 PR。  
     - 快速嘗試與快速淘汰。  
     - 僅用在熟悉的程式碼庫中，以降低審查成本。  

 - Spec-Driven Development:
    - [claude-code-spec-workflow](https://github.com/Pimzino/claude-code-spec-workflow)  
       - 把 Claude Code 轉化為可治理、可觀測的工作流：  
         - **新功能**：Requirements → Design → Tasks → Implementation  
         - **修 Bug**：Report → Analyze → Fix → Verify  
       - YouTube: [Claude Code Spec Workflow 完整示範](https://www.youtube.com/watch?v=ruAy8oBR5lA&ab_channel=AI%E8%B6%85%E5%85%83%E5%9F%9F) 
     - [claude-code-spec](https://github.com/gotalab/claude-code-spec)  
       - 將 **規格驅動開發（Spec-Driven Development, SDD）** 與 **AI-DLC（AI 開發生命週期）** 整合至程式庫中，讓 Claude Code 以指令化方式在「需求 → 設計 → 任務 → 實作（含 TDD）」下運行。

  - Spec 驅動開發（Spec-Driven Development, SDD)對照表:
  
| 面向                   | **Pimzino / claude-code-spec-workflow**                                                                                                                           | **gotalab / claude-code-spec（cc-sdd）**                                                                                                                          |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **定位/範疇**            | 把 Claude Code 變成**可治理工作流**：支援**新功能的 SDD** 以及**修 Bug 的四步法**（Report→Analyze→Fix→Verify）。README 並明確說明已將**主要開發重心轉向 MCP 版本**（提供即時儀表板與更廣工具相容），此倉庫仍可用但更新有限。 | 一條指令把 **AI-DLC（AI 驅動開發生命週期）＋ SDD** 安裝進專案，支援 **Claude Code 與 Gemini CLI**，並提供 **Kiro IDE 相容**的 SDD 流程（requirements→design→tasks→implementation）。   |
| **主要工作流（Spec）**      | **Spec 工作流**：`/spec-create` 一次產出 Requirements → Design → Tasks，並可**自動生成每個 task 的專屬執行指令**；`/spec-execute` 執行任務。                                      | **Kiro 風格 SDD**：`/kiro:spec-init`→`/kiro:spec-requirements`→`/kiro:spec-design`→`/kiro:spec-tasks`→`/kiro:spec-impl`；每階段具**品質閘（需人工核可，或 `-y` 自動）**。 |
| **Bug 工作流**          | 內建 **Bug 四步法**：`/bug-create`→`/bug-analyze`→`/bug-fix`→`/bug-verify`（明確將 Bug 流程標準化）。                                                                 | README 著重在 **Spec/SDD 主線**，未主打專用的 Bug 四步法命令。                                                                                                 |
| **上下文/記憶（Steering）** | 提供 `/**spec-steering-setup**` 建立 **product.md / tech.md / structure.md** 等長期上下文（Project Steering），並宣稱有**智能上下文共享與快取**以降低成本與重複載入。                    | 提供 `/**kiro:steering**` 建立 **Project Memory（Steering）**，作為單一事實來源供後續階段引用。                                                                       |
| **命令數量/型態**          | **10 條 Slash 命令**：Spec（5）＋ Bug（5）；另可為每個 task **自動產生對應命令**（提高可編排性）。                                                                                   | **8 條 Slash 命令**（`/kiro:*` 家族），覆蓋 Steering、Spec 起草、需求、設計、任務、實作等。                                                                                   |



## 📌 三、實作準則與架構決策對照

### 3.1 高見龍：AI 作為副駕駛的實作準則

- **實作準則**  
  1. 把 AI 當副駕駛，而非唯一開發者。  
  2. 建立檢驗機制（測試 + 人工審查）以控制品質。  
  3. 工程師專注於架構治理與非功能性需求。  

---

### 3.2 Migu：以流程驅動的 Vibe Coding 六迭代圈


- **實作準則**  
  1. 將問題轉為流程，避免即興式開發。  
  2. 將「六個迭代圈」制度化，形成團隊工作流。  
  3. 建立知識沉澱機制，累積模板與最佳實踐，降低重複試錯成本。  



## ✅ 有效建議摘要

1. **避免即興式 Vibe Coding，導入結構化流程**  
   - 在生成程式碼前，先完成需求澄清、架構規劃、任務拆解與驗收條件。  
   - 參考 Agile-AI 或 Spec-Driven Development，以「先規劃後生成」降低技術債。  

2. **將 AI 視為多角色協作者，而非單純工具**  
   - 讓 AI 分飾 BA/PM/Architect/PO/Scrum Master 等角色，提升需求完整度與交付可預測性。  
   - 工程師需保持「管理者」視角，負責監督、審查與品質把關。  

3. **以規範與測試作為人機協作的契約**  
   - 制定團隊規範（命名、目錄結構、不可修改區域），並讓 AI 遵循。  
   - 採用 TDD：先生成測試，再進行實作，確保 AI 輸出可驗證且可維護。  

4. **小步快跑，降低上下文負擔與成本**  
   - 每個 Story 以獨立對話處理，避免長上下文導致失控。  
   - 成本可控、上下文乾淨，便於迭代與回滾。  

5. **沉澱知識與持續改善**  
   - 將成功的提示、流程與規格沉澱為模板或知識庫，逐步形成團隊標準。  
   - 鼓勵 AI 在重用程式碼時，主動檢查並改善系統品質（消除重複、鬆耦合、現代化重構）。  

---

## ❓ 待解決的疑問

- **責任邊界與角色分工**: 在雛形開發與重複任務中 AI 能發揮效益，但在架構治理與非功能性需求上，如何清楚劃分 AI 與工程師的責任？  

- **流程效率與迭代成本**: Vibe Coding 需多輪迭代才能收斂，如何避免反覆試錯帶來的成本？

- **長期維護與可持續性**: AI 缺乏長期維護與團隊協作的視角，該如何確保程式碼在專案規模擴大後仍具可維護性與擴展性？  

---

## 🌐 四、外部資源（精選）

- [BMAD-METHOD GitHub](https://github.com/bmad-code-org/BMAD-METHOD) — 敏捷 AI 驅動開發完整方法論與範例。  
- [From Vibe Coding to Vibe Engineering](https://thenewstack.io/from-vibe-coding-to-vibe-engineering-its-time-to-stop-riffing-with-ai/) — 升級 Vibe Coding 的實踐指南。  
- [A Guide to Gen AI / LLM Vibecoding for Expert Programmers](https://www.stochasticlifestyle.com/a-guide-to-gen-ai-llm-vibecoding-for-expert-programmers/) — 由 MIT 合作者撰寫的進階指引。  
- [Claude Code Spec Workflow](https://github.com/Pimzino/claude-code-spec-workflow) — 以規格驅動開發（SDD）落實 AI 協作的完整流程。  
- [Claude Code Spec Workflow YouTube 示範](https://www.youtube.com/watch?v=ruAy8oBR5lA&ab_channel=AI%E8%B6%85%E5%85%83%E5%9F%9F) — 規格驅動的實際演示影片。  
- [Qoder](https://qoder.com/) — AI 驅動的智能代理式開發平台。 
- [LangExtract + RAG](https://www.youtube.com/watch?v=RPpGIxmdZYs&ab_channel=PromptEngineering)  
- [claude-auto-resume](https://github.com/terryso/claude-auto-resume)  
- [open-lovable](https://github.com/firecrawl/open-lovable)  
- [vllm-cli](https://github.com/Chen-zexi/vllm-cli)  
- [Claude Code + Remotion 動畫示範](https://www.youtube.com/watch?v=aY486RgplHo&ab_channel=SerenaWang-%E5%BF%83%E5%BF%83%E5%8A%A0%E5%B7%9E)  
