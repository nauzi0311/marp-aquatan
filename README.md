---
marp: true
paginate : true
theme : aquatan
math: mathjax
class: normal
---
<!--
_class: top
-->

# Marpの使い方
## t-tanimoto@そふらぼ


---

# メリットとデメリット

- メリット
  - 全てテキストで管理できる
  - VSCodeだけでできる
- デメリット
  - 柔軟なデザインができない


---
# 使い方

1. VS Codeの拡張機能でMarp for VS Codeを追加する
1. マークダウンファイル(.md)を作成する

<div style="font-size:100px;margin:15% auto">
以上
</div>


---
# 書き方

- マークダウンで資料が作れる
- 例えばこのページは下のように書ける．

```md

# 書き方

- マークダウンで資料が作れるよ
- 例えばこのページは下のように書ける．

```

---

# 見出し1

## 見出し2

### 見出し3

```md

# 見出し1

## 見出し2

### 見出し3

```

---

# 箇条書き

- 箇条書き
  - 1
  - 2
    - 3

<!-- 
箇条書きは - か *
-->
```md
- 箇条書き
  - 1
  - 2
    - 3

<!-- 
箇条書きは - か *
-->
```

---

# 箇条書き

1. 箇条書き
   1. 一つ目
   1. 二つ目
      1. 三つ目

<!-- 
箇条書きは 1. か 1)
-->
```md
1. 箇条書き
   1. 一つ目
   1. 二つ目
      1. 三つ目

<!-- 
箇条書きは 1. か 1)
-->
```

---

# 数式

- 数式：インライン形式
  - 式 $ax^2 + bx + c = 0$ の解の公式
- 数式：ブロック形式
$$ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

```md
- 数式：インライン形式
  - 式 $ax^2 + bx + c = 0$ の解の公式
- 数式：ブロック形式
$$ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$
```

---

# 画像
- 画像挿入
![width:200](./img/aquatan_gray.png)
> あくあたん

```md
# 書き方
- 画像挿入
![width:200](./img/aquatan_gray.png)
> あくあたん
```

---

# 画像
- 複数の画像挿入(横並び)
![width:200](./img/aquatan_gray.png) ![width:200](./img/aquatan_gray.png)
```md
- 複数の画像挿入(横並び)
![width:200](./img/aquatan_gray.png) ![width:200](./img/aquatan_gray.png)
```

---

# 画像
- 複数の画像挿入(縦並び)
![width:100](./img/aquatan_gray.png#center)
![width:100](./img/aquatan_gray.png#right)
```md
- 複数の画像挿入(横並び)
![width:100](./img/aquatan_gray.png#center)
![width:100](./img/aquatan_gray.png#right)
```

---

# 画像
- 画像加工
![width:150](./img/aquatan_gray.png)![width:150 sepia](./img/aquatan_gray.png) ![width:150 drop-shadow](./img/aquatan_gray.png) ![width:150 contrast](./img/aquatan_gray.png) ![width:150 invert](./img/aquatan_gray.png)

```md
- 画像加工
![width:150](./img/aquatan_gray.png)
![width:150 sepia](./img/aquatan_gray.png)
![width:150 drop-shadow](./img/aquatan_gray.png)
![width:150 contrast](./img/aquatan_gray.png)
![width:150 invert](./img/aquatan_gray.png)
```
他にもまだあるよ

---
# 表

| 左寄せ | 中央寄せ | 右寄せ |
| :-- | :-: | --: |
| 1 | 2 | 3 |

```md
| 左寄せ | 中央寄せ | 右寄せ |
| :-- | :-: | --: |
| 1 | 2 | 3 |
```

---

# ページスタイルの設定

- ファイルの一番初めに、ページのスタイルを設定できる。
```md
---

marp: true      <!--Marpの有効化-->
paginate : true <!--ページ番号あり-->
theme : aquatan <!--使用テーマ指定-->
math: mathjax   <!--数式のスタイル指定(katex or mathjax)-->
class: normal   <!--デフォルトのページのクラス指定-->

---
```

---

# ページスタイルの設定

| タグ名 | 説明 |
| :-: | :-- |
| marp | Marpの有効化 |
| paginate | ページ番号を付与 |
| header | ヘッダーを設定 |
| footer | フッターを設定 |
| class | ページのデフォルトのクラスを設定 |
| color | 文字色の設定 |

---
<!--
_color : red
_backgroundColor : rgba(150,150,150)
-->


# ページスタイルの設定

- **単一のページのみに別スタイルを適用することも可能**
```md
<!--
_color : red
_backgroundColor : rgba(150,150,150)
-->

<!--
 _ を先頭につければ指定しているページだけ反映される
ない場合はそれ以降のページすべてに反映される。
-->
# ページスタイルの設定

- **単一のページのみに別スタイルを適用することも可能**
```

---

<!--
_class : title_dark
_color : white
-->

# こういうページもできる

クラスごとに、テーマを設定することができる。

---

<!--
_class : title_dark
-->

# 応用

---

# 応用

- Marpは最終的に、HTMLの形式に変換される。
- このページは以下のように変換されると考えてよい。
```html
<section class="normal">
  <h1>応用</h1>
  <ul>
    <li>Marpは最終的に、HTMLの形式に変換される。</li>
    <li>このページは以下のように変換されると考えてよい。</li>
  </ul>
</section>
```
- なので、divタグとかを使えば割と好きなようにデザインできる。