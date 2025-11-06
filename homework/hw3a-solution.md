# HW3A Solution - Git and Version Control

## Part 1: Repository Cloning

I successfully cloned the class repository from `https://github.com/olearydj/INSY6500` to `~/insy6500/class_repo`.

### Key Commands Used

- `git clone <url>` - Create local copy of remote repository
- `git log` - View commit history
- `git remote -v` - Check remote repository connections

## Part 2: Portfolio Repository Creation

I created my personal course repository with:
- Professional README.md describing the project
- Proper .gitignore to exclude unnecessary files
- Organized directory structure for homework, projects, and notes

### Understanding Git Workflow

The three-stage workflow:
1. Working Directory: Where I edit files
2. Staging Area: Where I prepare commits with `git add`
3. Repository: Where commits are permanently stored with `git commit`

## Part 3: GitHub Publishing

Successfully published repository to GitHub:
- Used `git remote add origin` to connect local repo to GitHub
- Used `git push -u origin main` to upload commits
- Verified all files and commits are visible on GitHub

### The Remote Connection

My local repository is now connected to GitHub:
- `git remote -v` shows the remote URL
- `git push` will send my commits to GitHub
- `git pull` will get updates from GitHub (if changes are made on GitHub)

### Details

- Repository URL: https://github.com/nnineeight/py4eda-work

- Output of `git remote -v`: 
origin  https://github.com/nnineeight/INSY6500 (fetch)
origin  https://github.com/nnineeight/INSY6500 (push)

- The output of `git log --oneline`:
91f0b1a (HEAD -> master, origin/master) Remove wrong file named h3a-solution.md
d804a50 Add hw3a solution document
8aa9fa9 Add h3a solution document
0939804 Initial commit: Add README and .gitignore

## Questions

### Reflection Questions

*Question 1*

(a) Well, before learning about command line prompt and git commands, I mostly stored different versions of my work
with varying naming extensions (such as v1, v2, v3 etc.). That way of storing different versions were tedious, confusing, and
more prone to naming mistakes. Git commands cuts off these issues by offering convenient ways of handling, publishing, and
sharing documents.Git provides a very clear version control with access to go back to an earlier version if something wents
wrong. It also creates an extensive clone of any repository and lets anyone work and commit changes offline, without having to
rely on a single central server for version handling.

(b) When I was working on a thermophysical model in Python, everytime there was a error or invalid result I had to check what went
wrong and where manually. It was a very exhaustive process as I couldn't fully remember what I did that made it produce such
results. If I had been using Git with proper commits, I could have looked at the commit history to see the what I did actually and
I could also have reverted to a previous version or fixed the error very easily. In other words, Git's history would have turned 
guessing what I changed into seeing what was actually changed, making debugging much faster for me.

*Question 2*

(a) Keeping `class_repo` separate from `my_repo` prevents the mixing of documents that I got from the instructor (lectures, code
examples, class excercises etc.) with stuffs that I am/will be changing (homeworks, notes, project etc.). Had I put everything in
a single repository, my own edits would have been tangled with the instructor's documents. This would have eventually resulted in
conflicts whenever I tried to pull updates. Instead of providing a clear and concise way of version control, it would have created
mess in the repositories.

(b) For a group project, I would create a totally separate repo that is shared with my group members so that everyone can do
their parts, commit changes, and review changes. This way, I won't mix my personal repository with the group stuff.
For individual works or assignments, I would create separate repositories for each course. It would keep the course stuffs separate
from getting all mixed up.
The reference repo would be cloned from the instructor/TA and I would only pull updates from the repo.

*Question 3*

(a) The second one is much more comprehensive and useful. It tells me what I added and what it is about, whereas the first commit
message tells me nothing except that I have updated something in the repo. It would be useful later on to verify that I did the
solution and what was the topic for it. It will also help me if I need to fix something in the document, or to reuse that work etc.
(P.S.: Thanks for the best practice guides for Git Commit).

(b) For the data analysis project, I will commit whenever I finish doing a meaningful step. These might include “loaded and cleaned
raw CSV data”, “added engineered features”, “plotting of solar rad”, etc. Instead of doing a big commit at the end of each week 
or a few days, which will mix my distinct but necessary smaller steps and harder to debug, I will commit frequently whenever I have
done something in the project that works, advances the project, etc.

### Graduate Questions

*Question 1*

(a) Committing `README.md` and `.gitignore` files first sets up the repository and tells us what the repository is for and what are
the things that we don't want in Git. After doing that, I committed the homework solution, which is the actual assignment work for
this repository. If we comit everything at once, comit history won't show which changes were for structuring the repo and which are
the actual homeworks. And importantly if I ever needed to pull back the homework file, I might end up pulling back the repo setup
too.

(b) I will commit these things now: write code to load data, fix typo in a comment, update the README file; the only action for 
which I will wait on is the half-finished work on a new analysis function.
The first three aforementioned actions are complete, but the half-finished work is not completed yet, so it won't be committed
right now.
Staging helps me to pick which actions are completed and ready to be committed, leving unfinished or half-finished things behind.
I guess staging helps to separate completed actions from others even though everything is in the same directory or folder.

(c) `git status` tells me which files are new or not tracked, which files have been modified but not staged yet, and which files
are staged and will go into the next commit. This makes decision making process easy. If I see a file in modified which is actually
half-done, I don't stage that, instead I `git add` the completed files.
`git status` command should be run frquently. We should run in right after making any change to a file, before staging that file,
and before committing that file. It is so that I can double check that only the completed files are being committed.

*Question 2*

(a) Distributed version control means that each time I'm cloning the repository, I'm creating a full copy of the project's history.
Here everyone has a complete, self-contained copy of the original repository with its full history. There is no need of connecting 
to the central server of the original repository in order to do work.
This is very different from Google Drive or Dropbox, which are cloud storage services focused on file storage, sharing etc., where
files are synced copies of the original. Google Drive/Dropbox contains the latest versions of the uploaded documents, whereas Git
has the entire project with its complete history. Drive/Dropbox are online-dependent, but in Git one can work entirely offline.
Also, in Drive/Dropbox, all synchronization need to go through a central cloud server and no direct collaboration opportunity between two
individual user folders.

(b) Git enables a powerful, offline-capable working platform for developers where they have a copy of the original repository on
their local computer. It enables them to not entirely rely on network connectivity or fear about messing up with the original repo.
They can sync their work when they find it ready to be shared.
Git enables different workflows such as Centralized Workflow, Feature Branch Workflow, Forking Workflow etc. In Centralized
workflow, developers pull from and push to a single central repository. In the Feature Branch Workflow, they develop or fix a new
feature on a separate branch other than `main`, and once it is completed, that branch is merged back into the main branch. In
Forking Workflows, developers fork (i.e., copy) the entire repo, do their work on it and then propose changes to the original repo
through pull requests.

(c) `git clone` is the initial command that creates a complete local copy of the central repository on my computer, `git pull`
takes the latest changes from the original repository and then merges them into my local repository, and `git push` is the upload
command that sends my commits from local computer to a central repository. The relationship is that, `git clone` for setting up,
then repeated use of `git pull` and `git push` to get/send updates from/to central repo.

*Question 3*

(a) For committing, I will ask myself is this work complete or not, if it is then I can commit the change. Otherwise, I need to
finish the work first and then commit the changes. I will be committing changes with clear messages so that when I return to this
change I can know what I did here. The idea is that, I will keep my main branch clean while using the feature branches to show my
process. I can also clean up my main branch's history before a final push so that my main branch reamins as a final polished
report.

(b) A portfolio README file is to showcase a professional introduction about something. To be more specific, it is something
that will spark interest in peoples mind. Key things that will make this effective could be a demo usage link, brief overview,
tools used to create it, what are its key features, and my role in building this etc.
An Open-Source README file is more like a user manual that tells people how to install a particular technology/software, how to 
use it, its documentation, etc. For this type of README file, key effective things will be providing brief intro to this technology/
software, quick installation and documentation guide, use examples etc.

(c) Starting to build this portfolio now will revert from a last-minute task to a genuine record of my growth over the time period.
It will also develops things I can talk about during an interview, and I guess most importantly a consistent documentation habit 
and style. Last-minute actions might be fruitful but what's the point in doing stuffs like this!!!
I will try to develop some habits from now such as, updating README files immediately after finishing projects, keeping commit
history clean and meaningful, frequent use of Git commands to get used to, regular push and pull to keep my work always updated.


## Generative AI Disclosure

I have used Generative AI (ChatGPT 5 Thinking) for assistance during this assignment. Instead of using it answering questions, I
used this tool to learn things about Git that I did not know earlier. No answer in this assignment is copied or generated using 
Generative AI tool.

