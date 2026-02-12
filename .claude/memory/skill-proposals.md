# Skill Proposals — Implementation Plan

## Tier 1: Immediate Impact

### /stock-screener
- Purpose: ティッカー → 買い/見送り/要監視を自動判定
- Checks: 決算サプライズ、チャート条件、テーマ適合、スクリーニング基準
- Structure: `SKILL.md` + `references/rules.md` + `references/checklist.md`
- Config: `disable-model-invocation: true`
- Priority: 1st

### /earnings-check
- Purpose: 直近決算のEPS/売上サプライズ、ガイダンス、コールトーン要約 + 過去2年傾向
- Output: 結論→理由→リスク→次の一手
- Priority: 2nd

### /market-brief
- Purpose: ウォッチリスト前日終値・変動率・ニュース一覧 + 損切りライン接近アラート + ブレイクアウト候補フラグ
- Tech: WebSearch + 動的データ取得
- Use case: 早朝ルーティン1コマンド化
- Priority: 3rd

## Tier 2: Workflow Efficiency

### /weekly-review
- Purpose: 週次ポートフォリオレビュー（パフォーマンス、利確/損切りチェック、リバランス提案、サテライト比率確認）
- Guard: 感情売買の兆候検出 → 警告

### /sales-prep
- Purpose: 企業名 → 企業概要・ニュース・意思決定者・想定課題・提案切り口
- Config: `context: fork`（サブエージェント実行）

### /study-plan
- Purpose: 宅建学習進捗管理（今日の範囲提案、弱点復習、模試スコア追跡）

## Tier 3: Meta Skill

### /memory-maintenance
- Purpose: 全memory/ファイルの重複排除・剪定・行数制限チェック
- Config: `allowed-tools: Read, Edit, Glob, Grep`

## Design Principles (All Skills)
- Progressive Disclosure: 投資ルール等は references/ に分離、SKILL.md < 500行
- Privacy: ポートフォリオ情報はSkillに焼き付けず実行時渡し
- Output Format: 全Skill統一 → 結論→理由→リスク→代替案→次の一手
