# An effort to rename racist language in computer terminology

Renaming default 'master' branch created by git to something more semantically appropriate like 'production', 'release', or 'main'. Looking into other languages that have already begun this effort in development.
    
This was inspired by a tweet from @leahculver [https://twitter.com/@leahculver]

[https://twitter.com/leahculver/status/1269109776983547904]
> @leahculver [https://twitter.com/@leahculver]
> I refuse to use “whitelist”/“blacklist” or “master”/“slave” terminology > for computers. Join me. Words matter.

To which I retweeted and said:

[https://twitter.com/haveboard/status/1269287535072751616]
> @haveboard [https://twitter.com/haveboard]
> git operation:kill your masters” starts today.
> 
> `production` or `release` seem more semantically correct anyways.
> 
> #gitoperationkillyourmasters
> #operationkillyourmasters
> #gitkillyourmasters
> 
> [https://stackoverflow.com/questions/8762601/how-do-i-rename-my-git-master-branch-to-release]
> ```bash
>git checkout -b release master    # create and >switch to the release branch
>git push -u origin release        # push the release >branch to the remote and track it
>git branch -d master              # delete local >master
>git push --delete origin master   # delete remote >master
>git remote prune origin           # delete the >remote tracking branch
>```
>
>
> Words matter (The “kill” In this respect is in reference to a non-violent action of changing a programming convention)
>
> #peacefulprotest
>

 I did start converting repos this week and will continue to document here whatever I find that might be helpful.

## Goals

Provide a collection of resources to make renaming things straightforward and provide examples for multiple scenarios.

Long term goal would be to see `git` and other tools to implement this renaming from a default level in future releases.

## Suggested Alternatives
 - `production`
 - `prod`
 - `main`
 - `release`
 
## Github and Bitbucket default branch settings

Github and Bitbucket require slightly different settings in order to accomplish these changes.

### GitHub

From your repository you need to go to `Settings` -> `Branches` and set the defaut branch to your new branch before removing the `master` branch.

### Bitbucket

From your repository you need to go to `Repository settings` -> `Branching model` and set the defaut branch to your new branch before removing the `master` branch.

## Examples

```bash
## from `git init`
## replace _BRANCH_NAME_ with what you would like to replace master with
git init
git symbolic-ref HEAD refs/heads/_BRANCH_NAME_
```
[version control - How do I rename my git 'master' branch to 'release'? - Stack Overflow](https://stackoverflow.com/questions/8762601/how-do-i-rename-my-git-master-branch-to-release?)


```bash
## Existing master branch to rename
## replace _BRANCH_NAME_ with what you would like to replace master with
git checkout -b _BRANCH_NAME_ master    # create and switch to the release branch
git push -u origin _BRANCH_NAME_        # push the release branch to the remote and track it
git branch -d master                    # delete local master
git push --delete origin master         # delete remote master - bitbucket you need to set default branch in repository settings first
git remote prune origin                 # delete the remote tracking branch
```
[Google Groups](https://groups.google.com/forum/?fromgroups#!searchin/git-users/master%7Csort:date)
 
## django and drupal have already made efforts here

hat tip to @mikeyp [https://github.com/mikeyp] for pointing this out

Drupal
[https://www.drupal.org/project/drupal/issues/2275877?fbclid=IwAR0CoST6cvPVXK3cyJwmYFeoY7OppykCCpKOFd08KOTWRbaRy-Y5Bdjucdg]
Django
[https://github.com/django/django/pull/2692]
[https://github.com/django/django/commit/beec05686ccc3bee8461f9a5a02c607a02352ae1]

## Links
Wiki reference:
[https://en.wikipedia.org/wiki/Master/slave_(technology)]

Wrong Answers only thread on twitter:
[https://twitter.com/talia_nassi/status/1271547824493285376]


### Inspiration

Thank you to Run the Jewels [https://runthejewels.com/] for the metaphor that I borrowed for the name of this project.

[https://www.youtube.com/watch?v=pg0byaqVaXo]
[https://www.daylightcurfew.com/collections/kill-your-masters]
