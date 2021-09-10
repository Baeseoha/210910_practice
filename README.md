# 발견 문제점
## 1. 실행시 에러 발생

> 원인 : WriteDAO.xml 에서 mapper 경로를 잘못 기재
```java
// 수정 
<mapper namespace="com.lec.spring.domain.WriteDTO"> ==>   
<mapper namespace="com.lec.spring.domain.WriteDAO">
```

## 2. '상세 내용 보기' 시 내용이 안보이는 증상 발생

> **원인** : view.jsp 에서 parameter name에 오타

``` html
// 수정 
조회수: ${list[0].viewcnt } => 조회수: ${list[0].viewcnt }<br>
``` 

## 2. '상세내용 페이지에서 신규등록' 시 내용이 안보이는 증상 발생

> **원인** : view.jsp 에서 신규등록 페이지 경로를 잘못 기재

``` html
// 수정 
<button onclick="location.href='write.jsp'">신규등록</button> =>  
<button onclick="location.href='write.do'">신규등록</button>
``` 








