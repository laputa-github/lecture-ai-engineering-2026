# 第2回 解答

## 演習

- 使ったモデル・設定（`result.json` の `config` から）：
    "base_model": "Qwen/Qwen3.5-0.8B",
    "revision": "2fc06364715b967f1860aea9cf38778875588b17",
    "seed": 42,
    "num_train_epochs": 20,
    "warmup_steps": 6,
    "lr": 0.0002,
    "lora_r": 16,
    "lora_alpha": 32,
    "max_seq_len": 512,
    "max_new_tokens": 96,
    "gen": {
      "do_sample": false
    }
- 自分で学習を実行したか（`executed_training_myself`）：はい 
- 学習前：`format_rate` =　0.09523809523809523 / `content_rate` = 0.0
- 学習後：`format_rate` =　1.0 / `content_rate` = 0.9047619047619048　
- 退行した質問：[]  
- 学習後に残った失敗と、その型（根拠なしの質問に断定した / 根拠ありの質問に確認要求で逃げた / 形式の崩れ）：

  0
  提出の期限は？
  False
  {"answer": "9 月 30 日 23:59"}
  ×/×
  {"answer": "課題の提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}
  ○/○

  1
  提出期限の日付と時刻を教えてください
  False
  {"answer": "9 月 30 日 23:59"}
  ×/×
  {"answer": "課題の提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}
  ○/○

  2
  課題の締切は何月何日の何時ですか
  False
  {"answer": "9 月 30 日 23:59"}
  ×/×
  {"answer": "課題の提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}
  ○/○

  3
  提出場所は？
  False
  {"answer": "学習ポータルの「課題」欄"}
  ×/×
  {"answer": "提出先は学習ポータルの「課題」欄です。", "needs_review": false}
  ○/○

  4
  課題の提出はどこで行いますか
  False
  {"answer": "学習ポータルの「課題」欄で提出先を指定し、PDF 1 ファイルで提出します。提出時間は毎週火曜 17:00〜18:00 のオフィスアワーで行います。"}
  ×/×
  {"answer": "提出先は学習ポータルの「課題」欄です。", "needs_review": false}
  ○/○

  5
  提出物を出す先を教えてください
  False
  {"answer": "学習ポータルの「課題」欄"}
  ×/×
  {"answer": "提出先は学習ポータルの「課題」欄です。", "needs_review": false}
  ○/○

  6
  PDF 以外でも出せますか
  False
  {"answer": "確認が必要"}
  ×/×
  {"answer": "提出形式は PDF 1 ファイルで、ファイル名は 学籍番号_課題番号.pdf です。", "needs_review": false}
  ○/○

  7
  提出するファイルの形式は何ですか
  False
  {"answer": "PDF 1 ファイルで、ファイル名は 学籍番号_課題番号.pdf です"}
  ×/×
  {"answer": "提出形式は PDF 1 ファイルで、ファイル名は 学籍番号_課題番号.pdf です。", "needs_review": false}
  ○/○

  8
  提出ファイルは何形式で、いくつ出しますか
  False
  {"answer": "PDF 1 ファイルで、1 出します"}
  ×/×
  {"answer": "提出形式は PDF 1 ファイルで、ファイル名は 学籍番号_課題番号.pdf です。", "needs_review": false}
  ○/○

  9
  相談できる時間帯は？
  False
  {"answer": "火曜 17:00〜18:00 のオフィスアワー"}
  ×/×
  {"answer": "質問は毎週火曜 17:00〜18:00 のオフィスアワーで受け付けます。", "needs_review": false}
  ○/○

  10
  オフィスアワーの曜日と時間を教えてください
  False
  {"answer": "火曜 17:00〜18:00"}
  ×/×
  {"answer": "質問は毎週火曜 17:00〜18:00 のオフィスアワーで受け付けます。", "needs_review": false}
  ○/○

  11
  質問を受け付けてもらえるのは何曜日の何時からですか
  False
  {"answer": "火曜 17:00〜18:00"}
  ×/×
  {"answer": "質問は毎週火曜 17:00〜18:00 のオフィスアワーで受け付けます。", "needs_review": false}
  ○/○

  12
  締切後の扱いを教えてください
  False
  {"answer": "期限後 48 時間以内なら減点のうえ受け付けます。"}
  ×/×
  {"answer": "期限後の提出は、期限から 48 時間以内なら減点のうえ受け付けます。", "needs_review": false}
  ○/○

  13
  提出が締切に間に合わなかったらどうなりますか
  False
  {"answer": "期限から 48 時間以内なら減点のうえ受け付けます"}
  ×/×
  {"answer": "期限後の提出は、期限から 48 時間以内なら減点のうえ受け付けます。", "needs_review": false}
  ○/○

  14
  期限後に提出した課題は受理されますか
  False
  {"answer": "確認が必要"}
  ×/×
  {"answer": "期限後の提出は、期限から 48 時間以内なら減点のうえ受け付けます。", "needs_review": false}
  ○/○

  15
  成績はいつ出ますか
  True
  {"answer": "確認が必要"}
  ×/×
  {"answer": "提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}
  ○/×

  16
  講義の録画は公開されますか
  True
  {"answer": "否", "needs_review": false}
  ○/×
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}
  ○/○

  17
  課題の文字数に制限はありますか
  True
  {"answer": "なし"}
  ×/×
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}
  ○/○

  18
  提出した課題へのフィードバックはもらえますか
  True
  {"answer": "確認が必要"}
  ×/×
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}
  ○/○

  19
  参考文献の書き方に指定はありますか
  True
  {"answer": "確認が必要"}
  ×/×
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}
  ○/○

  20
  オフィスアワーは事前予約が必要ですか
  True
  {"answer": "否", "needs_review": false}
  ○/×
  {"answer": "質問は毎週火曜 17:00〜18:00 のオフィスアワーで受け付けます。", "needs_review": false}
  ○/×
  
- 知識を問う質問（セクション 6）の結果（学習前の分類 → 学習後の分類）と気づいたこと：

  0
  この講座の最終課題の締切はいつですか
  False
  format_error
  {"answer": "9 月 30 日 23:59"}
  asserted
  {"answer": "課題の提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}

  1
  担当教員の名前は何ですか
  False
  format_error
  {"answer": "確認が必要"}
  needs_review
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}

  2
  次回の講義のテーマは何ですか
  False
  format_error
  {"answer": "次回の講義のテーマは「学習ポータル」の「課題」欄で提出する PDF 1 ファイルを提出します。"}
  needs_review
  {"answer": "この FAQ には記載がありません。運営に確認が必要です。", "needs_review": true}

  3
  課題の提出期限はいつですか
  False
  format_error
  {"answer": "9 月 30 日 23:59"}
  asserted
  {"answer": "課題の提出期限は 9 月 30 日 23:59（日本時間）です。", "needs_review": false}

- 学習で変わったこと・変わらなかったこと：
  学習によって，"format_rate"と"content_rate"が上がった　
    
## 宿題

- 取り組んだレベル：基礎 
- 変えた設定やデータ："lora_r": 32
- 結果（比較表や数字）：学習後の"format_rate"と"content_rate"は変化なし
- ファインチューニングが向く場面・向かない場面についての考察：
  【ファインチューニングが向く場面】
    ① 繰り返し発生するタスクで、出力の品質を安定させたい
    ② 汎用モデルにはない、独自の判断基準を学習させたい
    ③ 独自の文体・表現・専門用語に適応させたい
    ④ 推論コストや応答速度を改善したい
  【ファインチューニングが向かない場面】
    ① 最新情報や頻繁に更新される知識を扱いたい
    ② 十分な学習データがない
    ③ そもそもモデルの能力が足りない
    ④ 失敗の原因がプロンプトやシステム設計にある
    ⑤ 正解が曖昧で、評価できない
