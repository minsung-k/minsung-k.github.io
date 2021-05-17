---
title: 'Github 사용시 이슈'
date: 2021-05-17
permalink: /posts/2021/05/blog-post-1/
tags:
  - Github
  - github.io
  - 홈페이지
---


## Github Error
<br>
이 페이지에서는 내가 github을 사용하다 발생한 문제를 적고 누군가 여기서 해결책을 찾길 바란다.

### Unable to build page. Please try again later.


<figure>
 <img src ='https://i.imgur.com/VJDFBVg.png', width='400'/>
</figure>

블로그를 포스팅 했는데 잘 안되면 왜 안되는지에 대한 이유를 적어준다 (위)
하지만 처음으로 이런 메세지가 왔다.

  **Unable to build page. Please try again later.**

이유를 알려주지 않아 뭐지? 잘 몰랐었는데,,
역시 구글에는 이미 나와 같은 일을 겪은 사람이 있었다.

[이곳](https://sunyrora.github.io/blog.test/GitHub-Pages/)을 참조했다. 


이분은 잘 해결되지 않아 더 많은 방법을 시도했는데, 난 첫번째 방법만 써서 문제를 해결했다.


  git config --global user.name [사용자이름]
  git config --global user.email [이메일 주소]

안되면 윗 글에 들어가서 여러 방법을 다양하게 시도해 보시길...
