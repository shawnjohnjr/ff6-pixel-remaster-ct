FF6 Pixel Remaster — 造訪所有地方成就／All-locations achievement
Steam build 20265119 · 實測／Validated: 2026-10-15
File: FF6_PR_WorldVisitAchievement_20265119.CT

效果／Effect
指定 area_visit，透過遊戲的 SteamSDKManager.SetAchievment 與 UploadUserStats 解鎖。只處理 Steam 成就，不傳送角色、不修改造訪／探索／劇情旗標，不會讓未到過的地方變成遊戲內已造訪。
Unlocks area_visit through the game's SteamSDKManager.SetAchievment and UploadUserStats. Targets the Steam achievement only; does not teleport, edit visit/exploration/story flags or mark unvisited locations as visited in the game.

實測／Observed result
area_visit: 0→1；Steam area_visit stat 保持 0。
area_visit changed 0→1; the readable Steam area_visit stat remained 0.
本次套用前後：持有 Gil 909037、累計 Gil 38360、主存檔／圖鑑擊破數 247、358 筆怪物記錄加總 552 均維持。與前一份測試不同的基準，來自兩次操作之間的正常遊玩。
Before/after this operation: held Gil 909037, lifetime Gil 38360, main-save/bestiary kills 247 and the 358-record sum 552 were retained. The baseline differs from the preceding test because normal play occurred between operations.
一般背包數量、角色資料、技能、魔石、目前區域／地圖與序列化地圖資料核對不變；其餘 36 項成就未變。
Normal-inventory quantities, characters, abilities, magicite, current area/map and serialized map data were unchanged; the other 36 achievements were unchanged.
Steam API 已確認解鎖；使用者在 Steam 頁面的確認尚待回覆。
The Steam API confirmed the unlock; user confirmation on Steam's page is pending.

需求與使用／Requirements and use
僅支援 Steam build 20265119、Cheat Engine Mono collector、已初始化的 Steam 與已讀取的遊戲存檔。停在一般地圖並暫停操作後，連接 FINAL FANTASY VI.exe，開啟 CT 並勾選唯一項目一次。開檔預設不啟用；不要同時套用其他 CT。
Requires Steam build 20265119, Cheat Engine Mono collector, initialized Steam integration and a loaded save. Remain idle on a normal field map, attach to FINAL FANTASY VI.exe, open the CT and enable its single entry once. Opening does not execute it. Do not run other edits simultaneously.

修改前在 Cheat Engine 安裝目錄建立狀態 JSON 快照，完成訊息顯示路徑。無法寫入快照會停止。這不是可直接取代加密存檔的檔案，也不會撤銷已解鎖的 Steam 成就。完整存檔備份另保留在本機，不公開。
Creates a JSON state snapshot in the Cheat Engine installation directory before changes, showing the path on completion. Snapshot-write failure stops execution. The snapshot cannot directly replace encrypted saves or undo unlocked Steam achievements. Full save backups are kept locally and are not published.

取消勾選不會撤銷成就。只在目前帳號／版本實測；未完整重啟遊戲、未測其他帳號／系統／版本或長期遊玩。成就解鎖與遊戲存檔統計可以不同，不能以 Steam 統計當成遊戲記錄已被修改的證據。
Disabling does not revoke achievements. Tested only on the current account/build; a full restart, other accounts/systems/builds and long-term play were not tested. Achievement/platform statistics may differ from game-save statistics; a platform stat change alone does not show that the save was edited.
