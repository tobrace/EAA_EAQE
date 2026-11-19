# AnkiDroid 下載與使用教程

本教程說明如何在 Android 手機上，用官方 AnkiDroid 應用程式下載、導入並複習本包中的自擬閃卡。

請先閱讀同目錄的 `README.md`：本包不是地產代理監管局或香港特區政府的官方材料，亦未經其認可或背書；只是用 AI 生成的自用複習題目。

下列步驟依據 [AnkiDroid 使用手冊](https://docs.ankidroid.org/manual.html)（2026 年 11 月查閱）。不同手機廠商的檔案管理介面可能略有差異。若選單名稱與下文不完全相同，請以 App 內實際選項和官方手冊為準。

## 一、下載並安裝 AnkiDroid

請只從以下官方來源安裝，不要從不明網站下載安裝檔。

### 1. Google Play（建議優先使用）

前往 [AnkiDroid Flashcards（Google Play）](https://play.google.com/store/apps/details?id=com.ichi2.anki)，或在 Play 商店搜尋「AnkiDroid Flashcards」。套件名稱應為 `com.ichi2.anki`。從這裡安裝之後，系統可自動更新。

### 2. F-Droid

若你使用 F-Droid，可安裝 [AnkiDroid（F-Droid）](https://f-droid.org/packages/com.ichi2.anki/)。

### 3. GitHub 官方發布頁

若沒有 Play 商店或 F-Droid，可到 [AnkiDroid GitHub Releases](https://github.com/ankidroid/Anki-Android/releases) 下載官方 APK：

- 請下載**最新穩定版**，不要選標明 Pre-release、alpha 或 beta 的測試版。
- 多數現時手機應選 Assets 裡檔名含 `arm64-v8a` 的 APK。若無法安裝，再按該發布頁的說明嘗試其他官方構建（例如 `full` 或 `Parallel`）。
- GitHub 不會自動更新已用這種方式安裝的 App。
- 用系統檔案管理器打開該 APK 進行安裝。系統可能要求允許「安裝未知應用程式」，請只對你用來打開該檔案的應用開啟此權限。
- 如需核對 APK 簽名，[AnkiDroid 官方 README](https://github.com/ankidroid/Anki-Android) 公布的簽署憑證指紋為：
  - SHA-256：`2071534f0f4b5e54ae952dd275d70da6e3459ee69909d2ab1b4843c4c5b21a45`

安裝後打開 AnkiDroid。如需更改介面語言：從畫面左側滑出導航選單（或點左上角選單圖示）→「設定」（Settings）→ 在 AnkiDroid 分類中選擇「語言」（Language）。

## 二、取得並解壓本複習包

1. 從本 GitHub 倉庫下載壓縮包（倉庫中的 ZIP，或 Releases 資產，視實際上傳方式而定）。
2. 用手機的「檔案」或「我的檔案」應用解壓。解壓後應看到多個 `.apkg`、若干 `.tsv`，以及 `README.md`、本教程和 `SHA256SUMS.txt`。
3. 如需核對檔案完整性，可對照 `SHA256SUMS.txt`。
4. 本包無配圖，不需要額外的 `media` 資料夾。

## 三、選擇要導入的檔案

請只導入**一個** `.apkg`。不要把「全部」和「僅章節／僅仿真／單章」重複導入，以免牌組疊加。

| 建議情境 | 導入這個檔案 |
| --- | --- |
| 一般完整練習 | `EAA_EAQE_all.apkg`（1800 題：章練 800 + 仿真 1000） |
| 只做章節練習 | `EAA_EAQE_chapters_only.apkg`（800 題） |
| 只做仿真試卷 | `EAA_EAQE_mocks_only.apkg`（1000 題，20 套） |
| 只導入某一章 | `EAA_ch01.apkg` … `EAA_ch08.apkg`（各 100 題） |

本包的 `.apkg` 是牌組包（deck package），導入後會與你現有的牌組合併，**不會**清空 AnkiDroid 裡的全部內容。只有檔名以 `.colpkg` 結尾的集合包才會完全取代現有內容；本包不含此類檔案。

**請不要把 `.tsv` 直接導入 AnkiDroid。** 官方手冊寫明：AnkiDroid 只能直接導入 `.apkg`，不能直接導入其他格式（包括文本檔）。`.tsv` 是給電腦版 Anki 作備份導入用的。

也不要透過 AnkiDroid 主畫面藍色「＋」裡的「取得共享牌組」（Get shared decks）來尋找本包；那是 AnkiWeb 的共享牌組目錄，不是本倉庫的檔案。

## 四、把 .apkg 導入 AnkiDroid

可用以下任一方法。

### 方法一：用系統打開檔案（較常用）

1. 用「檔案」應用找到解壓後的 `.apkg`。
2. 點該檔案，選擇用 AnkiDroid 打開。
3. 出現確認對話框後，點確定（OK）完成導入。

官方手冊說明：`.apkg` 會自動關聯到 AnkiDroid；例如從郵件附件打開時，也會出現導入確認。

### 方法二：在 AnkiDroid 裡手動導入

1. 打開 AnkiDroid，進入牌組列表（主畫面）。
2. 點右上角「更多」選單，選擇「匯入」（Import 或 Import file）。
3. 選取剛才的 `.apkg`，再點確定。

若檔案仍在電腦上，也可用 USB 把 `.apkg` 複製到手機的 AnkiDroid 資料夾，再按上述步驟在 App 內匯入。

導入完成後，牌組列表應出現 `EAA`，展開後可見：

- `EAA::章節練習::第一章` … `第八章`
- `EAA::仿真試卷::第01套` … `第20套`

## 五、開始複習

1. 在牌組列表點牌組名稱（平板也可能看到「STUDY」按鈕），進入學習畫面。
2. 螢幕上先顯示題幹和選項。想好答案後，點「顯示答案」（Show answer）。
3. 下方會出現 2 至 4 個作答按鈕（視該卡以往作答情況而定）。按鈕上會顯示下次出現的間隔，例如 `10m` 代表 10 分鐘，`5d` 代表 5 天。按你實際記得的程度點選即可。
4. 若點錯，可用學習畫面的「復原」（Undo）撤銷上一張的作答。
5. 牌組名稱旁邊有三個數字：左邊藍色是今日新卡，中間紅色是學習中的卡片，右邊綠色是到期複習卡。全新牌組剛導入時，紅、綠通常為 0。
6. 預設每天新卡約 20 張，可在該牌組的「牌組選項」（Deck options）裡調整。
7. 當天到期卡片複習完畢後，會回到牌組列表並顯示完成提示。若要加練，再點該牌組，可選擇繼續學習或自訂學習（詳見官方手冊的 filtered deck / custom study 說明）。

卡片正面為題幹和選項，背面為答案與解說。

## 六、其他說明

- 同步到 AnkiWeb 是可選的，不是使用本包的必要步驟。若要在電腦和手機之間同步，請先在 [AnkiWeb](https://ankiweb.net) 註冊，再按官方手冊「Using Anki Desktop with AnkiDroid」一節操作。
- 更完整的功能說明和支援入口：
  - [AnkiDroid 使用手冊](https://docs.ankidroid.org/manual.html)
  - [AnkiDroid 說明與支援](https://docs.ankidroid.org/help.html)
