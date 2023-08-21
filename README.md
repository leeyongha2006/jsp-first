# jsp-first
jsp 첫걸음

## 전역변수와 지역변수

``` jsp
<b> 전역변수와 지역변수의 선언 및 이용하기</b><br>
	<%!
		int global_var = 0; //전역변수를 선언하는 선언문
	%>
	
	<%--
		// 스크립트릿에서 지역변수 선언
		int local_var = 1;
		out.print("global_var = " + global_var + "<br>");
		out.print("local_var = " + local_var + "<br>");
```
#### <%   %> : 일반적으로 자바코드를 묶는 블록으로 지연변수를 선언할 때 사용한다 = 스크립트릿(표현식)
#### <%!   %> : jsp페이지에 메소드를 생성한다. 전역변수 선언시 사용한다 = 선언문
---
# 성적처리
## for문을 사용한 예제

#### 두 사람의 시험점수 합계를 각각의 배열방에 저장
``` jsp
<% // 스크립틀릿

 String name[] = {"김미영", "김민성"};
 int score[][] = {{80,90,70},{50,25,30}};
 float avg[] = new float[2];
 int total[] = new int[2];
 
 for(int i = 0; i < 2; i++){
	 for(int j = 0; j < 3; j++){
		 total[i] += score[i][j];
	 }
	 avg[i] = total[i]/3;
 }
  
%>
```
#### 출력
``` jsp

	<h1> 김미영의 성적</h1>
	<b> 김미영의 국어점수는 : <%= jumsu[0][0] + "점" %></b><br>
	<b> 김미영의 영어점수는 : <%= jumsu[0][1] + "점" %></b><br>
	<b> 김미영의 수학점수는 : <%= jumsu[0][2] + "점" %></b><br>
	<b> 김미영의 총합계는 : <%= total1 + "점" %></b><br>
	<b> 김미영의 평균은 : <%= avg1 + "점" %></b><br>

	<h1> 김민성 성적</h1>
	<b> 김민성의 국어점수는 : <%= jumsu[1][0] + "점" %></b><br>
	<b> 김민성의 영어점수는 : <%= jumsu[1][1] + "점" %></b><br>
	<b> 김민성의 수학점수는 : <%= jumsu[1][2] + "점" %></b><br>
	<b> 김민성의 총합계는 : <%= total2 + "점" %></b><br>
	<b> 김민성의 평균은 : <%= avg2 + "점" %></b><br>
```
![image](https://github.com/leeyongha2006/jsp-first/assets/126844590/b859fb1e-af8c-49e8-a32f-9f560356ae75)


