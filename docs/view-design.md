# VIEW DESIGN
見た目の設計

htmlを書きたくないので[ココ](https://www.tablesgenerator.com/text_tables)で作成

## Index Page

最初のページ

`https://karatube/?page={page}`

```
+--+---------------+--------------------+-------+--+
+--+---------------+--------------------+-------+--+
|  | KaraTube                                   |  |
+--+---------------+--------------------+-------+--+
|  | <seek path>                                |  |
+--+---------------+--------------------+-------+--+
|  | title         | tags               | star▼ |  |
+--+---------------+--------------------+-------+--+
|  | <video title> | [x|dog], [x|funny] | ☆☆★★★ |  |
+--+---------------+--------------------+-------+--+
|  | <video title> | [x|dog], [x|funny] | ☆☆★★★ |  |
+--+---------------+--------------------+-------+--+
|  | <video title> | [x|dog], [x|funny] | ☆☆★★★ |  |
+--+---------------+--------------------+-------+--+
|  |                   pager                    |  |
+--+---------------+--------------------+-------+--+
+--+---------------+--------------------+-------+--+
```

- ソート考えてない -> TODO
- seek path
  - タグをクリックしたらそのタグの動画の一覧になる
  - star▼ をクリックすると小窓から6種類のスターを選べて、クリックするとそのスターの動画一覧になる
  - 上の方法で絞り込んだ時、seek pathにどこから来たのかわかる表示が出る
     - 初期状態 -> `top`
     - "dog" の タグから来た -> `top > tags > dog`
     - "☆☆☆☆★" から来た -> `top > 4star `

## Video Page

個別の動画ページ

`https://karatube/videos/{id}?seekpath={seekpath}`


```
+--+--------------------------------+--+
+--+--------------------------------+--+
|  | video title                    |  |
+--+--------------------------------+--+
|  | <seek path>                    |  |
+--+--------------------------------+--+
|  | <video view>                   |  |
|  |                                |  |
|  |                                |  |
|  |                                |  |
|  |               (▷)              |  |
|  |                                |  |
|  |                                |  |
|  |                                |  |
+--+--------------------------------+--+
|  | (-)☆☆★★★(+)                    |  |
+--+--------------------------------+--+
|  | [x|dog], [x|funny], [add tag]  |  |
+--+--------------------------------+--+
+--+--------------------------------+--+
```

- スターは (-/+) して五段階くらい調節
- タグをつけたい
- タグをクリックしたらIndex Pageへ

## Tags Page
タグの一覧

- 雑にタグが並んでいる
  - 多い順にソート？
  - その動画の数とか出ると嬉しい？
- タグをクリックしたらIndex Pageでそのタグの一覧へ
