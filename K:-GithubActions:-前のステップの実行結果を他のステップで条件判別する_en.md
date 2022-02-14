https://translate.google.com/translate?hl=ja&sl=ja&tl=en&u=https://github.com/shimajima-eiji/__Backup_Images/blob/main/.github/workflows/convert_webp.yml#L18-L33

```
# webp変換した場合(結果が0以外)のみ処理する
- name: Commit files
run: |
if [ $(tail -n 1 file2webp.log) -ne 0 ]
then
rm file2webp.log  # 先にログファイルを消さないと、ログファイルもpushしてしまう
git config --global user.email "${{ secrets.EMAIL }}"
git config --global user.name "${{ secrets.USER ​}}"
​git add -A
​git commit -m "[Update]converted webp by Github Actions"
​git pull
​git push
​echo "[COMPLETE] convert to webp."
​else
​echo "[SKIP] No convert."
​fi
```
