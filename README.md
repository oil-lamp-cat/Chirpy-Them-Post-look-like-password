# Chirpy-Them-Post-password
This isn't intended for actual security or encryption; it's only meant to give the appearance that a password is needed.

## 한글

이건 chirpy 테마를 사용하다가 포스트에 비밀번호를 걸어보고 싶다는 간단한 생각으로 변경한 코드일 뿐이지 실질적인 보안, 암호화 기능은 없으니 그리 알아주시면 감사하겠습니다!

![password protection](https://github.com/user-attachments/assets/9f3bb31f-0bae-4777-ad89-f7b2eddb757a)

포스트를 올릴 때에 

```md
---
title: "[HTB] Editor (Easy)"
date: 2025-09-20 15:01:15 +09:00
categories: [hacking, saturnx operators]
tags: [Hack The Box]
pin: true
password: "0000"
---
```

위와 같이 여러 태그를 달게 되는데 이 때에 `password`라는 태그를 달아 `md`파일을 작성하게 되면 그 비밀번호를 넣을 때에만 페이지가 보이게 만들 수 있다.

이를 위해 기본적으로 `chirpy` 테마를 사용하고 있어야 하며 `post.html`과 `password-protection.js`를 넣어줘야 한다.

- post.html은 `/_layouts/post.html`을 덮어씌우면 되고
- js는 `/assets/js/password-protection.js`를 만들면 된다.

참고로 사진과 같은 디자인은 난 전혀 할줄 모르기에 claude를 이용했고 필요시 바꿔서 사용하면 된다.

다시 말하지만 이것은 보안기능이나 암호화 등이 없이 그저 보는 사람에게 저렇게 뜨기만 할 뿐 실제론 개발자도구(F12)로 뜯어보거나 github에 들어가 보면 보인다.

하지만 여기저기 찾아봐도 이런 기능을 구현해 놓은 사람이 없어 직접 구현했다.

## English

This is just a simple code modification I made because I wanted to try adding a password to a post while using the Chirpy theme. Please be aware that it has **no actual security or encryption features**.

When you upload a post, you add various tags like this:

```md
---
title: "[HTB] Editor (Easy)"
date: 2025-09-20 15:01:15 +09:00
categories: [hacking, saturnx operators]
tags: [Hack The Box]
pin: true
password: "0000"
---
```

If you add the `password` tag when writing the `md` file, you can make the page visible only when that password is entered.

To do this, you must be using the `chirpy` theme and need to add `post.html` and `password-protection.js`.

  - Overwrite `/_layouts/post.html` with the new `post.html`.
  - Create `/assets/js/password-protection.js` for the JS file.

For reference, I have no design skills, so I used Claude to create the design shown in the picture. Feel free to change it as needed.

To reiterate, this provides **no actual security or encryption**. It only appears that way to the viewer. The content can be easily seen by using developer tools (F12) or by viewing the files on GitHub.

However, I couldn't find anyone who had implemented a feature like this, so I decided to create it myself.