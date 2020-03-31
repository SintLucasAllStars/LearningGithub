# LearningGithub

## Terms covered
### Repository
That's where your project lives
### Clone
Create a local version of your repository. You will work, add and commit on this version and then push it all to the server.
### Add
Add a new file to the project so that it's version gets tracked or mark your current changes to an existing file so that they get commited on the next commit
### Commit
Create a new version of your project locally with all the changes you have added. You should do this often, everytime you add a new feature or finish a part of your code. The more you do this the more control over your history you will have.
### Push
Send all the new commits to the server
### Pull
Update your local clone with anything new from the server.
### Diff
Check a file and compare the differences between two different versions of that file.
### Branch
This is similar to creating a separate copy of the project to develop a specific feature or test a solution. The two versions can evolve in parallel and you can jump from one to the other or merge them back into one at a future point.
### Merge
Takes all the changes from one branch and merges them to another.
### Checkout
move your local copy between different versions, for example go back to a past version or switch to a different branch.
### Fork
Create a FULL NEW repository based on this one. This is different from branching because it basically copys all your history into a new repository and makes an exact copy. This copy can in the future be merged into the original though.

## Other terms you can check on your own

### Tags
### Releases

## Workflow (Commandline)

1) Create repository on github.com
2) Clone repository to your local copy.
```
git clone https://....

```

3) code your awesome features
4) Add all modified files.
```
git add file1.txt file2.md file3.cs

```
5) Commit
```
git commit -m"What I have done..."

```
6) Push to the github server
```
git push
```

7) Git pull get latest version
```
git pull
```

8) Create a new branch for a feature or to isolate your work.

```
git checkout -b myNewBranchName
```



## Git with Unity

```
__  __      _ __       _____ ____
/ / / /___  (_) /___  _|__  // __ \
/ / / / __ \/ / __/ / / //_ </ / / /
/ /_/ / / / / / /_/ /_/ /__/ / /_/ /
\____/_/ /_/_/\__/\__, /____/_____/  
              /____/              
```
Using git with Unity has a few caveats. There are a lot of files being changed and managed by the editor and that cause chaos and conflicts very easily. Therefore here are some useful tips.

0. Use the Unity .gitignore from github (already included in our assignments).
1. Make sure your Unity Project lives IN THE ROOT of your repository. This means your Folder structure should be:
```
MyRepository <- ROOT
     |- .gitignore
     |- Assets
     |- Library
     |- ...
```

## Unity plugin

There is a unity github plugin that can help you configure everything and manage commits push pull etc all from within Unity.
Probably a good idea to try (GitHub for Unity)[https://unity.github.com/].

