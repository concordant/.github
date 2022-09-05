# Contributing to projects in Concordant

Welcome, so you are thinking about contributing to PouchDB? Awesome, this is a great place to start.

## Pull requests

All bug reports, desired features, suggestions, etc to Concordant projects should be submitted using
`Issues`.

All contributions to Concordant projects should be made through `pull requests`, where you submit
your change for approval by the project `Maintainers`.
You can **NOT** commit directly to the `master` branch.
Note that the `master` and `dev` branches are protected so that:

- only maintainers can merge changes to `dev` and `master`
- pull requests are first merged to `dev`, then stable releases are merged to `master`

## Get in touch

The following documentation should answer most of the common questions about how to get starting contributing, if you have any questions, please feel free to get in touch @ the Issue menu in the current repository, or send a direct email to [our support](support@concordant.io).

## Pull Requests organisation

Each contribution should address an issue that has been previously created in the Github. These
issues are tickets that will be followed by one maintainer. The progress of issues can be followed
through the Github Issues board.

### Guide to creating an Issue

- Almost all Pull Requests for features or bug fixes will need tests
- You can create an Issue to the corresponding repository from its Issues menu
- Almost all Pull Requests for features or bug fixes will need tests
- We follow [Felix's Node.js Style Guide](https://github.com/felixge/node-style-guide)
- Almost all Pull Requests for features or bug fixes will need tests (seriously, it's really important)
- Commit messages should follow the following style:

```txt
(#99) - A brief one line description < 50 chars

Followed by further explanation if needed, this should be wrapped at
around 72 characters. Most commits should reference an existing
issue
```

Give an explicit title to your issue. You should also add a longer explanation in the `Description`
field.

### Labels

To ensure a better monitoring it is recommended to add one or more tags to your new issue using the
`Labels` multi choice menu on the right panel of the issue page.

#### Global labels

Here are described the global (group-level) labels:

##### Type
- ~"bug"			Something already done does not work for **users**
- ~"feature"			Functionnality related; prefer feature::* when possible
- ~"feature::addition"		New functionnality (with tests & doc)
- ~"feature::enhancement"	Enhancement to an existing feature (visible to the user)
- ~"feature::maintenance"	Code enhancement, not visible to the user
			  	  (cleanup, refactoring, dependency update…)
- ~"tooling"			Configuration of engineering tools ; prefer tooling::* when possible
- ~"tooling::workflow"		Configuration of build tools and linters
- ~"tooling::pipelines"		Configuration of CI/CD pipelines
- ~"documentation"		Documentation-only issue
- ~"meta"			Project management (tickets management, labels creation…)
- ~"support"			Support request for user;
				  may not imply any modification on our side
- ~"test"			Test-related issue: test failure or test-only improvement
- ~"security"			Security issue

##### Type Refinement
- ~"failure"			Failure of automated test
- ~"failure::investigating"	Failure of automated test: cause unknown
- ~"failure::broken-test"	Failure of automated test, due to a bug in tests
- ~"failure::stale-test"	Automated test was not updated to follow code modifications
- ~"failure::flaky-test"	Non-deterministic failure of automated test
- ~"failure::test-environment"	Failure of the testing infrastructure (runner…)

##### Severity for user
- ~"bug::blocking"		Broken feature that blocks the user, leads to data loss…
- ~"bug::critical"		Broken feature, workaround is possible but complex
- ~"bug::major"			Broken feature, with easy workaround
- ~"bug::minor"			Inconvenient

##### Feature classification
- ~"UI"				Related to UI

##### Workflow
- ~"suggestion"			Suggestion: poster is unsure issue is valid
- ~"discussion"			Needs discussion
- ~"design"             Design investigation
- ~"confirmed"			Issue confirmed
- ~"Workflow::Product Backlog"	Issue is refined and prioritised; ready to dev
- ~"Workflow::Sprint backlog"	Selected for current sprint, to do
- ~"Workflow::In Progress"	In current sprint, work being done
- ~"Workflow::Ready for review"	In current sprint, done, review in progress
- ~"Workflow::Ready for Release" Merged	into dev, ready for next release
- ~"blocked"		    	Waiting for another issue, or for dependency evolution
- ~"invalid"			Issue is invalid (bug is not reproducible,
  				  functionality already exists,
				  posted in wrong repository…)
- ~"wontfix"			Described behaviour is intentional
- ~"upstream"			Bug in a dependency, waiting for upstream
				  (outside of our control) to fix;
				  add link to upstream issue

#### Weight
- ~"Weight::0"
- ~"Weight::1"
- ~"Weight::3"
- ~"Weight::5"			To be refined
- ~"Weight::10"
- ~"Weight::30"
- ~"Weight::50"

#### Repository-specific labels

Can be added (sparingly) when needed.

##### Website
- ~Content			Related to website content, not code

### Board organization

The Github board is the one from the concordant organisation.

This board classes issues in 5 distinct status (one per column): `Open`, `To-Do`, `Assigned`, `Ready
for review`, `Closed`.

1. When you create an issue it will be automatically put as `Open`.

2. Later during development status meetings  we select `Open` tasks that should be done during the
next week(s). These tasks should be marked as `To-Do`.

3. During stand-up calls each person receives task(s) to be done for the next day(s). These tasks
should be `Assigned` to the person. To do so, in the issue page select the person responsible to
solve it with the `Assignee` multi choices menu. The task should be marked as `Assigned`.

4. When the tasks is completed the person submits a pull resquest and marks the task as `Ready for
review`.

5.  When the pull resquest is accepted the task automatically becomes closed.

To change the status of a task (e.g., from `To-Do` to `Assigned`) one can simply use drag and drop
in the board page or change the `Label` of the issue as described in the above section.

## Contributing through pull request

When a tasked have been `Assigned` to you, you should respond to it using a pull request by
following the below described steps.

### Create a branch for your contribution

For creating a branch directly from the Github website go to the targeted issue webpage. With the
green multi choices menu select `Create a branch`.

In your local machine you need to clone if you do not have it, or at least update it by running:

```shell
git pull
```

You should go to your new branch by running:

```shell
git checkout my_branch
```

You can also create a new branch in your local machine and if you already have cloned the project,
use the following command:

```shell
git checkout -b my_new_branch
```

You should also create a remote branch in the Github repository, for storing the changes you
perform. You do not need to do this immediately, but you will need to do it before submitting your
pull resquest. You can do this by running:

```shell
git push --set-upstream origin my_new_branch
```

For integrating the changes made into the master in your branch, you can execute the following
command:

```shell
git rebase origin/master
```

### Make your changes and save them

Perform your changes in the local files, and use git as usual.

For adding a new file, run:

```shell
git add filename
```

For committing your changes, run:

```shell
git commit -m "Say something relevant here"
```

A commit message should reflect your intention, not just the contents of the commit. The commit
message should explain **why** you made those changes. The words “change”, “improve”, “fix”, and
“refactor” do not add much information to a commit message.

For pushing your changes to your branch in the local repository, run:

```shell
git push
```

### Submit a pull resquest

After finishing your changes, you can submit a pull resquest in the Github interface. For avoiding
conflicts when submitting the pull resquest, make sure you update your branch before submitting the
pull resquest.

Each pull resquest should be associated with an issue. So, in the Github web interface, create a
pull resquest in the issue being solved by:

1. selecting your branch as the source and the master branch as the target;

2. assign the pull resquest to another person (preferably, the leader of the
   project);

3. select the option to delete your branch when the pull resquest is finalized;

4. change the board status of the issue to `Ready for review`.

### Review a pull resquest

While reviewing a pull resquest you should focus on the following points:

- look at the results of the CI pipeline (it should be passed, with a green
  check);

- read the code and make sure you understand it;

- check for added dependencies, avoid them if possible;

- test the code if possible;

- check unit tests, ask for them if there are none.

On the pull resquest's webpage you can comment the pull resquest if you want. Your comment can be a
thread if you specify it with the left green multi choices menu. If you put each problem in a
separated thread it helps to manage the evolution of the pull resquest. For instance, Github
provides a counter of threads left, etc.

If there is still some changes to be made do not hesitate to move the status of the corresponding
issue from `Ready for review` to `Assigned`.

After iterating, if you feel comfortable with the submitted code, you can accept the pull resquest.

## Add License

All our software should be under the MIT License.  It is very simple to apply as it's the same block
of text ([please find it here](https://concordant.io/static/LICENSE)) that have to be copied in all
locations:

- (required) a "LICENSE" file at the Root directory of each project artifact;

- (required) common deployed packages have a "License" header entry that should be set to "MIT
  License";

- (optional but encouraged) as a header comment at the beginning of each code file.