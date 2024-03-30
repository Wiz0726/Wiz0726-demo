<h2>Clone and Status Commands</h2>
<br>
<b>Clone -</b> Cloning a repository on our local machine
<i>git clone <-some link-></i>

<b>Status</b> - Displays the state of the code
<i>git status</i>

<ol>
    We have 4 types of status
    <li>
        <b>untracked:</b> new files that git doesn't yet track
    </li>
    <li>
        <b>modified:</b> changed
    </li>
    <li>
        <b>staged:</b> file is ready to be committed
    </li>
    <li>
        <b>unmodified:</b> unchanged
    </li>
<ol>
<br>
<h2>Add and Commit Commands</h2>
<b>Add:</b> adds new or changed files in your working directory to the Git staging area.
<i> git add <-file name-></i>

<b>Commit:</b> it is the record of change
<i>git commit -m "some message"</i>
<br>
<hr>
<h2>Push Command</h2>
<b>Push:</b> upload local repo content to remote repository
<i>git push origin main</i>
<hr>
<h2>Innit Command</h2>
<b>Innit:</b> used to create a new git repository
<i>
    <ul>
        <li>git init</li>
        <b>
            The git init command is used to initialize a new git repository or reinitialize an existing one. The git init command transforms the current directory into a Git repository, i.e., a . git directory with subdirectories for objects , refs/heads , refs/tags , and template files. It will also create a new master branch.
        </b>
        <li>git remote add origin <-link-></li>
        <b>
        The command git remote add origin <link> is used in Git to add a remote repository as a named alias, typically named 'origin', to your local repository. Here's what each part of the command means:
        - git remote: This part of the command tells Git that you're going to manage remote repositories.
        - add: This subcommand indicates that you want to add a new remote repository.
        - origin: This is the name you're giving to the remote repository. 'Origin' is a conventional name used to refer to the - primary remote repository, but you can use any name you like.
        - &ltlink&gt: This is the URL of the remote repository you want to add. This URL typically points to a Git repository hosted on a platform like GitHub, GitLab, Bitbucket, or a remote server.
        When you execute this command, you're essentially telling Git that the remote repository located at the provided URL should be associated with the name 'origin' in your local repository. After adding the remote repository, you can use commands like git push and git pull to interact with it.
        </b>
        <li>git remote -v</li> <b>to verify remote</b>
        <li>git branch</li> <b>to check branch</b>
        <li>git branch -M main</li> <b>to rename branch</b>
        <li>git push origin main</li>
        <li>git push -u origin main</li>
        <b>
        The command git push -u origin main is used in Git to push your local commits to a remote repository. Let's break down each part of the command:
        - git push: This is the main command used to push your local commits to a remote repository.
        - -u or --set-upstream: This flag sets the upstream branch for the current local branch. When you set an upstream branch, Git remembers the remote repository and branch you want to push to or pull from, so you can use git push and git pull without specifying the remote branch name every time. This is particularly useful for tracking changes between your local and remote repositories.
        - origin: This is the name of the remote repository. In Git, 'origin' is the conventional default name given to the remote repository you cloned from. You can push your changes to this remote repository.
        - main: This is the name of the branch you want to push your changes to on the remote repository. In Git, the main branch is often called main, master, or develop, depending on the conventions used by the project. Replace main with the appropriate branch name if it's different in your repository.
        So, when you execute git push -u origin main, you're pushing the changes from your local branch (likely main or another branch) to the main branch on the remote repository named origin, and you're setting the upstream branch so that future pushes and pulls can be done without specifying the remote and branch again.
        </b>
    </ul>
</i>
<hr>

<h2>WorkGlow</h2>
<b>Local Git</b>
<p>GitHub repository ---> Clone ---> Changes ---> Add ---> Commit ---> Push </p>
<hr>
<h2>Git Branches</h2>
<h2>Branch Commands</h2>
<i>git branch</i> <b>to check branch</b>
<i>git branch -M main</i> <b>to rename branch</b>
<i>git checkout <- branch name -></i> <b>to navigate</b>
<i>git checkout -b <-new branch name-></i> <b>to create new branch</b>
<i>git branch -d <-branch name-></i> <b>to delete branch</b>