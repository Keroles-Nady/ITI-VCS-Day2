# ITI Version Control System

Lab #2 Answers...

## Create a new project on your local machine then push it to your remote repo.

![01](https://github.com/Keroles-Nady/ITI-VCS-Day2/assets/69374852/cf377e3f-6877-4ae9-a880-98343b8b4e60)


## Create an annoted tag with tagname v1.4.

![03](https://github.com/Keroles-Nady/ITI-VCS-Day2/assets/69374852/a0c1a980-d5eb-451c-9260-97742eb23600)



## How to remove branches locally and remotely?

- Delete a local Git branch
```
    # git branch -d <branch_name>
    It only works if the branch has been sucessfuly merged.

$ git branch -d test

    # git branch -D <branch_name>
    If the branch has not been merged.

$ git branch -D test
```
- Delete a remote Git branch
```
    # git push <remote> :<branch_name>
![Screenshot from 2023-11-27 14-11-51](https://github.com/Keroles-Nady/ITI-VCS-Day2/assets/69374852/dff89689-4aff-4aac-8a4d-9218ea5e98c4)

$ git push origin :test
```


## How to list tags locally?
```
$ git tag
```

## How to delete tag locally and remotely?
- Delete a local Tag
```
$ git tag -d v1.4
```

```
$ git push --delete origin v1.4
$ git push origin :refs/tags/v1.4
```

## What is git rebase? Give me an example.
is a Github utilities to integrate changes from one branch onto another.
It's the process of combining or moving a sequence of commits on top of a new base commit. Git rebase is the linear process of merging.


Use Case:
We are a team working on a project, one of our developer, has a long task "on another branch {Feature}", meanwhile the rest of the team has been making progress in the project "main branch" and add many contributes.

This developer wants to be up to date with all changes in the master branch so he has 2 ways to do that.

![My Remote Image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Git_Rebase_1.PNG)


### - merge master branch onto his own branch using git merge.
```
$ git merge main
```
This creates a new merge commit to merge these changes into his own branch.

![My Remote Image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Git_Rebase_2.PNG)



### - Rebasing branches.
```
$ git rebase main
```
This basically putting one branch on top of the another one.


![My Remote Image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Git_Rebase_3.PNG)

Here we moved the branch of feature on the main branch.
