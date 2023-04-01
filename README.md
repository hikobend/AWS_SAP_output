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
