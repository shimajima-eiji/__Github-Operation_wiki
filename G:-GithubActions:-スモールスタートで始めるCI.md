https://github.com/shimajima-eiji/__Githut-Action_demo/blob/main/.github/workflows/add_dummy.yml

```
name: small git push
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2  # git clone (this)
      - name: git setting
        run: |
          git config --global user.email "${{ secrets.EMAIL }}"
          git config --global user.name "${{ secrets.USER }}"
      - name: Commit files
        run: |
          TZ=JST-9 date '+%Y/%m/%d %H:%M:%S (%Z)' >dummy
          git add .
          git commit -m "Update dummy by Github Actions" -a
          git pull
          git push
```

で見ると分かりやすい。
不要なものはなるべく取り除いているが、git cloneはコマンド実行できない点とタイムゾーンがUTCである事に注意する。