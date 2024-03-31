<h1>Git Commands Reference</h1>

<h2>Clone and Status Commands</h2>

<p><strong>Clone:</strong> Cloning a repository on our local machine<br>
<code>git clone &lt;some link&gt;</code></p>

<p><strong>Status:</strong> Displays the state of the code<br>
<code>git status</code></p>

<ol>
    <li><strong>untracked:</strong> new files that Git doesn't yet track</li>
    <li><strong>modified:</strong> changed</li>
    <li><strong>staged:</strong> file is ready to be committed</li>
    <li><strong>unmodified:</strong> unchanged</li>
</ol>

<h2>Add and Commit Commands</h2>

<p><strong>Add:</strong> Adds new or changed files in your working directory to the Git staging area.<br>
<code>git add &lt;file name&gt;</code></p>

<p><strong>Commit:</strong> Records changes<br>
<code>git commit -m "some message"</code></p>

<h2>Push & INIT Command</h2>

<p><strong>Push:</strong> Upload local repo content to remote repository<br>
<code>git push origin main</code></p>

<p><strong>Init:</strong> Used to create a new Git repository</p>

<ul>
    <li>
        <code>git init</code><br>
        The git init command is used to initialize a new git repository or reinitialize an existing one.
    </li>
    <li>
        <code>git remote add origin &lt;link&gt;</code><br>
        The command git remote add origin &lt;link&gt; is used in Git to add a remote repository as a named alias, typically named 'origin', to your local repository.
    </li>
</ul>

<p>
    <code>git remote -v</code> to verify remote<br>
    <code>git branch</code> to check branch<br>
    <code>git branch -M main</code> to rename branch<br>
    <code>git push -u origin main</code> to push local commits to a remote repository
</p>

<h2>Workflow</h2>

<p>Local Git:<br>
GitHub repository ---&gt; Clone ---&gt; Changes ---&gt; Add ---&gt; Commit ---&gt; Push</p>

<h2>Git Branches</h2>

<h3>Branch Commands</h3>

<ul>
    <li><code>git branch</code>: Check branch</li>
    <li><code>git branch -M main</code>: Rename branch</li>
    <li><code>git checkout &lt;branch name&gt;</code>: Navigate</li>
    <li><code>git checkout -b &lt;new branch name&gt;</code>: Create a new branch</li>
</ul>

<h2>Merging Code</h2>

<p><strong>Way 1:</strong><br>
<code>git diff &lt;branch name&gt;</code> To compare commits, branches, files & more<br>
<code>git merge &lt;branch name&gt;</code> To merge 2 branches</p>

<p><strong>Way 2:</strong> Create a PR (Pull Request)</p>

<h2>Pull Command</h2>

<p><code>git pull origin main</code> used to fetch and download content from a remote repository and immediately update the local repository to match that content.</p>

<h2>Resolving Merge Conflicts</h2>

<p>An event that takes place when Git is unable to automatically resolve differences in code between two commits.</p>

<h2>Undoing Changes</h2>

<p><strong>Case 1:</strong> Staged Changes</p>
<ul>
    <li><code>git reset &lt;file name&gt;</code>: Unstage changes made to a file.</li>
    <li><code>git reset</code>: Resets the staging area.</li>
</ul>

<p><strong>Case 2:</strong> Committed changes (for one commit)</p>
<ul>
    <li><code>git reset HEAD~1</code></li>
</ul>

<p><strong>Case 3:</strong> Committed Changes (for many commits)</p>
<ul>
    <li><code>git reset &lt;commit hash&gt;</code></li>
    <li><code>git reset --hard &lt;commit hash&gt;</code></li>
</ul>

<h2>Fork</h2>

<p>A fork is a new repository that shares code and visibility settings with the original "upstream" repository. A fork is a rough copy.</p>
