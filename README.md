# 自由大新倉頡RIME輸入方案

## 字典修改

- 移除
  - 網址
  - email
  - 電話
  - 表符
  - 常用語

## 安裝方法

將以下檔案拷貝到`%AppData%\Rime`目錄下，執行重新部署，即可在選單內找到該輸入法

### 自由大新

- newcj.schema.yaml
- newcj.dict.yaml

### 個人化修改

自由大新<=>注音互相反查(以 ` 啟用反查)\
啟用詞句輸入(以'斷字)\
部分標點改為半形輸出

- bopomofo.custom.yaml
- newcj.custom.yaml

## newcj.txt

將以上碼表轉換為 [MicrosoftCangjieTool](https://github.com/Arthurmcarthur/MicrosoftCangjieTool) 可讀格式

由於 Microsoft Cangjie 只支援 a-z[^1]

- 將候選字用的 `;` 轉換為 `x`(難)
- 將字碼內含有 a-z 之外的條目刪除
  - 捨棄原本用於 `食` 字旁和 `禾` 字旁的 `;`
  - 其它所有標點 `,` `.` `[` `]` `'` `/`

由於 Microsoft Cangjie 不支援詞組，將非一單字元的條目刪除

[^1]: <https://github.com/Arthurmcarthur/MicrosoftCangjieTool/blob/fb4efdc0ac5e01a03c09ba285f780fc2188e565f/src/MSCJTable.cpp#L183>

## ChtCangjieExt.lex

將 `newcj.txt` 以 MicrosoftCangjieTool 轉換出的 lex 檔案

How to use it: <https://www.chinesecj.com/forum/forum.php?mod=viewthread&tid=194346&extra=&page=1>

> 若這個版本為2004，請進入 C:\Windows\System32\zh-hk 文件夾，刪除 ChtCangjie.sdc、ChtCangjie.spd 和 ChtCangjieExt.lex 文件，順便也要做好備份工作。然後將 ChtCangjieExt.lex 複製到文件夾中（請注意不要弄錯文件名）。

## 參考網址

RIME | 中州韻輸入法引擎 <https://rime.im/> \
大新倉頡共同編輯計畫 <https://hyperrate.com/thread.php?tid=343>
