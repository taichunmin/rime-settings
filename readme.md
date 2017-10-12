# 如何安裝

## 安裝 Rime

<http://rime.im>

## 抓取繁體中文

<https://github.com/rime/rime-bopomofo>

* 下載整份專案後，放到 Rime 設定資料夾中
  - macOS: `~/Library/Rime`

* macOS

```sh
cd ~/Library
git clone https://github.com/rime/rime-bopomofo.git
mv -v ~/Library/rime-bopomofo/*.yaml ~/Library/Rime/
rm -rf ~/Library/rime-bopomofo
```

## 抓取本專案

<https://github.com/taichunmin/rime-settings>

* 下載整份專案後，放到 Rime 設定資料夾中
  - macOS: `~/Library/Rime`

* macOS

```sh
cd ~/Library
git clone https://github.com/taichunmin/rime-settings.git
mv -v ~/Library/rime-settings/* ~/Library/Rime/
rm -rf ~/Library/rime-settings
```

## 參考來源

1. <https://github.com/yjlintw/rime_zhtw_setting>
2. <https://github.com/arsenali/rime>

## 備註

* 移除重複詞指令 `comm -1 -3 <(sort terra_pinyin.dict.yaml) <(sort terra_pinyin.my.dict.yaml) > test.yaml`
* 萌典產生詞典指令 `sed -nE '/^ {6}/p' ~/Downloads/dict-cat.json | sed -E 's/\s*"([^"]+)",?/\1/g' > moe.dict.yaml`
  ```yml
  ---
  name: moe
  version: "2017.10.12"
  sort: by_weight
  use_preset_vocabulary: true
  ...
  ```
