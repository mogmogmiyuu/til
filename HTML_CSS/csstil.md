## overflowプロパティ
- 領域内に収まりきらないものをどう表示するかを指定できる

|option|detail|
|:--|:--|
|visible|領域をはみ出して表示する|
|hidden|はみ出た部分を表示しない|
|scroll|スクロールで表示する|
|auto|自動|

## positionプロパティ
- `absolute`と`relative`がある
### absolute
- 絶対の位置関係
  - 親ボックスが基準、親から数えた指定位置に描画される
### relative
- 相対の位置関係
  - absoluteで描画されるはずだった場所が基準、そこから数えた指定位置に描画される
  
## センタリング
😫ボタンには ` text-align:center; ` や ` margin:0 auto; ` によるセンタリングが効かない  
- 横方向のセンタリング  
    - ブロック要素のセンタリング  
    ` margin: 0 auto; `  
    - テキストのセンタリング  
    ` text-align:center; `  
- aタグの中の文字を上下左右中心に配置
  ```css
  text-align: center;
  line-height: 50px;
  ```
### flexbox
- 中の要素をいい感じに均等に配列してくれるプロパティ  
` display: flex; `

### before/after
- その要素の前、後にCSSを適応してくださいという命令
  - リストの前に共通してアイコンをつけるとかそういう使い方ができる

## SCSS
### &
- &を使うことでcssのクラス名を省略？したり使い所の制限？をしてわかりやすくできる
#### &.
```css
.hode_parent_class {
~~~~~
~~~~~
  &.hoge_child_class {
  ~~~~~
  ~~~~~
  }
}
```
- 親クラス内にある子クラスにだけcssを適応させられる

#### 省略
`class="hoge"`　と `class="hoge_piyo` があるとき
```css
.hoge {
~~~~~
~~~~~
  &_piyo {
  ~~~~~
  ~~~~~
  }
}
```
とすることでつなげて？かける

