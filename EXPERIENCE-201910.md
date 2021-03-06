# CMS開発のふり返り

![./memory-small.png](./memory-small.png)

## タイトル

2019年10月のCMS開発ふり返りページです。
ところどころ柔らかい表現(？)に変えて、ふり返ります。

## 目次

* [どうやって始まった](#経緯)
* [とりあえず思い出に残る１枚](#画面キャプチャ)
* [どんな機能を開発したか](#機能)
* [どのように進めたか](#案件の流れ)
* [どの技術を使って開発したか](#利用技術)
* [この開発に点数をつけるとしたら](#総評)

## 経緯

* 同じお客様から違う仕事をお引き受けしていたが状況が変わった。
* そして代わってこの仕事（CMS開発）の要望を頂いた。
* お客様は、開発歴30年・社会人歴50年くらいの、開発色も強いベテランでした。
* お客様は、最初のお打ち合わせの際に、NoSQL(Firestore)を使いたいと要望を頂く。
* 当初希望納期が9月上旬(リリースまで１週間くらいしかない・・)雰囲気でした。
* 明確な期日には一切触れずに、緊張しつつ、自らを試すことを決意し開発をスタートしました。（^^;

## 画面キャプチャ

* こういう雰囲気のCMSを開発しました。

![./memory-small.png](./memory-small.png)

## 機能

```
ユーザ管理
  新規ユーザ登録
  ユーザ編集
  ユーザ退会
  ユーザ編集(割当済ワーカー確認)
  ユーザ編集(保存確認)
リソース管理
  新規リソース登録
  リソース編集(一覧へ戻る)
  一括取込
  一括割当(上書きする・しない)
```

## 体制

* お客様と2名の協力スタッフ(秘書の方が1名、マネジメントなど担当されるスタッフの方が1名)
* 開発側は自分（藤川）１名

## 納品形式

お客様のアカウントのFirebaseプロジェクトに納品

## 案件の流れ

* 以下の流れで約1ヶ月です。

```
8/31 会議スペースでお打ち合わせ・簡単なご用件のヒアリング
9/1 LINE上でCMSの開発依頼を受領
9/2 LINEで利用イメージ（シナリオ）と公開方法・認証周りの提案を送付して了承をえる。
9/9 LINEで一通りの機能実装を完了。課題等のまとめを送付
9/11 Whereby（Web会議）にて状況報告を実施・指摘・要望を受領
9/13 firebaseプロジェクト(浦本様アカウント)のセットアップを代行
9/13 要望に対応 ユーザ管理機能修正。idの発番体系・入力項目の並び順を修正
9/13 要望に対応 リソース管理機能修正。 １リソースを複数のユーザで共有できるように修正
9/25 要望に対応 ユーザ管理機能修正。ユーザ情報の入力項目の一部を削除
10/1 タイトル等の軽微な修正
10/12 検収・請求
```

## 利用技術

* ホスティング

```
Firebase Hosting
```

* データベース

```
Firebase Firestore
```

* 開発環境
  - 開発言語
    * Typescipt
  - ライブラリ
    * firebase 6.5.0
    * firebaseui: 4.2.0
    * vue: 2.5.17
    * vuikit: 0.8.1
    * webpack: 4.39.3

## 総評

* 点数

```
70点
```

* 理由

```
個人事業主として、お客様を交えて最後まで気持ちよく終えることが出来て、まずは安心。

LINEで一通りの機能実装を完了を報告した際
「相当に詰まっており、久しぶりに、まともな技術者と出会った気がします」とコメントを頂いた。
技術者としてのご経験が豊富なお客様だったので、正直に嬉しい気持ちでした。

一方で、後半に上がった指摘、IDのルール、バリデーション、入力項目の並びなど予測可能な課題について
後から修正が入る場面があり、次回は前もって認識を合わせたい。（短期間だったとは言え反省）
Firebaseの実績がまた一つ仕上がってよかった。別なお客様の案件でも [利用技術](#利用技術)と同様のスキルセットは応用する見込みがあり、個人の総評としては及第点です。
```
