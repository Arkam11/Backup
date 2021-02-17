##### 1. clone The remote repository
```
> git clone -b dev [URL remote library address]
```

##### 2. switch the local Dev branch and the local personal development branch, and replace the branch name you defined
```
> git checkout -b dev（//The current operation is under the local master branch）
> git checkout -b branch（//The current operation is under the local dev branch）
```

##### 3. Write the Code on the local personal development branch*
##### 4. Submit amendments to the local repository
```
> git add .（//The current operation is under the local personal development branch）
> git commit -m "write the code"（//The current operation under in the local personal development branch
```

##### 5. Switch the Dev branch, get the remote Dev branch and merge it into the local development branch
```
> git checkout dev（//The current operation is under the local personal development branch）
> git pull origin dev（//The current operation is under the local dev branch
> git checkout branch（//The current operation is under the local dev branch
> git rebase dev（//The current operation is under the local personal development branch）
To deal with conflict...
```

##### 6. After the conflict is resolved, will be re-submited to the local library, merged to the local dev branch, and submitted to the remote dev branch
```
> git add .（//The current operation is under the local personal development branch）
> git rebase --continue（//The current operation is under the local personal development branch）
> git checkout dev（//The current operation is under the local personal development branch）
> git merge branch（//The current operation is under the local dev branch）
> git push origin dev（//The current operation is under the local dev branch）
```

##### note: 
1. Pull the remote code on the local Dev branch every day and merge it into the local personal development branch
2. Code needs to be written on the local personal development branch
3. When resolving a conflict, do not delete code written by the others. Otherwise have to inform with them before you will delete.
4. Resolve the conflict only on the local personal development branch
5. The local dev branch has three steps: pull the remote dev branch, merge the local personal development branch into dev, and then push the remote dev branch after has been merged into dev