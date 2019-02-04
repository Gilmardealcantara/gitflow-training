# Git and git flow trainning

## GIT
```
git init 
echo "Hello World" > test.txt
git add test.txt
git commit -m 'First commit
echo "How are you?" >> test.txt
git add test.txt
git commit -m 'Second commit'
git checkout master^ # change to removed last commit branch
git log
git diff master
git checkout master
git branch nova-branch
git checkout nova-branch
echo "I'm fine" >> test.txt
git add test.txt
git commit -m 'Third commit'
git checkout master
echo 'Hello World 2' > test2.txt 
git add test2.txt
git commit -m 'Fourth commit'
git merge nova-branch
git log --graph
```

## GIT FLOW 
```
brew install git-flow # if no install git flow
git flow init 
# if have problems create a branch develo before.
git flow feature start recurso-milionario
echo 'Este é o melhor recurso criado desde sempre!' > recurso.txt
git add recurso.txt
git commit -m 'Finished feature'
git flow feature finish recurso-milionario
git log
git branch 

git flow release start 0.1.0
# change content
echo 'Este talvez seja o melhor recurso criado desde sempre!' > recurso.txt
git add recurso.txt
git commit -m 'Little bug-fix in feature'

git flow hotfix start 0.1.1
echo 'Este talvez não seja o melhor recurso criado desde sempre! Mas é um dos mais legais!' > recurso.txt
git add recurso.txt
git commit -m 'Little hotfix in a feature'
git flow hotfix finish 0.1.1
```