## リッチメニューをMessagingAPIに組み込む
- [公式](https://developers.line.biz/ja/docs/messaging-api/using-rich-menus/#creating-a-rich-menu-using-the-messaging-api)
- [自作ツール](https://qiita.com/e_chan1007/items/cd34ce0871943ee34396)
  - [応用: ゲームブック](https://qiita.com/poruruba/items/28c1c4ba95c4eaf2b739)
どれも大変素晴らしい情報である事は間違いないが、残念ながら教育コスト面を考えるとMessagingAPIでリッチメニューを作るのがとても面倒臭いので、なるべく公式の既存機能を使って頑張って実装する。

### 留意事項
MessagingAPIを活用する方法は、従来のリッチメニュー設定でできなくなる機能がある。  
ここでは店舗ではなく個人で運用する想定であるのと、コミュニケーションが目的なので困る事はない。

## 技術要件
|ツール|操作手順|用途|
|---|---|---|
|[GAS](https://script.google.com/home)|プロジェクト|本来MessagingAPIでやることを全部担う|
|[LINEBotのリッチメニュー設定](https://manager.line.biz)|トークルーム→リッチメニュー|LINEの画面側の設定。|
|[LINEBotのMessagingAPI設定](https://developers.line.biz/console)|Messeging API→Webhook　Settings|GASのWebhookURLを設定|

## やること
