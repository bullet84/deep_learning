# Rebase merge 연습

이 PR에는 문서를 작성하고 보완하는 두 개의 커밋이 있습니다.
Rebase merge는 별도의 병합 커밋 없이 각 커밋을 main 위에 순서대로 적용합니다.

아래 명령의 `PR_NUMBER`를 이 문서를 추가한 PR 번호로 바꾸세요.

```powershell
gh pr view PR_NUMBER --json commits
gh pr diff PR_NUMBER
gh pr merge PR_NUMBER --rebase --delete-branch
```

## 병합 후 확인

```powershell
git switch main
git pull --ff-only
git log --oneline --graph -10
```

두 커밋이 유지되면서 선형 이력으로 이어지는지 확인하세요.
GitHub에서 rebase merge한 커밋에는 새로운 SHA가 부여됩니다.
저장소에서 rebase merge를 허용해야 사용할 수 있습니다.
