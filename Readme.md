# Rolling Scopes School Nodejs AWS Course 2021

<br/>

### Task 2 - S3, Cloudfront, Serverless

<br/>

    $ aws configure

    $ yarn add serverless-finch
    $ serverless create --template aws-nodejs --path ./sl

<br/>

    $ yarn build
    $ yarn client:deploy

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

cloudfront - https://d3mar97h1cxegg.cloudfront.net/

bucket - http://webmak-manual-bucket.s3-website.eu-central-1.amazonaws.com/

<br/>

**Автоматический деплой скриптами**

<br/>

    $ yarn install

    // Нужно использовать следующую команду
    $ yarn cloudfront:update:build:deploy:nc

<br/>

cloudfront - https://webmak.site/

Или

d2siadvb5bmoyb.cloudfront.net

bucket - http://webmak-auto-bucket.s3-website.eu-central-1.amazonaws.com/
