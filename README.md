[JP] 02. 開発ガイドライン - BFF API (v2.0)
    1. 概要
 BFFとは
BFF (Backend for Frontend) パターンは、アプリケーション開発、特にウェブやモバイルアプリケーションの開発において一般的なアーキテクチャモデルである。BFFの主なアイデアは、フロントエンドとバックエンドのサービス間にシンプルなインターフェースとして機能することである。
 構成要素と役割
 Model: エンティティ、リクエスト/レスポンスを管理する。
 Controller: クライアントからのHTTPリクエストを処理し、サービス層のメソッドを呼び出して結果を返す。
 Service: アプリケーションのビジネスロジック処理を含む。リポジトリ層のメソッドを呼び出してバックエンドサービスとやり取りし、データを処理してコントローラーに結果を返す。
 Repository: クライアントからのリクエストをバックエンドサービスに転送し、データを処理してサービス層に結果を返す。  アーキテクチャ図
以下の図はシステムの主要な構成要素とそれらがどのように相互作用するかを描いた設計図となる。 (BFF_DetailDiagram.md - Repos (azure. com))



    2. インプット

参照資料
ファイル名
参照内容
API設計基準

04API設計基準 - Overview (azure. com)
APIを実装する際の基準
日付基準設計

03日付基準設計 - Overview (azure. com)
日付と時間データの取り扱いに関する基準
マスタ管理規約（フロントエンド）

マスタ管理規約（フロントエンド）. md - Repos (azure.com)
コードリスト/マスタの使用に関する規約
方式設計
01方式設計.md

非機能要件
システムアーキテクチャ設計
BFF API設計
KFKNGxxxxxxxAxx_.md
BFF APIの業務要件の説明
BFF API yaml
KFKNGxxxxxxxAxx_.yaml
BFF APIに適用するOpenAPI仕様
適用する範囲
PropertyDtoの作成 ResponseDtoの作成
単体チェック処理の作成に使用
common_request_info用の yaml
common_request_info.yaml
共通情報リクエストに適用するOpenAPI仕様
item_kihon_data_base用の yaml
item_kihon_data_base.yaml
リクエストAPIのデータフィールドに適用するOpenAPI仕様
message_info_<http status code>用のyaml
message_info_<http status code>.yaml
HTTPステータスコードに応じるレスポンスに適用するOpenAPI仕様
BE APIのED
KBKSKxxxxxxxAxx_~API .md
バックエンドAPIのインターフェースの説明
BE APIのyaml
KBKSKxxxxxxxAxx_~API .yaml
BE APIに適用するスOpenAPI仕様
BEでの適用する範囲 PropertyDtoの作成 ResponseDtoの作成
yamlファイルとマッピングできるようにモデルを作成する際はJsonPro pertyName属性を指定する必要がある。
共通要件
FBSS_基盤_要件確認事項.xlsx
参照資料に基づいてまとめた総合基準
