# Bio470: Thesis with Anna Ritz

This is the content for Reed College's thesis (Bio470) advised by Anna Ritz.

[https://reed-compbio-classes.github.io/bio470-thesis-with-ritz/](https://reed-compbio-classes.github.io/bio470-thesis-with-ritz/)

### Developer Notes

**To run locally:** tested with Ruby 3.1.3 and jekyll 4.3.3. You might have to do `bundle install` or `bundle update` before serving the website locally.

```
bundle exec jekyll serve
```

**To pass GitHub actions:** if you change the `Gemfile`, you need to `bundle update` to get the addtional gems installed. This changes the `Gemfile.lock` file. If you commit the lock file, you need to add the linux platform to it so GitHub actions work and the website is deployed without error:

```
bundle lock --add-platform x86_64-linux
```

**To get relative links:** I had to add the `jekyll-relative-links` gem to the Gemfile (this should be distributed with GitHub pages, but it didn't work with just-the-docs template).

# Convert website to PDF

Requires the [pandoc](https://pandoc.org/installing.html) tool.

Concatenates all the files in the order that they are shown on the left-hand banner on the website. 

```
pandoc index.md \
    doc/goals.md \
    doc/support.md \
    doc/policies.md \
    doc/assessment.md \ 
    -o bio470-F24-syllabus.pdf \
    -M title="Thesis with Ritz Fall 2024 Syllabus"
``` 

Then, move the file to `doc/archive/`.