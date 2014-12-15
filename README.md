Ele-Fee
=======

This project could work by doing this:
Altitude-master play a role as a Altitude sensor. It works in the platform of Android(actually, it is a android APK), first compiling by eclipse ADT. This program mobilize cellphone's Air pressure sensor（yes, not Gravity sensor）every 1 sec, by analysing Air-pressure's changings, it can get the number of floors and remember the time in such a format "2014-12-10-13-30-05", and write these information into file.txt.

elefee, acts as the network server. Coding by Java and compiling in eclipse, it can get the Altitude-master's file.txt and anylysing it. most importantly, it is a The Card Reader, users enter elevator by swipe the ID card(each card has their Identity information. Now the server remember this and doing analysing, gathering each user's records of elevator. Finally get a *.sql file, in order to push into MYSQL Cloud database for User's Searching on the Internet.

myele, acts on the Internet, for Searching how much they will pay, and show user records. It consists of Action(Java) and Html/Css/JS/Bootstrap, of course.

试想一下，小区用户凭刷卡走入电梯，服务器自动记录每个用户使用电梯记录并以此分析每年/月的使用费用，实现公平公摊，网页查询费用并可定时推送邮箱，是多么美妙的事情啊（yy中==）。
