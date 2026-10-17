FF6 Pixel Remaster — 全員一般魔法／All normal magic
Steam Windows build 20265119
File: FF6_PR_AllMagic_20265119.CT

效果／Effect
依正式角色身分與職業辨識蒂娜、洛克、凱嚴、暗影、埃德加、馬修、塞麗絲、斯特拉格斯、瑞姆、塞策、莫古、嘎嗚。包含已加入的後備成員；未加入的角色跳過，不建立角色。每人補齊 54 種一般魔法（能力 ID 31–84），透過遊戲 LearningAbility 學會，不直接改學習百分比。已學滿的魔法保留。
Identifies Terra, Locke, Cyan, Shadow, Edgar, Sabin, Celes, Strago, Relm, Setzer, Mog and Gau by permanent role/job identity, including recruited reserves. Skips unjoined roles without creating characters. Learns all 54 normal spells (ability IDs 31–84) through the game's LearningAbility method rather than directly writing proficiency values. Retains mastered spells.

特殊角色／Special roles
格格（Gogo）與烏瑪羅（Umaro）不寫入一般魔法學習記錄，也不更換戰鬥指令。Gogo 可設定魔法指令並使用同隊成員已學會的魔法；Umaro 保留原本自動戰鬥機制。青魔法、狂怒、舞蹈、幻獸裝備與召喚不屬於這 54 種一般魔法。
Does not write normal-magic learning records for Gogo or Umaro or change their battle commands. Gogo can equip the Magic command and use spells known by current party members; Umaro retains his normal automatic combat. Lores, Rages, Dances, equipped magicite and summons are separate from these 54 spells.

操作／Use
連接 FINAL FANTASY VI.exe、讀取存檔並停在一般地圖，關閉對話與選單，暫停操作。載入 CT 不會執行，勾選唯一項目一次才會套用。完成後重開魔法清單確認，另存新欄位保留。取消勾選不會還原；相同角色重複執行不會超額累加。
Attach to FINAL FANTASY VI.exe, load a save and remain idle on a field map with dialogue and menus closed. Opening does not execute the table; enable its single entry once to apply. Reopen Magic to confirm and save to a new slot. Disabling does not undo learning; repeated runs skip mastered spells.
不在戰鬥、劇情或角色清單變動期間套用。此表檢查版本與資料結構，但不會自動阻止所有不合適的遊戲時機。
Do not apply during battle, events or roster changes. The table validates build and data structures but does not automatically detect every unsuitable game state.

備份與核對／Backup and verification
執行前在 Cheat Engine 安裝目錄寫入 FF6_AllMagic_before_*.json 狀態快照；無法寫入就停止。FF6_ALL_MAGIC_BACKUP_DIR 可指定已存在且可寫入的資料夾。快照不是可直接載入的遊戲存檔；請先自行備份存檔。沒有自動回復；錯誤時保留備份並停止，請先檢查狀態。
Writes a FF6_AllMagic_before_*.json state snapshot in the Cheat Engine installation directory before mutation; failure stops execution. FF6_ALL_MAGIC_BACKUP_DIR may specify an existing writable folder. The snapshot is not a loadable game save; back up saves separately. There is no automatic rollback; errors retain backups and stop execution for inspection.
核對全部目標角色各 54 種魔法均已學滿，保留其他技能、指令、等級、經驗、HP/MP、能力值、裝備魔石、一般背包與重要道具、持有與累計 Gil、擊破數、圖鑑與事件資料、成就。
Verifies all 54 spells mastered for each target while preserving unrelated skills, commands, levels, EXP, HP/MP, stats, equipped magicite, normal/key inventory, held/lifetime Gil, kill counters, bestiary/event data and achievements.

驗證／Validation
2026-10-17 唯讀檢查：12 名角色均找到，54 種魔法的能力與內容映射核對完成；實際套用補齊 583 項學習紀錄；12 人各 54 種皆已學滿，其他資料核對不變，RESULT true nil。使用者確認魔法已齊全、可選用，遊戲正常。
2026-10-17 read-only preflight: found all 12 eligible roles and checked mappings for 54 spells; Live application learned 583 entries; all 12 roles verified at 54 mastered spells each, unrelated state unchanged, RESULT true nil. The user confirmed complete, selectable spell lists and normal gameplay.

版本與實測環境／Build and tested environment
僅限 Steam build 20265119，Cheat Engine Windows x64 7.7，CrossOver 26.3。其他版本、存檔重讀、完整重啟與正式勾選包裝尚未實測。
Steam build 20265119 only, Cheat Engine Windows x64 7.7 under CrossOver 26.3. Other builds, save reloads, full restarts and the published checkbox wrapper have not been tested.
