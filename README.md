# ecs-cfn-deploy
* CFn stackの作成
```
aws cloudformation create-stack --stack-name yoshida-stack --template-body file://hoge.yaml --capabilities CAPABILITY_NAMED_IAM
```

* 変更セットの作成
```
aws cloudformation create-change-set --stack-name yoshida-stack --template-body file://hoge.yaml --change-set-name yoshida-changeset --capabilities CAPABILITY_NAMED_IAM
```

* 変更セットの確認
```
# 一覧
aws cloudformation list-change-sets --stack-name yoshida-stack

# 変更内容
aws cloudformation describe-change-set --stack-name yoshida-stack --change-set-name yoshida-changeset
```

* 変更セットの適用
```
aws cloudformation execute-change-set --stack-name yoshida-stack --change-set-name yoshida-changeset
```
