全狂怒／全青魔法 — All Rages / All Lores
FF6 Pixel Remaster · Steam build 20265119

兩份獨立 CT，各自只有一個啟用項目，開啟檔案不自動套用。
Two separate CTs, each with one initially inactive entry; opening does not apply changes.

全狂怒 AllRages：嘎嗚的 252 種正常可學習狂怒。253 筆怪物對照去重為 252 種，排除對照外隱藏技能。
AllRages: 252 normally learnable Rages for Gau, deduplicated from 253 monster mappings. Unmapped hidden skills are excluded.

全青魔法 AllLores：斯特拉哥的 24 招玩家青魔法，不包含敵人專用變體。已實測 3→24，並由使用者確認可選用。
AllLores: Strago's 24 player Lores, excluding enemy-only variants. Applied from 3 to 24 and user-confirmed selectable.

使用 Use
備份存檔，等正式角色加入後讀取遊戲，停在一般地圖並暫停操作。Cheat Engine 連接 FINAL FANTASY VI.exe，開啟需要的 CT，勾選一次。重新開啟技能選單確認，再另存新欄位。
Back up the save. After the permanent character joins, load the game and stop moving on a normal field map. Attach Cheat Engine to FINAL FANTASY VI.exe, open the desired CT and enable it once. Reopen the skill menu to verify, then save to a different slot.

依角色身分與職業辨識嘎嗚／斯特拉哥，不以內部編號判斷；不會修改開場莫古利替身。找不到正確角色時以 ROLE_NOT_READY 停止。
Identifies Gau/Strago by status and job, not internal record ID, avoiding opening-sequence Moogle placeholders. Stops with ROLE_NOT_READY if the correct role is absent.

跳過已精通的技能。已有記錄但進度低於 100% 仍會補學，並核對全部目標達到 100%。
Skips mastered skills. Existing records below 100% are still completed, and every target is checked for 100% mastery.

需要 Mono collector，透過 OwnedCharacterClient.LearningAbility 學習。取消勾選不會還原。途中失敗不會撤回已學會的技能；完整還原請讀取原存檔。
Requires Mono collector and uses OwnedCharacterClient.LearningAbility. Disabling does not undo learning. A partial failure does not roll back completed skills; reload the original save to undo them.

實測 Validation — 2026-10-15
狂怒：嘎嗚身分／職業 12，內部記錄 ID 24。原本 9 種已精通，243 種已有記錄但進度為 0%；已補學 243 種，全部 252 種內容與進度 100% 逐項核對通過。
Rages: Gau status/job 12, internal record ID 24. Initially 9 mastered and 243 existing records at 0%; completed all 243, then individually verified content IDs and 100% progress for all 252.

角色身分、職業、等級、經驗值、四項能力、HP/MP、金錢、其他技能與指令均核對保持不變。使用者已確認狂怒清單新增且可選用；戰鬥效果與存檔重讀尚未測試。
Character identities/jobs, levels, EXP, four stats, HP/MP, Gil, unrelated skills and commands were verified unchanged. The user confirmed that the expanded Rage menu is selectable; combat effects and save/reload are untested.

青魔法 — 2026-10-16：斯特拉哥正式加入後，已補學 21 招，原有 3 招保留，全部 24 招進度 100%。使用者確認 24 招可選用；其他角色、技能、等級、能力值、背包與遊戲統計核對不變。戰鬥與存檔重讀未測。獨立全青魔法說明及實測紀錄詳見 AllLores-README.txt、AllLores-Validation.txt。
Lores — 2026-10-16: After permanent Strago joined, 21 Lores were learned and the original three retained, leaving all 24 at 100%. The user confirmed all 24 selectable; other characters, abilities, levels, stats, inventory and game statistics were unchanged. Combat and save/reload remain untested. See AllLores-README.txt and AllLores-Validation.txt for details.
