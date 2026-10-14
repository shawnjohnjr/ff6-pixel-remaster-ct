# FF6 Pixel Remaster Cheat Engine Tables

Steam build **20265119**. Tested on 2026-10-14 through CrossOver.

| Table | Function |
|---|---|
| [Gil1000000](FF6_PR_Gil1000000_20265119.CT) | Set Gil to 1,000,000 |
| [TopEquipment](FF6_PR_TopEquipment_20265119.CT) | Grant 62 equipment types; weapons to 8, armor/accessories to 4 |
| [Level99](FF6_PR_Level99_20265119.CT) | Current permanent party members to Lv99, including normal growth |

FF6 Pixel Remaster — Cheat Engine CT
Steam build 20265119

檔案
Gil1000000：將金錢設為 1,000,000 Gil。若原本金錢更多，也會降至此值。
TopEquipment：62 種頂級與實用裝備，武器總持有量補至 8、防具飾品補至 4；原有數量更多則保留。裝備放入背包，請自行穿戴。
Level99：目前隊伍的永久角色升到 Lv99，同步經驗值與遊戲正常升級成長。未加入目前隊伍的角色不變，臨時客串角色不支援。

使用
1. 先備份存檔，讀取存檔並停在一般地圖上，暫停操作。
2. Cheat Engine 連接 FINAL FANTASY VI.exe。
3. 開啟需要的 CT，勾選一次，等待完成提示。
4. 重新開啟選單核對，確認後另存新欄位。

檔案預設未勾選，不會在開啟時自動修改。三項可分別使用。取消勾選不會還原修改；要還原請讀取修改前存檔。版本不符或資料檢查失敗會停止。若失敗發生於修改過程，先前已成功修改的部分不會自動撤銷。

實測紀錄
2026-10-14：在使用者已開啟的 FF6 中測試，三項程式資料核對通過。
金錢：5,223 → 1,000,000。
裝備：62 種數量逐項核對通過。
艾德加：Lv7 → Lv99，最大 HP 9,796，最大 MP 996。
蒂娜：Lv5 → Lv99，最大 HP 9,788，最大 MP 999。
使用者確認：金錢、兩名角色 Lv99 與裝備背包皆正確顯示，遊戲操作正常。
僅測試當時的兩名隊伍角色；未測試所有角色、魔石加成組合或每件裝備的戰鬥效果。

技術說明
採用欄位讀取驗證物件，移除原本動態物件類別查詢；函式依實際類別到父類別順序查找，避免誤選父類別同名方法。金錢直接寫入已驗證欄位；裝備與升級使用遊戲原有處理流程。因此裝備與升級仍需要 Cheat Engine Mono collector，不宣稱完全不依賴 Mono。
初版檢查曾出現 Mono 逾時；調整後的唯讀預檢和三項實際套用均完成，沒有逾時。不能據此保證所有執行環境都不會逾時。


## Equipment list

See [equipment-list.txt](equipment-list.txt).
