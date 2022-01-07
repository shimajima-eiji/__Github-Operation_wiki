## ソースコード
https://github.com/shimajima-eiji/GAS_v5_GetPost-Debug

## 解説
APIを作るには、https://github.com/shimajima-eiji/GAS_v5_GetPost-Debug/blob/main/output.gs#L1-L8 にもあるが、ContentService.createTextOutput()を返す必要がある。  
`setContent()`に表示させたい内容(この場合はJSON-String）を渡せば良い

ロギングはスプレッドシートに追記するだけのスクリプトにしている。  
`SpreadsheetApp.openById(SSID).getSheetByName(SSNAME).appendRow()`に配列データを渡せば自動的に最下行にデータを追記していく。
