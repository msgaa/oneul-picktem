# 오늘의 픽템 (@oneul_picktem)

인스타그램 릴스에 나온 상품 번호를 입력하면 바로 상품 페이지로 연결되는 모바일용 링크 페이지입니다.

- 주소: <https://msgaa.github.io/oneul-picktem/>
- 구성: `index.html` (화면·검색), `data.js` (상품 목록)

## 상품 추가하는 법

`data.js`의 `window.PICKTEM_PRODUCTS` 배열에 한 줄을 추가하고 `main` 브랜치에 push하면 1~2분 안에 반영됩니다.

```js
{
  no: 3,                       // 릴스에 적는 번호와 동일
  name: "상품 이름",
  desc: "한 줄 설명",
  url: "https://link.coupang.com/...",  // 없으면 null (클릭 시 안내 문구만 표시)
  tag: "쿠팡",                 // 선택
  keywords: ["검색어", "동의어"]  // 선택
}
```

번호는 앞자리 0이 있어도 없어도 같은 상품으로 찾아집니다. (`1` = `01`)

## 배포

GitHub Pages, `main` 브랜치 루트. push 후 자동 빌드됩니다.
