# Docker-ninix-aya

[ninix-aya](http://sourceforge.jp/projects/ninix-aya/)をDocker化してみました。

# narファイルの入手

何とか頑張り、.narファイルをninixフォルダに格納して
以下を実行する


# イメージのビルド

```
docker build -t kjunichi/ninixaya .
```

# コンテナの起動

```
docker run -d -p 20022:22 -p 9801:9801 kjunichi/ninixaya
```

# コンテナを使う

パスワードは「ninix123」

## OSX

```
ssh -X root@$(boot2docker ip 2>/dev/null) -p 20022
ninix&
```

## その他

```
ssh -X root@localhost -p 20022
ninix&
```
