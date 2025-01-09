# 要件定義2


## 1.プロダクト名  スケダチ

**一言サービスコンセプト**

能登半島住民用の身近な困りごとを誰かに助けてもらえるよう呼びかけができるアプリ


## 2.誰のどんな課題を解決するのか？
**誰:**
- 能登半島の住民

- 能登半島の不便さの解消の助け、

- 手伝うことで報酬ををいただきたい人


**どんな課題:**
- 能登半島特有のの不便さ
  
 例:町に動物病院がない、大きな病院がない、除雪や草刈り一人暮らしだと大変、重たい買い物、能登半島にないチェーン店のものがたべたい(マック、ケンタッキー等)、ゴミ出し、スマホのアプリの使い方を知りたい等
  
- 車があること前提の社会なのでないと、本当に不便。
  
- ご近所さんには頼みにくい(気を使う、人間関係や距離感が変わる)、近所に頼める人がいない、第三者のほうが頼みやすい。

- お金を払って手伝ってもらう方が気持ち的に楽(ライドシェアに関しては報酬を金銭にしないことで合法的になる = 白タク行為にならない)
  

## 3.なぜそれを解決したいのか？
- 能登半島特有の不便さを解消したい。
- (例:町に動物病院がない、大きな病院がない、除雪や草刈り一人暮らしだと大変、重たい買い物を頼みたい、田舎町にないチェーン店がたべたい(マック、ケンタッキー等)、ゴミ出し、スマホのアプリの使い方を知りたい、電車が通っていない、バスの便数が少なすぎる、バス停まで遠すぎる、まともな公共施設が車がないといけない。仕事が少ない、雪で身動きが取れなくなる、草刈りが大変)


- 能登半島地震後、住民の3割は能登地区から避難中で自治体がこれ以上人がいなくならない(避難中の人が戻ってきてもらえる)によう施策を考えている。その助けをしたい。
  
- 被災地の復興の助けをしたい。
  
- 私の出身地を住みやすい町にしたい。

- 地域の結びつきが強くなるといい。

- 他県からの移住者もお願い事を手伝っているうちに馴染みやすくなる。

- アプリの完成時期に住民が戻ってくる復興フェーズに入りそう。


## 4.どうやって解決するのか？

** お願い事をアプリに投稿することで助けてもらう人とマッチさせて助けてもらう。 **

1. ** お願い事をする側(投稿者側) **
    - 1.アプリにお願い事とその報酬を投稿
    - 2.応募者が多数の場合は選定
    - 3.チャットでやりとり
    - 4.お助けしてもらう。
    - 5.お助けごとをしてもらった後は報酬を支払う。

2. ** お願い事を受ける側(応募者側) **
    - 1.アプリに投稿された助けてほしいことに応募する。
    - 2.投稿者に選定される。
    - 3.チャットでやり取りする。
    - 4.お手伝いする。
    - 5.報酬をもらう。


## 5.機能要件

### ユーザー機能
    - 新規登録・ログイン・ログアウト
    - マイページ
        ユーザー情報編集(名前やアイコン画像)
        
    - 投稿機能(お願い事を報酬付きで投稿できる。)
    - お願い事をする側も身分証が必要、メールアドレス認証とSMS認証
    
    - チャット機能
   
#### 投稿画面
    - お願い事タイトル
    - お願い事の種類
    - 詳細情報
    - その希望日(希望期間)
    - 報酬種類(金額、物など)
    - 金額(2万円以下)、具体的な物(畑の野菜など)
    - 所要時間
    - 場所?

##### 閲覧画面
    - 投稿されたお願い事が一覧で表示されている。


### お願い事詳細画面
    - お願い事タイトル
    - お願い事の種類
    - 詳細情報
    - その希望日(希望期間)
    - 報酬種類(金額、物など)
    - 金額　具体的な物(畑の野菜など)
    - 所要時間
    - ざっくりした場所の地図?
    - 完了したお願い事は完了と出る。



## 6.非機能要件
- セキュリティ対策のため石川県に住所がないものは登録できない?
- シンプルなUI/UX
  

## 7.認証機能
メールアドレス認証 Laravelの機能であり。

sms認証↓

Twilio
https://www.twilio.com/ja-jp


## 使うAPI

Stripe API

Twilio API

## 参考情報

** url一覧
類似アプリ↓
エニタイムス

https://www.any-times.com/

タイミー

** 自家用旅客有償運送について

自家用有償旅客運送
https://kotsutorisetsu.com/20200815-01/

自家用有償旅客運送に関する法律
[04.pdf](https://github.com/user-attachments/files/18315536/04.pdf)

自家用有償旅客運送の申請
https://www.pref.nagano.lg.jp/kotsu/kurashi/kotsu/bus/jikayouyusho/20150401.html

### 自家用有償旅客運送とは
地域住民の生活の維持に不可欠な過疎地や福祉の輸送がバス・タクシー事業では十分提供されない場合に、自治体や住民、事業者など地域の関係者が合意すれば、国土交通大臣等の登録を受けた上で、市町村やNPO等が自家用車を使用して有償で運送できる制度です。

** ライドシェアに関しては報酬を畑の野菜など金銭に変えにくいものにすることで白タク行為に当たらなくなる。(自治体の承認や国土交通大臣等の登録なくても問題ない。)
*** また自治体の承認のもと、国土交通省の登録をドライバーが受けることができれば有償での送迎が可能。

