FF6 Pixel Remaster — 隱藏道具全收集成就／Hidden-item Achievement
Steam build 20265119 · 實測／Validated: 2026-10-15
File: FF6_PR_HiddenItemAchievements_20265119.CT

標題與效果／Title and effect
隱藏道具全收集成就｜暫補 50 旗標→檢查成就→還原道具狀態｜不領取道具
Hidden-item achievement: temporarily complete 50 flags, check, restore; no loot.

獨立 CT，只有一個預設未勾選的項目，開檔不自動執行。只處理隱藏道具全收集成就，不需要其他 CT。
Standalone CT with one initially inactive entry. Opening does not execute it. Targets only the all-hidden-items achievement; no other CT is required.

依本版資料去重取得 50 個隱藏道具旗標，暫時補齊，呼叫遊戲的 AchievementManager.UpdateHiddenItems，隨即還原完整寶物旗標陣列並核對地圖資料，再上傳 Steam 成就。沒有直接呼叫 Steam 解鎖方法。
Temporarily completes this build's 50 distinct hidden-item flags, calls the game's AchievementManager.UpdateHiddenItems, immediately restores the entire treasure flag array and verifies map data, then uploads Steam stats. Does not directly invoke a Steam unlock method.

不補發道具、不永久標記為已取得。完成後遊戲內隱藏道具進度仍保持原值，未取得的位置保留原旗標供之後探索。寶箱收集旗標不變。
No items are granted and no permanent collected state is applied. The in-game hidden-item count returns to its original value; uncollected locations retain their flags for later exploration. Chest flags remain unchanged.

操作／Use
1. 先備份整個 FF6 PR 存檔資料夾。開啟 Steam、讀取存檔並停在一般地圖，執行期間不要移動、換地圖或存檔。
   Back up the entire FF6 PR save folder. Start Steam, load a save and remain idle on a normal field map. Do not move, change maps or save during execution.
2. Cheat Engine 連接 FINAL FANTASY VI.exe，開啟此 CT，勾選唯一項目一次，等待成就狀態與還原完成提示。
   Attach Cheat Engine to FINAL FANTASY VI.exe, open this CT, enable its single entry once and wait for the achievement/restoration message.
3. 在 Steam 成就頁確認隱藏道具全收集成就。此 CT 無需另存角色存檔；請等完成後才關閉工具或遊戲。
   Confirm the all-hidden-items achievement on Steam. No character-slot save is needed; wait for completion before closing the tool or game.
4. 完成後可取消勾選；再次執行需先取消再勾選。取消勾選不收回 Steam 成就。
   Uncheck after completion; uncheck and recheck to run again. Disabling does not revoke the Steam achievement.

需求與保護／Requirements and checks
僅支援 Steam build 20265119，需要 Mono collector、已初始化的 Steam 連線及可寫入的備份位置。使用 metadata 定位，無固定程序位址。版本、欄位、旗標對照或計數不符時，會在寫入前停止。
Requires Steam build 20265119, Mono collector, initialized Steam integration and a writable backup location. Uses metadata lookup without fixed process addresses. Build, field, flag or count mismatches stop before writing.

寫入前在 Cheat Engine 安裝目錄建立 FF6_HiddenFlags_before_日期_時間_編號.json，完成提示會顯示路徑。此檔為地圖資料明文快照，供復原工具使用，不能直接覆蓋加密存檔；請保留完整資料夾備份。
Creates FF6_HiddenFlags_before_DATE_TIME_TICK.json in the Cheat Engine installation directory before writing; the result dialog displays its path. This plaintext map snapshot is for recovery tooling, not a replacement for an encrypted save. Keep the full-folder backup too.

成就檢查發生一般 Lua／遊戲方法錯誤也會執行還原與驗證。工具或遊戲突然終止，則無法保證還原程式能完成。請保持地圖靜止，等提示完成。
Ordinary Lua/game-method errors still run restoration and verification. Abrupt termination of the tool or game can prevent cleanup. Stay idle until the completion message.

實測／Observed results
隱藏道具：9/50 → 暫時 50/50 → 還原 9/50；暫時補齊 41 個旗標。
Hidden items: 9/50 -> temporarily 50/50 -> restored 9/50; 41 flags temporarily completed.
寶箱：38/214 → 38/214；主存檔 openChestCount：38 → 38。
Chests: 38/214 -> 38/214; main-save openChestCount: 38 -> 38.
Steam API：get_hidden_item：0（未解鎖）→ 1（已解鎖）；其餘 36 項成就狀態不變。
Steam API: get_hidden_item changed from 0 (locked) to 1 (unlocked); all other 36 achievement states were unchanged.

此成就是完成與否的條件，不以可讀的 50 點 Steam 收集統計表示。GetAchievmentProgress('get_hidden_item') 本次仍回傳 0；解鎖驗證採用 GetAllAchievementsOnPlatform 的實際成就狀態。
This achievement uses a completion condition rather than a readable 50-point Steam collection stat. GetAchievmentProgress('get_hidden_item') still returned 0 in this test; unlock verification used the actual achievement state returned by GetAllAchievementsOnPlatform.

完整 512 bytes 寶物旗標及 DataStorage.Serialize 地圖資料核對一致。角色身分、技能、指令、等級、四項能力、HP/MP、經驗值、金錢、魔石、擊破數與目前地圖不變。正式 CT 的標題、未啟用預設、勾選執行、預設備份、雙語完成提示及重複執行已確認。
The full 512-byte treasure array and serialized map data matched their original snapshots. Character identities, abilities, commands, levels, four stats, HP/MP, EXP, Gil, magicite, kill count and map were unchanged. The delivered CT's title, inactive default, checkbox execution, default backup, bilingual result dialog and repeat execution were verified.

驗證範圍／Validation scope
Steam API 已確認解鎖；使用者已在 Steam 成就頁確認解鎖。未重啟整個遊戲，未測其他帳號／系統／版本，也未實際拾取還原後的隱藏道具。保留探索的驗證依據為完整旗標與地圖資料完全一致。
Unlock confirmed through the Steam API and by the user on Steam's achievement page. A full restart, other accounts/systems/builds and collecting a hidden item after restoration were not tested. Exploration-state preservation was verified by an exact flag-array and full map-data match.
