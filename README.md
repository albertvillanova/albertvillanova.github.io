# albertvillanova.github.io

Setup
-----

https://docs.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll

For Windows: https://jekyllrb.com/docs/installation/windows/
- Install Ruby
- Install Jekyll and Bundler
  ```
  gem install jekyll bundler
  ```
- Check if Jekyll has been installed
  ```
  jekyll -v
  ```
  ```
  jekyll 4.1.1
  
New site
-----------
Create a new Jekyll site:
```
jekyll new albertvillanova.github.io.new
```


Upgrade
-------

To upgrade github-pages to a newer version:
- See current github-pages version supported by GitHub Pages: https://pages.github.com/versions/
  - 207
- Edit the Gemfile
  - Replace the line:
    ```
    gem "github-pages", "~> 201", group: :jekyll_plugins
    ```
    with the current supported version
    ```
    gem "github-pages", "~> 207", group: :jekyll_plugins
    ```
- Update the gem and its dependencies
  ```
  bundle update github-pages
  ```

Testing
-------
- Run your Jekyll site locally:
  ```
  bundle exec jekyll serve
  ```
- Visit: http://localhost:4000

Adding content to your GitHub Pages using Jekyll
------------------------------------------------

https://docs.github.com/en/github/working-with-github-pages/adding-content-to-your-github-pages-site-using-jekyll



