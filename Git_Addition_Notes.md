> Please enter a commit message to explain why this merge is necessary,
> especially if it merges an updated upstream into a topic branch.

It's not a Git error message, it's the editor as git uses your default editor.

To solve this:

1. press "i" (i for insert)
2. write your merge message
3. press "esc" (escape)
4. write ":wq" (write & quit)
5. then press enter

> ### 执行完commit后，想撤回commit

`git reset --soft HEAD^`

1. ##### HEAD^

   意思是上一个版本，也可以写成HEAD~1。如果你进行了2次commit，想都撤回，可以使用HEAD~2。

2. ##### --mixed 

   意思是：不删除工作空间改动代码，撤销commit，并且撤销`git add . `操作

   这个为默认参数，`git reset --mixed HEAD^` 和 `git reset HEAD^`效果是一样的。

3. ##### --soft

   不删除工作空间改动代码，撤销commit，不撤销git add . 

4. ##### --hard

   删除工作空间改动代码，撤销commit，撤销git add . 

   注意完成这个操作后，就恢复到了上一次的commit状态。

