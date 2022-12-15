# Demo 1 

```
  503  mkdir my-local-git-repo 
  504  ls
  505  cd my-local-git-repo/
  506  ls
  507  echo "Welcome to the world of Git" > Hello.txt 
  508  ls
  509  cat Hello.txt 
  510  ls
  511  git status 
  512  git init 
  513  git status 
  514  git add Hello.txt
  515  git status 
  516  git commit -m "Initial Commit - Adding a new Hello.txt" 
  517  git status 
  518  git log 
  519  git config --list 
  520  cd 
  521  ls -a 
  522  cat .gitconfig 
  523  rm -rf .gitconfig 
  524  ls
  525  cd my-local-git-repo/
  526  ls
  527  vim Hello.txt 
  528  git status 
  529  git add Hello.txt 
  530  git status 
  531  git commit -m "Updated Hello file" 
  532  git config --global user.email "amitvashist7@outlook.com" 
  533  git config --global user.name "Amit Vashist" 
  534  git commit -m "Updated Hello file" 
  535  cat ../.gitconfig 
  536  ls
  537  git log
  538  echo  "Apple Pie" 
  539  echo  "Apple Pie" | git hash-object --stdin 
  540  echo  "Apple PiE" | git hash-object --stdin 
  541  echo  "Amit Vashist" | git hash-object --stdin 
  542  echo  "Amit Vashist" | git hash-object --stdin -w
  543  echo  "Apple PiE" | git hash-object --stdin -w
  544  echo  "Apple Pie" | git hash-object --stdin -w
  545  ls
  546  ls -a 
  547  cd .git/
  548  ls
  549  ls -R objects/
  550  ls
  551  git cat-file c42fe628543c9f330ea51dea312d32cd72d7f454 -t 
  552  git cat-file c42fe628543c9f330ea51dea312d32cd72d7f454 -p 
  553  git cat-file 9a1a79d3841d891b82d868d04f1bf6d8f1f8e2da -p 
  554  git cat-file 23991897e13e47ed0adb91a0082c31c82fe0cbe5 -p 
```


# Demo 2 

```
502  cd my-local-git-repo/
  503  ls
  504  git logs 
  505  git log
  506  ls
  507  mkdir -p demo{1..3}
  508  ls
  509  cp -rf Hello.txt demo1/
  510  cp -rf Hello.txt demo2
  511  cp -rf Hello.txt demo3
  512  ls
  513  ls -R . 
  514  ls
  515  git status 
  516  git add . 
  517  git status 
  518  git commit -m "Demo Code" 
  519  git status 
  520  ls
  521  mv demo3 demo4 
  522  rm -rf demo2 
  523  git status 
  524  git add . 
  525  git status 
  526  git commit -m "Demo Code - 2" 
  527  git status 
  528  ls
  529  git branch 
  530  git branch testing 
  531  git branch 
  532  git log 
  533  ls
  534  mv demo4 demo2 
  535  git add . ; git commit -m "Demo Code - 3" 
  536  git log 
  537  ls
  538  git branch 
  539  git checkout testing 
  540  git branch 
  541  ls
  542  echo "Hey Testing Branch" >> hello_testing.txt 
  543  cat hello_testing.txt 
  544  ls
  545  git status 
  546  git log 
  547  ls
  548  git add . ; git commit -m "added a new file hello_testing.txt" 
  549  ls
  550  git status 
  551  git logs 
  552  git log
  553  ls
  554  git branch production 
  555  ls
  556  git branch 
  557  git checkout production
  558  ls
  559  echo "Hey Production Branch" >> hello_Production.txt 
  560  git add . ; git commit -m "added a new file hello_production.txt" 
  561  git log 
  562  ls
  563  cd ..
  564  ls
  565  cd my-local-git-repo/
  566  ls
  567  git checkout master 
  568  ls
  569  l
  570  ls
  571  git logs
  572  git config --global help.autocorrect 1
  573  git logs
  574  git log 
  575  git log --oneline
  576  git log --oneline --graph
  577  ls
  578  git branch 
  579  git merge testing 
  580  git log --oneline --graph
  581  ls
  582  git log 
  583  ls
  584  git log --oneline --graph
  585  git merge production
  586  git log --oneline --graph
  587  ls
  588  ld
  589  git branch 
  590  git branch -d testing
  591  git branch 
  592  git branch -d production
  593  git log --oneline --graph
  ```


# Demo 3 

```

  505  git clone https://github.com/amitvashisttech/devops-ericsson-15-Dec-2022.git
  506  ls
  507  cd devops-ericsson-15-Dec-2022/
  508  ls
  509  cat Day1-History.md 
  510  git config --list 
  511  cd ..
  512  ks
  513  ls
  514  cd my-local-git-repo/
  515  ls
  516  git config --list 
  517  ls
  518  git remote add origin https://github.com/amitvashisttech/devops-test-repo-manual.git
  519  git branch 
  520  git push -u origin master
  521  ls
  522  cd /tmp/
  523  ls
  524  git clone https://github.com/amitvashisttech/devops-test-repo-manual.git
  525  ls
  526  cd devops-test-repo-manual/
  527  ls
  528  git logs 
  529  cd 
  530  ls
  531  cd devops-ericsson-15-Dec-2022/
  532  ls
  533  history 
  534  ls
  535  mkdir 01-Git
  536  mv Day1-History.md 01-Git/
  537  ls
  538  git add . 
  539  git commit -m "01-Git Folder is added" 
  540  git status 
  541  git logs --oneline 
  542  ls
  543  git push 
  544  git logs --oneline 
  545  ls
  546  vim README.md 
  547  git commit -m "README Updated with Git" 
  548  git add . ; git commit -m "README Updated with Git" 
  549  ls
  550  git logs --oneline 
  551  git push 
  552  git pull 
  553  ls
  554  git status 
  555  git add . ; git commit -m "Test Merge" ; git push 
  556  git pull 
  557  git config pull.rebase false
  558  ls
  559  git config pull.rebase false
  560  git add . ; git commit -m "Test Merge" ; git push 
  561  git fetch 
  562  git logs 
  563  ls
  564  git pull 
  565  git status 
  566  ls -ltr 01-Git/
  567  git add . ; git commit -m "Test Merge" ; git push 
  568  git log --online
  569  git logs --online
  570  git logs --oneline
  571  ls -ltr 01-Git/

```
