# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
* リポジトリとはファイルやディレクトリの状態を記録する場所を指す。
* リモートリポジトリとはソースコードの置き場をネット上に配置するもの。
* ローカルリポジトリとはその置き場をPC上に配置するもの。


## プッシュとマージの違いは何でしょうか？
* プッシュとはリモートリポジトリに変更内容を反映させるもの。
* マージとは分けたブランチを1つに統合すること。
* それぞれ変更内容の反映先が違う。


## コミットとプッシュの違い
* コミットはローカルリポジトリに変更内容を登録することで、プッシュは変更内容をリモートリポジトリに登録することなので、変更内容の反映先が違う。


## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
* 先頭に接頭辞(プレフィクス)を使うことで、コミットメッセージに含める情報を明確にする
* 一目で変更内容が分かるように簡潔に書いてあげるのが最適。
* 各チームやプロジェクト毎にルールがある場合はそれに従うのが良い。
* プレフィクスとは接頭辞(prefix)のことでコミットメッセージの先頭につけ、コミットメッセージのカテゴリーを明確にするもの
* プレフィクスの例としては、fix：既存の機能に問題があった場合に使用、add：新しいファイルや機能を追加する場合に使用、change：仕様変更により、既存の機能に修正を加えた場合に使用、などがある。


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
* ローカルでマージするフローは、ローカルの作業用のブランチの変更履歴をローカルのマスターブランチに反映させ(マージ)、ローカル側のマスターブランチの変更履歴をプッシュすることでリモートのマスターブランチにローカルの変更履歴を反映させる。
* プルリクエストでマージするフローは、ローカルの作業用のブランチの変更履歴をプッシュして、その変更履歴をリモート側のマスターブランチに反映させる(マージしてもらう)依頼をかける。
* リモートのマスターブランチに自分で直接マージをするか、マージをしてもらう依頼をかけるかがフローの大きな違い。
* ローカルでマージする場合はコードレビューなどを経由しないため早くマージすることができる。
* しかし、ローカルでマージする場合は、コードレビュー前に変更内容が反映されるため、コードにバグがあっても気づかれない可能性が、プルリクエストでマージする場合に比べると上がってしまう。


## コンフリクトを起こしてしまった場合、どう対処すべきですか？
* どのタイミングでマージされた変更内容を取り込むかを選択するが、実際の現場では自分以外の人が書いたソースコードの内容を把握する必要があるため、他のソースコードを書いた人と相談をした後に、エディタを使って変更内容を取り込んだ処理で上書きを行うことで解決を図るべき。