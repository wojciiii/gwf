Git work flow (script)

```
gwf

What workflow do you want to execute?
Possible workflows:
cr <branch>  - create work branch.
pub          - pull followed by rebase.
th           - pull followed by rebase, take their version.
pr           - push ready branch.
am           - ammend last commit, edit message.
ac           - add modified files with commit message (work branch name).
reb          - list ten most recent branches.
lbr          - push local branch to remote server.
ec <message> - add empty commit with <message>.

More advanced usecases:
cp <branch> <id>
  Create <branch>. Cherry pick <id> and commiot it.
check
  Execute ${REPO_NAME}-check.sh script to execute any often executed checks prior to pushing.
  \{REPO_NAME} is the name of the gif repository in which this tool is executed.
  For this repository the script is located in /home/${USER}/.gwf/gwf-check.sh
```

Often used commands turned into simple workflows.

For example:
```
gfw cr update_something -> creates update_something branch tracking the remote main or master or whatever its called.
```
Update some files ..
```
gwf ac -> Create a commit with the changed files, use branch name as commit message.
```
Update some files ..
```
gwf am -> amend any changes to the , edit commit message.
gwf lbr -> push the branch with the same name as the local branch.
```

