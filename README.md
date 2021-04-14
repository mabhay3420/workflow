### Workflow we are going to use

git clone repo_url
git branch abhay_branch
git checkout abhay_branch
// Create a branch with similar name on github

// some change on this branch : Cannot push directly to origin master
// Can push to default branch only from local master branch

git add .
git commit -m "--"

git push --set-upstream origin abhay_branch
// Needed only first time : After that simply git push
// We want to have master --> origin/master    and  abhay_branch --> origin/abhay_branch	: This relationship


// An option of pull request should be present in github when switched to "abhay_branch" : for merging to main branch : Assign the OP as reviewer

//Update routine : updating main is unnecesary : avoid Merging local
//branch let's say "abhay_branch" with "master" branch and then pushing to 
// master branch : No option of pull request.

// e.g. assume some changes were done on branch "abhay_branch" locally 
// git checkout master
// git merge abhay_branch master
// git push	: will update origin/master directly : Undesirable

// What we will use

// Assume on branch "abhay_branch"

git add .
git commit -m "--"

git push	// assume --set-upstream origin abhay_branch already set
		// otherwise : git push origin abhay_branch


// Update routine : After reviewing OP's changes and merging the his branch
// with master

// Updating master is unnecessary : Avoid using the local master
// git checkout master
// git pull	// by default remote : origin/master : Can be done to have an updated local copy

// Update local branch regularly after reviewing changes
git checkout abhay_branch
git pull origin master

// Having said that Handle conflicts wisely : One pull request at a time
// Decide the parts each of us will be working on : Both wastes our time as well
// complicate the merging process
