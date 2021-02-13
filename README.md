
## docker

```
docker build . -t shigasy/test
```

```
docker run -p 8080:8080 shigasy/test
```

```
docker rm {コンテナID} -f
```

```
docker rmi {イメージID}
```

## GCP

Cloud Buildを使って、ビルドしたイメージをGoogle Container Registryにdockerイメージを保存

project-idを取得
```
gcloud config get-value project
```

Dockerイメージをビルドして保存
```
gcloud builds submit --tag gcr.io/{PROJECT-ID}/helloworld
```

cloud runにデプロイ
```
gcloud run deploy --image gcr.io/PROJECT-ID/helloworld --platform managed
```

### GAE SE
```
gcloud app deploy
```