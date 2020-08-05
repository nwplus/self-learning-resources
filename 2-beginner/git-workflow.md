# Git Workflow & Common Pitfalls/Mistakes

## **git workflow**

1. (first time setup) clone the repository `git clone https://github.com/dryu99/infinite-animal-crossing-lofi.git`
    - what does cloning the repository mean?
        - you're "grabbing" the latest version of the code from GitHub
        - you only need to do this once at the beginning
        - this is what it could look like
![git setup photo 1](https://i.imgur.com/w8Ww9U2.png)

2. check out a new branch `git checkout -b NAME-OF-BRANCH`
    - it should look like this:
        - the name of the **default** branch in my example is called `CREDITSS` (shown in a blue colour)
            - the default branch is called `master` by default, although it varies by repository
        - we checked out to a new branch called EXAMPLE
![git setup photo 1](https://i.imgur.com/CSaDxcv.png)        
    - checking out a new branch means that you're working on a different version
        - like a paper - this means you're working on a draft involving one idea for the final paper
        - you don't want to work on the idea directly on the final paper but rather on a draft
        - if you don't use the "draft" having branches makes it easier to not include it
        - if you do use the "draft" you can easily put it in the final paper - master
3. make your changes, go wild!
    - you can add something to the README or do some code!
4. tell git to track your changes by doing `git add .`
    - try to do this in the beginning before you start making any changes
    - `git add .` will add ALL changes; you can add only some changes by specifying a file instead of `.`
5. save your changes and give it a meaningful name by doing `git commit -m "describe your changes here"`
6. double check to see what git is keeping track of by doing `git status`
7. push those changes up to github `git push origin NAME-OF-BRANCH`
8. go to github and make a pull request!
9. merge it into master branch 

## Common Pitfalls/Mistakes

### **common pitfalls**

1. help! what do i do if my git says "failed to push some refs to origin"
    1. you wanna pull your changes and do `git pull origin master`
2. help! i wanna revert to an earlier version!
    1. find the last time you saved your work by doing `git log` and keep track of the hash
    2. then `git reset --hard <hash>`
3. how do i update my local version to be up to date with github?
    1. `git pull origin NAME-OF-BRANCH` will update the a specific branch
4. how do i switch branches?
    1. `git checkout NAME-OF-BRANCH`

### common mistakes

- not including spaces between your commands `gitcommit` vs `git commit`
- not pushing or pulling your repository
    - not pulling -this means that you aren't working on the latest version of the project
    - not pushing - that means you haven't uploaded the latest version of the project
- working on the wrong branch
    - you meant to do it in branch A but you did it in branch B
    - check which branch you're on in git
- working on the master directly (if there are multiple people working or different versions)
    - similarly to a paper, it would be as if you're working on the final paper rather than a draft
    
