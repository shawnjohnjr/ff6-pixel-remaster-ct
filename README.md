# FF6 Pixel Remaster Cheat Engine Tables｜作弊表

**Steam build 20265119 · CrossOver · 驗證日期／Validation dates: 2026-10-14–16**

獨立 CT 檔案，依需要分開使用。README 提供中英雙語；部分附加清單與舊版使用說明仍以繁體中文撰寫。

Independent Cheat Engine tables for separate use. This README is bilingual; some supplementary lists and older usage notes remain in Traditional Chinese.

## 相容性與需求｜Compatibility and requirements

- 僅針對 Steam build **20265119**；其他版本會停止，不宣稱支援所有更新版本。仍需要 Cheat Engine Mono collector。

  Targets Steam build **20265119** only. Other builds are rejected. Cheat Engine's Mono collector is still required.
- 遊戲有 **14 名正式角色**，但內部清單可包含更多臨時與歷史記錄。CT 依正式角色身分辨識修改對象，不把記錄編號當作角色身分。

  The game has **14 permanent playable roles**, but its internal list can include additional guest and historical records. Character edits identify the actual role rather than treating a record ID as a character identity.
- 已修正早期最多 16 筆角色記錄的假設；目前 24 筆記錄的存檔已通過唯讀預檢。這不代表已驗證全部劇情與角色組合。

  The original 16-record assumption has been removed. Read-only preflight passed on the current save with 24 records. This does not establish compatibility with every story event or party combination.

## 檔案與用途｜Tables and effects

| CT | 中文 | English |
|---|---|---|
| [Gil1000000](FF6_PR_Gil1000000_20265119.CT) | 金錢設為 1,000,000；原本更多也會降至此值 | Sets Gil to 1,000,000, including reducing a higher balance |
| [TopEquipment](FF6_PR_TopEquipment_20265119.CT) | 62 種裝備：武器補至 8，防具／飾品補至 4；更多則保留 | Tops up 62 equipment types: weapons to 8, armor/relics to 4; preserves higher totals |
| [Level99](FF6_PR_Level99_20265119.CT) | 目前隊伍正式角色升至 Lv99，包含正常升級成長 | Raises current permanent party members to Lv99 using normal level growth |
| [StatsBoost](FF6_PR_StatsBoost_20265119.CT) | 四項能力各加 1–30，預設 +10，自然能力上限 128 | Adds 1–30 to Strength, Speed, Stamina and Magic; default +10, natural-stat cap 128 |
| [Supplies](FF6_PR_Supplies_20265119.CT) | 特級乙太、終極萬靈藥、傳送石、魔石碎片，各自選擇補至 1–99 | Separate target totals of 1–99 for X-Ether, Megalixir, Teleport Stone and Magicite Shard |
| [TerraUltimaQuick](FF6_PR_TerraUltimaQuick_20265119.CT) | 僅讓蒂娜學會究極與神速 | Teaches only Ultima and Quick to Terra |
| [AllMagicite](FF6_PR_AllMagicite_20265119.CT) | 補齊全部 27 種魔石；不自動學會魔法 | Grants all 27 magicite; does not teach spells automatically |
| [AllRages](FF6_PR_AllRages_20265119.CT) | 嘎嗚學會 252 種狂怒 | Teaches Gau all 252 Rages |
| [AllLores](FF6_PR_AllLores_20265119.CT) | 斯特拉哥學會 24 招青魔法；取得尚未實測 | Teaches Strago all 24 Lores; acquisition remains untested |
| [AllBestiary](FF6_PR_AllBestiary_20265119.CT) | 全圖鑑 346/346，並透過遊戲正常檢查圖鑑成就 | Completes the 346-entry bestiary and invokes the game's normal bestiary achievement check |
| [ChestAchievements](FF6_PR_ChestAchievements_20265119.CT) | 只解寶箱成就：暫補 214 旗標、檢查後還原；不領取道具 | Chest achievements only: temporarily complete 214 flags, check, then restore; no loot |
| [HiddenItemAchievements](FF6_PR_HiddenItemAchievements_20265119.CT) | 只解隱藏道具全收集成就：暫補 50 旗標、檢查後還原；不領取道具 | Hidden-item achievement only: temporarily complete 50 flags, check, then restore; no loot |
| [Kill2000Achievement](FF6_PR_Kill2000Achievement_20265119.CT) | 解鎖 2000 隻成就；Steam 可能連帶低階成就；遊戲擊破數不變 | Unlocks 2000 kills; lower Steam tiers may follow; game kill counts unchanged |
| [Gil500kAchievement](FF6_PR_Gil500kAchievement_20265119.CT) | 解鎖 50 萬 Gil 成就；可能連帶 1 萬／10 萬；持有與累計 Gil 不變 | Unlocks 500k Gil; 10k/100k may follow; held/lifetime Gil unchanged |
| [MachineryAchievement](FF6_PR_MachineryAchievement_20265119.CT) | 補齊 8 種機械各至少 1 個並正常檢查成就；已有更多保留 | Grants missing tools to own all 8 and checks the achievement; preserves higher quantities |
| [WorldVisitAchievement](FF6_PR_WorldVisitAchievement_20265119.CT) | 解鎖造訪所有地方成就；不傳送、不補造訪／劇情旗標 | Unlocks all-locations achievement without teleporting or visit/story flag edits |
| [JokerAchievement](FF6_PR_JokerAchievement_20265119.CT) | 只解鎖致命鬼牌成就；不執行老虎機、不改角色與存檔統計 | Unlocks Joker’s Death achievement only; no Slots execution or character/save-stat edits |
| [AllDances](FF6_PR_AllDances_20265119.CT) | 莫古學會全部 8 種舞蹈；補齊未精通項目，不改等級與能力值 | Teaches Mog all 8 dances, skipping mastered entries; levels and stats unchanged |

## 使用方式｜How to use

1. 備份存檔，讀取遊戲，停在一般地圖上並暫停操作。
   Back up your save, load the game, and stop moving on a normal field map.
2. Cheat Engine 連接 `FINAL FANTASY VI.exe`，開啟需要的 CT。
   Attach Cheat Engine to `FINAL FANTASY VI.exe` and open the desired CT.
3. 勾選項目一次，依提示輸入數值，等待完成。
   Enable the desired entry once, enter any requested value, and wait for completion.
4. 重新開啟相關遊戲選單核對，確認後另存新欄位。
   Reopen the relevant in-game menu to verify the result, then save into a different slot.

寶箱與隱藏道具成就 CT 完成時會自動還原各自的收集旗標，只保留已解鎖的成就，不需要另存角色存檔。

The chest and hidden-item achievement CTs automatically restore their collection flags on completion, retaining unlocked achievements; no character-slot save is needed.

檔案預設未啟用，開啟 CT 不會自動套用。取消勾選不會還原；要完整還原請讀取原存檔。下次執行先取消勾選再勾選。除非個別表明確說明，途中失敗不會自動撤銷已完成的修改。

Tables start inactive and do not apply changes merely by opening. Disabling does not undo changes; reload the original save to undo them fully. Uncheck and recheck to run again. Unless explicitly documented for a particular table, a failure does not automatically roll back earlier completed changes.

## 行為細節｜Behavior notes

- **Lv99／能力提升：**兩份分開。Lv99 不會把力量、敏捷、體力、魔力補滿，也不補發歷史魔石加成。能力提升不改等級／經驗值，每次啟用再次累加；遇到隊伍臨時角色會停止。

  **Lv99 / stat boosts:** Separate tables. Lv99 does not maximize the four stats or retroactively award esper bonuses. Stat boosts preserve level/EXP and stack on repeated activation. Temporary party roles are rejected.
- **補給：**輸入的是目標總數，不是額外增加數量；目前更多則保留。按取消不補給。

  **Supplies:** The input is a target total, not an amount to add. Higher existing totals are preserved. Cancelling does not replenish anything.
- **魔石：**保留原有項目與順序，包含奧汀與萊汀。不自動裝備，不直接改劇情旗標；後續事件相容性未完整驗證。失敗會嘗試移除本次新增項目。

  **Magicite:** Preserves existing entries/order and includes both Odin and Raiden. Does not equip magicite or directly edit story flags. Later event compatibility is not fully verified. On failure it attempts to remove this run's additions.
- **技能：**只操作指定正式角色，未加入時以 `ROLE_NOT_READY` 停止。跳過已精通技能；已有記錄但進度為 0% 或未完成的技能仍需補學，不能只以「記錄存在」判定完成。

  **Skills:** Targets only the specified permanent role and stops with `ROLE_NOT_READY` if absent. Mastered skills are skipped. Existing records at 0% or incomplete progress still need learning; record existence alone does not establish mastery.
- **狂怒／青魔法：**252 種狂怒依此版本的 253 筆怪物對照去重，不包含對照外隱藏技能；青魔法只含 24 招玩家技能。

  **Rages / Lores:** The 252 Rages are deduplicated from this build's 253 monster mappings; unmapped hidden skills are excluded. Lores include only the 24 player skills.

## 驗證範圍｜Validation scope

| 功能／Feature | 實際驗證／Observed validation | 尚未驗證／Not tested |
|---|---|---|
| 金錢、裝備、Lv99／Gil, equipment, Lv99 | 實際套用，使用者確認顯示及操作正常／Applied; user confirmed menus and normal operation | 全部角色與裝備戰鬥效果／Every character and equipment combat effect |
| 補給／Supplies | 四項各 0→99；互不影響且金錢不變；輸入與取消介面確認／All four 0→99; other supplies/Gil preserved; input and cancellation checked | 道具使用效果、存檔重讀／Item effects and save/reload |
| 能力提升／StatsBoost | 四名隊伍角色、16 項能力唯讀預檢通過／Read-only preflight passed for 16 fields across four party members | 寫入、戰鬥、存檔重讀／Writes, combat and save/reload |
| 蒂娜魔法／Terra spells | 究極保留 100%；神速 0→100%；使用者確認兩招可選用／Ultima stayed 100%; Quick 0→100%; user confirmed both selectable | 戰鬥施法、存檔重讀／Combat casts and save/reload |
| 全魔石／AllMagicite | 4→27，新增 23 種逐項核對；使用者確認清單與裝備／4→27, all 23 additions verified; user confirmed menu/equipment | 召喚、學習、存檔重讀、後續劇情／Summons, learning, save/reload and later events |
| 全狂怒／AllRages | 9→252，新增 243 種且全部進度 100%；其他技能與角色資料核對不變；使用者確認清單新增且可選用／9→252, 243 learned; all at 100%; unrelated skills and character data verified unchanged; user confirmed the expanded menu is selectable | 戰鬥效果、存檔重讀／Combat effects and save/reload |
| 全青魔法／AllLores | ID、Lua 編譯與角色未加入保護確認／IDs, Lua compilation and missing-role guard checked | 取得、選單、戰鬥、存檔重讀／Acquisition, menus, combat and save/reload |
| 全怪物圖鑑／AllBestiary | 54→346；50% 與 100% Steam 成就解鎖且經使用者在 Steam 確認；共用圖鑑檔重讀通過／54→346; 50% and 100% Steam achievements unlocked and user-confirmed on Steam; shared-file reload passed | 完整重啟、其他帳號／系統／版本／Full restart, other accounts, systems or builds |
| 寶箱成就／ChestAchievements | 暫時 38→214→還原 38；隱藏道具 9 不變；50% 與 100% Steam 成就解鎖且使用者確認；完整旗標與地圖資料一致／Temporary 38→214→restored 38; hidden items remain 9; 50%/100% unlocks user-confirmed on Steam; exact flag/map restoration | 完整重啟、其他帳號／版本、還原後開箱／Full restart, other accounts/builds, opening a chest afterward |
| 隱藏道具成就／HiddenItemAchievements | 暫時 9→50→還原 9；寶箱維持 38；Steam API 與使用者在 Steam 確認解鎖；完整旗標與地圖資料一致／Temporary 9→50→restored 9; chests remain 38; Steam API and user on Steam confirm unlock; exact flag/map restoration | 完整重啟、其他帳號／版本、還原後拾取／Full restart, other accounts/builds, collecting afterward |
| 擊破成就／Kill2000Achievement | 1000 與 2000 隻解鎖，使用者確認；遊戲總數 245、358 筆次數不變／1000 and 2000 unlocked, user-confirmed; game total 245 and all 358 records unchanged | 其他帳號、完整重啟／Other accounts, full restart |
| Gil 成就／Gil500kAchievement | 10 萬與 50 萬解鎖，使用者 Steam 確認；持有 908303、累計 37626 不變／100k and 500k unlocked, user-confirmed; held 908303/lifetime 37626 unchanged | 其他帳號、完整重啟／Other accounts, full restart |
| 機械／MachineryAchievement | 4→8 種，補 4 種各 1；正常成就檢查通過；使用者確認清單與成就／4→8 types, four missing tools added; normal achievement check passed; menu/unlock user-confirmed | 戰鬥效果、存檔重讀／Combat effects, save/reload |
| 全地點成就／WorldVisitAchievement | area_visit 0→1；地圖／背包／遊戲統計與其他 36 成就不變／area_visit 0→1; map/inventory/game stats and other 36 achievements unchanged；使用者已確認／user confirmed | 完整重啟／Full restart |

| 致命鬼牌成就／JokerAchievement | gambler_master 0→1；其餘 36 成就、角色、背包與遊戲統計不變；使用者 Steam 確認／gambler_master 0→1; other 36 achievements, characters, inventory and game statistics unchanged; user-confirmed on Steam | 完整重啟、其他帳號／版本／Full restart, other accounts/builds |
| 全舞蹈／AllDances | 1→8，新增 7 種、全部熟練度 100；其他角色／技能與統計不變；使用者確認全部可選用／1→8, seven learned, all at 100; other characters/abilities/statistics unchanged; user confirmed all selectable | 戰鬥效果、存檔重讀／Combat effects, save/reload |

角色清單相容性修正後，12 段程式皆成功編譯並在目前存檔做唯讀預檢：11 段通過，青魔法因斯特拉哥尚未加入而正確停止。這輪沒有重複套用其他修改。不要把部分成功實測解讀成所有劇情皆適用。

After the character-record compatibility fix, all 12 Lua bodies compiled and underwent live read-only preflight: 11 passed; AllLores correctly stopped because Strago was absent. That pass did not reapply the other cheats. Successful tests of specific operations do not imply universal story compatibility.

## 全圖鑑與成就實測｜Full bestiary and achievement test

**已套用並解鎖：圖鑑 54/346 → 346/346；Steam 的 50% 與 100% 圖鑑成就皆由未解鎖變為已解鎖，使用者已在 Steam 成就頁確認。**

**Applied and unlocked: the bestiary changed from 54/346 to 346/346. Steam's 50% and 100% bestiary achievements changed from locked to unlocked, confirmed by the user on Steam's achievement page.**

此版本的 358 筆怪物／型態資料合併為 346 項。只將缺少或為零的記錄補至 1，保留原有次數與總擊破數，再用遊戲原本的 `UpdatePictureBook` 重新計算並同步。沒有直接呼叫 Steam 解鎖方法。重讀共用圖鑑檔後仍為 346/346；正式 CT 的再次啟用、預設備份及完成提示也已測試。

This build groups 358 monster/form records into 346 entries. Only missing or zero records are raised to 1; existing counts and the total defeat counter are retained. The game's `UpdatePictureBook` recalculates and uploads the result without a direct Steam unlock call. A shared-bestiary file reload retained 346/346. Repeat execution, default backup creation and the delivered CT's completion message were also checked.

圖鑑跨存檔共用，且會立即保存；讀取較舊角色存檔或取消勾選不會還原。請先備份整個存檔資料夾。CT 也會在 Cheat Engine 安裝目錄建立 JSON 快照；該快照供復原工具使用，不能直接覆蓋加密存檔。已解鎖的 Steam 成就不會因還原圖鑑而自動收回。

The bestiary is shared across slots and saved immediately; loading an older character save or disabling the entry does not undo it. Back up the entire save folder first. The CT also writes a JSON snapshot to the Cheat Engine installation directory; this snapshot is for recovery tooling, not a replacement for an encrypted save. Restoring the bestiary does not automatically revoke unlocked Steam achievements.

完整遊戲重啟、其他 Steam 帳號、系統及版本未測試。[中英雙語使用說明／Bilingual usage notes](AllBestiary-README.txt) · [實測紀錄／Validation](AllBestiary-Validation.txt) · [358 筆對照清單／358-record mapping](AllBestiary-list.txt)。

A full game restart, other Steam accounts, systems and builds were not tested. The links above provide bilingual instructions, validation and the underlying mapping.

## 寶箱成就與旗標還原｜Chest achievements with flag restoration

**已實測並由使用者在 Steam 確認：50% 與 100% 寶箱收集成就均已解鎖。寶箱進度為 38 → 暫時 214 → 還原 38，隱藏道具維持 9。**

**Tested and confirmed by the user on Steam: both 50% and 100% chest achievements unlocked. Chest progress was 38 → temporarily 214 → restored 38; hidden items remained at 9.**

此獨立 CT 的標題直接註明「暫時補齊 214 旗標→檢查成就→還原寶箱｜不領取道具」。依本版資料去重取得 214 個寶箱旗標，暫時設為完成，呼叫遊戲原本的 `UpdateChest`，立即還原完整 512 bytes 旗標陣列並核對完整序列化地圖資料一致，再上傳 Steam。沒有直接呼叫 Steam 解鎖方法、不補發道具、不永久全開，也不解鎖隱藏道具成就。

The standalone CT title describes its full effect: temporarily complete 214 flags, check achievements, restore chests, no loot. It targets this build's 214 distinct chest flags, invokes the game's `UpdateChest`, immediately restores all 512 bytes of treasure flags and verifies an exact serialized-map match before uploading Steam stats. It does not directly call a Steam unlock method, grant loot, permanently open chests or target hidden-item achievements.

遊戲的寶箱進度保持原值，Steam 的 `treasure_box` 統計可為 214；這是保留探索進度的設計。執行期間請保持一般地圖靜止，不要移動、切換地圖、存檔或關閉工具。一般方法錯誤也會執行還原，但突然終止程序無法保證清理完成。先備份完整存檔資料夾；CT 另於 Cheat Engine 安裝目錄建立明文地圖快照，不能直接取代加密存檔。

The in-game chest count stays at its original value while Steam's `treasure_box` stat can read 214; this intentionally retains exploration progress. Stay idle on a normal field map; do not move, change maps, save or close the tool during execution. Ordinary method errors run cleanup, but an abrupt process termination can prevent it. Back up the full save folder first. The CT also creates a plaintext map snapshot in the Cheat Engine installation directory; it cannot directly replace an encrypted save.

正式 CT 的勾選執行、預設備份、完成提示及重複執行已驗證。完整遊戲重啟、其他帳號／系統／版本及還原後實際開箱未測試。[中英雙語說明／Bilingual notes](ChestAchievements-README.txt) · [實測紀錄／Validation](ChestAchievements-Validation.txt)。

The delivered CT's checkbox execution, default backup, completion dialog and repeat execution were verified. A full restart, other accounts/systems/builds and actually opening a chest afterward were not tested. See the bilingual notes and validation linked above.

## 隱藏道具成就與還原｜Hidden-item achievement with restoration

**實測：隱藏道具 9 → 暫時 50 → 還原 9；寶箱維持 38。Steam API 的 `get_hidden_item` 從未解鎖變為已解鎖，其餘 36 項成就狀態不變。使用者已在 Steam 成就頁確認解鎖。**

**Tested: hidden items 9 → temporarily 50 → restored 9; chests remained at 38. Steam API `get_hidden_item` changed from locked to unlocked; all other 36 achievement states were unchanged. The user confirmed the unlock on Steam's achievement page.**

獨立 CT 的標題註明「暫補 50 旗標→檢查成就→還原道具狀態｜不領取道具」。本版 53 筆隱藏道具資料對應 50 個不重複旗標，與寶箱無重疊。暫時補齊後呼叫遊戲原本的 `UpdateHiddenItems`，隨即還原完整 512 bytes 寶物旗標並驗證完整地圖資料一致，再上傳 Steam。遊戲內進度保留原值，不補發道具、不永久標記取得，也不直接呼叫 Steam 解鎖方法。

The standalone CT title explains its effect: temporarily complete 50 flags, check achievements, restore item states, no loot. This build's 53 hidden-item rows map to 50 distinct flags with no chest overlap. It calls the game's `UpdateHiddenItems` during temporary completion, immediately restores the entire 512-byte treasure flag array, verifies an exact full map-data match, then uploads Steam stats. In-game progress returns to its original value. No loot, permanent collected state or direct Steam unlock call is used.

保持一般地圖靜止，執行期間不要移動、切圖、存檔或關閉工具。一般方法錯誤也會執行還原；突然終止程序仍可能阻止清理。先完整備份存檔；CT 另在 Cheat Engine 安裝目錄建立明文地圖快照，不能直接取代加密存檔。無須另存角色存檔。

Stay idle on a normal field map; do not move, change maps, save or close the tool during execution. Ordinary method errors run cleanup; abrupt termination can prevent it. Back up the full save folder. A plaintext map snapshot is also created in the Cheat Engine installation directory and cannot directly replace encrypted saves. No character-slot save is needed.

正式表的標題、預設未啟用、實際勾選、預設備份、雙語完成提示與重複執行已確認。未測完整重啟、其他帳號／系統／版本或還原後實際拾取。[中英雙語說明／Bilingual notes](HiddenItemAchievements-README.txt) · [實測紀錄／Validation](HiddenItemAchievements-Validation.txt)。

The delivered title, inactive default, checkbox execution, default backup, bilingual result dialog and repeat execution were checked. A full restart, other accounts/systems/builds and collecting an item afterward were not tested. See the bilingual notes and validation linked above.

## 擊破、Gil、機械與全地點｜Kills, Gil, tools and locations

**擊破與 Gil 成就表直接指定 Steam 成就，保留遊戲統計。Steam 的共用進度可能提高並連帶解鎖低階成就，標題已註明。** 擊破實測：遊戲總數維持 245，358 筆怪物次數不變；Steam 進度 246→2000，1000 與 2000 隻成就解鎖，使用者接受連動並確認。Gil 實測：持有 908303、累計 37626 不變；Steam 進度 37626→500000，10 萬與 50 萬成就解鎖並經使用者在 Steam 確認。

**The kill and Gil achievement tables directly target Steam achievements while retaining game statistics. Linked Steam progress can rise and unlock lower tiers, as stated in the titles.** Kill test: game total stayed 245 with all 358 monster records unchanged; Steam progress 246→2000 unlocked the 1000/2000 tiers, accepted and confirmed by the user. Gil test: held 908303 and saved lifetime 37626 were unchanged; Steam progress 37626→500000 unlocked 100k/500k, confirmed by the user on Steam.

原本 `Gil1000000` 只修改目前持有金錢，不代表累計獲得金錢成就會解鎖；它與新的 `Gil500kAchievement` 分開使用，原表維持原用途。

The original `Gil1000000` edits currently held money; this does not establish completion of lifetime-Gil achievements. It remains separate from `Gil500kAchievement` and retains its original purpose.

**機械表會實際補道具。** 只將缺少的 8 種機械補至各 1 個，更多保留，再呼叫遊戲原本的 `UpdateMachineAll`。實測 4→8 種、`machinery_master` 解鎖，背包其餘數量、金錢與擊破數不變，使用者已確認。請另存新欄位保留道具；戰鬥使用與存檔重讀未測試。

**The tools table grants actual items.** It adds one only for each missing tool, retains higher quantities and calls the game's normal `UpdateMachineAll`. The test changed 4→8 types and unlocked `machinery_master`, with other inventory quantities, Gil and kills unchanged; the user confirmed both. Save to a new slot to retain the tools. Combat use and save/reload were not tested.

全地點表只解鎖 `area_visit`，不傳送角色、不補造訪或劇情旗標，也不把未到過的地方改成已造訪。API 實測 0→1；完整地圖快照、背包、遊戲統計及其他 36 項成就不變。使用者已在 Steam 成就頁確認解鎖。

The locations table unlocks only `area_visit`; it does not teleport, edit visit/story flags or mark unvisited places as visited. The API test changed 0→1; the complete map snapshot, inventory, game statistics and other 36 achievements were unchanged. The user confirmed the unlock on Steam's achievement page.

這四份表各自獨立、預設未啟用，會先在 Cheat Engine 安裝目錄建立狀態快照。快照不是加密存檔替代品，也不能撤銷成就；完整存檔備份僅留本機。擊破、Gil、全地點表無須另存角色存檔來保存 Steam 成就。完整重啟、其他帳號／系統／版本未測試。

All four tables are independent and initially inactive, creating a local state snapshot in the Cheat Engine installation directory before changes. Snapshots cannot replace encrypted saves or revoke achievements; full save backups remain local. The kill, Gil and locations tables do not need a character-slot save for Steam achievements. Full restarts and other accounts/systems/builds were not tested.

[擊破說明／Kill notes](Kill2000Achievement-README.txt) · [Gil 說明／Gil notes](Gil500kAchievement-README.txt) · [機械說明／Tools notes](MachineryAchievement-README.txt) · [8 種機械清單／Tool mapping](MachineryAchievement-list.txt) · [全地點說明／Locations notes](WorldVisitAchievement-README.txt)

## 致命鬼牌與莫古全舞蹈｜Joker’s Death and Mog’s dances

致命鬼牌表只透過遊戲的 Steam 成就介面解鎖 `gambler_master`，不實際轉動老虎機或執行戰鬥。實測成就 0→1；持有 Gil 682904、累計 Gil 44127、主存檔與圖鑑擊破數 281、各怪物次數、角色／技能、背包、地圖資料與其餘 36 項成就均不變。使用者已在 Steam 成就頁確認解鎖。

The Joker table unlocks only `gambler_master` through the game's Steam achievement interface, without executing Slots or battles. The achievement changed 0→1; held Gil 682904, lifetime Gil 44127, main-save/bestiary kills 281, individual monster counts, characters/abilities, inventory, map data and the other 36 achievements were unchanged. The user confirmed the unlock on Steam.

全舞蹈表透過遊戲的 `OwnedCharacterClient.LearningAbility`，只補齊正式莫古尚未精通的舞蹈。這次辨識到的莫古記錄 ID 為 16（正式角色身分為 11），不是固定修改第 11 筆。原有黑暗鎮魂曲保持 100，其餘 7 種由 0→100；使用者確認全部 8 種都有顯示且能選用。持有 Gil 687904、累計 Gil 49127、擊破數 281、其他角色／技能、等級與能力值、背包、地圖與全部 37 項成就核對不變。舞蹈需要另存新欄位保留。

The dances table uses the game's `OwnedCharacterClient.LearningAbility` to complete unmastered dances for permanent Mog. This save's Mog record ID was 16 (role identity 11); record 11 is not hardcoded. Twilight Requiem stayed at 100 and the other seven dances changed 0→100. The user confirmed all eight are displayed and selectable. Held Gil 687904, lifetime Gil 49127, kills 281, other characters/abilities, levels/stats, inventory, map data and all 37 achievements were unchanged. Save to a new slot to retain the dances.

兩份 CT 獨立且預設未啟用；開檔不執行，套用前在 Cheat Engine 安裝目錄寫入狀態快照，無法寫入就停止。快照不等於可讀取的完整存檔，也不是自動還原功能。相同核心 Lua 已經由本機測試包實測；正式 CT 勾選介面與預設備份位置未另行實測。未測其他帳號／版本、完整重啟、戰鬥效果與存檔重讀。

Both tables are independent and initially inactive. Opening does not run them. Before applying, they create a state snapshot in the Cheat Engine installation directory and stop if writing fails. Snapshots are not loadable full saves or automatic undo facilities. The same core Lua was tested via local wrappers; the formal checkbox interface and default backup location were not separately exercised. Other accounts/builds, full restart, combat behavior and save/reload were not tested.

[致命鬼牌說明／Joker notes](JokerAchievement-README.txt) · [致命鬼牌實測／Joker validation](JokerAchievement-Validation.txt) · [全舞蹈說明／Dance notes](AllDances-README.txt) · [8 種舞蹈清單／Dance mapping](AllDances-list.txt) · [全舞蹈實測／Dance validation](AllDances-Validation.txt)

## 實作與更新｜Implementation and updates

使用 IL2CPP／Mono metadata 定位欄位與方法，依實際類別再往父類別查找同名方法。物件以欄位及類別指標核對，避免先前造成逾時的動態物件類別查詢。裝備、升級與技能取得透過遊戲方法處理；金錢與能力加值寫入已驗證欄位。曾遇過 Mono 逾時；調整後的實測通過，但不保證其他環境不會逾時。

Uses IL2CPP/Mono metadata to locate fields and methods, searching the actual class before its parents. Objects are checked using fields and class pointers, avoiding the dynamic class query that previously caused timeouts. Equipment, leveling and skill acquisition use game methods; Gil and stat bonuses use validated fields. Earlier Mono timeouts were addressed in the tested setup, but other environments may still time out.

請重新下載修正版 CT；既有下載檔不會自動更新。

Re-download updated CT files; existing downloads do not update automatically.

## 清單與補充說明｜Lists and supplementary notes

- [裝備清單／Equipment list](equipment-list.txt)
- [狂怒清單／Rage list](AllRages-list.txt) · [青魔法清單／Lore list](AllLores-list.txt)
- [魔石清單／Magicite list](AllMagicite-list.txt)
- [補給說明／Supply notes](Supplies-README.txt)
- [能力提升說明／Stat boost notes](StatsBoost-README.txt)
- [蒂娜魔法說明／Terra spell notes](TerraUltimaQuick-README.txt)
- [全魔石說明／All-magicite notes](AllMagicite-README.txt)
- [角色清單相容性驗證／Character-record compatibility validation](Validation-20261015.txt)
