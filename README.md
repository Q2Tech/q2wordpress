# Blackbird Consulting WordPress
This is [Blackbird Consulting's](www.blackbirdconsult.com) base WordPress installation for use on all new projects. This git repository contains two additonal submodules that pull in the most current [WordPress](https://github.com/WordPress/WordPress) installation and [WP-Sync-DB](https://github.com/wp-sync-db/wp-sync-db), a custom plugin that assists with database migration.

## wp-content *outside* wordpress directory

This WordPress install is set up in a way that places the ```wp-content``` directory *outside* the main ```wordpress``` directory. This setup also places the ```index.php``` and ```wp-config.php``` files outside the ```wordpress``` directory. Thes files have been edited appropriately. This setup is oriented to be developed locally but pushed periodically to a staging environment. Thus, the ```wp-config.php``` has also been customized to allow enable inputting two sets of database credentials, one for your local development environment and one for the staging environment. 

To clone this repository and include the submodules, issue the following git command:

    user@computer:~$ git clone --recursive git@github.com:Herm71/bbwordpress.git yournewprojectdirectory

To use this repository in a new project, first clone this repository into a temporary new bare repository, like this:

    user@computer:~$ git clone --bare --recursive git@github.com:Herm71/bbwordpress.git /path/to/tempbbwordpress.git
    # Make a bare clone of the repository

Next, mirror this temporary clone to a new project repository

    blackbird@computer:~$ cd tempbbwordpress.git
    #Enter temporary project repository directory
        
    blackbird@computer:~$ git push --mirror https://github.com/exampleuser/new-repository.git
    # Mirror-push the temporary clone to a new repository

Remove the temporary clone

    user@computer:~$ cd ..
    #move up one level

    blackbird@computer:~$ rm -rf tempbbwordpress.git
    #remove temporary repository

Finally, create a new project directory on your development machine and clone the new repository into it:

    blackbird@computer:~$ mkdir newprojectdirectory
    # Create a new directory for your project

    blackbird@computer:~$ cd newprojectdirectory
    # Enter the newly created directory

    blackbird@computer:~$ git clone --recursive https://github.com/exampleuser/new-repository.git
    # Remember to use recursive to include all submodules

#Changelog
Apple has a formalised version number structure based around the NumVersion struct, which specifies a one- or two-digit major version, a one-digit minor version, a one-digit "bug" (i.e. revision) version,
##0.0.1
-still very much in development mode