# Jekyll CLI via Rake

A Rakefile for Jekyll which provides a full CLI for creating posts, editing, tagging, etc.

# Install

- Copy `cli.rake` into your Jekyll directory.
- Add the required gems (`chronic`, `colorize`) to your Gemfile if they aren't there already.
- Add `import "cli.rake"` to your Rakefile. If you don't have a Rakefile, create an empty one.
- Run `rake fixids` to add ids to your posts.

# Features

## IDs

Every post will be assigned an internal id. Many commands (e.g. `edit`, `tag`, etc) can take a post id as their first parameter. If no post id is specified, the commands will operate on the most recently modified post (that's usually the one you want). Similar to git, you don't have to type out the full id. You can just type the first few numbers, and Rake will find the most recently modified post that matches.

## Commands

```
rake default             # List all tasks
rake edit                # Open existing post in editor
rake fixids              # Fill in missing post ids
rake ls                  # List latest posts
rake new                 # Create a new post with the given title and open it in the editor
rake preview             # Build and serve site locally
rake push                # Commit to git and push
rake redate              # Change the date on a post
rake rename              # Change the title of a post
rake retime              # Change the time on a post
rake retouch             # Touch last 20 posts so "rake ls" lists them in date order
rake tag                 # Add tag
rake tags                # List tags
rake untag               # Remove tag
```
