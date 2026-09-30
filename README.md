# empty-teams-custom-application-package

Teamsカスタムアプリの登録・追加可否を確認するための、最小構成の検証パッケージと日本語マニュアルです。

**現在はZIP化前の準備版です。** 会社名とURLは未設定値のため、実際の情報に変更してからZIP化してください。お客様テナントへの登録・ユーザー追加は未実施です。

## 内容

```text
TeamsImportVerification/
├── TeamsImportTest/
│   ├── manifest.json
│   ├── color.png
│   └── outline.png
├── docs/
│   ├── Teamsカスタムアプリ_インポート可否検証手順書.*
│   ├── 配布前チェック結果.md
│   └── 修正内容一覧.md
└── sources/
    ├── MicrosoftTeams.v1.19.schema.json
    └── icons/
```

個人用タブを1つ定義しています。業務画面、Bot、SSO、外部API連携は実装していません。登録・追加の成功と、タブの画面表示は別に判定します。

## 利用手順

1. [準備一式の案内](TeamsImportVerification/README.md)を確認します。
2. [manifest.json](TeamsImportVerification/TeamsImportTest/manifest.json)の会社名、各URL、`validDomains`を実値に変更します。
3. [手順書](TeamsImportVerification/docs/Teamsカスタムアプリ_インポート可否検証手順書.md)の配布前チェックを実施します。
4. `TeamsImportTest`内の3ファイルだけをZIP直下に格納します。
5. お客様の管理者が、利用対象を確認したうえで管理センターから登録します。

## マニュアル・検査結果

- [Word版](TeamsImportVerification/docs/Teamsカスタムアプリ_インポート可否検証手順書.docx)
- [PDF版](TeamsImportVerification/docs/Teamsカスタムアプリ_インポート可否検証手順書.pdf)
- [HTML版](TeamsImportVerification/docs/Teamsカスタムアプリ_インポート可否検証手順書.html)
- [配布前チェック結果](TeamsImportVerification/docs/配布前チェック結果.md)
- [修正内容一覧](TeamsImportVerification/docs/修正内容一覧.md)

マニフェストv1.19の公式スキーマによる構造検査はエラー0件でした。実際のURLへの差し替え後は再確認が必要です。構造検査の合格は、Teamsへの登録成功を保証するものではありません。
