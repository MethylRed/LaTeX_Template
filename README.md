# LaTeX_Template

## Docker

1. ctrl+@でターミナルを開く(VScode)
2. cd でtexファイル、docker-compose.yml、.latexmkrcがあるファイルに移動
3. `docker-compose up -d tex` \\Containerの起動
4. `docker-compose exec tex latexmk hogehoge.tex` \\texファイルのコンパイル
拡張子の.texがなくてもコンパイルできる
5. `docker-compose down` \\Containerの停止削除
`docker stop コンテナ名`の方が良い

(`docker-compose exec tex bash`でコンテナに入ることもできる)

## docker-compose.ymlの書き方(てきとう)
version: '3'
services:
--------------------ここまでテンプレ
  gcc:                            <- texならtex、pythonならpython3かpython2(バージョンによる)
    image: gcc                    <- image名
    container_name: gcc           <- コンテナの名前を決める(削除したり停止させたりするときに便利)
    tty: true                     <- コンテナを起動させ続ける
    volumes:                      <- 自分のPC(ローカルという)とコンテナの中身をリンクさせる
      - ./:/gcc                   <- [ローカル]:[コンテナ]で書く
      　　　　　　　　　　　　　　　　　ローカルは自分のいる場所が基本、コンテナはなんでもいい(わかりやすい名前にしておくといい)

## Git

1. `WebでGithubにLogin`
2. `Repositories->New->Create repository`
3. `Clone or downloadでURLをクリップボードにコピー`
4. `On GitBash\\repositoryを置くディレクトリに移動 cd`
5. `git clone URL`

1. `git add .`
2. `git commit -m "hogehoge"`
3. `git push origin master`
4. `usernameとpasswordの入力`
