문제 파악
----------------------------------------------------------------
1. 자동차 이름 입력
- println : "경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"
- 쉼표로 구분
- 각 이름은 5자 이하 (1자~5자)
- 문자열로 입력받음

2. 시도할 횟수 입력
- println : "시도할 횟수는 몇회인가요?"
- 문자열로 입력받음
- 숫자로 바꿔야함

3. 전진 조건
- 0~9사이 무작위 수 -> 4이상이면 전진
- 각 자동차 별 count 추가

4. 실행
- println : "실행 결과"
- 1턴마다
- println : "n번째 이름: " + "-"*n

5. 우승 처리
- "최종 우승자 :" + 이름
- 공동 우승자면 이름1+", "+이름2
----------------------------------------------------------------
구현 목록
----------------------------------------------------------------
1. 입력 (userInput)
- value
  - [ ] 자동차 이름 문자열
  - [ ] 시도 횟수 문자열
  - [ ] validator
- func
  - [ ] 자동차 이름 입력받기 (검증)
  - [ ] 시도 횟수 입력받기 (검증)
  - [ ] 자동차 이름 getter
  - [ ] 시도 횟수 getter

2. 검증 (validator)
- func
   - [ ] String -> 자동차 이름 입력 검증 (에러)
   - [ ] String -> 시도 횟수 검증 (에러)
 
3. 자동차 (car)
- value
  - [ ] 자동차 이름 (name)
  - [ ] 이동한 거리 (moving)
- func
  - [ ] 자동차 이름 setter / getter
  - [ ] 이동한 거리 setter / getter

4. 자동차들 (Cars)
- value
  - players : List<car>
- func
  - [ ] userInput.carsName(String) -> player.name setting
  - [ ] userInput.carMoving(String) -> player.moving set
  - [ ] go or stop : player 수 만큼 0~9 사이 수 랜덤 뽑기, 4 이상(player.moving up)
  - [ ] getWinner : player.moving이 가장 큰 player 반환 (List<car>)
  
5. 레이싱 게임 (racing)
- value
  - [ ] turn (시행 횟수)
  - [ ] Cars
  - [ ] userInput
- func
   - [ ] play (ready, start, end)
   - [ ] ready (userInput 입력 및 출력, Cars+turn 설정)
   - [ ] start (turn만큼 반복-Cars.go or stop)
   - [ ] end (winner : Cars.getWinner, winner 출력)

6. 출력 (printUtil)
- func
   - [ ]  "경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"
   - [ ]  "시도할 횟수는 몇회인가요?"
   - [ ]  "실행 결과"
   - [ ]  Cars -> car.name + ": " + "-"*car.moving
   - [ ]  "최종 우승자 :" + winner

----------------------------------------------------------------
주의 사항
----------------------------------------------------------------
- JUnit 5와 AssertJ를 이용하여 본인이 정리한 기능 목록이 정상 동작함을
테스트 코드로 확인.
- test/java/study를 참고
- camp.nextstep.edu.missionutils.Randoms or Console 사용
