# CSRF漏洞（Cross-Site Request Forgery）

​			什么是CSRF漏洞：是指利用受害者尚未失效的身份认证信息（ cookie、会话等信息），诱骗其点击恶意链接或者访问包含攻击代		码的页面，在受害人不知情的情况下以受害者的身份向服务器发送请求，从而完成非法操作（如转账、改密、信息修改等操作）。

## CSRF漏洞分析

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315100350334.png" alt="image-20230315100350334" style="zoom:50%;" />

   **CSRF和XSS的区别**

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315104138330.png" alt="image-20230315104138330" style="zoom:50%;" />

## CSRF漏洞挖掘

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315110009793.png" alt="image-20230315110009793" style="zoom:50%;" />	

## CSRF漏洞防御

​			如何解决漏洞防御呢？把不是自己网站发的请求拒绝掉就行

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315110833153.png" alt="image-20230315110833153" style="zoom:50%;" />

​			对referer进行判断，观察是否来自于本站。（但是可以通过BP进行修改包的来源）那我们怎么解决BP包的问题呢？

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315111119599.png" alt="image-20230315111119599" style="zoom:50%;" />

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315111252175.png" alt="image-20230315111252175" style="zoom:50%;" />

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315111334519.png" alt="image-20230315111334519" style="zoom:50%;" />

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20230315111350047.png" alt="image-20230315111350047" style="zoom:50%;" />

​				有没有更加安全的方式吗？二次验证（滑动解锁、验证码、二维码登录）