FF6 Pixel Remaster — 選擇角色設定四項能力／Select a character and set four stats
Steam build 20265119 · 2026-10-16
File: FF6_PR_CharacterStats_20265119.CT

效果／Effect
每次選擇一名目前存檔中的正式角色，再分別輸入力量、敏捷、體力、魔力的目標值。這是設定目標，不是每次加上輸入的數字；相同目標重複執行不會累加。
Selects one permanent role present in the loaded save and prompts separately for Strength, Speed, Stamina and Magic targets. These are absolute targets rather than increments; repeating the same targets does not stack increases.

角色選擇／Character selection
清單使用本版角色的繁中名稱與英文名稱，並標示隊伍位置或後備。以 characterStatusId 與 jobId 辨識 14 種正式角色，不將內部記錄 ID 或隊伍第幾位當成身分。只列出目前記錄中可辨識的角色，不新增尚未出現的角色。臨時／歷史記錄中身分或職業不符者不列入；重複身分會停止。
The list shows this build's Traditional Chinese and English role names plus current party position or Reserve. Identifies the 14 permanent roles using characterStatusId and jobId rather than record IDs or party positions. Lists only roles recognized in the current records; does not create absent characters. Guest/historical records with mismatched status/job are excluded; duplicate role identities stop execution.

「基礎數值」定義與範圍／Meaning of natural stats and allowed range
目標是不含裝備加成的永久能力，即遊戲 NaturalPower / NaturalAgility / NaturalVitality / NaturalMagic。透過角色存檔的四個永久能力加值設定，保留角色原生基值，不更改共用角色模板。原有魔石成長／先前修改形成的能力加值會計入目前值。
Targets are the permanent stats before equipment, as returned by the game's NaturalPower / NaturalAgility / NaturalVitality / NaturalMagic. Sets the four saved permanent stat bonuses while preserving innate base fields and shared character templates. Existing esper growth or earlier edits contribute to the current value.
各項可輸入範圍會顯示在提示：該角色原生基值（至少 1）至 128，只接受整數。可降低之前提高過的能力，但此版不支援低於角色原生基值，不寫入負數加值。
Each prompt shows its allowed range: the character's innate base (at least 1) through 128, integers only. Previously boosted stats can be reduced, but this version does not lower them below the innate base or write negative bonuses.
輸入 60 是讓不含裝備的能力變成 60；裝備加成仍另外計算。例如塞策原本敏捷 57、裝備 +3、畫面 60，若在此表輸入敏捷 60，裝備不變時畫面預期為 63，而不是維持 60。
Entering 60 targets the value before equipment. Equipment still applies separately: Setzer with natural Speed 57 and equipment +3 displays 60; entering 60 here would normally display 63 with the same equipment.

使用／Use
1. 備份存檔；讀取遊戲，停在一般地圖並暫停操作。
   Back up the save, load the game and remain idle on a normal field map.
2. Cheat Engine 連接 FINAL FANTASY VI.exe，載入 CT，勾選唯一項目。
   Attach Cheat Engine to FINAL FANTASY VI.exe, open the CT and enable its single entry.
3. 由名稱清單選擇一名角色；依序輸入四項目標。預設為目前不含裝備數值；不想改某項可直接保留預設。
   Select a role by name, then enter four targets. Defaults are the current natural values; retain a default to leave that stat unchanged.
4. 最後摘要顯示角色與四項原值→目標，選「是」才會寫入。若角色選單關閉、任何輸入按取消、最後選否，四項皆不套用。非法輸入也會在寫入前停止。
   The final summary shows the role and all four before→target values; Yes applies the edit. Closing role selection, cancelling any input or choosing No applies none of the four changes. Invalid input also stops before writing.
5. 重開角色狀態頁核對，另存新欄位；換裝後顯示數值可能不同。
   Reopen the status menu, verify and save to a new slot. Displayed stats may change with equipment.

保護與備份／Checks and backup
僅支援 Steam build 20265119，需 Mono collector。開啟檔案不執行，取消勾選不會還原。此表與 StatsBoost（目前隊伍每項加 1–30）分開；勿同時套用其他 CT 或在輸入期間操作遊戲。
Requires Steam build 20265119 and Mono collector. Opening does not run the table; disabling does not undo it. Separate from StatsBoost, which increments current-party stats by 1–30. Do not run other CTs or play while entering values.
輸入完成後會重核對快照；角色、裝備造成的計算值或相關遊戲資料若變動則停止。寫入前會在 Cheat Engine 安裝目錄保存帶原加值與目標值的文字快照，寫入失敗會停止。快照不是可直接載入的完整存檔；記憶體位址只對當次程序有效。
Rechecks the snapshot after input; changes to captured character/calculated equipment values or related game data stop the edit. Before writes, saves a text snapshot with original and target bonuses in the Cheat Engine installation directory; backup failure stops execution. This is not a loadable full save, and memory addresses are valid only for that process.
只寫所選角色的四項永久能力加值，呼叫遊戲 UpdateParameter 更新，核對目標與其他角色／技能、等級／經驗值／HP／MP、魔石、背包、金錢、各種擊破數、地圖與成就；失敗會嘗試還原本次四項原加值。還原本身失敗時會回報錯誤及備份路徑。
Writes only the selected role's four permanent stat bonuses, calls the game's UpdateParameter, and verifies targets plus unrelated characters/abilities, levels/EXP/HP/MP, magicite, inventory, Gil, kill counts, map and achievements. On failure it attempts to restore the four original bonuses; rollback failure reports an error and backup path.

驗證／Validation
2026-10-16：相同核心 Lua 全文成功編譯並完成唯讀預檢，目前 12 名正式角色／48 項能力全部通過。已在實際選單看到塞策標示隊伍第 4 位，不需輸入記錄編號。
2026-10-16: The complete core Lua compiled and passed live read-only preflight for all 12 current roles / 48 stats. The actual role menu displayed Setzer as Party 4; no record number is required.
以不寫入模式測試角色選單、四項輸入、最終摘要：選塞策、四項輸入 60，摘要顯示力量 36→60、敏捷 57→60、體力 32→60、魔力 29→60；最後按否，回報 STAT EDITOR CANCELLED final confirmation; no writes，RESULT true nil。
Tested role selection, all four inputs and the final summary in no-write mode: selected Setzer and entered 60 for all four, displaying Strength 36→60, Speed 57→60, Stamina 32→60 and Magic 29→60. Chose No; the log reported STAT EDITOR CANCELLED final confirmation; no writes, RESULT true nil.
本次沒有套用任何能力修改；塞策維持不含裝備敏捷 57、畫面 60。新版四項實際寫入、回復流程、預設備份位置、正式 CT 勾選介面、存檔重讀、完整重啟及其他角色／版本的寫入尚未實測。先前塞策單項敏捷修改成功，不等於這份四項流程已完成寫入實測。
No stat edits were applied during this work; Setzer retained natural Speed 57 and displayed 60. The new four-stat write/rollback paths, default backup location, formal CT checkbox interface, save/reload, full restart and writes for other roles/builds were not tested. The earlier successful single-stat Setzer edit does not establish live write validation for this four-stat editor.
