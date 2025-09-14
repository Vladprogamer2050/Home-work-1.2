1.	Чем отличаются git commit и git commit --amend? Когда --amend опасен?
git commit создает коммит а git commit --amend ти изменяет последний коммет? опасмность в том что может переписать историю если отправлен в удаленный репозиторий
2.	Что делает git branch -d и чем отличается от -D?
-d удаляет ветку
-D принудительно удаляет
3.	Для чего используют git checkout <branch> и git checkout <commit>? Что такое «detached HEAD»?
branch переключение по веткам
commit переключение по коммитам
detached HEAD нахождение вне ветки без сохранений
4.	В чём разница между reset --soft, --mixed (по умолчанию) и --hard?
не знаю
5.	Зачем нужен git revert, и чем он принципиально отличается от git reset?
revert создает новый коммит
reset удаляет коммиты и перемещает HEAD
revert для гитхабной истории, а reset для одиночек
6.	Что делает git merge --no-ff? Когда уместен --squash?
не знаю
7.	Что происходит при git rebase <base>? Как безопасно прервать ребейз?
делает историю более красивой и линейной
git rebase --abort
8.	Как перенести 3 конкретных коммита на текущую ветку с помощью cherry-pick? Что дают флаги -n, -x, -e?
git cherry-pick commit1 commit2 commit3
9.	Как отменить конфликтный cherry-pick/merge/rebase?
git cherry-pick --abort
git merge --abort
git rebase --abort
10.	Что такое «родитель» для merge-коммита и зачем нужен git revert -m?
git rever -m p1 commit1

git checkout -b feature/header
git branch -m feat/header
git branch -d feature/header

- echo "header section" >> app.txt
- git add app.txt
- git commit -m "h1: add header"
- git checkout main
- echo "footer section" >> app.txt
- git commit -am "c3: add footer"

- git revert HEAD^
- git reset --hard HEAD^
- git reflog -10
- git reset --hard <SHA>