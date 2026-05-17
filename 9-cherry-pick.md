git cherry-pick `<commit>`：挑一个 commit

git cherry-pick `<c1>` `<c2>` `<c3>`：挑多个 commit

git cherry-pick A..B：挑 A（不含）到 B（含）之间的所有 commit

遇到冲突时，手动解决后，git add 后再 git cherry-pick --continue，中途想放弃就 git cherry-pick --abort
