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
## Solving conflicts
Sometimes when you try to pull code from a colleague or when you try to merge your branch into another, you can have conflicts. This means the same file got changed in the same place by both versions and git does not know which one to keep or how to merge them together. In most cases you will get simple conflicts where you want to either keep your version or the other version, in these cases Github Desktop will give you a way to solve these conflicts very easily by just selecting to keep one version or another.
In any case, when a conflict happens git will change your file and add some weird markings to it. It will look something like this:

```
if(alive) {
<<<<<<< HEAD
  Die();
=======
  ContinueGame();
>>>>>>> master
}
```
In this example, you decided to call Die() when alive is true, and on master someone decided that ContinueGame() should be called instead.
To solve the conflict you always havo to delete the lines that start with "<<<<<<<" or ">>>>>>>" or "=======". And merge the code appropriately.
In this case you would have 4 options:
1) Call Die() and keep your own version discarding the other:
```
if(alive) {
  Die();
}
```
2) Call ContinueGame() and keep the version in master:
```
if(alive) {
  ContinueGame();
}
```
3) Merge the two by, for example calling Die() first and then ContinueGame()
```
if(alive) {
  Die();
  ContinueGame();
}
```
4) You can also decide to do something completely different:
```
if(alive) {
  KillAllOtherPlayers();
}
```

There are tools to help you find and fix all your conflicts for the major editors we use:\
[Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol#_merge-conflicts)\
[Rider](https://www.jetbrains.com/help/rider/Resolving_Conflicts.html#vcs-resolve-conflicts)\
Visual Studio has the feature but no clear documentation.

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
2. Make sure you have the Unity configurations noted [here](https://thoughtbot.com/blog/how-to-git-with-unity)

## Unity plugin

There is a unity github plugin that can help you configure everything and manage commits push pull etc all from within Unity.
Probably a good idea to try [GitHub for Unity](https://unity.github.com/).

