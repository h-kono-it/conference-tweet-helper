# Conference Tweet Helper

カンファレンスでのツイートを補助するWebアプリ。

https://h-kono-it.github.io/conference-tweet-helper/

## カンファレンスの追加方法

`index.html` 内の `<script id="conference-config" type="application/json">` を編集する。

```json
{
  "キー名": {
    "name": "カンファレンス表示名",
    "trackRows": [
      [
        { "name": "トラック名", "hashtags": ["ハッシュタグ1", "ハッシュタグ2"] }
      ]
    ]
  }
}
```

### trackRows の構成

`trackRows` は「行の配列」で、各行に含めたいトラックを並べる。行内のトラック数が列数になる。

```json
"trackRows": [
  [
    { "name": "メイン", "hashtags": ["kinoko2026"] }
  ],
  [
    { "name": "Track A", "hashtags": ["kinoko2026", "a"] },
    { "name": "Track B", "hashtags": ["kinoko2026", "b"] },
    { "name": "Track C", "hashtags": ["kinoko2026", "c"] }
  ]
]
```

上記の場合、1段目にメインが1列、2段目にA・B・Cが3列で表示される。

### 複数カンファレンスの例

```json
{
  "kinoko2026": {
    "name": "きのこカンファレンス 2026",
    "trackRows": [ ... ]
  },
  "hoge2026": {
    "name": "HogeConf 2026",
    "trackRows": [ ... ]
  }
}
```
