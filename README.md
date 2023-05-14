# 進め方
- 先に学習メモ書き出す。
- 各リソースごとにディレクトリを作成し、 学習メモを分けてリソースごとに復習しやすいように管理する。

# AWS_SAP_output

IDフェデレーションとロールベースのアクセス制限は、オンプレミスのActive DirectoryとIAMロールに接続するADコネクターが必要。

IDプロバイダーとフェデレーションを使用して、アプリケーションベースの認証を行うことができる。
一時的なアクセスのS3オブジェクトと認証のために、ユーザーごとにフォルダーを作成して、各ユーザーのアクセス許可をそれぞれのフォルダーに制限できる。
ユーザーの画像の保存にS3を使用し、これらの画像へのアクセスをユーザーに認証して承認する方法。単一のS3バケット内の全てのユーザーオブジェクトのユーザーIDで設定されるキーベースの命名方式を使用し、アプリケーションベースでユーザーを認証し、AWS STSを使用して、S3オブジェクトにトークンベースの認証を付与する。

AWS STS : IAMに含まれる機能であり、一時的に認証トークンを発行する。

クロスアカウントアクセスはITガバナンスの提供に役立つ。一括背級を使用して、部門アカウントを親企業に管理アカウントにリンクすることでコストの監視に役立つ。

監査人は読み取り専用のアクセスのみを必要とするため、読み取り専用アクセス、最小限のアクセス権限を持つIAMユーザーを作成する

タグ付けを実装して、タグ付けしたリソースに適切な権限と制限を定義できる。既知のIPアドレスからのみ送信されるようにすることもできる。

サーバー側の暗号化でS3は保存時に暗号化を提供し、HTTPSを使用してデータをS3いプッシュして転送中に暗号化することができる。エフェメラルドライブは趣味レーションの実行に役立ち、EC2インスタンスが終了するまで使用できる。

VPN : VPCとオンプレミス間で暗号化接続を確立させるしゅだんの一つ。オンプレ側にAWSとの接続要件を満たすVPNせつぞくが可能なネットワーク機器を用意。NPC側にオンプレのネットワーク機器に対応したCGWとAWS側のVPC機能を有効にするためにVGWを作成し、VPC接続を確立する。

2つのデータセンターにそれぞれ別のCGWを追加し、データセンタ間を2つのデータセンター間を2つのトンネルを持つVPN接続を作成する。

インスタンスボリュームは一時的な保管スペース。バックアップ用途に向かない

Direct Connectを使用し、VPCとオンプレミス環境の間で、ネットワークのコストを削減し、帯域幅のスプープットを向上させmインターネットベースの接続よりも安定したものを提供できる。

VPN接続はコストを低く抑えられるが、低速で帯域を確保するのが難しい。

System Managerはパッチ適用のプロセスの自動化に役立つ。

署名付きURLを使用したオブジェクトのアップロードには、有効なセキュリティ資格情報を使用した署名付きURLがないとアップロードをムクメタアクセスができない。また有効期限が切れるとアップロードを含めたアクセスができない。

署名付きURLから「書き込み」許可を受ける。

VPCピアリング : 異なるVPCを接続することができる。

Direct connect : キャリアから調達する専用線の片端とAWSCloudをDirect Connectロケーションで接続するサービス。
https://speakerdeck.com/recruitengineers/awsyan-xiu-amazon-snstoamazon-sqs?slide=23

- system namager patch manager : パッチ適用のプロセスの自動化に奴立つ。マネージドインスタンスにパッチを適用するプロセスを自動化　https://d1.awsstatic.com/webinars/jp/pdf/services/20200212_AWSBlackBelt_SystemsManager_0214.pdf

- VGW : VPCに付与するもの。 単一障害点。 デュアルトンネルVPNを使用するなどして、単一障害点の問題を解決する。
