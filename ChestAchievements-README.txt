FF6 Pixel Remaster — 寶箱收集成就／Chest Collection Achievements
Steam build 20265119 · 驗證／Validated: 2026-10-15

檔案／File: FF6_PR_ChestAchievements_20265119.CT
獨立 CT，只有一個預設未勾選的項目；開檔不自動執行。
Standalone CT with one initially inactive entry; opening does not execute it.

標題與效果／Entry title and effect
寶箱全收集成就｜暫時補齊 214 旗標→檢查成就→還原寶箱｜不領取道具
Chest achievements: temporarily complete 214 flags, check achievements, restore original flags; no loot.

只解鎖寶箱收集成就。暫時補齊本版 214 個寶箱旗標，呼叫遊戲的 AchievementManager.UpdateChest，隨即還原整個寶箱旗標陣列，再上傳 Steam 成就。沒有直接呼叫 Steam 解鎖方法，也不保存暫時的全開狀態。
Targets chest achievements only. Temporarily completes this build's 214 chest flags, calls the game's AchievementManager.UpdateChest, immediately restores the entire treasure flag array, then uploads Steam stats. It does not call a Steam unlock method directly or save the temporary all-open state.

完成後遊戲內寶箱收集進度仍是原本的數量，Steam 的 treasure_box 成就統計則可為 214。這是本 CT 刻意保留探索進度的效果，不代表還原失敗。未開啟寶箱的旗標會保持原樣，之後仍可正常探索；不補發寶箱道具，不永久標記全開，也不解鎖隱藏道具收集成就。
Afterward the game's chest count remains at its original value while Steam's treasure_box stat can read 214. This intentionally preserves exploration progress. Originally unopened flags remain unchanged for later exploration. No chest loot is granted, no permanent all-open state is applied, and hidden-item achievements are not targeted.

操作／Use
1. 備份整個 FF6 PR 存檔資料夾。開啟 Steam、讀取遊戲並停在一般地圖上，執行期間不要移動、切換地圖或存檔。
   Back up the entire FF6 PR save folder. Start Steam, load the game and remain idle on a normal field map. Do not move, change maps or save during execution.
2. Cheat Engine 連接 FINAL FANTASY VI.exe，開啟此 CT，勾選唯一項目一次，等待還原完成提示。
   Attach Cheat Engine to FINAL FANTASY VI.exe, open this CT, enable its single entry once and wait for the restoration message.
3. 至 Steam 成就頁確認寶箱收集的 50% 與 100% 成就。此 CT 無須另存角色存檔；完成提示出現前請勿關閉工具或遊戲。
   Confirm the 50% and 100% chest achievements on Steam. No character-slot save is needed for this CT; do not close the tool or game before completion.
4. 可取消勾選；再次使用需先取消再勾選。取消勾選不會收回已解鎖的 Steam 成就。
   Uncheck after completion; uncheck and recheck to run again. Disabling does not revoke Steam achievements.

保護與備份／Checks and backup
限定 Steam build 20265119，透過 metadata 定位，不使用固定程序位址。需要 Mono collector、已初始化的 Steam 與可寫入的備份位置。版本、資料、214 個旗標與現有計數不符時會在寫入前停止。
Restricted to Steam build 20265119, with metadata-based lookup and no fixed process addresses. Requires the Mono collector, initialized Steam integration and a writable backup location. Build, data, flag or count mismatches stop execution before writing.

寫入前會在 Cheat Engine 安裝目錄建立 FF6_ChestFlags_before_日期_時間_編號.json，提示會列出路徑。這是地圖資料明文快照，供復原工具使用，不能直接覆蓋遊戲加密存檔；完整存檔資料夾備份仍應保留。
Before writing, creates FF6_ChestFlags_before_DATE_TIME_TICK.json in the Cheat Engine installation directory and displays its path. This plaintext map-data snapshot is for recovery tooling, not a replacement for an encrypted game save. Retain the full-folder backup too.

即使成就檢查發生一般 Lua／遊戲方法錯誤，也會執行旗標還原與驗證。整個程序或遊戲突然中斷則無法保證還原程式能執行。執行時保持地圖靜止，避免暫時旗標期間發生其他遊戲操作。
Restoration and verification run even if the achievement check raises an ordinary Lua/game-method error. An abrupt tool or game termination can prevent cleanup. Remain idle to avoid unrelated game operations during the temporary flag window.

實測／Observed test
寶箱：38/214 → 暫時 214/214 → 還原 38/214；本次暫時補齊 176 個旗標。
Chests: 38/214 -> temporarily 214/214 -> restored 38/214; 176 flags temporarily completed.
隱藏道具：9 → 9；主存檔寶箱計數：38 → 38。
Hidden items: 9 -> 9; main-save chest counter: 38 -> 38.
Steam treasure_box_22: 1 -> 1; treasure_box_107: 0 -> 1; treasure_box_214: 0 -> 1.
Steam treasure_box progress: 38 -> 214.
使用者已在 Steam 成就頁確認 50% 與 100% 兩項皆已解鎖。
The user confirmed both 50% and 100% unlocks on Steam's achievement page.

完整 512 bytes 寶箱旗標陣列及序列化地圖資料核對一致；主線旗標、全域／區域／地圖變數不變。角色技能、指令、等級、能力、HP/MP、經驗值、金錢、魔石、擊破數與目前地圖核對不變。其餘 34 個 Steam 成就狀態不變。
The entire 512-byte treasure flag array and serialized map state matched their original snapshots; scenario flags and global/area/map variables were unchanged. Checked character abilities, commands, levels, stats, HP/MP, EXP, Gil, magicite, kill count and current map were unchanged. The other 34 Steam achievement states were unchanged.

正式 CT 的標題、預設不啟用、實際勾選執行、預設備份路徑、雙語完成提示與再次執行均已確認。
The delivered CT's title, inactive default, actual checkbox execution, default backup location, bilingual completion message and repeat execution were checked.

限制／Limits
未重啟整個遊戲，未在其他帳號／系統／版本實測，也未實際打開一個還原後的寶箱。保留探索的驗證依據是旗標陣列與完整地圖資料完全一致。
A full game restart, other accounts/systems/builds and opening a chest after restoration were not tested. Preservation of exploration state was verified by an exact flag-array and full map-data match.
