perfect_rails
=============

パーフェクトなRailsを読書します

毎回の流れ
---

+ 前日まで
 + ファシリテーターが開催日のイベントをg+に投稿
  + Rubyコミュニティのページからイベント作成しましょう
 + ファシリテーターが開催日用の実況板をgithub issueに作成
 + 班分け
+ 当日
 + 班分けで席作成
 + ファシリテーターが章の簡単な説明(〜ページまでですくらい)
 + 班に分かれて予習内容の共有
  + みんなでissueに実況してもらう
 + 全体共有
 + 次回の範囲決め
 + 次回のファシリテーターとレポーターの指名(なるべくみんなやる)
+ 金曜まで
 + レポーターの人がissue読みながら開催レポートをPull Requestで提出
 + ファシリテーターの人がPull Request読んでマージ

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

# コミットする
git add `date +"%Y%m%d"`
git commit -m "第N回のレポートを作成"

# レポートをリモートブランチにプッシュする
git push origin `date +"%Y%m%d"`

# その後 https://github.com/ValLaboratory/perfect_rails からPR作成
# hubコマンドツール( https://github.com/github/hub )導入済みならば
hub pull-request
~~~

実況板
---

各班の状況がわかるとレポートも書きやすいので、<br>
適度にGitHubのissueに実況をお願いします。

環境構築
---

基本は本の通りで良いと思いますが、悩んだらVagrantでCentOSの環境を入れましょう<br>
(presented by o-sawa)

２つ用意してありますので、お好きな方をお使いください。<br>
設定してあることなどは各gistのreadme.mdに入っておりますので、そちらをご覧ください。
 1. 社内Proxy設定有り<br>
    git@gist.github.com:/ab19a6513991e324f2d4.git
 1. Proxy設定なし<br>
    git@gist.github.com:/347da47a0cede44f551e.git

~~~
# o-sawaのvagrant設定を手元にクローン(pathは利用する環境により読み替えてください)
git clone git@gist.github.com:/347da47a0cede44f551e.git

# クローンしたディレクトリに移動
cd 347da47a0cede44f551e

# Vagrantfileを元にCentOSマシンを立ち上げる
vagrant up

# マシン内仮想CentOSにログイン
vagrant ssh
~~~
