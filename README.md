

# MMA7 SPA Application

## プロジェクト概要
MMA7のSPA（Single Page Application）プロジェクトです。LaravelとVueを使用した最新のWeb開発プラットフォームです。

## 技術スタック
- Backend: Laravel 10.x
- Frontend: Vue.js
- Database: MySQL
- Authentication: Laravel Sanctum

## 必要要件
- PHP 8.3.21
- Node.js v18.18.1
- Composer 2.6.5以上
- MySQL 5.7以上

## インストール手順
1. リポジトリのクローン
```bash
git clone [repository-url]
```

2. 依存関係のインストール
```bash
composer install
npm install
```

3. 環境設定
```bash
cp .env.example .env
php artisan key:generate
```

4. データベースの設定
- .envファイルでデータベース接続情報を設定
- マイグレーションの実行
```bash
php artisan migrate
```

5. アプリケーションのビルド
```bash
npm run build
```

## 開発環境での実行
```bash
php artisan serve
npm run dev
```

## デプロイ手順
1. 本番環境での設定
```bash
composer install --optimize-autoloader --no-dev
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

2. フロントエンドのビルド
```bash
npm run build
```

## 主な機能
- ユーザー認証
- [その他の主要機能をリスト化]

## 注意事項
- PHP 8.3.21での動作を確認しています
- 本番環境ではデバッグモードを無効にしてください

## ライセンス
[ライセンス情報を記載]