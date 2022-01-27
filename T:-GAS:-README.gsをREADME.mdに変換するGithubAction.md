基本的に[GASテンプレートリポジトリ](https://github.com/shimajima-eiji/--GAS_v5_Template)から持ってくる想定

```
name: README.gsをREADME.mdに変換
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2  # git clone (this)
      - name: run
        run: |
          cat README.gs | sed '1d' | sed '$d' >README.md
          git config --global user.email "${{ secrets.EMAIL }}"
          git config --global user.name "shimajima-eiji"
          git add -A
          git commit -m "Create README.md from README.gs by Github Actions"
          git pull
          git push
```