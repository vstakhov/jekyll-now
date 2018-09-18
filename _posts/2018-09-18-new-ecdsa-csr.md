---
layout: post
title: "Create ECDSA key + csr"
---

~~~command
openssl ecparam -genkey -name prime256v1 -out ssl.key
openssl req -new -key ssl.key -text -sha256 -out ssl.req
~~~
