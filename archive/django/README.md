# Django 版アーカイブ

GitHub Pages 向けに静的サイトを本体へ戻したため、Django プロジェクト一式をここに退避しています。

含まれるもの（概ね）:

- `manage.py`
- `requirements.txt`
- `config/` — Django プロジェクト設定
- `quiz/` — クイズアプリ（views / services / static / templates）

## ローカル実行（参考）

```bash
cd archive/django
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

※ モジュールパスは `config` / `quiz` がカレント想定です。  
Character DB 系の未マージ PR 作業とは別物です。
