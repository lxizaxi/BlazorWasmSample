# 目的
- Blazorのお勉強

# 使い方メモ
## wasmのprojectの作成
```
$ dotnet new blazorwasm -o (プロジェクト名)
```
## app起動方法
作成したプロジェクト直下で、以下のコマンド
```
$ dotnet run
```
## ホットリロードの設定の仕方
1. `Properties > launchSettings.json`の該当箇所に以下のように`hotReloadProfile`の設定を追記
```
"profiles": {
    "(プロジェクト名)": {
      ：
      ：
      "hotReloadProfile": "blazorwasm"
    },
```
2. appを以下のコマンドで起動
```
$ dotnet watch --project .
```
3. `https`ではなく`http`の方にアクセスする（httpsの方は証明書関係で上手くいっていないっぽい）

# 参考
- [使い方その1](https://aimek-developer.blogspot.com/2020/11/blazor-webassemblyvscode.html)
- [使い方その2](https://blogs.jp.infragistics.com/entry/blazor-getting-started-vscode)
- [REST api 作りたい時](https://dotnet.microsoft.com/ja-jp/apps/aspnet/apis)