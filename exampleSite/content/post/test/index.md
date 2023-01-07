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



```html
    <p>Bilibili 视频av号或BV号错误！请检查视频av号或BV号是否正确</p>
    <p>当前视频av或BV号：{{ $vid }}，视频分P：{{ $videopage }}</p>
```



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
