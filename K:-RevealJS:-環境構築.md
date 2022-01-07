# RevealJS_demo
- [デモページ](https://shimajima-eiji.github.io/RevealJS_demo/sample.html)
- [ソースコード](https://github.com/shimajima-eiji/RevealJS_demo)

## 閲覧できない環境について
同じchromium系のブラウザでも見れたり見れなかったりしたので、閲覧環境に指定がある可能性が高い。
おそらく拡張機能？か何かの都合でうまく表示できなくなっている事があると考えられる。

## 作り方
1. [VSCode](https://code.visualstudio.com/)に[vscode-reveal](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)を入れる
2. 所定のフォーマット（後述）でマークダウンを作成する
3. 「Shift+Ctrl(Command)+P」キー：「Export in HTML」でファイルを作成する
4. 「export」ディレクトリが作成され、以下に`index.html`と`lib`ディレクトリが作成されている

### 所定のフォーマット
最もシンプルな例は[sample.md](https://github.com/shimajima-eiji/RevealJS_demo/blob/main/sample.md)を参照。

- [公式](https://github.com/hakimel/reveal.js/)
- [参考](https://zatsugaku-engineer.com/html-css-javascript/reveal-js)

## 注意
revealJSはいろいろな方法で使われるが、環境によっては動いたり動かなかったりする。
たとえば、当方の環境ではreveal-ckはうまく使えなかったため、作り方の方法で作成している。

## ファイル解説
ホスティングをする場合に着目して解説。

- `index.html`で`http://localhost:52248/`を参照している場所があるが、これはアップロード時に変更する必要はない
- `lib`ディレクトリはルートに置いておくと、ファイル追加時は`index.html`（と、必要に応じmdファイル）だけを置けば良い事になる。
- 想定では階層を分けて`index.html`を置く運用を想定しているが、階層化しなくてもファイルをリネームして配置してもきちんと参照できる。

よく考えれば、ただのHTMLファイルでしかないので、通常のHTMLのルールに則っている。

## RevealJSページの埋め込みについて
内容が内容なので、Webサイトに組み込みたいシーンは多い。
よく使われるのが

- iframe
- object

のどちらかのタグだろう。
どちらでも問題ないことを確認しているので、好みでつけて良い。

## Github Pagesのテーマと共存できるか
できる。

- [トップページ](https://shimajima-eiji.github.io/RevealJS_demo): config.ymlが適用されている
- [デモページ](https://shimajima-eiji.github.io/RevealJS_demo/sample.html): RevealJSが適用されている

導入時はBranch protection rulesを設定している場合は組み込みに苦戦するので、一時的に無効化した方が楽。
