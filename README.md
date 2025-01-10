# 要件定義

## 1.プロダクト名  スケダチ

**一言サービスコンセプト**

能登半島住民用の身近な困りごとを誰かに助けてもらえるよう呼びかけができるアプリ

## 2.誰のどんな課題を解決するのか？
**誰:**
- 能登半島の住民
- 手伝うことで報酬を得たい人

**どんな課題:**
- 能登半島特有のの不便さ
   - 例:交通の不便さ、除雪や草刈り一人暮らしだと大変、重たい買い物、ゴミ出し等 
- ご近所さんには頼みにくい、近所に頼める人がいない。

## 3.なぜそれを解決したいのか？  
- 被災地の復興の助けをしたい。  
- 私の出身地を住みやすい町にしたい。
- 地域の結びつきの強化をしたい。

## 4.どうやって解決するのか？

### 依頼事をアプリに投稿することで助けてもらう人とマッチさせて助けてもらう。

   #### 投稿者側(依頼者)
    - 1.アプリに依頼とその報酬を投稿
    - 2.応募者がその投稿をみて応募
    - 3.チャット機能でより詳細な条件を教える、応募者の条件を確認
    - 4.応募者が多数の場合は選定
    - 5.応募者を決定し、決定ボタンを押下(ステータスを募集中→応募者決定に変える)、募集を終了させる。
    - 6.チャット機能で指定場所等を教える。
    - 7.応募者に指定場所まで来てもらう。
    - 8.依頼者、応募者共に作業開始ボタン押下(ステータスを応募者決定→作業中に変わる)
    - 9.応募者に依頼事を手伝ってもらう。
    - 10.依頼完了後は依頼完了ボタンを押下(ステータスを作業中→完了に変える)
    - 11.依頼完了後、報酬を支払う。

   #### 応募者側(受注者)
    - 1.依頼事一覧画面より気になる依頼事投稿をクリック
    - 2.投稿一覧詳細画面に遷移し詳細を確認後、良ければ応募
    - 3.チャット機能でより詳細な条件を教えてもらう。
    - 4.投稿者に受注者として選定される。
    - 5.チャット機能で依頼場所等を教えてもらう。
    - 6.チャット機能で教えてもらった依頼場所まで移動
    - 7.依頼者、応募者共に作業開始ボタン押下(ステータスを応募者決定→作業中に変わる)
    - 8.依頼を手伝う。
    - 9.報酬をもらう。

## 5.機能要件

#### ユーザー画面
    - 新規登録・ログイン・ログアウト
    - ユーザー情報
      - 名前
      - アイコン画像
    - メールアドレス認証とSMS認証
     
#### 依頼事投稿画面
    - 依頼事タイトル
    - 依頼事の種類
    - 詳細情報
    - その希望日(希望期間)
    - 報酬種類(金銭、物品)
    - 所要時間
    - 大まかな場所

#### 依頼事一覧閲覧画面
    - 投稿された依頼が一覧で表示されている。
    - 閲覧詳細
       - 依頼事タイトル
       - 依頼事の種類
       - 依頼事に関する画像
       - 報酬種類(金額、物など)
       - 大まかな場所
       - 希望日(希望期間)
       - ステータス(募集中、依頼者決定、作業中、完了)

#### 依頼事詳細画面
    - 依頼事タイトル
    - 依頼事の種類
    - 詳細情報
    - 依頼事に関する画像
    - 希望日(希望期間)
    - 報酬種類(金額、物など)
    - 所要時間
    - 大まかな場所
    - チャット画面に遷移ボタン
    - ステータス(募集中、応募者決定、作業中、完了)
    - 投稿時のステータスは募集中
    - 投稿削除ボタン(ステータスが募集中時のみ表示)
    - 応募者決定ボタン(ステータスは募集中時、依頼者側のみ表示)
       ⚫︎ 押下 → ステータスが応募者決定に変わる。(募集を終了する)
          ⚪︎ キャンセルボタン(ステータスが応募者決定時に表示)
             ⚫︎ 押下　→ ステータスが募集中に変わる。 
       ⚪︎ 作業開始ボタン押下(ステータスを応募者決定時に表示)
          ⚫︎ 作業者、応募者共に押下　→ ステータスが作業中に変わる。
       ⚪︎ 完了ボタン(ステータスが作業中時、依頼者側のみ表示)
          ⚫︎ 押下　→ ステータスが完了に変わる。(依頼事が完了し、決済もしくは物品を渡す)
   
#### チャット画面
    - チャット機能
    
## 6.非機能要件
- 石川県に住所がある人しか登録できない(能登半島向けのアプリのためユーザーの身元を保証するしたい。)
- シンプルなUI/UX

## 7.認証機能
メールアドレス認証
   - Laravelの機能で実装。

sms認証
   - Twilioのapiを使って実装。

## 8.使うAPI
Stripe API
   - 決済機能のため
     
Twilio API
   - SMS認証機能のため
