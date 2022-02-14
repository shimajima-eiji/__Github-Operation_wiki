https://translate.google.com/translate?hl=ja&sl=ja&tl=en&u=https://github.com/shimajima-eiji/__Githut-Action_demo/blob/main/.github/workflows/add_dummy.yml



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





