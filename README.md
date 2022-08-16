# oshwhub 自动登陆签到笔记

1. 取登陆用的lt值    
   GET https://passport.szlcsc.com/login?service=https://oshwhub.com/login?f=oshwhub  
    值在页面里
2. 登陆  
   POST https://passport.szlcsc.com/login
   登陆成功跳转   
   GET https://oshwhub.com/login?f=oshwhub&ticket=*********-cas.test.com
   带cookie带跳转   
   GET https://oshwhub.com/login?f=oshwhub
   
3. 用cookie签到  
   POST https://oshwhub.com/api/user/sign_in  
   返回的字段里带签到天数 weekCount  
3.1 用cookie3领天礼  
   GET https://oshwhub.com/api/user/sign_in/getTreeDayGift  
3.2  用cookie领7天礼   
   POST https://oshwhub.com/api/user/sign_in/getSevenDayGift
