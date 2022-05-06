# 📅 2022-05-06 TIL

## ❓ 무엇을 배웠나요?
- 자바스크립트 프로젝트(금융웹앱 만들기)를 시작했다.
  - 이전에 조원들과 구조를 파악하며 간단히 마크업 해둔 것을 바탕으로 마크업, 스타일 적용, 그리고 입출금 내역 데이터를 출력하기까지 구현했다.
  - `<body>` 태그에 크기를 지정하고 배경색을 입혀도 지정한 크기 안에만 입혀지는 것이 아니라 웹 전체에 입혀진다.. `<body>`에 함부로 스타일을 적용하면 안 된다..!
  - json 파일에서 데이터를 받아와서 HTML에 요소를 생성 및 추가(`createElement`, `appendChild`)하고 데이터를 출력하기.
    ```js
    const ulElem = document.querySelector(".history");
    for(let i=0; i<obj.length; i++) {
      // li 만들기
      const li = document.createElement("li");
      li.className = "history_item" + i;
      // ul에 li 붙이기
      ulElem.appendChild(li);
      
      const liElem = document.querySelector(".history_item"+i);
      const span_item = document.createElement("span");
      const span_price = document.createElement("span");
      // item의 value 가져와서 li에 넣기
      span_item.textContent = obj[i].item;
      span_price.textContent = priceToString(obj[i].price);
      liElem.appendChild(span_item);
      liElem.appendChild(span_price);
    }
    ```
  - 정규표현식을 이용한 천 단위로 숫자에 콤마(,) 넣어주기.
    ```js
    function priceToString(price) {
      return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
    }
    ```

<br/>

## 👍 칭찬
- 목표한 것보다 많이 구현했다!
<br/>

## 🥲 아쉬운 점
- 없음!! 열심히 했다 오늘!!!👏
<br/>

## ✅ 내일 할 일
- 자바스크립트 프로젝트하기
  - 다른 페이지 구현(마크업, 스타일 입히기)? or 오늘 구현한 페이지에 자바스크립트 구현? 고민!
- 쓰다만 5월 4일자 블로그 마저 정리하기
- 해커톤: 맡은 페이지(행사 정보) 레이아웃 짜기
- GitHub 오늘의 회고 작성하기
- 아침 스트레칭하기
<br/>