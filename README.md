perfect_rails
=============

パーフェクトなRailsを読書します

レポート
---

レポーターの方はPull Requestで該当回のレポートをお願いします<br>
フォーマットは [第1回](https://github.com/ValLaboratory/perfect_rails/blob/master/reports/20140826.md) を参考にしてみてください

+ このリポジトリを手元にクローンする
+ 勉強会の日付(yyyyMMdd) でブランチを切る (git checkout -b 20990401)
+ reports/(勉強会の日付).md というファイルにmarkdown形式でレポートを書く
+ ブランチをpushし、Pull Requestを出す

UNIX系OSでの実施手順は以下の通りです

~~~
# リポジトリを手元にクローン
git clone git@github.com:ValLaboratory/perfect_rails.git

# クローンしたディレクトリに移動
cd perfect_rails

# 今日の日付でブランチを切ってチェックアウト
git checkout -b `date +"%Y%m%d"`

# reports/(今日の日付).md というファイルを作る
touch reports/`date +"%Y%m%d"`.md

# レポート書く(viじゃなくてもいいです)
vi reports/`date +"%Y%m%d"`.md

# レポートをリモートブランチにプッシュする
git push origin `date +"%Y%m%d"`

# その後 https://github.com/ValLaboratory/perfect_rails からPR作成
~~~

実況板
---

各班の状況がわかるとレポートも書きやすいので、<br>
適度にGitHubのissueに実況をお願いします。

環境構築
---

基本は本の通りで良いと思いますが、悩んだらVagrantでCentOSの環境を入れましょう<br>
(thx to おおさわさん)

~~~
# おおさわさんのvagrant設定を手元にクローン
git clone git@gist.github.com:/347da47a0cede44f551e.git

# クローンしたディレクトリに移動
cd 347da47a0cede44f551e

# Vagrantfileを元にCentOSマシンを立ち上げる
vagrant up

# マシン内仮想CentOSにログイン
vagrant ssh
~~~
