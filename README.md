# stripethree.github.io

# Up and running

```
bundle config set path 'vendor/bundle'
bundle install
bundle exec jekyll serve
```

### Before a branch is pushed...

_perhaps this should be a git hook...._

```
bundle exec jekyll build
bundle exec htmlproofer ./_site --allow-hash-href --check-favicon --check-html --disable-external
```

### Branches are auto-deployed to S3:

http://stripethree.github.io.s3.amazonaws.com/${BRANCH_NAME}/index.html
