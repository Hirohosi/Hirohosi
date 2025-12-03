# 開発の紹介

## 勤怠管理 SaaS（開発中）
サービスURL

※現在クローズド運用中

開発期間

2025/7 〜 開発継続中

### サービス概要

中小企業向けの シンプル × 正確 × 低コスト を重視した勤怠管理SaaS。

打刻・休暇・残業計算・締め処理までを一気通貫で処理でき、
スマホ・PC・タブレットに依存しない柔軟な打刻方法 を提供。

勤怠データは自動で整形され、給与計算システムにCSV連携可能。

現場負担ゼロで導入できる「導入しやすさ」と、
毎月の締め作業を大幅に削減する「省力化」を両立。

### 目的・解決したい課題
プロダクトの目的

中小企業の「勤怠締めの毎月の地獄」を解消

シンプルで使いやすい UI によって現場のストレスをゼロに

社労士さんにとっても使いやすいシステムを構築

給与システムとの連携負荷を軽減

解決したい課題

紙・LINE・Excel 混在の勤怠管理からの脱却

月末の締め作業に発生する膨大な工数

勤怠データのフォーマット不一致問題

給与計算システムとの連携コスト

従業員・管理者双方の「入力負担の高さ」

技術的な目的

Next.js + React の実務レベルの深掘り

Multi-tenant な SaaS 設計の実践

NestJS での RBAC・API設計の習熟

AWS ECS（Fargate）・RDS の運用経験

Terraform による IaC 化

Stripe を用いたサブスク課金（Seat課金＋Trial）

EventBridge + Lambda によるバッチ処理の構築

### 技術的スタック
フロントエンド

React / TypeScript / Next.js

tailwindCSS

Zustand / React Hook Form

Storybook / Chromatic（UI検証）

バックエンド

NestJS（認証・権限・API層）

RBAC

JWT・Refresh Token

Class-Validator / Swagger

インフラ

AWS ECS Fargate

RDS (PostgreSQL)

ALB + ACM

EventBridge → Lambda（締め処理・勤怠補正バッチ）

S3

CloudWatch

Terraform（IaC）

Cognito

課金 / 認証

Stripe（Seat課金・Trial期間・無料枠対応）

その他

Github Actions による CI/CD

PR ベース開発

Notion の仕様書・タスク管理

### 主な機能

出退勤打刻

自動休憩 / 自動丸め設定

残業計算（法定内 / 法定外 / 深夜）

休暇申請・承認フロー

シフト登録

勤怠一覧 / 月次締め

CSVエクスポート

マルチテナント（企業ごとに独立）

権限管理

部署管理

ロールごとのダッシュボード

### 構築・工夫したポイント
✔ 月次締めの省力化

勤怠データを日別 → 月別へ自動集計し、残業・深夜・休暇を自動計算。

給与計算担当者が
CSV インポートだけで弥生給与に取り込める 形式に整形される。

✔ Multi-tenant / RBAC の本格実装

企業（テナント）ごとのデータ隔離、
管理者 / 従業員の権限分離など、
実際の SaaS 要件に沿った設計を経験。

✔ 実運用を想定した導線設計

社労士ネットワークへの展開を前提として、
導入時の “最初のハードル” を徹底して下げる UI/UX を採用。

### 今後の展望

弥生給与 API 連携（CSV不要化）

モバイルアプリ（React Native）

AI 日報解析（勤怠の異常検知）

タイムカードの自動OCR

Slack / LINE 通知連携

社労士ダッシュボード（顧問先一覧＋締め状況管理）

## デジタク
### サービスURL
iOS: https://apps.apple.com/app/id6477824613

Android: https://play.google.com/store/apps/details?id=com.corepra.gyotaku

### 開発期間
2023/7~2024/3
### サービス概要
魚の写真から、背景を切り抜き、背景や文字を合成して魚拓を作るサービス

### 目的
プロダクトの目的
- 魚拓作成にかかるコストを下げる
- 魚拓という文化を広めること

技術面の目的
- モバイル開発の設計のキャッチアップ
- 宣言的なUIのキャッチアップ
- モバイル開発のリリースの経験

### 技術的スタック
iOS
- Swift
- SwiftUI、Combine
- Alamofire、Swinject、VisionKit
- MVVMとクリーンアーキテクチャの採用

Android
- Kotlin
- JetpackCompose、AAC
- Retrofit、Hilt
- MVVMとクリーンアーキテクチャの採用

バックエンド,インフラ
- Python
- Docker
- AWS Lambda,APIGW

その他
- Githubでのコード管理
- Notionでのタスク管理

## TechCurrent
### サービスURL

https://tech-current.com

※スマホUI非対応

### 開発期間
2024年の8~9月

### サービス概要
技術系の記事のキュレーションサイト

ユーザーごとに見たい記事のカスタマイズができ、必要な情報だけを素早くキャッチアップできる。

### 目的・解決したい課題
プロダクトの目的
- 自身の情報のキャッチアップの効率化のために作成
- 技術記事の情報を集約
- 技術記事のキャッチアップのコストを下げる

技術的な目的
- Goのキャッチアップ
- Nextのキャッチアップ
- Supabaseの利用
- バックエンドでのクリーンアーキテクチャの利用
- GCPの利用
- CICDの設定

### 技術的スタック
フロントエンドおよびバックエンド
- react,typescript,Next.js
- tailwindCSS
- Docker
- CICD設定

バッチ処理
- Go
- クリーンアーキテクチャ
- Docker

インフラ
- ホスティング：GCPのCloudRun
- DB,認証:Supabase

その他
- Githubでのコード管理
- Githubのissueでのタスク管理


## 釣りのバトルアプリ

### サービスURL
https://main.d36ssoxvo58uld.amplifyapp.com/

### 開発期間
2024年の6~7月

### サービス概要
釣りの大会や対戦をオンラインベースで行うことができる

釣った魚に応じたポイントで対戦が可能

ポイントの設定はカスタマイズ可能
#### 目的・解決したい課題

プロダクトの目的
- 釣りの時に仲間内で使用するために作成
- 地理的に離れた仲間ともオンラインベースで対戦が可能に

 技術的な目的
- Nextのキャッチアップ
- tailwindCSSのキャッチアップ
- FirebaseのFirestoreの利用

#### 技術的スタック
フロントエンド
- react,typescript,Next.js
- tailwindCSS

バックエンド,インフラ
- FirebaseのFirestoreの利用
- AWS AmplifyでのNextアプリのホスティング

その他
- Githubでのコード管理
- Notionでのタスク管理
