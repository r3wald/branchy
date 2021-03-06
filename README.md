# branchy

* Version: 1.0-dev
* Date Not yet released

**branchy** is a subversion tool to control and manage branches in a feature driven way. Similar to gitflow by nvie <https://github.com/nvie/gitflow>.

## Example Usage

### Start the Feature Branch

Create a new feature branch `awesome_extension`

    $ branchy start-feature awesome_extension

The tool will create a branch called `/branches/awesome_extension`.

It will also switch the local copy to the branch.

### Continue developing

Now you can commit into that branch.

### Getting latest changes from `trunk`

If you want to merge latest changes from branch, do it with this little wrapper (around svn merge):

    $ branchy merge-trunk

After this merge, you have to `svn commit` the changes! If you want to automaticlly commit the changes, do it with the auto-merge-trunk option:

    $ branchy auto-merge-trunk

### Show changes

If you want to see what changed in your branch, you can show the changes against the `trunk` with

    $ branchy show-changes

### Finish the Feature Branch

If you finished your work, you can finish the feature with this

    $ branchy finish-feature

This will merge all changes back into the `/trunk` and delete the branch. 

## Additional Features

### Checkout features

If you want to checkout a specific feature, you can list all available features with:

    $ branchy features

and checkout a specific feature with:

    $ branchy checkout awesome_feature

If you want to checkout the trunk you can do it like this:

    $ branchy cehckout trunk

## License

This work is copyright by DracoBlue (<http://dracoblue.net>) and licensed under the terms of MIT License.
