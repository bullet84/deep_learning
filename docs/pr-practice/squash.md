# Squash merge 연습

이 PR에는 문서를 작성하고 보완하는 두 개의 커밋이 있습니다.
Squash merge를 사용하면 이 변경을 main의 커밋 하나로 합칠 수 있습니다.

아래 명령의 `PR_NUMBER`를 이 문서를 추가한 PR 번호로 바꾸세요.

```powershell
gh pr view PR_NUMBER --json commits
gh pr diff PR_NUMBER
gh pr merge PR_NUMBER --squash --delete-branch
```

## 병합 후 확인

```powershell
git switch main
git pull --ff-only
git log --oneline -5
```

PR의 두 커밋이 main에서는 새로운 커밋 하나로 정리되는지 확인하세요.
저장소에서 squash merge를 허용해야 사용할 수 있습니다.
