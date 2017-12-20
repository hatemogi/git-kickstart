# Git 브랜치와 태그 관리

## 사전 지식 강화

커밋아이디의 의미

## 주요 명령어

git branch
git checkout
git merge
git tag
git rebase

## 브랜치나 태그 커밋을 가리키는 방법
## 태그

git tag v1


## 리베이스

## Merge VS Rebase

The final result of the rebase is very similar to the merge. The greet branch now contains all of its changes, as well as all the changes from the master branch. However, the commit tree is quite different. The commit tree for the greet branch has been rewritten so that the master branch is a part of the commit history. This leaves the chain of commits linear and much easier to read.

## When to Rebase, When to Merge?

Don’t use rebase …

If the branch is public and shared with others. Rewriting publicly shared branches will tend to screw up other members of the team.
When the exact history of the commit branch is important (since rebase rewrites the commit history).
Given the above guidelines, I tend to use rebase for short-lived, local branches and merge for branches in the public repository.
