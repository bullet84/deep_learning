# Merge commit 연습

이 문서는 GitHub CLI로 Pull Request를 병합하는 연습을 위한 자료입니다.

## 실행 순서

아래 명령의 `PR_NUMBER`를 이 문서를 추가한 PR 번호로 바꾸세요.

```powershell
gh pr view PR_NUMBER
gh pr diff PR_NUMBER
gh pr merge PR_NUMBER --merge --delete-branch
git switch main
git pull --ff-only
git log --oneline --graph -10
```

## 확인할 결과

원래 커밋을 유지하면서 main에 병합 커밋이 추가됩니다.
저장소에서 merge commit 병합을 허용해야 사용할 수 있습니다.
