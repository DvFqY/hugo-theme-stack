+++
author = "Hugo Authors"
title = "建设中...."
date = "2023-1-6"
description = "建设中...."
categories = [
    "建设中....",
    "建设中...."
]
tags = [
    "建设中....",
    "建设中....",
    "建设中...."
]
image = "2.jpg"

{{ $vid := (.Get 0) }}
{{ $videopage := default 1 (.Get 1) }}
{{ $basicQuery := querify "page" $videopage "high_quality" 1 "as_wide" 1 }}
{{ $videoQuery := "" }}

{{ if strings.HasPrefix (lower $vid) "av" }}
    {{ $videoQuery = querify "aid" (strings.TrimPrefix "av" (lower $vid)) }}
{{ else if strings.HasPrefix (lower $vid) "bv" }}
    {{ $videoQuery = querify "bvid" $vid }}
{{ else }}

```html
    <p>Bilibili 视频av号或BV号错误！请检查视频av号或BV号是否正确</p>
    <p>当前视频av或BV号：{{ $vid }}，视频分P：{{ $videopage }}</p>
```

{{ end }}

<div class="video-wrapper">
    <iframe src="https://player.bilibili.com/player.html?{{ $basicQuery | safeURL }}&{{ $videoQuery | safeURL }}"
            scrolling="no"
            frameborder="no"
            framespacing="0"
            allowfullscreen="true"
    >
    </iframe>
</div>



+++

建设中....
