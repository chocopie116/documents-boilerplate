# ER図

ER図を描画できるTool(https://github.com/BurntSushi/erd)をいい感じにできるようにした


## how to

#### ER図のテキストを編集
src/*.erファイルを編集する
```
$ cat src/example/001_example.er
```

#### テキスト情報をerdコマンドを使って画像に変換

```
$ make generate
```

## artifacts
変換の結果以下のような画像ファイルが生成されます
```
$ls img/example
001_example.png 002_example.png all_erd.png
```


![](img/example/all_red.png)


