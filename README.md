# dr-stone-team for Claude Code

『Dr.STONE』の7人に着想を得た、非公式のClaude Code用Skillとサブエージェント設定です。原作の台詞や公式設定を再現するサービスではありません。会話の口調より、各人の異なる視点と仕事の進め方を重視します。

## 内容

- `.claude/skills/dr-stone-team/`：会話の切り替えとチーム分担を行うSkill
- `.claude/agents/dr-stone-*.md`：千空、クロム、ゲン、龍水、カセキ、スイカ、羽京の7人のサブエージェント

## 使い方

このリポジトリをClaude Codeで開けば、プロジェクト用のSkillとエージェントとして使えます。別のプロジェクトでも使う場合は、クローン後に以下をPowerShellで実行し、ユーザー用ディレクトリへコピーしてください。

```powershell
New-Item -ItemType Directory -Force "$HOME/.claude/skills", "$HOME/.claude/agents" | Out-Null
Copy-Item -LiteralPath ".claude/skills/dr-stone-team" -Destination "$HOME/.claude/skills/dr-stone-team" -Recurse -Force
Copy-Item -Path ".claude/agents/dr-stone-*.md" -Destination "$HOME/.claude/agents" -Force
```

Claude Codeで `/dr-stone-team` を呼び出し、続けて「ゲンに交代」「龍水と相談したい」「7人全員の意見を聞きたい」のように依頼します。エージェントだけを指名する場合は、Claude Codeの `@` メニューから人物を選べます。新しい `agents` ディレクトリを初めて作った場合、Claude Codeのセッションを再起動すると認識されます。

## 出典と扱い

人物設定の根拠と、原作・アニメ本編で未確認の表現の区別は [調査メモ](.claude/skills/dr-stone-team/references/voice-research.md) に記載しています。出典未確認の言い回しを原作の正確な引用とは表示しません。事実の確認、ユーザーの明示的な依頼、利用環境の権限がキャラクター演出より優先されます。
