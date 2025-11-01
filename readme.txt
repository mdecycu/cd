cd 倉儲一開始為空倉儲, 組長將兩位組員納為協同者, 也就是 scrum-1 與 scrum-2

階段一: 由組長建立專案的網頁架構, 讓組員可以採非同步協同的方式進行 plotter 與 openduck 機電系統模組等兩個 projects.

組長先在自己的電腦上建立一個 cd 目錄, 然後利用 scite readme.txt 建立這個說明檔案

階段二: plotter 尺寸設計與零組件繪圖

階段三: openduck 零組件繪圖

組長對於起始 cd 近端倉儲的操作:

Y:\>cd tmp

Y:\tmp>mkdir cd

Y:\tmp>scite readme.txt

執行 readme.txt 檔案的編輯

Y:\tmp>cd cd

Y:\tmp\cd>git init

hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in C:/Users/hpeng/Desktop/portable_2026/data/tmp/cd/.git/

Y:\tmp\cd>git branch -M main

強制將目前所在分支命名為 main

Y:\tmp\cd>git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        readme.txt

nothing added to commit but untracked files present (use "git add" to track)

Y:\tmp\cd>git add readme.txt

Y:\tmp\cd>git commit -m "新增 readme.txt"

[main (root-commit) ffec433] 新增 readme.txt
 1 file changed, 9 insertions(+)
 create mode 100644 readme.txt

Y:\tmp\cd>git remote add origin git@mdecycu:mdecycu/cd.git

mdecycu 用戶的近端 ssh session 名稱為 mdecycu, 此指令組長利用 git remote 指令, 建立一個近端倉儲設定, 以 origin 為代號, 將此代號設定為 git@mdecycu:mdecycu/cd.git, 此設定執行後將會寫入 cd 倉儲的 .git/config 檔案中

Y:\tmp\cd>git push -u origin main

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 561 bytes | 561.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To mdecycu:mdecycu/cd.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

git push 指令額外使用 -u 表示要內定 upstream (上游) 倉儲的分支為 origin 這個代號所對應的倉儲, 其中的 main 分支

指令執行之後, 若近端的 ssh privatekey 與 github key server 上已經登錄的 public key (可以視為維護(開啟)倉儲的鎖頭) 為一個 pair, 則可以將近端的提交內容, 推送到 github 倉儲中

Y:\tmp\cd>

組長完成上述內容編輯後的指令:

Y:\tmp\cd>git add .

Y:\tmp\cd>git commit -m "在 readme.txt 中說明組長在近端的指令操作"

[main 7e52c5b] 在 readme.txt 中說明組長在近端的指令操作
 1 file changed, 238 insertions(+), 1 deletion(-)

Y:\tmp\cd>git push

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.82 KiB | 1.82 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To mdecycu:mdecycu/cd.git
   ffec433..7e52c5b  main -> main

Y:\tmp\cd>

Y:\tmp\cd>git add .

Y:\tmp\cd>git commit -m "針對第二次提交所使用的指令說明"

[main 9ec70a2] 針對第二次提交所使用的指令說明
 1 file changed, 26 insertions(+)

Y:\tmp\cd>git push

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 620 bytes | 310.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To mdecycu:mdecycu/cd.git
   7e52c5b..9ec70a2  main -> main

Y:\tmp\cd>










































































































































































