# 깃 커밋 메시지(Git Commit Messages) 가이드

## 좋은 커밋 메시지가 중요한 이유
커밋 메시지를 잘 쓰기 위해 노력해야 하는 이유는 서로 다를 수 있지만, 잘 쓰인 커밋 메시지가 더 유익하다는 사실에는 많은 프로그래머들이 동의할 것이다. 그 중 대표적인 3가지를 꼽아보면 다음과 같다.

* 더 좋은 커밋 로그 가독성

* 더 나은 협업과 리뷰 프로세스

* 더 쉬운 코드 유지보수

## 좋은 커밋 메시지의 7가지 규칙

* 제목과 본문을 한 줄 띄워 분리

* 제목은 영문 기준 50자로 제한

* 제목과 첫글자를 대문자로

* 제목 끝에 `.` 금지

* 제목은 `명령조` 사용

* 본문은 영문 기준 72자로 줄 바꿈

* 본문은 `무엇을` 보다 `무엇을`, `왜`를 작성

## 커밋 메시지 구조
커밋 메시지의 기본적인 구조는 제목(Subject), 본문(Body), 꼬리말(Footer) 3개의 구역으로 나누며, 각 구역은 한 칸의 빈 줄로 구분한다.

```text
<type>[optional scope]: subject <description>

[optional body]

[optional footer(s)]
```

## 제목(Subject)
제목은 50자 이하여야 하며 대문자로 시작하고 마침표로 끝나지 않아야 한다.

커밋이 무엇을 했는지보다는 무엇을 하는지 설명하려면 명령형 어조를 사용한다. 예를 들어 `change`를 사용하고 `changed` 혹은 `changes`를 사용하지 않는다.

### 커밋 타입

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

## 본문(Body)
모든 커밋이 본문을 보증할 만큼 복잡한 것은 아니므로 선택 사항이며 커밋에 약간의 설명과 컨텍스트가 필요한 경우에만 사용된다. `어떻게(how)`가 아니라 약속의 `무엇(what)`과 `왜(why)`를 설명하기 위해 본문을 사용한다.

본문을 작성할 때 제목과 본문 사이에 공백 줄이 필요하며 각 줄의 길이를 72자 이내로 제한해야 한다.

## 꼬리말(Footer)
바닥글은 선택 사항이며 이슈 추적 ID를 참조하는데 사용된다.

### 라벨의 종류

| 키워드 | 설명 |
|-----|-----|
| Resolves | 문의나, 요청에 의한 이슈에 해당하는 경우 이슈 번호 |
| Closes | 일반적인 개발과 관련된 이슈에 해당하는 경우 이슈 번호 |
| Fixes | 버그 픽스, 핫 픽스 관련 이슈에 해당하는 경우 이슈 번호 |
| See also | 커밋의 이슈와 연관되어 있는 이슈들이 존재 하는 경우, 또는 관련된 이슈들이 있는 경우 이슈 번호 |

## 전체 커밋 예시

* type(타입): subject(제목)

* body(본문)

* Resolves: #issueNo (해결한 이슈)

* See also: #issueNo (참고 이슈)

```text
feat: Summarize changes in around 50 characters or less

 More detailed explanatory text, if necessary. Wrap it to about 72
 characters or so. In some contexts, the first line is treated as the
 subject of the commit and the rest of the text as the body. The
 blank line separating the summary from the body is critical (unless
 you omit the body entirely); various tools like `log`, `shortlog`
 and `rebase` can get confused if you run the two together.

 Explain the problem that this commit is solving. Focus on why you
 are making this change as opposed to how (the code explains that).
 Are there side effects or other unintuitive consequenses of this
 change? Here's the place to explain them.

 Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
    by a single space, with blank lines in between, but conventions
    vary here

 If you use an issue tracker, put references to them at the bottom,
 like this:

 Resolves: #123
 See also: #456, #789
```

## 커밋 메시지 비교

### Good

* feat: improve performance with lazy load implementation for images

* chore: update npm dependency to latest version

* Fix bug preventing users from submitting the subscribe form

* Update incorrect client phone number within footer body per client request

### Bad

* fixed bug on landing page

* Changed style

* oops

* I think I fixed it this time?

* empty commit messages

## [출처 및 참고]
* [https://git-scm.com/docs](https://git-scm.com/docs)
* [https://cbea.ms/git-commit/](https://cbea.ms/git-commit/)
* [https://udacity.github.io/git-styleguide/](https://udacity.github.io/git-styleguide/)
* [https://meetup.nhncloud.com/posts/106](https://meetup.nhncloud.com/posts/106)
* [https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)
* [https://jane-aeiou.tistory.com/93](https://jane-aeiou.tistory.com/93)
