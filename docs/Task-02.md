# Rolling Scopes School Nodejs AWS Course 2021

<br/>

### Task 2 - S3, Cloudfront, Serverless

<br/>

### Ручной деплой

<br/>

![Application](/img/task-02-pic-01.png?raw=true)

<br/>

**webmak-manual-bucket policy**

<br/>

```json
{
  "Version": "2012-10-17",
  "Id": "Policy1628970986955",
  "Statement": [
    {
      "Sid": "2",
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity E1D3SOT9QYSYDB"
      },
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::webmak-manual-bucket/*"
    }
  ]
}
```

<br/>

**Автоматический деплой скриптами**

<br/>

    $ aws configure

    $ yarn add serverless-finch
    $ serverless create --template aws-nodejs --path ./sl

<br/>

    $ yarn build

    // деплой приложения в bucket
    $ yarn client:deploy

<br/>

<br/>

**Автоматический деплой всего**

    $ yarn install

    // Нужно использовать следующую команду
    $ yarn cloudfront:update:build:deploy:nc
