FF6 Pixel Remaster — 致命鬼牌成就／Joker’s Death achievement
Steam build 20265119 · 2026-10-16
File: FF6_PR_JokerAchievement_20265119.CT

效果／Effect
只解鎖「在老虎機擲出致命鬼牌」成就（gambler_master），透過遊戲的 SteamSDKManager.SetAchievment 與 UploadUserStats。不是強制老虎機結果，不會觸發致命鬼牌、戰鬥結算或擊倒敵人。
Unlocks only gambler_master through the game's SteamSDKManager.SetAchievment and UploadUserStats. Does not force Slots results, execute Joker’s Death, resolve battles or defeat enemies.

使用／Use
僅支援 Steam build 20265119。Cheat Engine 連接 FINAL FANTASY VI.exe，讀取存檔後停在一般地圖並暫停操作。載入 CT 預設不執行，勾選唯一項目一次。
Requires Steam build 20265119. Attach Cheat Engine to FINAL FANTASY VI.exe, load a save and remain idle on a normal field map. Opening the table does not execute it; enable its single entry once.

套用前會在 Cheat Engine 安裝目錄建立 JSON 狀態快照；無法寫入就停止。這不是可直接取代加密存檔的完整備份，也無法撤銷 Steam 成就。取消勾選不會撤銷成就。
Creates a JSON state snapshot in the Cheat Engine installation directory before unlocking; stops if the snapshot cannot be written. This is not a complete replacement for encrypted saves and cannot undo Steam achievements. Disabling does not revoke the achievement.

實測／Validation
唯讀檢查通過；同份核心 Lua 已經由本機測試包套用，RESULT true nil。
Read-only preflight passed; the same core Lua was applied through a local test wrapper with RESULT true nil.
gambler_master 0→1；可讀取的 Steam gambler_master stat 維持 0。其餘 36 項成就不變。
gambler_master changed 0→1; the readable Steam gambler_master stat remained 0. The other 36 achievements were unchanged.
持有 Gil 682904、累計 Gil 44127、主存檔與圖鑑擊破數 281、358 筆各怪物記錄加總 586 均不變。
Held Gil 682904, lifetime Gil 44127, main-save/bestiary kills 281 and the sum of 358 individual monster records (586) were unchanged.
背包數量、角色／技能／指令、魔石、地圖與劇情／寶箱資料核對不變。技能記錄以清單順序逐筆比對，保留相同編號的重複項目。
Inventory quantities, characters/abilities/commands, magicite and serialized map/story/chest data were verified unchanged. Ability records are compared individually in list order, preserving repeated IDs.
實測前完整存檔備份與狀態快照留在本機，不公開。
Full save backup and state snapshots were retained locally and are not published.

限制／Limitations
正式 CT 勾選介面與預設備份位置未另行實測；核心程式經本機測試包實測。未測完整重啟、其他帳號、版本或長期遊玩。使用者已在 Steam 成就頁確認解鎖。
The formal CT checkbox interface and default backup location were not separately exercised; the core code was tested via a local wrapper. Full restart, other accounts/builds and long-term play were not tested. The user confirmed the unlock on Steam's achievement page.
