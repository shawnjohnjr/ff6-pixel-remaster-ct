FF6 Pixel Remaster — 50 萬 Gil 成就／500,000 Gil achievement
Steam build 20265119 · 實測／Validated: 2026-10-15
File: FF6_PR_Gil500kAchievement_20265119.CT

效果／Effect
指定 total_gil_500000 成就，透過遊戲的 SteamSDKManager.SetAchievment 與 UploadUserStats 處理。不修改持有金錢 owendGil 或存檔累計 totalGil，不發放戰鬥獎勵。
Targets total_gil_500000 through the game's SteamSDKManager.SetAchievment and UploadUserStats. Does not edit held money (owendGil), saved lifetime Gil (totalGil), or battle rewards.

標題明列可能連帶解鎖 1 萬／10 萬 Gil 成就。原本補錢的 Gil1000000 CT 維持原用途；此表不需要啟用它。
The title states that the 10,000/100,000 Gil tiers may unlock too. The existing Gil1000000 table retains its money-editing purpose and is not required by this table.

實測／Observed result
持有 Gil：908303→908303；存檔累計 Gil：37626→37626。
Held Gil: 908303→908303; saved lifetime Gil: 37626→37626.
Steam total_gil stat: 37626→500000.
total_gil_10000: 1→1; total_gil_100000: 0→1; total_gil_500000: 0→1.
其餘 34 項成就不變。使用者已在 Steam 確認 10 萬與 50 萬兩項解鎖。
The other 34 achievements were unchanged. The user confirmed both the 100,000 and 500,000 unlocks on Steam.

擊破數、358 筆怪物記錄、角色、技能、魔石與序列化地圖資料均核對不變。正式 CT 的預設未啟用、實際勾選再次執行、預設備份路徑與雙語完成訊息已確認；重複執行不再呼叫解鎖。
Kill counts, 358 monster records, characters, abilities, magicite and serialized map data were verified unchanged. The delivered inactive default, actual repeat checkbox execution, default backup path and bilingual result dialog were checked. Repeat activation skips unlocking an already-unlocked target.

需求與使用／Requirements and use
僅支援 Steam build 20265119、Cheat Engine Mono collector、已初始化的 Steam 與已讀取的遊戲存檔。停在一般地圖並暫停操作後，連接 FINAL FANTASY VI.exe，開啟 CT 並勾選唯一項目一次。開檔預設不啟用；不要同時套用其他 CT。
Requires Steam build 20265119, Cheat Engine Mono collector, initialized Steam integration and a loaded save. Remain idle on a normal field map, attach to FINAL FANTASY VI.exe, open the CT and enable its single entry once. Opening does not execute it. Do not run other edits simultaneously.

修改前在 Cheat Engine 安裝目錄建立狀態 JSON 快照，完成訊息顯示路徑。無法寫入快照會停止。這不是可直接取代加密存檔的檔案，也不會撤銷已解鎖的 Steam 成就。完整存檔備份另保留在本機，不公開。
Creates a JSON state snapshot in the Cheat Engine installation directory before changes, showing the path on completion. Snapshot-write failure stops execution. The snapshot cannot directly replace encrypted saves or undo unlocked Steam achievements. Full save backups are kept locally and are not published.

取消勾選不會撤銷成就。只在目前帳號／版本實測；未完整重啟遊戲、未測其他帳號／系統／版本或長期遊玩。成就解鎖與遊戲存檔統計可以不同，不能以 Steam 統計當成遊戲記錄已被修改的證據。
Disabling does not revoke achievements. Tested only on the current account/build; a full restart, other accounts/systems/builds and long-term play were not tested. Achievement/platform statistics may differ from game-save statistics; a platform stat change alone does not show that the save was edited.
