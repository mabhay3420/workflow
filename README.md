### Workflow we are going to use
```
	git clone repo_url
	git branch abhay_branch
	git checkout abhay_branch
	// Create a branch with similar name on github
```
Normal working on local branch
```
	git add .
	git commit -m "--"
```
Push only to your branch : When done working Create a pull request on Github and set the OP as reviewer
```
	git push --set-upstream origin abhay_branch
	// Needed only first time : After that simply "git push"
```
We want to have master This relationship:	master --> origin/master    and  abhay_branch --> origin/abhay_branch


Update both branches ( All ) with origin/master : origin/master Should contain all Approved work
```
	git checkout master
	git pull origin master

	git checkout abhay_branch
	git pull origin master
```
The last step might have some unwanted changes : Or A pull request from OP.

1. First check for Pull request
2. Review if any
3. Update your local branch after reviewing and merging the request


## Minimal Workflow	: After setup

```
	//Ensure no pending pull request on github
	git pull origin master
	//On branch master

	git checkout abhay_branch
	git pull origin master
	
	// update remote branch too
	git push

	// Do Changes

	git add .
	git commit -m "--"

	git push
	// Must create a pull request on github
	// Should push to origin/abhay_branch
```

Creating a pull request is important otherwise the process of update for OP will be cumbersome.