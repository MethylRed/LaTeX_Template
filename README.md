# LaTeX_Template

## Docker

1. `docker-compose up -d tex` \\Containerの起動
2. `docker-compose exec tex latexmk hogehoge.tex` \\texファイルのコンパイル
3. `docker-compose down` \\Containerの停止削除

(`docker-compose exec tex /bin/sh`でコンテナに入ることもできる)

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