## Documentation
-------------

### Motivation

Documentation has a possibility of inconsistency between the website Guide and the Readme.
Modify automatically as code is updated. See motivation-guidelines-documentation.md.

### Suggested improvement
  auto generate documentation from markdown for website

Github Pages
> Do not support old versions of documentation apart from what is in the
  README(s) of older HiGHS code checkout

> documentation will be outside of HiGHS repo

### Suggestion improvement implementation

docsy is needed to merge what is now in README (which will refer to it) and
website (which will refer to both) 

Website
GitHub pages
  - Uses jekyll static site generator uses markdown parser.
> can host on highs.dev website 

Docsy
  Website example: galabovaa/docsy
  website url: github.io