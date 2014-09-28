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

# Blackbird Consulting WordPress
This is [Blackbird Consulting's](www.blackbirdconsult.com) base WordPress installation for use on all new projects. This git repository contains two additonal submodules that pull in the most current [WordPress](https://github.com/WordPress/WordPress) installation and [WP-Sync-DB](https://github.com/wp-sync-db/wp-sync-db), a custom plugin that assists with database migration.

## wp-content *outside* wordpress directory

This WordPress install is set up in a way that places the ```wp-content``` directory *outside* the main ```wordpress``` directory. This setup also places the ```index.php``` and ```wp-config.php``` files outside the ```wordpress``` directory. Thes files have been edited appropriately. This setup is oriented to be developed locally but pushed periodically to a staging environment. Thus, the ```wp-config.php``` has also been customized to allow enable inputting two sets of database credentials, one for your local development environment and one for the staging environment. 

To clone this repository and include the submodules, issue the following git command:

```git clone --recursive git@github.com:Herm71/bbwordpress.git yournewprojectdirectory
```