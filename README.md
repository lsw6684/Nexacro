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
- `Design 탭에서 "Ctrl + B"로 바인딩 상태를 노출시킬 수 있습니다.`

### Dataset
내부 Data로, 컴포넌트와 바인딩 시 사용됩니다.
- 데이터를 테이블(2차원) 형태로 관리하는 오브젝트.
- 서버와 통신 시 Data를 주고 받는 형식으로 사용.
- 데이터가 수정, 삭제되면 변경 내용을 Origin Buffer에 저장.

### Inner Dataset
목록형 컴포넌트(Combo 대상)에 데이터를 바인딩 하기 전에, 우선적으로 설정하는 Dataset입니다. Inner Dataset을 바인딩 한 후에, 목록형 컴포넌트를 바인딩 해주는 방법으로 연결합니다.

## Scope
폼 내에서 this를 사용하여 범위를 한정해 줘야 합니다.
```js
this.Hello_onclick = function(obj:nexacro.Form,e:nexacro.ClickEventInfo)
{
	this.alert("Hello");

	this.Hello_onclick.set_text("이름 변경");	// id 값이 변경 되면 별도로 변경 필요.
	obj.set_text("이름 변경");;					// 하위 설명 참고
};
```
- 함수엔 객체(obj)와 이벤트(e)가 항상 포함 되는데, **obj**으로 컨트롤 하면 id값이 바뀌어도 작동 가능합니다. (this의 한계 해결)


















