# VB Console Test (4 build)

VB (.NET Framework) をコマンドラインからビルドしたりデバッグしてみるテストのやつです

## REFERENCED:

- [VSCodeで.NET Frameworkコンソールアプリをビルド＆デバッグする - Qiita](https://qiita.com/hibara/items/fa66c3241293b7d43eae)

## HOW to USE (つかいかた)

### BEFORE

#### 1. add `MSBuild.exe` dir PATH to `$Env:Path`

1. `スタートメニューボタン` を右クリック > `システム` を押す
2. `システムの詳細設定ボタン` を押す
3. `環境変数ボタン` を押す
4. `ユーザー環境変数` のリストから `PATH` または `Path` を選択し、 `編集` ボタンを押す
    - 存在する場合は`環境変数名の編集 ウィンドウ` が開く
    - > `PATH` などが存在しない場合は別途、 `新規ボタン` を押し、名前に `Path` を入力し、以降の手順に続く
5. `MSBuild.exe` が存在するディレクトリのパスを追加する
    - Windows10の2025年05月10日現在更新がサポートされているバージョンであれば、 `編集ボタン` から開かれたウィンドウの `新規ボタン` を押して追加する
    - > 新しく `PATH` 変数を追加した場合は、値に `MSBuild.exe` のディレクトリのパスを入力して `OKボタン` を押す
6. `OKボタン` を押して `環境変数の編集ウィンドウ` を閉じる
7. `Microsoft Powershell` を開き、以下のコマンドでエラーが出ず、何らかの値が出力されればOK
    ```powershell
    echo $Env:PATH
    ```

#### 2. install plugin on `vscode`

https://marketplace.visualstudio.com/items/?itemName=HarryHopkinson.vs-code-runner

### BODY

#### 1. exec build to `.vbproj`

1. `MSBuild` を実行する
    ```powershell
    MSBuild ./ConsoleApp1/ConsoleApp1.vbproj
    ```
