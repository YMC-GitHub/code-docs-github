## basic do

- [x] set git default branch
```bash
git config --global init.defaultBranch main
```

- [x] ini git repo
```bash
[ ! -e .git ] && git init;
```

- [x] set user name and email
```bash
git config --global user.name "yemiancheng" ;git config --global user.email "ymc.github@gmail.com";
```

- [ ] change the master branch to "main" from "master"
```bash
git branch -M main
```

- [ ] change the master branch to "main" from "master" (remote github repo)
```powershell
git push -u origin main
# put the main branch in github repo (webui)
# ...
# then:
# git push origin --delete master


# If other people on your team have local clones of the repository:
git checkout master
git branch -m master main
# Get the latest commits (and branches!) from the remote:
git fetch
# Remove the existing tracking connection with "origin/master":
git branch --unset-upstream
# Create a new tracking connection with the new "origin/main" branch:
git branch -u origin/main
```

[refer:1 git-rename-master-to-main/](https://www.git-tower.com/learn/git/faq/git-rename-master-to-main/)

- [x] add github repo (in plan)
```bash
# copy token files to current project
# cp /d/code/shell/github-cli/secrets/* ./secrets


workspace=$(pwd);
cd /d/code/shell/github-cli;shfile=./index.sh;
repourl="ymc-github/code-docs-github";repodesc="code docs in markdown for github preview";

# add repo with default desc
$shfile $repourl add # (in plan)
# put repo desc
$shfile "$repourl" put "$repodesc" # (process)
# $shfile $repourl del

cd "$workspace"
```



- [x] add remote repo url
```bash
# git remote add origin https://github.com/YMC-GitHub/code-docs-github.git
git remote add origin git@github.com:YMC-GitHub/code-docs-github.git

# git remote add github https://github.com/YMC-GitHub/code-docs-github.git
# git remote add github git@github.com:YMC-GitHub/code-docs-github.git
```

- [x] set gitignore and commit it
```bash
git add .gitignore;git commit -m "build(core): add gitignore";
git add .gitignore;git commit -m "build(core): set note for go allow list";
git add .gitignore;git commit -m "build(core): put gitignore to design project dirs";
```

[fefer: some gitignore template](https://github.com/github/gitignore)


- [x] set edifotconfig and commit it
```bash
git add .editorconfig ; git commit -m "build(core): add editor config";
```

- [x] set license and commit it
```bash
git add LICENSE ; git commit -m "build(core): add license";
```

- [x] set readmd and commit it
```bash
git add README.md ; git commit -m "docs(core): add readme";
git add README.md ; git commit -m "docs(core): put readme to update pass.p1 usegae";
git add README.md ; git commit -m "docs(core): put readme to update ps1 usage";
git add README.md ; git commit -m "docs(core): put readme to note powershell trending in github";

```

- [x] set gitattributes and commit it
```bash
git add .gitattributes ; git commit -m "build(core): add gitattributes to manage large files";

git add .gitattributes ; git commit -m "build(core): set language type displayed by repository repo";

git add .gitattributes ; git commit -m "build(core): disable other with linguist-detectable for md";
```

[refer:1 changing-your-repo-s-language-in-github](https://dev.to/katkelly/changing-your-repo-s-language-in-github-5gjo)

[refer:2 linguist in github](https://github.com/github-linguist/linguist)

- [ ] get time with format
```bash
format="+%Y-%m-%d %H:%M:%S";time="2021-05-18 13:12:19";date -d "$time" "$format";
```

- [ ] git commit files with custom date
```bash
git commit -m "chore(core): update readme in github action" --date "$(date "+%Y-%m-%d %H:%M:%S" -d "+8 hour") +0800"
```

- [ ] design project dirs
```bash
git add release_win/.gitignore;git commit -m "build(core): add gitignore to design project dirs";
git add release_win/README.md;git commit -m "docs(core): output *.exe files here";
git add release_win/*.ico;git commit -m "build(core): output icon files here";


git add icons/.gitignore;git commit -m "build(core): add gitignore to design project dirs";
git add icons/README.md;git commit -m "docs(core): put icon files here as resources";
git add icons/*.ico;git commit -m "build(core): add resources files icon";

git add .vscode/.gitignore;git commit -m "build(core): add gitignore to design project dirs";
git add .vscode/README.md;git commit -m "docs(core): put vscode editor config files of project level here";

git add dist/.gitignore;git commit -m "build(core): add gitignore to design project dirs";
git add dist/README.md;git commit -m "docs(core): build powershell script files to here";
```

- [ ] add docs about how to setup this
```bash
git add README.01-SETUP.md ; git commit -m "docs(core): add readme to setup this";
```

- [ ] add docs about how to code before coding
```bash
git add README.02-BEFORE-CODE.md ; git commit -m "docs(core): add readme to code this";
```

- [ ] add docs about some libs i noted
```bash
git add README.03-LIB-NOTE.md ; git commit -m "docs(core): add readme to note libs";
```

- [ ] add go code snippets in project level
```bash
git add .vscode/.gitignore;git commit -m "build(core): add go code snippets in project level";
git add .vscode/go.code-snippets;git commit -m "docs(core): add go code snippets";
```

- [ ] add hello world in root dirs
```bash
git add main.go;git commit -m "build(core): add hello world in root dirs";
```

- [ ] add go mod and workspace
```bash
git add go.mod go.sum go.work.sum;git commit -m "build(core): add mod and workspace";
```

- [ ] add mod chapter01
```bash
git add src/chapter01/higo;git commit -m "build(core): add mod chapter01";
```

- [x] add powershell program
```bash
git add dist/pass.ps1 ; git commit -m "feat(core): add program to encode string for your password or something";
git add dist/pass.ps1 ; git commit -m "feat(core): put program to enale help and version";

git add dist/edit-env-path.ps1 ; git commit -m "feat(core): add program to set or get env path value";
git add dist/edit-env.ps1 ; git commit -m "feat(core): add program to set or get env value";
```


- [x] push to github repo (the first)
```bash
git push -u origin main
```

- [ ] replace git protocol with https when failed
```bash
# set
git config --global url."https://".insteadof git://
# unset
# git config --global --unset url."https://".insteadof 
```

- [x] rename github repo remote name from "origin" to "github"
```bash
git remote rename origin github
```

- [ ] remove github repo remote
```bash
git remote remove github
```

- [ ] set remote repo url from https to git
```bash
git remote set-url origin git@github.com:YMC-GitHub/code-docs-github.git
# git remote set-url github git@github.com:YMC-GitHub/code-docs-github.git
```


- [x] speedup github for `git clone`
```bash
# set
git config --global url."https://ghproxy.com/https://github.com".insteadOf "https://github.com"
# unset
# git config --global --unset url."https://ghproxy.com/https://github.com".insteadOf 
# get
# git config --global url."https://ghproxy.com/https://github.com".insteadOf
```

- [x] unset speedup github for `git clone` when pushing
```bash
# unset
git config --global --unset url."https://ghproxy.com/https://github.com".insteadOf 
```


- [x] mgnt git credential
```powershell
# git config --global credential.helper manager
# git config --global credential.helper cache
# git config --global --unset credential.helper
# https://zhuanlan.zhihu.com/p/157751660
```



- [x] add docs about using git for this repo i noted
```bash
git add README.04-GIT.md ; git commit -m "docs(core): add readme to note git for this repo";
git add README.04-GIT.md ; git commit -m "docs(core): put readme to note git for this repo";

```

- [ ] use readme.05-ssh.md file from remote file
```bash
curl -sfLO https://ghproxy.com/https://raw.githubusercontent.com/ymc-github/smallgo/main/README.05-SSH.md
```

- [x] add docs about using ssh in github i noted
```bash
git add README.05-SSH.md ; git commit -m "docs(core): add readme to note ssh";
```

- [x] add docs about using gpg in github i noted
```bash
git add README.06-GPG.md ; git commit -m "docs(core): add readme to note gpg";
```

- [x] add docs about choose open code license i noted
```bash
git add README.07-Licnese.md ; git commit -m "docs(core): add readme to note open code license";
```

- [x] add docs about huggingface i noted
```bash
git add README.HF.md ; git commit -m "docs(core): add readme to note huggingface";
```

- [x] set pull action for this repo
```bash
# zero:knowledge:s:pull-action
# you must know .
# git config pull.rebase false  # merge
git config pull.rebase true   # rebase
# git config pull.ff only       # fast-forward only
# zero:knowledge:e:pull-action
```

- [x] keep workspace clean before pulling
```bash
# git stash
```

- [x] pull remote github repo before pushing again
```bash
git pull origin main
# git pull github main
```

- [x] push remote github repo (no the first time)
```bash
git push origin main
```


- [ ] add requirements
```bash
git add requirements.txt ; git commit -m "build(core): add requirements nodes";
```

- [ ] add current custom nodes
```bash
git add __init__.py YMC_Node_Suite.py; git commit -m "feat(core): add custom nodes";
```

- [ ] move *.ps1 from dist to scripts
```bash
git mv dist scripts
git add scripts ; git commit -m "refactor(core): build powershell script files to here";
git add README.md ; git commit -m "docs(core): build powershell script files to here";
```

- [ ] enalbe get-help for *.ps1
```powershell
# get-help get-item -online 
# get-help scripts\pass.ps1
# get-help scripts\edit-env.ps1
git add scripts/pass.ps1 ; git commit -m "feat(core): enalbe get-help for pass.ps1";
git add scripts/edit-env.ps1 ; git commit -m "feat(core): enalbe get-help for pass.ps1";
git add scripts/edit-env-path.ps1 ; git commit -m "feat(core): enalbe get-help for this ps1";
```

- [ ] add go powershell snippets in project level
```bash
git add .vscode/.gitignore;git commit -m "build(core): add ps1 code snippets in project level";
git add .vscode/powershell.code-snippets;git commit -m "docs(core): add ps1 code snippets";
```