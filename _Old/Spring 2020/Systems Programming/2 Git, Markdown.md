# Git, Markdown

## Git
* Version control system designed to handle everything from small to very large projects with speed and efficiency

### Fundamental Ideas
#### Journal
* A ledger, keep track of work
* Keeps work in a repo that contains data and a journal that describes history of changed data
* Commits records to the journal

#### Time Machine
* Git can serve as a time machine 
* throw away changes
* revert to previous states

#### Shared Space
* Can be shared with multiple people
* Can merge in changes from different people
* Git alerts if there are merge conflicts

### Mental Model
#### Upstream (in cloud)
* Original repository 

#### Origin (in cloud)
* `fork` copy of upstream repository to a personal repo

#### Local
* `clone` origin to local repository
* `push` the new commits into the `origin`
* `pull` changes from `origin` into the local repository
* `checkout`  different points in the ledger
* 
* **Working Directory**
	* List of all changes and transactions and presents in local
* **Staging Area**
	* `add` to place "draft" of changes into a staging area
	* `commit` records the "draft" into a new entry in the local ledger

#### Branching
* `checkout -b` new branch
* `checkout` different branches