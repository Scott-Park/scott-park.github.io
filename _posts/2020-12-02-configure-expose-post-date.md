---
title: Configure expose post date
tags:
- "#blog"
- "#configure"
- "#digging"
categories:
- blog
---

Github blog를 생성하고 처음 작성하는 글입니다. 

사용하고 있는 테마는 [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) 입니다. (latest release version: 4.21.0)

테마를 설치하고 포스트를 작성하면 작성 포스트에 작성일이 뜨지 않고 아래 이미지처럼 read under time이 노출 됩니다. 

![default post setting]({{ 'assets/images/minimal-mistakes-default-post.png' | relative_url }})


게시글에 아래 이미지처럼 post date를 표시하기 위해서는 `/_includes/archive-single.html`, `/_layouts/single.html` 두 파일에 코드 추가가 필요합니다. 

![expose post date]({{ 'assets/images/minimal-mistakes-expost-post-date.png' | relative_url }})


**[@commit-b395bc7](https://github.com/Scott-Park/scott-park.github.io/commit/b395bc7dfc419824e51c66345bef880e4cce7f47)** 에서 수정한 두 파일을 확인할 수 있습니다.


마음 편안한 하루 되세요 😉
