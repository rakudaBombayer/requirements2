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
   - 例:交通の不便さ、除雪や草刈り一人暮らしだと大変、重たい買い物、ゴミ出し、スマホのアプリの使い方を知りたい等 
- ご近所さんには頼みにくい、近所に頼める人がいない。

## 3.なぜそれを解決したいのか？  
- 被災地の復興の助けをしたい。  
- 私の出身地を住みやすい町にしたい。
- 地域の結びつきの強化をしたい。

## 4.どうやって解決するのか？

### 依頼事をアプリに投稿することで助けてもらう人とマッチさせて助けてもらう。

   #### 依頼者(投稿者側)
    - 1.アプリに依頼とその報酬を投稿
    - 2.応募者がその投稿をみて応募
    - 3.チャット機能でより詳細な条件を教える、相手の条件を確認。
    - 4.応募者が多数の場合は選定 
    - 5.チャット機能で指定場所等を教えてる。
    - 6.応募者に指定場所まで来てもらう。
    - 7.依頼完了後は依頼完了ボタンを押す。
    - 8.依頼完了後、報酬を支払う。

   #### 受注者側(応募者側)
    - 1.依頼事一覧画面より気になる依頼事投稿をクリック。
    - 2.投稿一覧詳細画面に遷移し詳細を確認後応募。
    - 3.チャット機能でより詳細な条件を教えてもらう。
    - 4.投稿者に選定される。
    - 5.チャット機能で依頼場所等を教えてもらう。
    - 6.チャット機能で教えてもらった依頼場所まで移動
    - 7.依頼を手伝う。
    - 8.報酬をもらう。

## 5.機能要件

#### ユーザー画面
    - 新規登録・ログイン・ログアウト
    - マイページ
        ユーザー情報編集(名前やアイコン画像)
    - メールアドレス認証とSMS認証
     
#### 投稿画面
    - 依頼事タイトル
    - 依頼事の種類
    - 詳細情報
    - その希望日(希望期間)
    - 報酬種類(金額、物など)
    - 金額(2万円以下)、具体的な物(畑の野菜など)
    - 所要時間
    - 大まかな場所

##### 閲覧画面
    - 投稿された依頼が一覧で表示されている。

#### 依頼事詳細画面
    - 依頼事タイトル
    - 依頼事の種類
    - 詳細情報
    - 依頼事に関する画像
    - 希望日(希望期間)
    - 報酬種類(金額、物など)
    - 金額　具体的な物(畑の野菜など)
    - 所要時間
    - 大まかな場所
    - チャット画面に遷移ボタン
    - 依頼事完了ボタン。

#### チャット画面
    -チャット機能
    
    
## 6.非機能要件
- セキュリティ対策のため石川県に住所がある人しか登録できない。
- シンプルなUI/UX

## 7.認証機能
メールアドレス認証:Laravelの機能で実装。

sms認証:Twilioのapiを使って実装。

## 使うAPI
Stripe API
   - 決済機能のため
     
Twilio API
   - SMS認証機能のため
