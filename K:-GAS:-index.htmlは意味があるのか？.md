## 結論
その気になれば、GASでホスティングしたURL自体を使ってサイトとして扱うことはできなくはない。  
が、かなり手間がかかって面倒臭い。  
https://qiita.com/taromorimotohf/items/82a02bdeb21b1d74c5e8

似たようなサービスに[Firebase](https://firebase.google.com)があるので、こちらを使った方が利口か。  
また、GHPを使う方法もある。

## vueぐらいなら動く
これはGASでもFirebaseでもGHPでも言えることだが、vueはCDNがあり、これを使えば欲しいデータを引っ張ってくる事ができる。  
Axiosを使う場合は接続情報を書く必要があるため、途端にGHPでの障壁は高くなる。

## GHPやGASのページでスコア100は出せるのか？
https://qiita.com/reireias/items/9233e1f1b989db4f6b40