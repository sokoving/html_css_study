# head 요소에도 순서가 있다
https://www.w3.org/ > 웹 표준 명시

# <span class="lnr lnr-chevron-right"></span>
    linear icons에서 지시하는 아이콘 넣는 방법


# 박스 안에 이미지 넣기
    a>img 이기 때문에 a에 
     display: block;과  width: 100%;를 준다
    가로나 세로 중 하나 값만 주면 나머지는 맞춰짐
1. 
header .inner-header .logo{
    background: tomato;
    flex: 1;
    width: 150px;
}
header .inner-header .logo a{
    display: block;
    width: 100%;        
}
header .inner-header .logo img{
    width: 100%;
}   

2. 
section.contents .project ul{
    /* background: pink; */
    display: flex;
    justify-content: space-evenly;
}
section.contents .project ul li{
    /* background: tomato; */
    height: 400px;
    overflow: hidden;
}
section.contents .project ul li a{
    display: block;
}
section.contents .project ul li a img{
    width: 100%;
}


# img와 background-img의 차이점
 overflow: hidden;이 자동 적용 여부
 cover가 자동 적용, 수동 적용
 img 위치는 position: absoute; 걸어서 

# 메뉴 픽스드
header{
    position: fixed;
    width: 100%;    > position 주면 가로 깨짐
    top: 0;         > 항상 위에 있으니까
    z-index: 1000;  > 깔리지 말라고
}

# flex에서 박스 내리기
    부모 요소에 flex-wrap: wrap;
    자식 요소에 width를 100%에 맞에 잘
    100%가 넘어가는 번째 아이템은 아래로