# Bridge 기능구현목록
## View
### 입력받기 -> InputView
- 1) 다리 길이 숫자로 입력받기 (3~20)
- 2) 다리 위치 선택 (U,D)
- 3) 재시작/게임종료 (R, Q)

### 출력하기 -> OutputView
- [ | | ] 다리 형식에 문자열로 다리 반환하는 메서드
- 최종게임결과 반환
- 게임성공여부 반환 (Q를 입력하면 바로 실패 반환)
- 총시도한횟수 반환

## Model
### Random 0,1 생성
- BridgeRandomNumberGenerator 0,1 랜덤 생성

### Bridge 생성 (BridgeMaker.js)
- 입력받은 숫자만큼 0,1random 생성
- 0:D, 1:U 배열로 바꾸는 메서드 

## Controller
- 입력받은 문자가 U면 윗다리, D면 아랫다리에 표시되게 하는 메서드
- Bridge 생성에서 만든 배열 순서와 입력값이 같으면 0, 다르면 x를 출력하는 메서드
- 재시작 R이면, R 입력횟수만큼 시도횟수 +1을 해주는 메서드
- BridgeMaker의 배열과 입력값이 모두 같으면 게임종료 반환

