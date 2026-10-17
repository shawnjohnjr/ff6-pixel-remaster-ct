FF6 Pixel Remaster — 珊瑚碎片與劇情計數同步／Coral and scenario-counter sync
Steam build 20265119 · 2026-10-17
File: FF6_PR_CoralSync25_20265119.CT

效果／Effect
將重要道具「珊瑚碎片」（content ID 47）與 ScenarioVariable[7] 都設為 25，已有更多也會降為 25。用遊戲 OwnedItemClient 增減道具，並透過 DataStorage.Set(Category=8, index=7, value=25) 同步計數。
Sets both Coral (important item content ID 47) and ScenarioVariable[7] to exactly 25, including reducing higher totals. Uses OwnedItemClient to adjust the item and DataStorage.Set(Category=8, index=7, value=25) for the counter.

適用時機／When to use
僅限埃博希岩島洞窟的餵食寶箱事件。先觸發相關劇情，帶斯特拉哥進入洞窟，停在一般地圖且沒有對話時套用。不要在其他劇情、戰鬥或對話執行中使用。此表不自動辨識目前地圖或任務階段；版本檢查不代表時機檢查。
Use only for the hungry-chest event in Ebot's Rock. Trigger the relevant quest, bring Strago, and apply while idle on the field with dialogue closed. Do not use during other story events, battle or dialogue. The table does not automatically identify the current map or quest stage; its build guard is not a context guard.

原理／Why both values matter
本機遊戲資源 map_30861 的 sc_e_0943 在餵食時先讀 ScenarioVariable[7]：0 走無道具分支，小於 22 走「不夠」分支。達到 22 後仍有斯特拉哥／事件旗標分支。sc_e_0948_1 至 _4 的拾取事件，會分別增加劇情計數與道具。只增加背包道具不會同步這個獨立計數。
The installed map_30861 resource's sc_e_0943 checks ScenarioVariable[7]: zero takes the no-coral branch and values below 22 take the insufficient-coral branch. At 22 or more, character/event-flag conditions still apply. Pickup scripts sc_e_0948_1 through _4 separately increase the counter and grant the item. Adding inventory alone does not update this independent counter.
不足分支會清空計數並移除珊瑚道具；成功分支也會清空兩者。CT 不設定通關旗標、不隱藏寶箱，也不自動餵食。
The insufficient-coral branch resets the counter and removes Coral; success also clears both. The table does not set passage flags, hide the chest or automatically feed it.

操作／Use
連接 FINAL FANTASY VI.exe，載入 CT，勾選唯一項目一次。開檔不執行。成功後回遊戲選擇餵食，確認寶箱吃飽讓路，再另存新欄位。取消勾選不會還原；相同目標重複套用不會累加。
Attach to FINAL FANTASY VI.exe, open the table, and enable its single entry once. Opening alone does not execute it. Feed the chest normally, confirm that it moves aside, then save to a new slot. Disabling does not undo the edit. Reapplying sets the same targets rather than adding more.

備份與驗證／Backup and verification
修改前在 Cheat Engine 安裝目錄建立狀態 JSON 與 .map.json 完整事件資料快照；無法建立快照就停止。可透過 Lua 變數 FF6_CORAL_BACKUP_DIR 指定已存在且可寫入的資料夾。快照不是可直接載入的遊戲存檔，也沒有自動復原功能；請先自行備份存檔。
Before mutation, writes a state JSON and a .map.json event-state snapshot in the Cheat Engine installation directory; failure stops execution. FF6_CORAL_BACKUP_DIR may point to an existing writable folder. Snapshots are not loadable game saves and do not provide automatic undo; back up saves separately first.
核對一般背包、其他重要道具、角色資料、能力值、金錢、擊破數、魔石、成就與完整序列化事件資料；事件資料只允許 global 陣列第 7 號（從 0 起算）變為 25。執行中保持靜止，不移動、切圖、存檔或操作其他 CT。
Verifies normal inventory, other important items, characters, stats, Gil, kills, magicite, achievements and the full serialized event state. Only zero-based global index 7 may change to 25. Stay idle during execution; do not move, change maps, save or run another table.
錯誤會停止並保留備份；此表不實作自動回復。若修改後發生核對錯誤，不要反覆套用，先確認遊戲狀態。
Errors stop execution and retain backups; this table has no automatic rollback. If post-write verification fails, inspect game state before reapplying.

驗證範圍／Validation scope
相同核心已由本機測試包套用成功，使用者確認正常餵食後寶箱吃飽讓路。正式 CT 的勾選包裝與預設備份位置未另行執行實測。未測存檔重讀、完整重啟、其他版本／帳號。
The same core was applied through a local harness, and the user confirmed that normal feeding satisfied the chest and opened the passage. The published checkbox wrapper and default backup location were not separately live-tested. Save reloads, full restarts, other builds/accounts are untested.
