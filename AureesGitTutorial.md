# Aurees Git Tutorial

This is a extremely quick tutorial showing you how to connect to and push/pull updates to and from git repos using Aurees. No commandline necessary! With Git, you can store multiple versions of files, instantly get updates from other team members, and even be able to try out or view what other developers have worked on! There's even an automatic version history keeper that will give developers the ability to roll back to an older version of the project in case of emergencies.

## 1: Make an account on Gitlab

For now, I decided to use gitlab.com because it has free private projects, compared to github's paid private option.

Make an account at https://gitlab.com/ and confirm with the link sent to your email. **IMPORTANT NOTE:** The email you use will be seen by anyone else part of the project, so keep that in mind!

Once that's done, it's time to install and configure Aurees!

## 2: Configuring Aurees and pulling your first repo

Install Aurees, agree to the usage agreement, and copy-paste the url to the repo in the text-box provided. You will see a folder path appear under the url, and you are free to select an empty folder for the repo. **IMPORTANT NOTE:** Anything you put in the folder can be seen by any other project members so _Keep that in mind._

A box will come up asking you to provide your email and password for gitlabs. Fill that out, and Aurees will automatically clone the repo and have it ready for you. With that, you're all done setting up aurees! All that's left is making sure your username/email that's listed in the project itself is what you want it to be, if not you can change it to whatever you'd like.

![](http://i.imgur.com/QccnPyX.png)

Onto actually using the program!

## 3: Using Git and RPGMAKER.

Now that you have git set up, if you open up rpgmaker and make a few changes, you will see the following changes to your screen.

![](http://i.imgur.com/wYy9kZy.png)

It may be self-explanatory, but we'll still go through this one step at a time.

1. This is the changes notification. All it does is tell you how many changes you have made since you last saved (or "committed")
2. This is essentially the "save". It takes all your changes and gets it ready to be sent to the server. All you have to do is click on the greyed out checkmarks (or the black checkmarks right above them to select them all), write a commit message and click on commit. Be sure to be descriptive!!
3. This is if you made a mistake and need to roll back to the beginning of the currently selected branch (more on that later)
4. This is a list of the modified files that haven't been committed.

With all that in mind, you just select all the files you wish to push to the server, write a detailed commit message, and then commit! All that's left is to click the "push" button here.

![](http://i.imgur.com/lW3vdY1.png)

and let the magic happen! Congratulations you made your first push and your commit is live for all the other developers to view and try out!

Whenever there is an update to the master branch (or any branch, again, I will explain more below) that you yourself didn't push, you have to pull it (aka download it) in order to be up to date. You do this by selecting the bull button next to push.


## 4: Advanced techniques using Branches, and the limits of the program.

One great feature of git are branches. Think of a branch as a copy of the base project which gets edited, saved separately from the base project, and when accepted is eventually merged into the main project, alongside any compatible changes made by anyone else! This allows asset-makers to apply their assets freely while map/event-makers can work on their maps.

There are a few problems that can arise, but first I'll show you how to create a branch, push it, request it to be merged to the master (or core) branch, and finally how to update your branch once it is outdated.

### Creating a branch

First things first, select the base branch you want your branch to be copied from. It can be any branch you want, but it is best if it is the master or development branch (if there is one). You can select the current branch you're working with by selecthing here.

![](http://i.imgur.com/npu3gPo.png)

As you can see, creating a branch is as easy as typing in the text box, while switching simply requires you to select one of the ones listed. You can name the branch whatever you like, but try to keep the name descriptive and include your name if possible (Like, Bramblewitch-Assets) Once you create a branch, you are free to make changes and push it as you please.

### Requesting a merge

Once you believe your branch is far enough along to be included in one of the main branches, you have to make a merge request.

Go to the project's page, and click on the branch option.

![](http://i.imgur.com/ddjx9u7.png)

Once selected you will see every branch related to the project. Find the project you want to merge and hit the button Merge Request

![](http://i.imgur.com/3Q19qq7.png)

On the next page, you can fill out the request and include a different title. If you want the merge to go to a different branch than the default, be sure to select click on the change branches link near the bottom.

![](http://i.imgur.com/23Z9hON.png)

Once you're done, click on the submit button and wait for someone to merge it for you!

### Updating outdated branch

As you can see, when one of the branches is updated, all the branches that split off from it are now out of date. However, as long as there aren't any conflicting changes, there is a very easy way to update it.

With the branch you wish to updape selected, select the Diff Merge Rebase dropdown menu and select Merge the recently updated branch (Master in this case)

![](http://i.imgur.com/RUzdY2U.png)

Once it reloads, push the new changes and you're good to go.

### Strengths and Weaknesses with Git with RPGmaker 2003

As you can see, rpgmaker can indeed work great with rpgmaker projects. Everyone can have an up-to-date copy, and in many cases, even use their out of date copies and still push good updates. However, there are some drawbacks as we aren't working with plain text.

The first drawback is creating maps in rpgmaker. Different people editing separate maps works completely fine with this set-up, and someone can even create new maps while someone else edits already made ones. However, more than one person cannot create a new map without taking turns. If this accidentally happens however, it will result in a conflict error which will result in the branch's folder needing to be backed up, deleted from local and public repos, and manually combined with the latest core branch by a combiner. However, this is only a fraction of the amount of combining the combiners would have to compared to not using git. The same goes for a single map that is edited by two people at once.

One way to avoid this is to create several maps in the beginning, organize them under the names of the mappers/eventers, and be sure everyone only works on maps organized under their names unless decided otherwise. Something like this

![](http://i.imgur.com/WywvYoD.png)

However, as long as everyone communicates what they're working on, if/when they create maps, and remembers to pull, push, and update their branches regularly, it won't be a problem.
