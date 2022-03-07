# Nexacro
애플리케이션 설계/개발/테스트/디버깅/배포 등 일련의 작업을 지원하는 통합 개발 환경입니다. 디자인 환경을 제공하여 **빠르게 디자인 할 수 있으며**, **바인딩 상태나 컴포넌트 간 연관 관계를 직관적으로 확인**할 수 있습니다.

- [Generate](#generate)
- [Script 작성/접근](#script-작성접근)
- [Data Binding](#data-binding)
- [Scope](#scope)

## Generate
소스 코드를 JavaScript로 변환, 즉 Generate하는 과정이 필요합니다. 화면을 생성, 수정 후 저장하는 시점에 자동으로 처리합니다.




## Script 작성/접근

## Data Binding
바인딩이란, 데이터 컴포넌트와 표현컴포넌트를 스크립트 코딩 없이 연결하여 데이터 입출력, 혹은 컴포너트를 동작시킵니다.

## Scope
폼 내에서 this를 사용하여 범위를 한정해 줘야 합니다.
```js
this.Hello_onclick = function(obj:nexacro.Form,e:nexacro.ClickEventInfo)
{
	this.alert("Hello");
};
```


















