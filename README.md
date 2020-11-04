# メルマガ編集マニュアル

## 道具
- コードエディタ（普通のメモパッドでも編集できるがとてもやりづらい。[VS Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)がおすすめ）：コードの編集に使う
- ブラウザ（Chromeなど。普段使ってる物でOK）：見た目の確認に使う

**あるいは、任意のオンラインエディタを使用（例: [JSFiddle](https://jsfiddle.net)）**

## 編集手順

- 以下、[サンプルファイル](https://www.dropbox.com/s/5st63ekz7jmjqb0/mmHTML.html?dl=0)に従ってセクションごとに説明。セクションが見つからない場合は、ファイル内検索（Command+F）
- コードエディタでHTMLを開いて編集しながら、同時にブラウザでも同じHTMLを開いて、見た目を確認しながら進める
- **注意：タグ（`<p>`とか`<table>`）を１つ間違って消すだけでも表示が壊れるので、慣れるまでは慎重にいじる**

### 0. 広報担当者から当該号の掲載事項についての指示を受ける

### 1. セットアップ：JSFiddleを使う場合

- サンプルファイルをWordなどのテキストエディタで開き、全体をコピーする
- コピーしたコードをJSFiddleの「HTML」の欄に貼り付けた後、左上の「Run ▷」を押すと、「Result」の欄にブラウザ上での表示が現れる（下画像）

![](https://tva1.sinaimg.cn/large/0081Kckwgy1gkcw6udcl8j31100kl4cx.jpg)

### 2. 「Header」セクションでNoと日付を変更

```html
<!-- Header -->
<table border="0" cellpadding="5" cellspacing="0" style="margin-bottom: 1rem;">
  <tr>
    <td valign="top" align="center">
      <img src="https://i.ibb.co/QXfvHMt/logo-01-sp.jpg" alt="ロゴ" width="50" style="max-width:100%;">
    </td>
  </tr>
  <tr>
    <td valign="top" align="center">
      <h1 style="font-weight: bold; font-size: 1rem; margin: 0;">日本国際問題研究所</h1>
      <p style="font-weight: bold; font-size: .8rem; margin: 0;">JIIAメールマガジン　No.240 (2020年9月**日)</p>
    </td>
  </tr>
</table>
```

### 3. 「Featured」セクションでトップ記事のタイトル、画像、リンクを編集

- 記事へのリンクを`<a href="ヘッダーアイテムへのリンクURL">`のところにいれる（`<a>`はリンクを挿入するためのタグ）
- 画像URLを`<img src="...">`のところに入れる（`<img>`は画像を表示するためのタグ）
- タイトルを`<h2>...</h2>`のところに入れる
- 一番下の方の「国際問題月表」とあるところで、月表のタイトルとリンクを編集

＊リンク、画像、タイトルテキストの入れ方は、以下も全部同様

```html
<!-- Featured -->
<table width="600px" border="0" cellpadding="0" cellspacing="0" style="margin-bottom: 2rem;">
  <tr>
    <td valign="top" align="center">
      <a href="リンク">
        <img src="画像のURL" alt="logo" style="width: 100%;">
      </a>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h2>タイトル</h2>
    </td>
  </tr>
</table>
```

### 4. 「国際問題」セクションを編集

- 上の方で月、号、タイトルを編集
- `<tr class="item">`と書いてあるところが各論文です。それぞれの論文のリンク、タイトル、著者名（所属）を編集

```html
<!-- 国際問題 -->
<table class="sub_section" border="0" cellpadding="0" cellspacing="0">
  <tr class="ia_title">
    <td valign="top" align="left">
      <a href="https://www2.jiia.or.jp/BOOK/">
        <p style="font-size: .8rem; color: green; ">INTERNATIONAL AFFAIRS</p>
        <p style="font-size: 1.5rem; font-weight: bold;">国際問題</p>
        <p style="font-size: .8rem; color: green; ">
          <span style="font-size: 1.5rem;">XX</span>月 <!-- ココ -->
          <span style="background: green; color: white; padding: .1rem; margin: 0 .2rem;">2020年XX月号 No.XXX</span> <!-- ココ -->
          <span style="background: green; color: white; padding: .1rem;">電子版</span>
        </p>
      </a>
    </td>
  </tr>
  <tr class="ia_section_title">
    <td align="center"><!-- ココ -->
      焦点：XXX 
    </td>
  </tr>
  <tr class="item">
    <td>
      <a href="https://www2.jiia.or.jp/kokusaimondai_archive/2020/2020-07_001.pdf">
        <h4>◎巻頭エッセイ◎新型コロナウイルス後の海洋国際協力</h4>
        <p>浦辺 徹郎（国際資源開発研修センター顧問／東京大学名誉教授）</p>
      </a>
    </td>
  </tr>
  <tr class="item">
    <td>
      <a href="2本目のリンク">
        <h4>2本目のタイトル</h4>
        <p>2本目の著者（所属）</p>
      </a>
    </td>
  </tr>
  
  ...
  
  <tr class="ia_section_title">
    <td align="center">
      国際問題月表
    </td>
  </tr>
  <tr class="item">
    <td>
      <a href="https://www2.jiia.or.jp/kokusaimondai_archive/ebook/2020-07_m05.pdf">
        <h4>2020年5月1日ー31日</h4>
      </a>
    </td>
  </tr>
  
  ...
  
</table>
```

### 5. 各セクションを編集する

- サンプルファイルには「研究レポート」「研究報告」「Policy Brief」などのセクションがある。これは月ごとに変わるので、それに応じてセクションを足したり消したりする必要がある

- セクションを足す場合：以下のコードが１セクション分にあたるので、これを所定の位置に挿入した上で、セクションのタイトルと各アイテムの情報を編集

```html
<table class="sub_section">
  <tr class="sub_sec_title">
    <h3>セクションのタイトル</h3>
  </tr>
  <tr class="item">
    <td>
      <a href="１つめのアイテムへのリンク">
        <h4><span>1つめのアイテムの日付</span>1つめのアイテムのタイトル</h4>
        <p>1つめのアイテムの著者 (所属)</p>
      </a>
    </td>
  </tr>
  <tr class="item">
    <td>
      <a href="2つめのアイテムへのリンク">
        <h4><span>2つめのアイテムの日付</span>2つめのアイテムのタイトル</h4>
        <p>2つめのアイテムの著者 (所属)</p>
      </a>
    </td>
  </tr>
  
  ...アイテムの数に従って繰り返し
  
</table>
```

- セクションを消す場合：消したいセクションにあたるコードを削除。`<table>`タグはたくさんあるので、消したいセクションの始まり`<table class="sub_section">`に対応する終わりの`</table>`を間違えないように見つけて削除する

```html
<table class="sub_section">
  ...
</table>
```

### 6. テキスト変換

- HTMLが完成したら、全体をコピーし、[このサイト](https://templates.mailchimp.com/resources/html-to-text/)のテキストボックスに
ペースト

- 「convert」をクリック

- 下に出てきたテキストをコピーし、[このtxtファイル](https://www.dropbox.com/s/0qc38b3ephqgq4j/mmTEXT.txt?dl=0)の「Reply-To」の下に貼り付け

- ２行目の号を変更

### 7. 担当者宛にファイルを送る

- HTMLとテキストファイルの両方が完成したら、担当者宛にメールで送付する

以上
