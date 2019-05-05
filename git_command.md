# 全体
- コピー
    - clip < ファイルパス

- ファイル起動
    - code ファイルパス
        - ローカルリポジトリのディレクトリ配下であれば "code ." で OK

- エクスプローラー起動
    - start フォルダパス
        - ファイルまで指定すればファイルをダブルクリックした時と同じ状態となる

# SSH
- SSH Key 生成
    - ssh-keygen -t rsa -b 4096 -C "takenoriohyama@gmail.com"
        - -t : 生成する鍵の種類
        - -b : 生成する鍵のビット数
        - -C : コメント


- 鍵設定の確認
    - ssh -T git@github.com
        - -T : 不明

# Remote Repository
## 開始
- クローン
    - git clone git@github.com:take0118/ichiyasaGitSample.git
        - リモートリポジトリのURLは "Use SSH" で表示したものを使用

- リモートリポジトリの設定確認
    - git remote -v
        - v : 詳細情報

- ブランチ作成
    - git branch ブランチ名

- リモートリポジトリのコードをワークツリーに反映
    - git pull origin master

## 確認
- 使用中のブランチを確認
    - git branch

- 編集中ファイル状態を確認
    - git status

- 差分確認
    - git diff
        - 使用中のブランチにコミットしたコードと編集中のコードの差分を表示
    - git diff master
        - 使用中のブランチにコミットしたとmasterコードの差分を表示

## 実行
- 使用ブランチを切り替える
    - git checkout ブランチ名
        - -b : git branch XXX と git checkout XXX をまとめて実施

- 変更をコミット
    - git add ファイル名
        - ステージにあげる
        - -A : 変更したファイルをまとめて追加
    - git commit -m "コメント"
        - ローカルリポジトリにコミット
        - -m : メッセージ
        - -am : ステージングに追加とコミットをあわせて実施)(git add が不要)

## 終了
- 不要ブランチの削除
    - git branch -d ブランチ名
        - マージ済みのブランチを削除する
    - git branch -D ブランチ名
        - マージ済みの状況に関わらずブランチを削除
