It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com).

# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

*You **can** combine them*

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Apple[edit]
Apple has a formalised version number structure based around the NumVersion struct, which specifies a one- or two-digit major version, a one-digit minor version, a one-digit "bug" (i.e. revision) version, a stage indicator (drawn from the set development/prealpha, alpha, beta and final/release), and a one-byte (i.e. having values in the range 0–255) pre-release version, which is only used at stages prior to final. In writing these version numbers as strings, the convention is to omit any parts after the minor version whose value are zero (with "final" being considered the zero stage), thus writing 1.0.2 (rather than 1.0.2b12), 1.0.2 (rather than 1.0.2f0), and 1.1 (rather than 1.1.0f0).

# Blackbird Consulting WordPress
This is [Blackbird Consulting's](www.blackbirdconsult.com) base WordPress installation for use on all new projects. This git repository contains two additonal submodules that pull in the most current [WordPress](https://github.com/WordPress/WordPress) installation and [WP-Sync-DB](https://github.com/wp-sync-db/wp-sync-db), a custom plugin that assists with database migration.

## wp-content *outside* wordpress directory

This WordPress install is set up in a way that places the ```wp-content``` directory *outside* the main ```wordpress``` directory. This setup also places the ```index.php``` and ```wp-config.php``` files outside the ```wordpress``` directory. Thes files have been edited appropriately. This setup is oriented to be developed locally but pushed periodically to a staging environment. Thus, the ```wp-config.php``` has also been customized to allow enable inputting two sets of database credentials, one for your local development environment and one for the staging environment. 

To clone this repository and include the submodules, issue the following git command:

```git clone --recursive git@github.com:Herm71/bbwordpress.git yournewprojectdirectory
```
#Changelog
##0.0.1
-still very much in development mode