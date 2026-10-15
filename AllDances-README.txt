FF6 Pixel Remaster — 莫古全部 8 種舞蹈／Mog: all 8 dances
Steam build 20265119 · 2026-10-16
File: FF6_PR_AllDances_20265119.CT

效果／Effect
辨識正式角色 characterStatusId=11、jobId=11 的莫古，透過遊戲的 OwnedCharacterClient.LearningAbility 補齊全部 8 種舞蹈。只處理尚未完全學會的項目，保留已學會的舞蹈。莫古未正式加入時停止，不會建立角色或改劇情。
Identifies permanent Mog by characterStatusId=11 and jobId=11, and uses the game's OwnedCharacterClient.LearningAbility to learn all 8 dances. Processes only incompletely learned entries and retains learned dances. Stops if permanent Mog is absent; does not create a character or edit story progress.

清單／List
疾風狂想曲／Wind Rhapsody
森林夜曲／Forest Nocturne
沙漠催眠曲／Desert Lullaby
愛情小夜曲／Love Serenade
大地藍調／Earth Blues
流水和聲／Water Harmony
黑暗鎮魂曲／Twilight Requiem
雪人迴旋曲／Snowman Rondo
繁中名稱取自本版遊戲資料；能力 ID 164–171、內容 ID 494–501，群組 6。
Traditional Chinese names are taken from this build's game data; ability IDs 164–171, content IDs 494–501, group 6.

使用／Use
僅限 Steam build 20265119，需 Cheat Engine Mono collector。讀取存檔，停在一般地圖並暫停操作，連接 FINAL FANTASY VI.exe 後載入 CT，勾選唯一項目一次。開啟 CT 本身不執行。請勿同時套用其他 CT。
Requires Steam build 20265119 and Cheat Engine Mono collector. Load a save, remain idle on a normal field map, attach to FINAL FANTASY VI.exe, open the CT and enable its single entry once. Opening alone does not run it. Do not apply other CTs simultaneously.
完成後重開舞蹈清單確認，另存新欄位。取消勾選不會還原。
Reopen the dance menu to confirm, then save to a new slot. Disabling does not undo learning.

備份／Backup
執行前會在 Cheat Engine 安裝目錄寫入 JSON 狀態快照，訊息會顯示路徑；寫入失敗會停止。此快照不是可直接載入的加密存檔，也不是自動還原功能。實測前另做完整存檔備份，保留在本機，不公開。
Writes a JSON state snapshot in the Cheat Engine installation directory before learning, showing the path on completion; stops if writing fails. This snapshot is not a loadable encrypted save or an automatic undo facility. A separate full save backup was kept locally before testing and is not published.

實測紀錄／Validation
唯讀檢查成功。相同核心 Lua 已透過本機測試包實際套用，RESULT true nil。
Read-only preflight passed. The same core Lua was applied via a local test wrapper with RESULT true nil.
辨識到莫古的角色記錄 ID 為 16，並非把固定第 11 筆記錄當作莫古。
Mog's character record ID was 16; the table does not assume that record 11 is Mog.
原有「黑暗鎮魂曲」熟練度 100 保留；另外 7 種由 0→100，最後全部 8 種熟練度 100。
Existing Twilight Requiem proficiency 100 was retained; the other 7 changed from 0→100, leaving all 8 at 100.
持有 Gil 687904、累計 Gil 49127、主存檔與圖鑑擊破數 281 均不變。其他角色／技能／指令、等級／經驗值／HP／MP／四項能力、魔石、一般背包數量、各怪物擊破記錄、序列化地圖／劇情／寶箱資料與 37 項成就皆核對不變。
Held Gil 687904, lifetime Gil 49127 and main-save/bestiary kills 281 were unchanged. Other characters/abilities/commands, levels/EXP/HP/MP/four attributes, magicite, normal-inventory quantities, individual monster defeat records, serialized map/story/chest data and all 37 achievements were verified unchanged.
本次新增的是實際技能，不是只解鎖成就。
This grants actual abilities rather than just unlocking an achievement.

測試範圍／Test scope
已實測本機核心學習流程與前後核對；正式 CT 勾選介面及預設備份目錄未另行實測，其他帳號／版本／系統、戰鬥效果、存檔重讀與長期遊玩未測。使用者已確認全部 8 種舞蹈都有顯示且可以選用。
Core learning and before/after checks were tested locally. The formal CT checkbox interface and default backup directory were not separately exercised; other accounts/builds/systems, combat behavior, save/reload and long-term play were not tested. The user confirmed that all 8 dances are displayed and selectable in the game.
