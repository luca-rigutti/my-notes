# Database Wordpress

## Schema

The link to codex of [Wordpress schema](https://codex.wordpress.org/Database_Description)

## Why database is huge?

Database can be huge for many reason, here some things to check:

- [ ] Post table
- [ ] Option table

### Post table

Post table has all the CPT (Custom Post Type) of the site.

One thing that can be clean is the revision post, because each time we change and save the file, the whole content is saved in the table, so if you have 

### Option table

In this table we have all the setting that plugins and themes use. Maybe if you delete some plugins or change the theme, you can have some row that can be delete.

## Table constraint

WIP