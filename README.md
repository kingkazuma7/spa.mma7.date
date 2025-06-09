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

## Git開発フロー

### 1. 開発の開始
```bash
# 最新のmasterブランチを取得
git checkout master
git pull origin master

# 開発用のfeatureブランチを作成
git checkout -b feature-dev
```

### 2. ローカルでの開発
```bash
# 変更したファイルをステージング
git add .

# 変更をコミット
git commit -m "変更内容の説明"

# リモートにプッシュ
git push origin feature-dev
```

### 3. リモートとの同期
```bash
# リモートの最新状態を確認
git fetch origin

# ローカルとリモートの差分を確認
git log --graph --oneline --all

# リモートの状態に強制的に合わせる（注意: ローカルの変更は失われます）
git reset --hard origin/feature-dev

# または、変更を保持したい場合
git stash save "作業中の変更"
git reset --hard origin/feature-dev
git stash pop
```

### 4. コンフリクト解決
```bash
# コンフリクトの確認
git status

# コンフリクトを解決後
git add .
git commit -m "コンフリクトを解決"
git push origin feature-dev
```

### 5. masterへのマージ
```bash
# masterブランチに切り替え
git checkout master

# feature-devの変更を取り込む
git merge feature-dev

# リモートのmasterを更新
git push origin master
```

### 注意事項
- `git reset --hard`を使用する前に、必ず変更をバックアップしてください
- チーム開発の場合は、他の開発者に影響を与える可能性のある操作を行う前に連絡してください
- コミットメッセージは具体的で分かりやすい内容にしてください
- 定期的に`git fetch`で最新の状態を確認することをお勧めします