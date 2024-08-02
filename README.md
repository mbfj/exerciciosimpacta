@mbfj ➜ /workspaces/codespaces-blank/exercicio01 $ git init
Initialized empty Git repository in /workspaces/codespaces-blank/exercicio01/.git/
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 01 > arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "git add example - arquivo.txt"
[main (root-commit) b5eb3ef] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 02 > arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 03 > arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git restore --staged arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "Atualização do arquivo"
[main e70a505] Atualização do arquivo
 1 file changed, 1 insertion(+), 1 deletion(-)
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git log
commit e70a505de5cb766f216ba40f983ab9106ace3e27 (HEAD -> main)
Author: marcelo.fjunior <marcelo.fjunior@aluno.faculdadeimpacta.com.br>
Date:   Fri Aug 2 02:11:24 2024 +0000

    Atualização do arquivo

commit b5eb3eff3856e1bcdb44240d9c55de7a4aa09ce8
Author: marcelo.fjunior <marcelo.fjunior@aluno.faculdadeimpacta.com.br>
Date:   Fri Aug 2 02:10:32 2024 +0000

    git add example - arquivo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo '*.txt' > .gitignore
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 'novo.txt' > novo.txt
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add .gitignore
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "add .gitignore para ignorar arquivos .txt"
[main 1fe2082] add .gitignore para ignorar arquivos .txt
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
nothing to commit, working tree clean
@mbfj ➜ /workspaces/codespaces-blank/exercicio01 (main) $ 