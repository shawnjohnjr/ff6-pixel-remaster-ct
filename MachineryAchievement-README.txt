FF6 Pixel Remaster — 補齊 8 種機械與成就／All 8 tools and achievement
Steam build 20265119 · 實測／Validated: 2026-10-15
File: FF6_PR_MachineryAchievement_20265119.CT

效果／Effect
補齊本版 8 種機械道具（content ID 31–38），缺少的各補 1 個；已有數量保留，不減少或重複增加。以 OwnedItemClient.AddOwnedItem 正常取得道具，再呼叫 AchievementManager.UpdateMachineAll 與 Steam 同步。此表不是只有成就：會實際增加缺少的機械。
Completes the build's 8 tool items (content IDs 31–38), adding one only when absent and retaining higher quantities. Uses normal OwnedItemClient.AddOwnedItem acquisition, then AchievementManager.UpdateMachineAll and Steam upload. This table grants missing tools as well as checking the achievement.

實測／Observed result
持有機械種類：4→8。ID 33、35、36、37 各 0→1；31、32、34 保持 1；38 保持 2。
Owned tool types: 4→8. IDs 33,35,36,37 changed 0→1; 31,32,34 remained 1; 38 remained 2.
machinery_master: 0→1. Steam machinery stat remained 0; unlock status was verified through the actual achievement API.
一般背包其他道具逐項數量不變。持有 Gil 908303、累計 Gil 37626、主存檔／圖鑑總擊破數 245、個別次數加總 550 均維持。
All other normal-inventory quantities were unchanged. Held Gil 908303, lifetime Gil 37626, main-save/bestiary kill totals 245 and individual-count sum 550 were retained.
其餘 36 項成就狀態不變。使用者已確認 8 種機械清單與 Steam 成就。
The other 36 achievements were unchanged. The user confirmed all 8 tools in the menu and the Steam achievement.

道具保存與錯誤／Item persistence and errors
請在遊戲中另存新欄位以保留道具。未測存檔重讀或 8 種機械的戰鬥效果。取消勾選不移除道具；執行途中失敗可能留下已新增的道具，不宣稱完整自動回滾。
Save to a new game slot to retain the tools. Save/reload and the eight tools' combat effects were not tested. Disabling does not remove items; a failure mid-run can leave tools already granted, so full automatic rollback is not claimed.

需求與使用／Requirements and use
僅支援 Steam build 20265119、Cheat Engine Mono collector、已初始化的 Steam 與已讀取的遊戲存檔。停在一般地圖並暫停操作後，連接 FINAL FANTASY VI.exe，開啟 CT 並勾選唯一項目一次。開檔預設不啟用；不要同時套用其他 CT。
Requires Steam build 20265119, Cheat Engine Mono collector, initialized Steam integration and a loaded save. Remain idle on a normal field map, attach to FINAL FANTASY VI.exe, open the CT and enable its single entry once. Opening does not execute it. Do not run other edits simultaneously.

修改前在 Cheat Engine 安裝目錄建立狀態 JSON 快照，完成訊息顯示路徑。無法寫入快照會停止。這不是可直接取代加密存檔的檔案，也不會撤銷已解鎖的 Steam 成就。完整存檔備份另保留在本機，不公開。
Creates a JSON state snapshot in the Cheat Engine installation directory before changes, showing the path on completion. Snapshot-write failure stops execution. The snapshot cannot directly replace encrypted saves or undo unlocked Steam achievements. Full save backups are kept locally and are not published.

取消勾選不會撤銷成就。只在目前帳號／版本實測；未完整重啟遊戲、未測其他帳號／系統／版本或長期遊玩。成就解鎖與遊戲存檔統計可以不同，不能以 Steam 統計當成遊戲記錄已被修改的證據。
Disabling does not revoke achievements. Tested only on the current account/build; a full restart, other accounts/systems/builds and long-term play were not tested. Achievement/platform statistics may differ from game-save statistics; a platform stat change alone does not show that the save was edited.
