## Player: GreyGods
## Goal
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)
## Hints
+ `git branch -a` will let you see available branches
+ How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
+ Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
## Solution

```bash
─[parrot@parrot]─[~/picoCTF_2024]
└──╼ $unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/96/
 extracting: drop-in/.git/objects/96/f7309de67d785ec0b93b8766ff2882bef5c3ef  
   creating: drop-in/.git/objects/8c/
 extracting: drop-in/.git/objects/8c/1d254e2da6713e33acd6d622fc1dae357ec3c6  
   creating: drop-in/.git/objects/3d/
 extracting: drop-in/.git/objects/3d/5ec8a26ee7b092a1760fea18f384c35e435139  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/e1/
 extracting: drop-in/.git/objects/e1/237df82d2e69f62dd53279abc1c8aeb66f6d64  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
┌─[parrot@parrot]─[~/picoCTF_2024]
└──╼ $ls
challenge.zip  drop-in
┌─[parrot@parrot]─[~/picoCTF_2024]
└──╼ $cd drop-in/
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $ls
message.txt
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $cat message.txt 
TOP SECRET
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git branch -a
* master
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git log
commit e1237df82d2e69f62dd53279abc1c8aeb66f6d64 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:14 2024 +0000

    remove sensitive info

commit 3d5ec8a26ee7b092a1760fea18f384c35e435139
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:14 2024 +0000

    create flag
┌─[✗]─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git branch -a
* master
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git checkout master 
Already on 'master'
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git branch -a
* master
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git branch -a
* master
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git reflog
e1237df (HEAD -> master) HEAD@{0}: checkout: moving from master to master
e1237df (HEAD -> master) HEAD@{1}: commit: remove sensitive info
3d5ec8a HEAD@{2}: commit (initial): create flag
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $git checkout 3d5ec8a
Note: switching to '3d5ec8a'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 3d5ec8a create flag
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $ls
message.txt
┌─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $cat message.txt 
picoCTF{s@n1t1z3_30e86d36}
````

## Notes

## References