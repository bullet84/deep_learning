# Rebase merge 연습

이 PR에는 문서를 작성하고 보완하는 두 개의 커밋이 있습니다.
Rebase merge는 별도의 병합 커밋 없이 각 커밋을 main 위에 순서대로 적용합니다.

아래 명령의 `PR_NUMBER`를 이 문서를 추가한 PR 번호로 바꾸세요.

```powershell
gh pr view PR_NUMBER --json commits
gh pr diff PR_NUMBER
gh pr merge PR_NUMBER --rebase --delete-branch
```
