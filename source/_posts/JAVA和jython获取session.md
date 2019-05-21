---
title: JAVA和jython获取session
date: 2019-05-21 08:42:54
categories: JAVA
tags:
    - JAVA
---

### java获取session

#### Spring MVC中 
```java
HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();
HttpSession session = request.getSession(); 
```

#### 获取Session所有值
```java
HttpSession session = request.getSession();    
// 获取session中所有的键值  
Enumeration<String> attrs = session.getAttributeNames();  
while(attrs.hasMoreElements()){
    String name = attrs.nextElement().toString();
    Object value = session.getAttribute(name);
    System.out.println(name+":"+value);
```

### jython中也可以用
```python
from org.springframeword.web.context.request import RequestContextHolder

request=RequestContextHolder.getRequestAttributes().getRequest()
session=request.getSession()
print(session)
```