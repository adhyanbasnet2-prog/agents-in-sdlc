---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

**[GitHub Copilot CLI](https://docs.github.com/copilot/concepts/agents/about-copilot-cli)** は、ターミナルで GitHub Copilot をエージェント型のコーディング アシスタントとして利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業の流れを保てます。

このワークショップでは、Tailspin Toys で一連の作業を行います。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして基本操作を確認します。
2. 星評価の小さな変更を加え、ブラウザーで確認して、最初のプル リクエスト (PR) を手動でマージします。
3. フィルタリングの Issue から始め、Plan モードで方針を決め、Autopilot モードで実装し、Interactive モードでレビューします。
4. リポジトリの命令を更新し、フィルタリングの作業に適用します。
5. 既存の `quality-checks` スキルをカスタマイズし、プロジェクトのチェックを実行します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーでフィルタリングを確認します。
7. 品質保証 (QA) のカスタム エージェントを作成し、要件、カバレッジ、検証結果をレビューします。
8. フィルタリングの変更全体をレビューし、Agent Merge を使って該当する PR を処理します。
9. コンテキスト、モデル、共有、cloud agent への任意の委任に役立つスラッシュ コマンドを確認します。

ワークショップに集中できるよう、PR は 2 つ作成します。1 つ目は星評価、2 つ目は命令の更新、スキルの更新、QA プロファイル、テストを含むフィルタリングです。フィルタリングと品質改善の作業では 1 つの会話とブランチを使い、ツールを試しながら作業を進めます。

## 演習

| 演習 | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成する |
| [1. Copilot CLI をインストールする][ex1] | インストール | Copilot CLI をインストールして認証し、基本操作を確認する |
| [2. 星評価を追加する: 手早く成果を出す][ex2] | 最初の変更 | 既存の評価と null の場合の表示を追加し、最初の PR をマージする |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | Issue から機能を計画し、Autopilot で実装して Interactive でレビューする |
| [4. カスタム命令で Copilot をガイドする][ex4] | コンテキスト | 命令を確認、更新し、フィルタリングに適用する |
| [5. quality-checks スキルをカスタマイズして使う][ex5] | 繰り返し可能なチェック | 既存スキルを確認し、レポート形式を変更して実行する |
| [6. Playwright MCP で機能を検証する][ex6] | ブラウザーでの確認 | CLI で MCP を設定し、フィルタリングの動作を確認する |
| [7. QA エージェントを作成して使う][ex7] | 要件とカバレッジ | 専門プロファイルを作成して選択し、最終的な検証結果を集める |
| [8. 機能 PR を作成してマージする][ex8] | レビューとマージ | 変更全体をレビューして PR を作成し、Agent Merge を使う |
| [9. GitHub Copilot CLI のスラッシュ コマンド][ex9] | CLI 機能 | コンテキスト、モデル、共有、任意の委任を確認する |
| [10. 振り返りと次のステップ][ex10] | まとめ | ワークフロー、再利用可能なカスタマイズ、追加リソースを確認する |
| [オプション: Foundry を組み込む][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づくエージェントをデプロイして Web サイトに接続する |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと Codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランがありませんか。認証済みの学生は [GitHub Education][callout-student-plan-education] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用する agent、MCP、code review、Copilot CLI の機能が含まれているため、すべての harness を完了できます。

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## はじめる

**[演習 0: 前提条件から始める →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
