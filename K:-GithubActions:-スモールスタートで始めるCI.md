https://github.com/shimajima-eiji/__Githut-Action_demo/blob/main/.github/workflows/add_dummy.yml  
を例に考える

## .github/workflows/.ymlのコード
```
name: small git push
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2  # git clone (this)
      - name: Update and Commit
        run: |
          TZ=JST-9 date '+%Y/%m/%d %H:%M:%S (%Z)' >dummy
          git config --global user.email "${{ secrets.EMAIL }}"
          git config --global user.name "${{ secrets.USER }}"
          git add -A
          git commit -m "Update dummy by Github Actions"
          git pull
          git push
```

で見ると分かりやすい。
不要なものはなるべく取り除いているが、git cloneはコマンド実行できない点とタイムゾーンがUTCである事に注意する。

### 応用
https://github.com/shimajima-eiji/__Backup_Images/blob/main/.github/workflows/convert_webp.yml