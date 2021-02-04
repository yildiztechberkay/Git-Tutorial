# Git Komutları

### Init
*git init* komutu git yapılandırmasını dahil eder.
### Kullanım
    $ git init
    $ git init -b <branch-name>
-----------------

### Config
*git config* komutu git ile alakalı yapılandırmaları belirlemek için kullanılır.
### Kullanım
    $ git config --global user.name "ad soyad"
    $ git config --global user.email "ornek@mail.com"
    $ git config --list
-----------------

### Status
*git status* komutu git kullanarak takip edilen dizindeki dosyaların değişikliklerini listeler.
### Kullanım
    $ git status
    $ git status -s
    $ git branch -b
-----------------

### Add
*git add* komutu değişiklik yaptığımız dosyaları commit edilmek üzere 'stage' alanına eklememizi sağlar.
### Kullanım
    $ git add .
    $ git add fileName.txt
    $ git add file/path/fileName.txt
    $ git restore --staged fileName.txt
-----------------

### Restore
*git restore* komutu değişiklik yaptığımız dosyanın değişikliklerini geri almak için kullanılır.
### Kullanım
    $ git restore fileName.txt
-----------------

### Gitignore
*.gitignore* dosyasına dizindeki istemediğimiz veya gerek duymadığımız dosyaları ekleyerek git'e gönderilmesini ve değişikliklerin takip edilmeini engellemiş oluruz.
### Kullanım
    $ touch .gitignore
    $ nano .gitignore
    $ git status
-----------------

### Commit
*git commit* komutu dosyaların o anki durumunu kaydeder ve bir referans noktası oluşturur. Proje ilerledikten sonra isterseniz commit ettiğiniz başka bir noktaya geri dönüş yapmanızı sağlar.

![commit image](./images/01-commit.png "git commit workflow")

### Kullanım
    $ git commit -m 'this is commit message'
    $ git commit -a -m 'mesaj'
    $ git commit --amend -m 'edited commit message'

-----------------

### Log
*git log* komutu yapmış olduğumuz commit'leri listeler.
### Kullanım
    $ git log
    $ git log --oneline
    $ git log -all
    $ git log --decorate
    $ git log --graph
    $ git config --global alias.lo 'log --all --graph --decorate --oneline'

-----------------

### Reset
*git reset* komutu bulunduğumuz branch ile ilerideki veya gerideki bir commit'e gitmeyi sağlar.

![reset image](./images/01-reset.png "reset")

### Kullanım 
    $ git reset commitHash
    $ git reset --soft HEAD~1
    $ git reset --hard HEAD~3
    $ git reflog
    $ git reset -i HEAD~4
-----------------

### Revert
*git revert* komutu bir commit'te yaptığımız değişiklikleri iptal edip bu işlemi yaptığınıza dair yeni bir commit oluşturur.

![revert image 1](./images/01-revert.png "Reset image")
![revert image 2](./images/02-revert.png "Revert vs Reset")
### Kullanım
    $ git revert commitHash

-----------------

### Branch
*git branch* bir projede dallanmayı sağlar. Bir projede birden fazla kişi çalışırken kullanılması gerekir.

![Branch image 1](./images/01-branch.png "Branch image 1")
![Branch image 2](./images/02-branch.png "Branch image 2")

### Kullanım
    $ git branch new_branch
    $ git checkout new_branch
    $ git branch -d branch_to_delete
    $ git branch -M main

-----------------

### Checkout ve Switch
*git checkout* komutu branch'ler arasında geçiş yapmamızı ve istediğimiz bir commit'e gidip dosyaların o anki durumunu görmemizi sağlar.

![Checkout vs Switch](./images/01-checkout.png "Checkout vs Switch")
### Kullanım
    $ git checkout commitHash
    $ git checkout branchName
    $ git switch branchName

-----------------

### Diff
*git diff* komutu bir dosyadaki farklılıkları görmek için kullanılır.
### Kullanım
    $ git diff
    $ git diff fileName.txt
    $ git diff commitHash anothorCommitHash
    $ git diff master new_branch
    $ git diff master new_branch
    $ git diff master new_branch ./diff_test.txt

-----------------

### Merge
*git merge* komutu branchleri birleştirmek için kullanılır. Conflict meydana geldiğinde bunun çözülmesi kullanıcının sorumluluğundadır.

![Merge image 1](./images/01-merge.png "Merge image 1")
![Merge image 2](./images/02-merge.png "Merge image 2")

### Kullanım
    $ git checkout branchName
    $ git pull
    $ git merge anotherBranchName
    $ git add .
    $ git commit
    $ git merge --continue
    $ git merge --abort

-----------------

### Rebase
*git rebase* komutunu kullandığımızda A branchindeki her bir commit B dalına sanki commit işlemi B dalında yapılmış gibi yeniden yazılır.

![Rebase image 1](./images/01-rebase.png "Rebase image 1")

### Kullanım
    $ git rebase anotherBranch

-----------------
### Remote
*git remote* yerel depo ile takip edilen uzak depoyu kontrol edebilmeyi sağlar.

![Remote image](./images/01-remote.jpg "Remote image")

### Kullanım
    $ git remove -v 
    $ git remote add remoteRepoName URL
    $ git remote remove remoteRepoName

-----------------
### Clone
*git clone* Github'da varolan bir depoyu tüm dosyalar, dallar dahil olmak üzere klonlar(indirir).
### Kullanım
    $ git clone URL

-----------------

### Pull
*git pull* içerisinde bulunulan branch'in remote reposundaki değişikler ile bütün commitleri alarak günceller.
### Kullanım
    $ git pull
    $ git pull --rebase
    $ git pull --force
    $ git pull --all

-----------------

### Push
*git push* lokal branchteki commitleri remote repoya yükler.
### Kullanım
    $ git push -u remoteRepoName branchName
    $ git push --all
    $ git push --tags
    
-----------------
