FF6 Pixel Remaster — 全青魔法／All Lores
Steam build 20265119 · 2026-10-16
File: FF6_PR_AllLores_20265119.CT

效果／Effect
透過遊戲的 OwnedCharacterClient.LearningAbility，讓正式斯特拉哥學會全部 24 招玩家青魔法。角色身分 characterStatusId=8、jobId=8，並非固定修改第 8 筆記錄；未正式加入會停止。只補未精通項目，保留原有技能。
Uses the game's OwnedCharacterClient.LearningAbility to teach permanent Strago all 24 player Lores. Identifies characterStatusId=8 and jobId=8 rather than hardcoding record 8; stops if he has not joined permanently. Only completes unmastered entries and preserves existing abilities.

使用／Use
讀取存檔後停在地圖，暫停操作並連接 FINAL FANTASY VI.exe。載入 CT 預設不執行，勾選唯一項目一次。不要同時套用其他 CT。完成後重開青魔法清單，另存新欄位保留；取消勾選不會還原。
Load a save, remain idle on a field map and attach to FINAL FANTASY VI.exe. Opening does not execute the table; enable its single entry once. Do not run other CTs simultaneously. Reopen the Lore menu afterward and save to a new slot; disabling does not undo learning.

備份／Backup
套用前在 Cheat Engine 安裝目錄建立 JSON 狀態快照，失敗則停止。快照並非可直接載入的加密存檔，也不是自動還原功能。實測前另做完整存檔備份並保留本機，不公開。
Creates a JSON state snapshot in the Cheat Engine installation directory before learning and stops if writing fails. The snapshot is not a loadable encrypted save or automatic undo feature. A separate full save backup was kept locally before testing and is not published.

實測／Validation
2026-10-16 唯讀檢查與本機測試包實際套用成功（RESULT true nil）。相同核心 Lua 包含於獨立 CT。已改用逐筆比對其他技能，保留相同技能 ID 的重複項目。
Read-only preflight and live application through a local test wrapper passed on 2026-10-16 (RESULT true nil). The independent CT contains the same core Lua. Other abilities are compared individually, preserving repeated ability IDs.
找到斯特拉哥角色記錄 ID 27。原有水紋吐息、復仇衝擊、投石保持 100；其餘 21 招由 0→100，最後全部 24 招為 100。能力 ID 140–163、內容 ID 470–493。
Strago's record ID was 27. Aqua Breath, Revenge Blast and Stone remained at 100; the other 21 changed 0→100, leaving all 24 at 100. Ability IDs 140–163, content IDs 470–493.
持有 Gil 752869、累計 Gil 124293、主存檔與圖鑑擊破數 334 保持不變；其他角色與技能／指令、等級／EXP／HP／MP／四項能力、魔石、背包數量、各怪物次數、地圖／劇情／寶箱資料與全部 37 項成就核對不變。
Held Gil 752869, lifetime Gil 124293 and main-save/bestiary kills 334 were unchanged. Other characters/abilities/commands, levels/EXP/HP/MP/four attributes, magicite, inventory quantities, individual monster counts, map/story/chest data and all 37 achievements were verified unchanged.
使用者已確認全部 24 招都有顯示且可選用。
The user confirmed that all 24 Lores are displayed and selectable.

範圍／Scope
只處理技能，不新增背包道具、不直接解鎖成就。正式 CT 勾選介面與預設備份位置未另行實測；戰鬥效果、存檔重讀、完整重啟、其他帳號／版本與長期遊玩未測。
Processes abilities only, grants no inventory items and does not directly unlock achievements. The formal CT checkbox interface and default backup location were not separately exercised; combat behavior, save/reload, full restart, other accounts/builds and long-term play were not tested.
