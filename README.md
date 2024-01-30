# 基本情報

* 名前：山家 紳（やまが しん）
* 経験技術（実務）：PHP、Kotlin (得意)、TypeScript、Spring Boot、React、Terraform、AWS、Docker、Git
* 経験技術（個人開発・独学）：Python、Java、Ruby、Ruby on Rails
* やりたいこと・大切にしたいこと
    * 利用者のフィードバックを得ながらサービスの開発をすること
    * ドメイン知識を身につけること
    * 技術の好き嫌いをせず、目の前の課題に対して必要な技術を身につけること
* なりたいエンジニア像
    * プロダクト開発のあらゆる局面で活躍できるエンジニア
    * SRE的視点を持ったアプリケーションエンジニア

# 職務経歴

**株式会社コドモン (2022年4月〜現在)**

既存機能の運用保守や新規マイクロサービス開発を担当。
運用保守では、不具合改修や機能追加、ユーザーからの問い合わせ対応を担当。
新規開発では、アプリケーション開発に加え、CICDの整備やIaCツールによるインフラリソース構築を担当。

## 新規機能開発
2023年10月 - 現在

### 概要

施設と保護者間の用品販売・購入を管理する新規機能の開発

### 担当業務
* 仕様の検討・策定
* フロントエンド・バックエンド開発
* インフラ構築
* Design docの作成
* CICD整備
* 負荷試験

### 工夫したこと
* チームメンバーが苦手としていることを引き受けること。

    シニアメンバーが育休取得で不在になり、インフラに明るいメンバーがチームにいない状態となった。そこで、自らインフラ構築やCICD業務を引き受け、TerraformによるAWSリソース作成や、GitHub Actions、 ecspressoを利用したCICD整備を牽引した。また、SREチームから得た知見をチームに還元したり、Design Docを作成することでシステムに対する認知負荷を下げることに取り組んだ。その結果、チームが自立してインフラリソースやCICDの管理ができるようになった。

* 手戻りを防ぐための、PdM・PDとのE2Eテスト作成。

    考慮漏れによる実装の手戻りやテストケースの不足を防ぐため、実装前に自動E2Eテストの作成をPdMと実施した。Gauge/Playwrightを使用してマークダウン形式の自動E2Eスクリプトを作成することで、技術用語を使用せず受け入れ条件の認識を揃えることができた。


### 利用技術
Kotlin、 Spring Boot、 TypeScript、 React、 PostgreSQL、 AWS、 Terraform、GitHub Actions、 ecspresso、 DDD、 Clean Architecture

## 消費税計算・請求書作成機能のインボイス対応
2023年7月 - 2023年9月

### 概要
施設が保護者に請求する保育料のインボイス制度に対応する必要があった。消費税計算処理と、その結果を表示するブラウザ・Excel/CSV出力・モバイルアプリの改修を担当した。

### 担当業務
- クラス設計/開発/テスト

### 工夫したこと
* 手続き型プログラムのリファクタリング

    既存のソースコードは、各APIインターフェイスごとにビジネスロジックとDBアクセス処理が手続き型で実装されており、改修対象である消費税計算ロジックが各APIに点在している状態であった。そこで、変更を加える前に既存の消費税計算に共通化するリファクタリングを行った。その結果、消費税計算の処理のテスト容易性と変更容易性を向上した。

### 利用技術
PHP、 TypeScript、 DDD、 Clean Architecture

## 保育料計算バッジ処理の改修
2023年4月 - 2023年7月

### 概要
保育料計算バッチ処理の改修を担当。この機能は、施設種別や補助金の有無、各園児の契約状況・利用実績など、様々な変数によって算出を行うため、複雑な仕様理解と多角的なテストケースを必要とする改修であった。

### 担当業務
* ビジネスサイドとのリリーススケジュール調整
* 開発/テスト
* ドキュメント整備・新規参画メンバーのフォロー

### 工夫したこと
* 「動作し続ける状態を保つ開発」の提案・実施
    
    開発着手当初、クリーンアーキテクチャのユースケース・エンティティ層から実装し、最後にエントリーポイントとの疎通を実装するという計画を立てた。しかし以下の課題があった。
    
    * 全ての実装が完了するまで受け入れテストが実施できない
    * メンバー間で最終成果物のイメージに差が生じ、ペアプロでのコミュニケーションが円滑でない
    
    そこで、受け入れテスト（APIのインテグレーションテスト）と、APIエンドポイントを先に実装してから、ユースケース/エンティティ層との疎通をすることを提案、実施した。その結果、常に受け入れテストから成果物に対するフィードバックを得ながら、開発を進めることができた。

* チームメンバーのドメイン知識向上を促進
    メンバー間で保育料計算ロジックに対する理解度にばらつきがあった。そこでホワイトボードツール（Miro）を利用し、計算ロジックを図解できるようにした。また、多角的な計算パターンを機能から把握できるようにローカル環境にサンプルデータを作成した。その結果、メンバー間のドメイン知識の差を解消し、誰でも当機能の改修に参画することができるようになった。

### 利用技術
PHP、 TypeScript、 DDD、 Clean Architecture
