# AWS_SAP_output

IDフェデレーションとロールベースのアクセス制限は、オンプレミスのActive DirectoryとIAMロールに接続するADコネクターが必要。

IDプロバイダーとフェデレーションを使用して、アプリケーションベースの認証を行うことができる。
一時的なアクセスのS3オブジェクトと認証のために、ユーザーごとにフォルダーを作成して、各ユーザーのアクセス許可をそれぞれのフォルダーに制限できる。
ユーザーの画像の保存にS3を使用し、これらの画像へのアクセスをユーザーに認証して承認する方法。単一のS3バケット内の全てのユーザーオブジェクトのユーザーIDで設定されるキーベースの命名方式を使用し、アプリケーションベースでユーザーを認証し、AWS STSを使用して、S3オブジェクトにトークンベースの認証を付与する。

AWS STS : IAMに含まれる機能であり、一時的に認証トークンを発行する。
