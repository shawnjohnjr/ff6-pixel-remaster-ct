FF6 Pixel Remaster — 全怪物圖鑑／Full Bestiary CT
Steam build 20265119 · 驗證日期／Validated: 2026-10-15

檔案／File
FF6_PR_AllBestiary_20265119.CT
獨立的一次性 CT，不需要啟用其他作弊表。開啟時預設未勾選，不自動執行。
A separate one-shot table; no other cheat table is required. It starts inactive and does not run on opening.

效果／Effect
補齊本版 358 筆怪物／型態資料，對應 346 個圖鑑項目。已有擊破次數保留，缺少或為 0 的記錄只補至 1。
Registers the build's 358 monster/form records, corresponding to 346 grouped bestiary entries. Existing defeat counts are retained; missing or zero records are raised only to 1.

保存共用圖鑑，呼叫遊戲原本的圖鑑成就檢查與 Steam 同步。沒有直接呼叫 Steam 解鎖 API，也沒有偽造完成度數字。
Saves the shared bestiary and calls the game's own bestiary achievement calculation and Steam upload. It does not directly call a Steam unlock API or supply a fabricated completion value.

保留圖鑑原有劇情旗標與總擊破數，並核對角色身分、職業、技能、指令、等級、經驗值、四項能力、HP/MP、裝備魔石、金錢、主存檔擊破數及地圖不變。
Preserves the bestiary's scenario flags and total defeat counter. Checks character identities/jobs, abilities, commands, levels, EXP, four stats, HP/MP, equipped magicite, Gil, the main-save kill counter and map for changes.

需求／Requirements
僅限 Steam build 20265119，需要 Cheat Engine Mono collector、已初始化的 Steam 連線與可寫入備份檔的位置。版本或資料檢查失敗會停止。
Requires Steam build 20265119, Cheat Engine Mono collector, initialized Steam integration and a writable backup location. Build or data mismatches stop execution.

操作／Use
1. 先完整備份 FF6 PR 的存檔資料夾，包括共用圖鑑；讀取遊戲並停在一般地圖，暫停操作。
   Back up the entire FF6 PR save folder, including shared bestiary data. Load the game and stop moving on a normal field map.
2. Cheat Engine 連接 FINAL FANTASY VI.exe，開啟此 CT。
   Attach Cheat Engine to FINAL FANTASY VI.exe and open this CT.
3. 勾選唯一項目一次，等待完成提示。
   Enable its single entry once and wait for the completion message.
4. 在遊戲圖鑑與 Steam 成就頁核對。圖鑑本身會寫入共用圖鑑檔，不依賴另存角色存檔。
   Verify the in-game bestiary and Steam achievement page. The bestiary is written to its shared file independently of a character save slot.

備份與還原／Backups and undo
寫入前會在 Cheat Engine 安裝目錄產生 FF6_Bestiary_before_日期_時間_編號.json，完成提示會列出完整路徑。無法建立備份時，會在修改前停止。
Before writing, creates FF6_Bestiary_before_DATE_TIME_TICK.json in the Cheat Engine installation directory; the completion message shows its full path. If backup creation fails, it stops before changing the bestiary.

此 JSON 是供復原工具使用的明文快照，不是可直接覆蓋遊戲加密檔的存檔。請另保留前述完整資料夾備份。
The JSON is a plaintext snapshot for recovery tooling, not a file to copy over the game's encrypted data. Also retain the full-folder backup described above.

取消勾選不會撤銷登錄。共用圖鑑跨存檔共用，讀取較舊角色存檔不會自動還原；已解鎖的 Steam 成就也不會因此收回。
Disabling does not undo registration. The bestiary is shared across save slots, so loading an older character save does not restore it; unlocked Steam achievements are not revoked by doing so.

若替換記錄或保存前的核對失敗，會嘗試恢復原圖鑑字典並保存。成就同步失敗時，完成的圖鑑仍可能已保存；請以圖鑑和 Steam 回報分別判斷結果。
If record replacement or pre-save verification fails, it attempts to restore the original dictionary and save it. If achievement sync fails, the completed bestiary may already be saved; assess bestiary completion and Steam status separately.

實測結果／Observed results
圖鑑：54/346 → 346/346。怪物／型態記錄：54 → 358，補齊 304 筆。原有擊破數與總擊破數 238 均保留。
Bestiary: 54/346 → 346/346. Monster/form records: 54 → 358, completing 304 records. Existing counts and total defeats of 238 were preserved.

Steam：picture_book_173（50%）與 picture_book_346（100%）均從未解鎖變為已解鎖。10% 原本已解鎖，維持不變；其餘 34 個成就狀態未變。使用者已在 Steam 成就頁確認解鎖。
Steam: picture_book_173 (50%) and picture_book_346 (100%) changed from locked to unlocked. The already-unlocked 10% achievement remained unlocked, and the other 34 achievement states were unchanged. The user confirmed the unlocks on Steam's achievement page.

呼叫遊戲的圖鑑檔讀取方法重新載入後，仍為 346/346、358 筆記錄且缺少 0；Steam 三項圖鑑成就維持解鎖。正式 CT 的預設未啟用狀態、預設備份路徑、再次啟用不重複增加記錄及完成提示已確認。
After reloading the shared bestiary through the game's load method, it remained 346/346 with 358 records and 0 missing; all three bestiary achievements remained unlocked. The delivered CT's initially inactive state, default backup location, repeat execution without duplicate records and completion message were checked.

範圍／Scope
已驗證共用圖鑑檔重讀，未重啟整個遊戲，也未在其他帳號、作業系統或版本重測。不修改戰鬥或主線劇情進度。
Shared-bestiary file reload was verified; a full game restart and other accounts, operating systems or builds were not tested. Does not edit battles or story progress.
