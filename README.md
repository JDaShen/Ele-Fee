Ele-Fee
=======

某小区出现了这样的困扰：住户们对目前缴纳电梯费的机制不满意，认为不公平； –目前的机制：以楼层为基准； –不公平之处：有人用的很频繁，有人用的少，缴费额与实际使用情况不对应。 设计一种机制，可以采用软件和硬件相结合的策略，解决上述问题： –实时采集电梯使用数据（刷卡？摄像头？）； –对收集的数据进行周期性统计处理； –根据统计结果进行费用分摊； –产生费用报表； –收费策略； 该软件遵循C/S+B/S混合结构，C/S客户端部署于电梯中进行数据采集，B/S客户端由用户查询数据，服务器端进行数据处理和分析。若需要使用到硬件设备，通过模拟硬件接口完成功能。


This project could work by doing this:
Altitude-master play a role as a Altitude sensor. It works in the platform of Android(actually, it is a android APK), first compiling by eclipse ADT. This program mobilize cellphone's Air pressure sensor（yes, not Gravity sensor）every 1 sec, by analysing Air-pressure's changings, it can get the number of floors and remember the time in such a format "2014-12-10-13-30-05", and write these information into file.txt.

elefee, acts as the network server. Coding by Java and compiling in eclipse, it can get the Altitude-master's file.txt and anylysing it. most importantly, it is a The Card Reader, users enter elevator by swipe the ID card(each card has their Identity information. Now the server remember this and doing analysing, gathering each user's records of elevator. Finally get a *.sql file, in order to push into MYSQL Cloud database for User's Searching on the Internet.

myele, acts on the Internet, for Searching how much they will pay, and show user records. It consists of Action(Java) and Html/Css/JS/Bootstrap, of course.

试想一下，小区用户凭刷卡走入电梯，服务器自动记录每个用户使用电梯记录并以此分析每年/月的使用费用，实现公平公摊，网页查询费用并可定时推送邮箱，是多么美妙的事情啊（yy中==）。
