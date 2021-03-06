# Jekyll CLI via Rake

A Rakefile for Jekyll which provides a full CLI for creating posts, editing, tagging, etc.

# Install

- Install the required gems (`rake`, `chronic`, `colorize`) if you don't have them. Adding them to your Gemfile is a good idea.
- Copy `cli.rake` into your Jekyll directory.
- Add `import "cli.rake"` to your Rakefile. If you don't have a Rakefile, create an empty one.
- Run `rake fixids` to add ids to your posts.

# Features

## IDs

Every post will be assigned an internal id. Many commands (e.g. `edit`, `tag`, etc) can take a post id as their first parameter. If no post id is specified, the commands will operate on the most recently modified post (that's usually the one you want). Similar to git, you don't have to type out the full id. You can just type the first few numbers, and Rake will find the most recently modified post that matches.

## Commands

```
ls                  # List posts (recently modified posts first)
new                 # Create a new post with the given title and open it in the editor
edit                # Open existing post in editor

rename              # Change the title of a post
redate              # Change the date on a post
retime              # Change the time on a post
retouch             # Touch last 20 posts so "rake ls" lists them in date order

tags                # List tags
tag                 # Add tag
untag               # Remove tag

preview             # Build and serve site locally
push                # Commit to git and push

fixids              # Fill in missing post ids
```
