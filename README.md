## 👋 hitoshinaya

個人開発者です。Webサービスとゲームを作って、自分で運営しています。
株の自動売買システムを実弾で本番稼働させながら、日々改善しています。

企画・実装・デプロイ・障害対応まで、ひとりで完結させるのが好きです。

Solo developer. I build and operate my own web services and games,
and run an automated stock trading system in live production.

I handle everything end to end — design, implementation, deployment, and incident response.

---

### 🎮 作っているもの / What I'm building

**[Rhythm Sentence](https://skillyoron.com/en)** — Learn Japanese to the Beat.
リズムに合わせて単語をタップし、正しい語順で日本語の文を組み立てる学習ゲーム。
JLPT N5〜N1対応 / 1プレイ60秒 / ワールドランキング / Stripe決済

A rhythm game for Japanese learners. Tap words to the beat and build sentences in the correct order.
Supports all JLPT levels. 60 seconds per play. Global leaderboard.

**[SkillYoron](https://skillyoron.com/ja)** — 資格学習をゲームに。
簿記・FP・宅建などビジネス系資格を、隙間時間に遊びながら学べるサービス。

Turning certification study into a game. Bookkeeping, finance, real estate and more.

> 上記2つは単一の Next.js コードベースで、ロケールごとに別プロダクトとして提供しています。
> Both products run on a single Next.js codebase, served per locale.

**株式自動売買システム / Automated stock trading system**（非公開 / private）
証券会社のリアルタイムAPI（REST + WebSocket PUSH）で50銘柄を5分足監視し、
シグナル検出から発注・約定監視・決済までを自動化。実弾で本番稼働中。

- ATRベースのポジションサイジング、レバレッジ上限、日次損失上限による多層のリスク管理
- プロセス異常終了時に建玉を強制決済する**デッドマンスイッチ**（監視を別プロセスに分離し、単一障害点を排除）
- Optuna による戦略パラメータの最適化

Monitors 50 symbols on 5-minute bars via a broker's realtime API, fully automating
signal detection, order placement, fill monitoring and position closing. Running live with real capital.
Includes a **dead man's switch** that force-closes positions if the engine dies —
the watchdog runs in a separate process to avoid a single point of failure.

---

### 🛠 Tech Stack

**Web** — TypeScript, React, Next.js (App Router), Tailwind CSS
**Backend / DB** — Supabase (Auth / PostgreSQL / RLS), PostgreSQL, SQLite
**決済 / Payments** — Stripe
**Infra** — Vercel, 独自ドメイン運用 / custom domain
**Trading** — Python, asyncio, aiohttp, WebSocket, pandas, NumPy, Parquet, Optuna
**Game** — Unity, C#
**Test / Tooling** — pytest, pre-commit hooks, Git, VS Code, Claude Code

---

### 🔐 コードについて / About my code

受託案件のコードは守秘義務のため公開していません。
自社プロダクトも本番稼働中のため、リポジトリは非公開です。

実際に動いているものは上記のリンクからご覧いただけます。

Client work is under NDA, and my own products are in live production,
so those repositories are private. You can try the running products from the links above.

---

📫 info@skillyoron.com
