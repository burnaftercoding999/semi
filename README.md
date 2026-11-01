# 半導体市況研究・分析 公開ページ

半導体の上流・半導体売上・下流需要・AI関連企業の公開情報を分けて整理する研究用ページです。投資助言、個別銘柄の順位付け、株価予測、売買推奨は扱いません。

## 公開ページ

https://burnaftercoding999.github.io/semi/

ページには、報告値、会社計画、二次推計、仮定計算、検証済みチェックを区別して表示しています。USDを基準にし、表示用のJPY換算を併記しています。

## 読み方

最初に結論を読み、その後で公表値、予測の手順、期間別の結果、限界の順に確認できます。3か月先は四半期売上の探索的な計算、1年と3年は前提を置いたシナリオです。数字の種類と対象期間をそろえて読んでください。

## 初回設定

リポジトリの Settings → Pages → Build and deployment → Source で `GitHub Actions` を選択します。公開ワークフローは `.github/workflows/pages.yml` です。artifactの対象は `public/site` に限定しています。

## 更新

分析結果を保存し、公開ページを生成してpushする更新処理は、研究環境側で次のコマンドを実行します。

```powershell
.\publish_report.ps1 -Publish
```

生成と検査だけを行う場合は、次を実行します。

```powershell
.\publish_report.ps1 -SkipAnalysis -CheckOnly
```

push後は Actions の `Publish research report to GitHub Pages` を確認します。失敗時は、Pages設定、Actions権限、`pages: write`、`id-token: write` を確認してください。

## 公開範囲

公開対象は、公開ページ、ページ履歴、Pagesワークフロー、このREADMEだけです。認証情報、個人情報、内部メモ、原文PDF、生データ、取得マニフェスト、ハッシュ値は公開対象に含めません。
