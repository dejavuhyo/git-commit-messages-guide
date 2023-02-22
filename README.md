# 커밋 메시지(Commit Messages) 가이드

## 좋은 커밋 메시지가 중요한 이유
왜 커밋 메시지를 잘 쓰기 위해 노력해야 하는가? 이유는 서로 다를 수 있지만, 잘 쓰인 커밋 메시지가 더 유익하다는 사실에는 많은 프로그래머들이 동의할 것으로 여겨진다. 그 중 대표적인 3가지를 꼽아보면 다음과 같다.

- 더 좋은 커밋 로그 가독성
- 더 나은 협업과 리뷰 프로세스
- 더 쉬운 코드 유지보수

"좋은 커밋 메시지를 고민하는 건 괜찮은 생각인 것 같아요! 하지만 좋은 메시지에 딱부러진 정답이 있을지 모르겠네요. 사람들마다 좋은 커밋 메시지로 생각하는 기준이 모두 다를 것 같은데, 그렇다면 그나마 좀 더 많은 사람들이 공감하고 실천하고 있는, 좋은 커밋 메시지를 만드는 약속 같은 것이 있을까요?"

## 좋은 커밋 메시지의 7가지 규칙

- 제목과 본문을 한 줄 띄워 분리
- 제목은 영문 기준 50자로 제한
- 제목과 첫글자를 대문자로
- 제목 끝에 `.` 금지
- 제목은 `명령조` 사용
- 본문은 영문 기준 72자로 줄 바꿈
- 본문은 `무엇을` 보다 `무엇을`, `왜`를 작성

## 커밋 메시지 구조

- type(타입): title(제목)
- body(본문, 생략 가능)
- Resolves: #issueNo (해결한 이슈, 생략 가능)
- See also : #issueNo (참고 이슈, 생략 가능)

## 타입

| 키워드 | 설명 |
|-----|-----|
| feat | 새로운 기능 추가 |
| fix | 버그 수정 |
| chore | 자잘한 수정, 빌드 업무 수정, 패키지 매니저 수정 (dependency 업데이트, gitignore 수정 등) |
| refactor | 코드 리팩토링 |
| docs | 문서 수정 |
| style | 코드 스타일 변경 (코드 포매팅, 공백, 세미콜론 누락 등 기능 수정이 없는 경우) |
| design | 사용자 UI 디자인 변경 (CSS 등) |
| test | 새로운 테스트, 리팩토링 테스트 코드 |
| perf | 성능 개선 |
| ci | 지속적 통합 관련 수정 |
| build | 빌드 파일 수정, 외부 종속성 변경 사항 |
| revert | 이전 커밋을 되돌리기 |
| rename | 파일 혹은 폴더명을 수정만 한 경우 |
| remove | 파일을 삭제만 한 경우 |

## 이슈

| 시점 | 키워드 |
|-----|-----|
| 해결 | Closes(종료), Fixes(수정), Resolves(해결) |
| 참고 | Ref(참고), Related to(관련), See also(참고) |

## 커밋 메시지 비교

### Good

- feat: improve performance with lazy load implementation for images
- chore: update npm dependency to latest version
- Fix bug preventing users from submitting the subscribe form
- Update incorrect client phone number within footer body per client request

### Bad

- fixed bug on landing page
- Changed style
- oops
- I think I fixed it this time?
- empty commit messages

## [출처 및 참고]
- [https://git-scm.com/docs](https://git-scm.com/docs)
- [https://cbea.ms/git-commit/](https://cbea.ms/git-commit/)
- [https://meetup.nhncloud.com/posts/106](https://meetup.nhncloud.com/posts/106)
- [https://jane-aeiou.tistory.com/93](https://jane-aeiou.tistory.com/93)
