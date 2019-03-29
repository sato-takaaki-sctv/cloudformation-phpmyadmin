# phpMyAdmin on EC2

phpMyAdminがセットアップ済みのEC2を起動するCloudFormationテンプレートです。  
ちょっとRDSをGUIで操作したいときにサクッと立ち上げて、終わったら削除するような利用におすすめです。

# 使い方

AWSのCloudFormationで、スタックの作成からymlファイルを読み込ませてください。  
スタック作成完了後、出力タブにphpMyAdminのURIが出力されます。

## パラメータ

`AllowIp`  
phpMyAdminにアクセスするIPアドレスを指定してください。  

`DBHost`  
RDSのエンドポイントを指定してください。

`DBPort`  
RDSのエンドポイントのポート番号を指定してください。

`InstanceType`  
phpMyAdminを動かすインスタンスタイプを選択してください。

`RDSSecurityGroupId`  
RDSにアクセス可能なセキュリティグループを選択してください。

`SubnetId`  
EC2が配置されるサブネットIDを指定します。  
RDSへアクセス可能なパブリックサブネットを選択してください。

`VpcId`  
EC2が配置されるVPCIDを指定します。  
RDSと同一のVPCを選択してください。

# SSHしたいとき

Systems ManagerのSession Managerで接続してください。
