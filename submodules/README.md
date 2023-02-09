Git Katas: Submodules
Submodules are a way to embed other git repositories into your own, retaining a pointer to its origin. This allows you to grab source changes directly, as well as pushing them back.

Setup
Run source setup.sh (or .\setup.ps1 in PowerShell)
NOTE: If running setup.sh on windows, you can run into problems by sourcing the setup script. Instead, run ./setup.sh, and the folders would be created correctly.

The task
After running the setup script, you'll be left with three repositories inside the exercise folder.

A remote repository. This is the "remote" repository that would normally exist on your preferred Git repository host, e.g. github.com.
A component repository cloned from remote.
A product repository.
Go to the product repository.

Add component as a submodule of product by running git submodule add ../remote include.

What does your working directory look like?

Does git status look like you expect?

What if you cd to include?

Run git diff --staged in product. Where can you find the commit id shown in the +Subproject commit ... line?

Commit the changes on the product repository.

Go to the component repository.

Does it know that it is used as a submodule?

Make a change to the component repository and git commit and git push it.

Go to the product repository.

Does git status or git submodule foreach 'git status' tell you anything about this new commit?

Go to the include directory and git pull the latest version.

Verify that the change from the component repository is available in include.

Go to the product directory. What is the status now in your product repository? Also examine with git diff.

Go to your include folder. Make a change and push it back to its origin.

Go to the exercise directory. We will make a clone of product to illustrate how submodules in a clone must be initialized.

Run git clone product product_alpha.

Go to product_alpha directory, how does your working directory look, what does the log say and what is in the include directory?

Run git submodule init, what does your include dir look like?

Run git submodule update, what does your include dir look like now? (* Note: you can combine the previous two steps by doing git submodule update --init)

Is the latest change from component available in include?

Go to the product repository.

Commit the changes on the product repository. Please forget to push the changes for now ;-)

Go to the product_alpha repository. We'll ensure that we have the latest changes from product.

Run git submodule update.

Is the latest change from component available in include?

Examine the output of git submodule status. Compare the commit id with the component repository.

Run git submodule update --remote.

Is the latest change from component available in include?

Examine the output of git submodule status. Compare the commit id with the component repository.

As a bonus exercise, try to draw out this entire exercise on paper!

Useful commands
git diff [--cached] --submodule
git log -p --submodule