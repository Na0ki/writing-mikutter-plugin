---
layout: post
title:  "プログラムからツイートする"
date:   2016-05-11 00:00:00 +0900
categories:
- bot
---

自動ツイートに限らず、プログラムで処理した結果を直接投稿したい場合、次のようなコードでできます。

```ruby
world, = Plugin.filtering(:world_current, nil)
compose(world, message: "投稿したい内容")
```

これで、「投稿したい内容」とツイートできます。

## 実用例

次のコードは、毎日0時になったら自動的に「よるほー」とツイートする例です。24行目で`compose`を使用しています。

<script src="https://gist.github.com/toshia/1306093.js"></script>

## 参考
- [compose(twitter) Spell]({{ site.baseurl }}{% post_url 2017-11-28-spell %}#compose-twitter)
- <a href="http://mikutter.hachune.net/rdoc/MikuTwitter/APIShortcuts.html#method-i-post">MikuTwitter::APIShortcuts#update</a>
