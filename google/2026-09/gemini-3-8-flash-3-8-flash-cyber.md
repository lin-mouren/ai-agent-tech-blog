---
title: "Gemini 3.8 Flash と 3.8 Flash Cyber を発表"
vendor: google
source_url: https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/
published_at: 2026-09-04T02:00:03.528Z
crawled_at: 2026-09-07T02:00:26.880Z
word_count: 467
reading_time_minutes: 3
tags: [gemini, multimodal, safety, agents, evaluation, api, product, enterprise, coding]
---

# Gemini 3.8 Flash と 3.8 Flash Cyber を発表

2026年 9月 3日

- [x.com](https://twitter.com/intent/tweet?text=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8%20%40google&url=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8&u=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/&title=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8)
- [メール](mailto:?subject=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8&body=%E3%81%93%E3%81%AE%E8%A8%98%E4%BA%8B%E3%82%92%20Google%20Japan%20Blog%20%E3%81%A7%E8%AA%AD%E3%82%80:%0A%0AGemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8%0A%0Ahttps://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- リンクをコピー


* * *

Tulsee Doshi

Senior Director, Product Management

Raluca Ada Popa

Gemini Security Lead, Google DeepMind

Share


- [x.com](https://twitter.com/intent/tweet?text=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8%20%40google&url=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- [Facebook](https://www.facebook.com/sharer/sharer.php?caption=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8&u=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/&title=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8)
- [メール](mailto:?subject=Gemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8&body=%E3%81%93%E3%81%AE%E8%A8%98%E4%BA%8B%E3%82%92%20Google%20Japan%20Blog%20%E3%81%A7%E8%AA%AD%E3%82%80:%0A%0AGemini%203.8%20Flash%20%E3%81%A8%203.8%20Flash%20Cyber%20%E3%82%92%E7%99%BA%E8%A1%A8%0A%0Ahttps://blog.google/intl/ja-jp/company-news/technology/gemini-38-flash-38-flash-cyber/)
- リンクをコピー


* * *



Google は、これまでのモデルの中で最も優れた推論およびコーディング性能を誇る Gemini 3.8 を発表します。3 週間前に発表した [3.7](https://blog.google/intl/ja-jp/company-news/technology/gemini-37-flash/) と同等のスピードと低コストを維持しながら、Gemini 3.8 では以下の 2 モデルを提供します。

- **Gemini 3.8 Flash**：ソフトウェア エンジニアリング、エージェント タスク、そして専門領域における重要な多段階推論において、3.7 Flash から進化した最も高性能な主力モデルです。3.7 Flash と同じ初期提供価格¹ である入力 100 万トークンあたり 0.75 ドル、出力 100 万トークンあたり 3.75 ドル でご利用いただけます。
- **Gemini 3.8 Flash Cyber**：脆弱性検出と自動パッチ適用においてフロンティア モデルクラスの性能を発揮する、最も高機能なサイバーセキュリティ モデルです。新しい [Fairwind Program](https://deepmind.google/fairwind-program/) を通じて、パートナーの皆さまに提供されます。

本日公開した両モデル は、異なる運用環境に合わせて最適化されているものの、同一の基盤知能を備えています。さらに、基盤モデルを再帰的に評価・改善するように設計された、長時間実行型のエージェント ループによってその性能がさらに加速されています。この共通コアにおけるコーディングおよび推論能力の大幅な向上は、高い要求が課されるサイバーセキュリティ領域での厳格なトレーニングをはじめとする、数々の過程によって実現しました。

**Gemini 3.8 Flash：長期的なコーディングと自律型エージェントのために構築**

Gemini 3.8 Flash は、3.7 Flash から大幅な進化を遂げており、より高コストなフロンティア モデルの性能に迫る実力を発揮します。



長期間にわたるソフトウェア エンジニアリング能力を評価するベンチマーク DeepSWE v1.1（Long-Horizon Software Engineering）において、3.8 Flash は、複雑なエンジニアリング課題を自律的かつエンドツーエンドで解決する能力で、より大規模なフロンティア モデルの多くを上回りながら、そのコストはほんのわずかに抑えられています。

さらに、3.8 Flash は、専門知識を要する領域において、企業の重要なオペレーションに求められる高い信頼性を備えています。高度な分析やレポート作成が必要とされる定量的・専門的分野において、3.8 Flash は [Vals Finance Agent V2](https://www.vals.ai/benchmarks/fabv2) や Harvey 社の [Legal Agent Benchmark](https://www.vals.ai/benchmarks/hlab) などのベンチマークで、3.7 Flash や他のフロンティア モデルを上回るパフォーマンスを発揮します。また、HLE-Verified でも 54.9% を記録し、STEM、人文学、専門分野にまたがる複雑な多段階推論に対応できる能力を実証しています。

こうした性能向上は、「3.8 Flash がより熱心に処理に取り組む」という設計思想に基づいています。複雑なタスクにおいて、このモデルはより高い勤勉性を発揮し、追加の推論ステップを実行しながら、ツールを繰り返し呼び出します。特にエフォート レベル（思考の深さの度合い）を高く設定した場合には、パフォーマンスを最大限に引き出すために、より多くのトークンを消費することがあります。

計算効率が最優先される用途では、エフォート レベルを低く設定してトークンのオーバーヘッドを最小限に抑えることもできますし、効率重視のワークロード向けに引き続きフルサポートされている Gemini 3.7 Flash を活用し続けることも可能です。

**Gemini 3.8 Flash Cyber：専門性の高いサイバーセキュリティ性能**

Fairwind Program を通じて信頼できるパートナーの皆さまに提供される Gemini 3.8 Flash Cyber は、迅速な反復作業を可能にする Flash ならではのスピードと低コストを備え、今日の複雑なサイバーセキュリティ環境において優位性をもたらします。

自律的な脆弱性の発見

脆弱性発見の業界標準ベンチマークである「CyberGym」において、Gemini 3.8 Flash Cyber は自律的な脆弱性検出でフロンティア モデル級の性能を実証しました。3.5 Flash Cyber だけでなく、大幅に規模の大きいフロンティア モデルをも凌駕しています。



CyberGym のような C/C++ コードベースにとどまらない、現実世界の防御ニーズをより的確に捉えるため、20 種類ものプログラミング言語にまたがる複雑なコードベースから広範な脆弱性を検出する、包括的な社内ベンチマークでも Gemini 3.8 Flash Cyber を評価しました。この評価において、本モデルは従来のモデルから 70% を超える成功率を達成しています。



自動パッチ適用

Gemini 3.8 Flash Cyber の開発にあたり、Google は攻撃者に対して優位に立てる専門的な能力を提供することに注力しました。つまり、最初から脆弱性の修正に投資し、悪用などの攻撃的な機能よりも修正を優先しました。

パッチ適用能力を評価する難関の外部ベンチマークである Collinear 社の [CWE-Bench](https://cwe-bench.com/#leaderboard) において、Gemini 3.8 Flash Cyber はパレート境界に位置しています。主要なフロンティア モデルの pass@1 が 47.8% であるのに対し、Gemini 3.8 Flash Cyber は 47.2% を記録しながら、大幅に低いコストで提供されています。



実世界での成果：Google のコードの安全性を強化

Google では、社内全体のコードを保護するために、すでに Gemini 3.8 Flash Cyber を活用しています。例えば、以下のような成果が得られています。

- Chrome セキュリティ チームの検証では、3.8 Flash Cyber は、より大規模な最高峰の商用モデルと比べて、Chrome の脆弱性に対して 2.6 倍もの正確なパッチを生成しました。
- Wiz の社内ペネトレーション テスト ベンチマークにおいて、Gemini 3.8 Flash Cyber は、他の主要なフロンティア モデルと比較して 2.3 〜 5.2 倍低いコストでありながら、再現率が +7.5 〜 9.7% 向上したことが確認されました。
- Google Cloud の脆弱性調査チーム（Cloud Vulnerability Research team）は、通常であれば調査と発見に数か月を要するような重大な基盤の脆弱性を、3.8 Flash Cyber を活用して 2 時間足らずで発見しました。

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_3.8_Flash_Cyber_Launch_32Mb.mp4) and watch it with your favorite video player!

安全性を最優先した設計

3.8 Flash は、Google の [Frontier Safety Framework](https://deepmind.google/blog/strengthening-our-frontier-safety-framework/) に基づき、有益なユースケースを可能にしながら、化学・生物・放射線・核（CBRN）兵器およびサイバー攻撃への悪用を防ぐセーフガードを備えています。一方、3.8 Flash Cyber は、サイバーセキュリティ用途に対してより柔軟な緩和策を備えているため、より包括的なサイバー機能を必要とする信頼できる皆さまにのみ提供されます。

また、Gemini 3.8 モデルは、Gray Swan による測定においてプロンプト インジェクション耐性が飛躍的に向上しており、プロンプト インジェクションに関連する悪意ある攻撃から Gemini ユーザーをしっかりと保護します。



Gemini 3.8 Flash と Cyber：本日より提供開始

- 開発者の皆さま： [Google Antigravity](https://antigravity.google/) で 3.8 Flash を使った開発やエージェント ファーストのワークフローを体験していただけます。また、本日より [Google AI Studio](https://aistudio.google.com/prompts/new_chat?model=gemini-3.8-flash) や [Android Studio](https://developer.android.com/studio) を通じた Gemini API での開発、 [Stitch](http://stitch.withgoogle.com/) での UI 生成も可能です。まずは [開発者向けドキュメント](https://ai.google.dev/gemini-api/docs/latest-model) をご確認ください。
- 法人のお客様： [Gemini Enterprise](https://console.cloud.google.com/agent-platform/studio/multimodal?mode=prompt&model=gemini-3.8-flash) で 3.8 Flash をご利用いただけます。
- 一般ユーザーの皆さま：Google AI Pro および Ultra の登録ユーザーは、 [Gemini アプリ](http://gemini.google.com/)、 [Google 検索の AI モード](http://google.com/ai)、および [Google スプレッドシート](http://sheets.new/) の Gemini で 3.8 Flash をご利用いただけます。
- サイバーセキュリティ：新しい [Fairwind Program](https://blog.google/innovation-and-ai/technology/safety-security/fairwind-program) を通じて、信頼できる政府機関、重要インフラ事業者、およびソフトウェア メンテナーの皆さまに、Gemini 3.8 Flash Cyber への優先アクセスを提供します。詳細は [こちら](https://deepmind.google/fairwind-program/) をご確認ください。

関連タグ:

## 関連記事

[\\
\\
AI\\
**Create with AI: 東京藝術大学と AI を活用した創作活動を支援**\\
\\
By\\
\\
\\
奥山 真司](https://blog.google/intl/ja-jp/company-news/outreach-initiatives/create-with-ai-ai/)

[AI\\
**Gemini 3.7 Flash を発表** \\
\\
コーディングおよびエージェント向けの最も高性能な主力モデル\\
\\
By\\
\\
\\
Tulsee Doshi](https://blog.google/intl/ja-jp/company-news/technology/gemini-37-flash/)

[\\
\\
AI\\
**Google、日本のオープンソース半導体設計エコシステム確立に向けて OpenSUSI に特別賛助会員として参加**\\
\\
By\\
\\
\\
奥山 真司](https://blog.google/intl/ja-jp/feed/google-opensusi/)

[AI\\
**Gemini Robotics 2 が実現するロボットの全身知能** \\
\\
足から指先まで — ロボットに高度な全身制御、器用さ、そしてチームワークを学習させ、幅広い複雑なタスクの完遂を目指して何十年もの間、私たちはロボットが日常生活に自然に溶け込み、私たちの手助けをしてくれる未来を夢見てきました。そして今、そのビジョンは大きく前進しようとしています。多くのロボットは、限定的で反復的なタスクのために事前にプログ…\\
\\
By\\
\\
\\
Carolina Parada](https://blog.google/intl/ja-jp/company-news/technology/gemini-robotics-2/)

[\\
\\
AI\\
**Gemini 3.5 Flash Cyber を発表**\\
\\
By\\
\\
\\
Raluca Ada Popa and Four Flynn](https://blog.google/intl/ja-jp/company-news/technology/gemini-35-flash-cyber/)

[\\
\\
Gemini models\\
**Gemini Omni を発表**\\
\\
By\\
\\
\\
Koray Kavukcuoglu](https://blog.google/intl/ja-jp/company-news/technology/gemini-omni/)