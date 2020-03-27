#  Full-Stack Developer Test
## Brief
Develop a combined backend and frontend application that consumes a 200-article JSON feed, implements simple database search querying, and displays a (at minimum, barebones) website with basic category and search filtering.

## Requirements
We expect to see:

* A Laravel backend application in PHP that consumes the JSON feed, publishes it to a database, and exposes the database via APIs.
* These APIs should expose retrieval of lists of articles, and can perform simple filtering (against categories) and querying (search) of the article main body and title
    * The quality of the search results is not judged
* A database that stores the JSON feed in a well-formed way, with appropriate indexes
* An Vue.JS SPA frontend that calls the backend API, shows the articles and has UX for filtering the category names and a search box
* The design of the frontend is not important and is not judged in this test
* Memory usage should be a consideration
* A full git log showing work done
* A README to explain how to boot and run the end result

What would be nice to have:
* Unit tests
* Migrations
* Full docblock comments
* PHP 7.4 usage


## JSON Feed
A json file (`feed.json`) is bundled with the test.

Although quite verbose, the following fields are of importance (the rest can be ignored or consumed if desired):

* `title` – The title of the article
* `slug` – The unique id of the article
* `content` – This contains the main body of the article. In the provided feed only one array item exists which contains a html body.
* `categories` – Shows the categories associated to the article. primary being the single primary category, and additional being a 0-n list of additional categories. If an article does not have a primary category, use the first additional category.
* `media` – Associated media for the article. The featured type (which may not exist) should appear at the top of the article. If it does not exist, show a placeholder.

# Time Limit
We expect this test to take no longer than 6-8 hours, however there is no hard limit.

# Code style requirements

- https://chris.beams.io/posts/git-commit/
- https://sebastiandedeyne.com/setting-up-a-global-gitignore-file/
- https://github.com/prettier/plugin-php
sample `.prettierrc` file
```
printWidth: 95
tabWidth: 4
useTabs: false
semi: false
singleQuote: true
trailingComma: "es5"
bracketSpacing: true
jsxBracketSameLine: false
arrowParens: "avoid"
proseWrap: "never"
trailingCommaPHP: "php7.2"
braceStyle: "psr-2"
overrides:
  - files: "*.vue"
    options:
      printWidth: 95
    parser: "vue"
```

# Technical questions

Please answer the following questions in a markdown file called <code>Answers to technical questions.md</code>
- How long did you spend on the coding test? What would you add to your solution if you had more time? If you didn't spend much time on the coding test then use this as an opportunity to explain what you would add.
- How would you track down a performance issue in production? Have you ever had to do this?
- Please describe yourself using JSON.
