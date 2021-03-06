
# CRUD로 비교하는 FBV vs CBV

## 개요 (프로젝트 목표)

이 프로젝트는 django의 Function 기반 View (Function-Based View, 이하 FBV로 약칭) 와 Class 기반 View (Class-Based View, 이하 CBV로 약칭)로 CRUD를 구현함으로써,

두 방식은 구현에 있어 어떠한 차이가 있는지, 나아가 앞으로 배울 RESTful Framework에 있어 핵심적인 기능을 수행할 CBV는 어떠한 방식으로 동작하는지에 대해 이해하기 위해 본 프로젝트를 진행하였다.

CBV는 classcrud라는 앱으로 구현하였고
FBV는 viewvrud라는 앱으로 구현하였다

## 사진 및 기능

**외관이 그럴싸하지 않을 수 있겠지만, 

**이건 실제 이용자들에게 배포되는 사이트가 아니고, 

**django의 내부의 동작원리를 파악하기 위한 프로젝트이니 부디 너무 실망하지는 않기를...

![1.jpg](img/1.jpg "대문")

대문이다. 

CBV로 만들어진 Blog를 이용할지 
FBV로 만들어진 Blog를 이용할지 선택할 수 있다

**둘 중 무엇을 선택하든 뒤에 설명할 동일한 기능(블로그 글의 생성, 열람, 수정, 삭제 기능)을 수행할 것이다.**

일단 Class Based CRUD를 선택해보자

# C - Create

![2.jpg](img/2.jpg "CBV")

[새 글 추가] 링크를 누르면, 새로운 글을 추가할 수 있는 form 페이지로 이동한다. 여기서 새 글을 등록하면 블로그 목록이 있는 곳으로 redirection 된다

![3.jpg](img/3.jpg "Add POST")

# R - Read

 본문 자세히 보기를 누르면 방금 작성한 글을 자세히 볼 수 있는 페이지로 이동하게 된다

![4.jpg](img/4.jpg "Read Post")


# U - Update

수정하기 버튼을 누르면 방금 작성한 글을 수정할 수 있는 곳으로 이동하게 된다

![5.jpg](img/5.jpg "Update Post")

# D - Delete 

삭제하기를 누르면 정말로 삭제할 것인지를 묻는 페이지로 이동하고, 정말 삭제할 것임을 확인하면 해당 객체 (블로그 글) 이 삭제되는 형태로 구현하였다

![6.jpg](img/6.jpg "Delete Post")


