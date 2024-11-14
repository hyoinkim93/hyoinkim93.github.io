---
layout: post
comments: true
title: Postgresql id 자동생성
categories: [TIL]
---

이미 생성된 테이블에 id 자동생성 기능을 추가해보자.

```yaml
CREATE SEQUENCE id_seq;
ALTER TABLE tb_user_info ALTER COLUMN id SET DEFAULT nextval('id_seq');
```

동기화 진행안해서 여전히 중복된다함..
동기화 할 것
```yaml
SELECT setval('id_seq', COALESCE((SELECT MAX(id) FROM tb_user_info), 1));
```