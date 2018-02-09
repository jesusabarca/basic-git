# Git
# Awesomeness

---
## Characteristics

* Distributed version control
* Snapshots, not differences
* Integrity by using SHA-1 checksums
* Fast by doing operations locally

---
### Local version control

![Local version control](images/local_vs.png)

---
### Centralized version control

![Centralized version control](images/centralized_vs.png)

---
### Distributed version control

![Distributed version control](images/distributed_vs.png)

---
### Snapshots, not differences

![Changes based version control](images/changes_vs.png)
![Snapshots based version control](images/snapshots_vs.png)

---
### Integrity by using
### SHA-1 checksums

```ruby
require 'digest'

Digest::SHA1.hexdigest '<some awesome code>'
=> "ad23275837d17962d3deaa004d663e76c4fb17f1"
```
---
### Fast by doing operations
### locally

```bash
$ ls -a

drwxr-xr-x   7 jesus  staff   224B Feb  9 11:47 ./
drwxr-xr-x@  7 jesus  staff   224B Feb  1 16:30 ../
drwxr-xr-x  11 jesus  staff   352B Feb  9 11:47 .git/
-rw-r--r--   1 jesus  staff    13B Feb  1 17:03 config.yml
drwxr-xr-x   7 jesus  staff   224B Feb  9 11:39 images/
drwxr-xr-x  12 jesus  staff   384B Feb  9 11:29 slides/
-rw-r--r--   1 jesus  staff   998B Feb  9 11:47 slides.md
```

---
## Basic config

```bash
$ git config --global user.name "Jesús Abarca"
$ git config --global user.email jesus@abarca.xyz
```

---
## Getting a repo

* Initialize a new repo
```bash
$ git init
```
or:

* Clone an existing repo
```bash
$ git clone https://github.com/jesusabarca/basic-git.git
```

---
## Checking the status
## of a repo

```bash
$ git status
```

```bash
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   slides.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        config.yml
        images/
        slides/
```

---
## Untracked
## vs
## tracked files

---
## Ignoring files

```bash
$ cat .gitignore
```

```bash
*.a
build/
doc/*.txt
```

* Ignoring new files
vs
* Ignoring already tracked files

---
## Three states of
## "tracked"

![States of tracked](images/states_of_tracked_vs.png)

---
## Staging changes

```bash
$ git add some_file.rb
```

* Staging untracked files
vs
* Staging already tracked files

---
#### Note: a file can be on different
#### states of "tracked" at once

```bash
$ git status
```

```bash
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   slides.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   slides.md
```

---
## Viewing changes

* Unstaged changes

```bash
$ git diff
```

* Staged changes

```bash
$ git diff --staged
```

---
## Commiting changes
## (snapshots)

* With text editor

```bash
$ git commit
```

```bash
$ git config --global core.editor nvim
```

* Inline comment

```bash
$ git commit -m 'An awesome commit message.'
```

---
## Removing files

```bash
$ rm slides.md
```

```bash
$ git add slides.md
```

---
```ruby
[:a, :b].each do |a|
  puts a
end
```

# Slide 2

Is less important
