<h2>
    Clone and Status Commands
</h2><br>

<p>
    <b>Clone:</b> Cloning a repository on our local machine
    <i>
        git clone &lt;-some link-&gt;
    </i>

    <b>Status:</b> Displays the state of the code
    <i>
        git status
    </i>
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
</ol>
</p>
<hr>

<h2>Add and Commit Commands</h2>
<p>
    <b>Add:</b> adds new or changed files in your working directory to the Git staging area.
    <i> git add &lt;-file name-&gt;</i>

    <b>Commit:</b> it is the record of change
    <i>git commit -m "some message"</i>
</p>
<hr>

<h2>Push & INIT Command</h2>
<p>
    <b>Push:</b> upload local repo content to remote repository
    <i>git push origin main</i>
    <br>

    <b>Init:</b> used to create a new git repository
    <ul>
        <ol>
            <li>
                <b><i>git init</i></b><br>
                The git init command is used to initialize a new git repository or reinitialize an existing one. The
                git init command transforms the current directory into a Git repository, i.e., a . git directory
                with subdirectories for objects , refs/heads , refs/tags , and template files. It will also create a
            </li>
    
            <li>
                <i><b>git remote add origin &lt;-link-&gt;</b></i><br>
                The command git remote add origin
                &lt;link&gt; is used in Git to add a remote repository as a named alias, typically named 'origin', to your
                local repository. Here's what each part of the command means:
                <ul>
                    <li>
                        git remote: This part of the command tells Git that you're going to manage remote repositories.
                    </li>
                    <li>
                        add: This subcommand indicates that you want to add a new remote repository.
                    </li>
                    <li>
                        origin: This is the name you're giving to the remote repository. 'Origin' is a conventional name
                        used to refer to the - primary remote repository, but you can use any name you like.
                    </li>
                    <li>
                        &ltlink&gt: This is the URL of the remote repository you want to add. This URL typically points to
                        a Git repository hosted on a platform like GitHub, GitLab, Bitbucket, or a remote server.
                    </li>
                </ul>
                When you execute this command, you're essentially telling Git that the remote repository located at
                the provided URL should be associated with the name 'origin' in your local repository. After adding
                the remote repository, you can use commands like git push and git pull to interact with it.
            </li>
        </ol><br>

        <li>
            <i><b>git remote -v</b></i> to verify remote
        </li>
        <li>
            <i><b>git branch</b></i> to check branch
        </li>
        <li>
            <i><b>git branch -M main</b></i> to rename branch
        </li>
        <li>
            <i><b>git push origin main</b></i>
        </li>
        <li>
            <i><b>git push -u origin main</b></i>
            The command git push -u origin main is used in Git to push your local commits to a remote
            repository. Let's break down each part of the command:
            <ul>
                <li>
                    git push: This is the main command used to push your local commits to a remote repository.
                </li>
                <li>
                    -u or --set-upstream: This flag sets the upstream branch for the current local branch. When you
                    set an upstream branch, Git remembers the remote repository and branch you want to push to or pull
                    from, so you can use git push and git pull without specifying the remote branch name every time.
                    This is particularly useful for tracking changes between your local and remote repositories.
                </li>
                <li>
                    origin: This is the name of the remote repository. In Git, 'origin' is the conventional default
                    name given to the remote repository you cloned from. You can push your changes to this remote
                    repository.
                </li>
                <li>
                    main: This is the name of the branch you want to push your changes to on the remote repository. In
                    Git, the main branch is often called main, master, or develop, depending on the conventions used by
                    the project. Replace main with the appropriate branch name if it's different in your repository.
                </li>
            </ul>
            So, when you execute git push -u origin main, you're pushing the changes from your local branch
            (likely main or another branch) to the main branch on the remote repository named origin, and you're
            setting the upstream branch so that future pushes and pulls can be done without specifying the
            remote and branch again.
        </li>
    </ul>
</p>
<hr>

<h2>WorkGlow</h2>
<p>
    <b>Local Git</b>
    GitHub repository ---&gt; Clone ---&gt; Changes ---&gt; Add ---&gt; Commit ---&gt; Push
</p><hr>

<h2>Git Branches</h2>
<h4>Branch Commands</h4>
<p>
    <ul>
        <li>
            <i>git branch</i> to check branch
        </li>

        <li>
            <i>git branch -M main</i> to rename branch
        </li>

        <li>
            <i>git checkout &lt;- branch name -&gt;</i> to navigate
        <li>
            <i>git checkout -b &lt;-new branch name-&gt;</i> to create a new branch
            <ul>
                <li>This command is used to create a new branch and switch to it in one step.</li>
                <li>If the branch with the specified name already exists, Git will give an error.</li>
                <li>For example: <i>git checkout -b new_branch</i></li>
                <li>This command creates a new branch named new_branch and switches to it.</li>
            </ul>
            <b>Uses</b>
            <ul>
                <li>Use this command when you want to create a new branch and immediately switch to it.</li>
                <li>It's useful when you're starting work on a new feature or fixing a bug and want to work on it in isolation
                    from the main branch (usually master or main).</li>
                <li>For example, if you're starting work on a feature called "login-page", you would use: <i><b>git checkout -b
                    login-page</b></i></li>
                <li>This creates a new branch named login-page and switches to it, allowing you to start working on the
                    feature immediately.</li>
            </ul>
        </li>

        <li>
            <i>git checkout -B &lt;-new branch name-&gt;</i>
            <ul>
                <li>This command is used to either create a new branch or move to an existing branch, forcefully overwriting
                    the branch if it already exists.</li>
                <li>If the branch with the specified name already exists, Git will switch to it and reset it to the specified
                    commit or HEAD, effectively discarding any changes made to the branch.</li>
                <li>If the branch does not exist, Git will create a new branch with the specified name.</li>
                <li>For example: <i>git checkout -B existing_branch</i></li>
                <li>This command forcefully switches to the existing_branch, discarding any changes that were previously on
                    it.</li>
            </ul>
            <b>Uses</b>
            <ul>
                <li>Use this command when you want to switch to an existing branch or create a new branch, forcefully overwriting the branch if it already exists</li>
                <li>It's useful when you want to reset an existing branch to a specific state (like HEAD or a particular commit) or if you're sure you want to discard any changes on that branch.</li>
                <li>For example, if you want to discard any changes on an existing branch named bug-fix and reset it to the latest commit on master, you would use: <i><b>git checkout -B bug-fix master</b></i></li>
                <li>This switches to the bug-fix branch and resets it to the latest commit on master, effectively discarding any changes made on bug-fix.</li>
            </ul>
        </li>

        <li>
            <i>git branch -d &lt;-branch name-&gt;</i> to delete branch
        </li>
    </ul>
</p><hr>

<h2>Merging Code</h2>
<p>
    <b>Way 1</b>
    <i>git diff &lt;-branch name-&gt;</i> To compare commits, branches, files & more
    <i>git merge &lt;-branch name-&gt;</i> To merge 2 branches
        <br>
    
    <b>Way 2</b>
    <i>Create a PR (Pull Request)</i> A Pull request lets you tell others about cahnges you've pushed to a branch in a repository on GitHub.</i>
</p><hr>

<h2>Pull Command</h2>
<p>
    <i>git pull origin main</i> used to fetch and downliad content from a remote repository and immediately update
    the local repsutory to match that content.   
</p><hr>

<h2>Resolving Merge Conflicts</h2>
<p>
    <i>An event that takes place when Git is unable to automatically resolve diffrences in code between two commits.</i>
</p><hr>

<h2>Undoing Changes</h2>
<p>
    <b>Case 1:</b> Staged Changes
    <ul>
        <li>
            <i>git reset &lt;-file name-&gt;</i>
            This command is used to unstage changes made to a file. If you've already added changes to the staging area
            using git add, but you want to remove them from the staging area (while keeping the changes in your working
            directory), you can use git reset &ltfile&gt. For example: git reset example.txt
            This command removes example.txt from the staging area, but the changes in the file are still present in
            your working directory. You can then make further modifications to the file before staging and committing
            them again.
        </li>
        <li>
            <i>git reset</i>
        </li>
        <li>
            <i>git restore &lt;-file name-&gt;</i>
            This command is used to restore the contents of a file in your working directory to a specific state. It is
            similar to the git checkout command, but it's primarily focused on restoring files rather than switching
            branches or commits. For example: git restore example.txt
            This command restores the contents of example.txt to the state it was in the last committed revision.
        </li>
    </ul>
    
    <b>Case 2:</b> Commited changes (for one commit)
    <ul>
        <li><i>git reset HEAD~1</i></li>
    </ul>
    
    <b>Case 3:</b> Commited Changes (for many commits)
    <ul>
        <li><i>git reset &lt;-commit hash-&gt;</i></li>
        <li><i>git reset --hard &lt;-commit hash-&gt;</i></li>
    </ul>
</p><hr>

<h2>Fork</h2>
<p>
    A fork is a new repository that shared code and visibility settings with the original "upstream" repository.
    Fork is a rough copy.
</p>