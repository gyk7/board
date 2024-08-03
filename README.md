# 스프링부트 게시판 구현

* 기간 : 2024.07.30 ~ 2024.08.03

## **기능**
1. 게시글 작성 폼 구현
2. 글 작성, 수정, 삭제, 검색
3. 글 작성 시 파일 업로드
4. 게시글 리스트


## **어려웠던 점**
1. springboot 1.X는 parameter를 사용하지 않아도 되는 경우가 많았는데
   springboot 2.X는 @Pathvariable, @RequestParam 등 parameter을 사용해야함. parameter을 붙이지 않아 에러가 몇 번 남.
2. BoardController에서 list를 구현할 때
   ![image](https://github.com/user-attachments/assets/f18cd705-f0c7-414e-b865-497f09cfa94b)
   여기에서 String searchKeyword 앞에 @RequestParam("searchKeyword")를 붙였는데 에러가 남.
   => 검색을 할 수도, 안 할수도 있기 때문에 searchKeyword에 값없이 ""으로 빈 문자열이 들어오면 에러가 발생함.
      값이 넘어오지 않는 경우를 생각해 defaultValue로 기본 값을 설정해줌.
   

## **시도할 내용**
1. 댓글 작성, 수정, 삭제
2. 게시판 글 작성 폼 사용자 편의 생각해서 수정
   
