FF6 Pixel Remaster — 擊破 2000 隻成就／2000-kill achievement
Steam build 20265119 · 實測／Validated: 2026-10-15
File: FF6_PR_Kill2000Achievement_20265119.CT

效果／Effect
指定 Steam monster_hunt_2000 成就，透過遊戲的 SteamSDKManager.SetAchievment 與 UploadUserStats 處理。不寫入主存檔擊破數、共用圖鑑總數或各怪物次數，不重播戰鬥。
Targets Steam monster_hunt_2000 through the game's SteamSDKManager.SetAchievment and UploadUserStats. Does not write main-save kills, shared-bestiary totals or individual monster counts, or replay battles.

Steam 可能連動提升 monster_hunt 進度並解鎖 100／1000 隻低階成就；標題已註明，不能保證只解一項。此次實測連帶解鎖 1000 隻，使用者同意保留並已確認成就達成。
Steam may raise the linked monster_hunt stat and unlock the 100/1000 lower tiers; the title states this, and a single unlock is not guaranteed. This test also unlocked the 1000 tier; the user accepted retaining both and confirmed achievement completion.

實測／Observed result
主存檔 245→245；圖鑑總數 245→245；358 筆怪物次數逐筆不變，加總 550→550。
Main-save kills 245→245; bestiary total 245→245; all 358 individual counts unchanged, sum 550→550.
Steam monster_hunt: 246→2000.
monster_hunt_100: 1→1; monster_hunt_1000: 0→1; monster_hunt_2000: 0→1.
其餘 34 項非擊破成就狀態不變。修正後的完整程式已通過語法與唯讀預檢；再次啟用時若目標已解鎖，會跳過解鎖呼叫。
All other 34 non-kill achievement states were unchanged. The final full script passed compilation and read-only preflight. If the target is already unlocked, repeat activation skips the unlock call.

驗證說明／Validation note
首次實測的舊檢查原本要求 Steam 擊破統計不變，因此在平台連動後停止。後續完整唯讀回查確認遊戲計數不變；正式版已依使用者接受的連動效果修正檢查與標題。
The initial verifier expected the Steam kill stat to remain unchanged and stopped after platform linkage changed it. A complete read-only reconciliation confirmed unchanged game counts. The delivered checks/title reflect the linkage accepted by the user.

需求與使用／Requirements and use
僅支援 Steam build 20265119、Cheat Engine Mono collector、已初始化的 Steam 與已讀取的遊戲存檔。停在一般地圖並暫停操作後，連接 FINAL FANTASY VI.exe，開啟 CT 並勾選唯一項目一次。開檔預設不啟用；不要同時套用其他 CT。
Requires Steam build 20265119, Cheat Engine Mono collector, initialized Steam integration and a loaded save. Remain idle on a normal field map, attach to FINAL FANTASY VI.exe, open the CT and enable its single entry once. Opening does not execute it. Do not run other edits simultaneously.

修改前在 Cheat Engine 安裝目錄建立狀態 JSON 快照，完成訊息顯示路徑。無法寫入快照會停止。這不是可直接取代加密存檔的檔案，也不會撤銷已解鎖的 Steam 成就。完整存檔備份另保留在本機，不公開。
Creates a JSON state snapshot in the Cheat Engine installation directory before changes, showing the path on completion. Snapshot-write failure stops execution. The snapshot cannot directly replace encrypted saves or undo unlocked Steam achievements. Full save backups are kept locally and are not published.

取消勾選不會撤銷成就。只在目前帳號／版本實測；未完整重啟遊戲、未測其他帳號／系統／版本或長期遊玩。成就解鎖與遊戲存檔統計可以不同，不能以 Steam 統計當成遊戲記錄已被修改的證據。
Disabling does not revoke achievements. Tested only on the current account/build; a full restart, other accounts/systems/builds and long-term play were not tested. Achievement/platform statistics may differ from game-save statistics; a platform stat change alone does not show that the save was edited.
