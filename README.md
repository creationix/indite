# in·dite

1. (verb archaic) write; compose.

  > "he indites the wondrous tale of Our Lord"

2. (noun modern) a git based blogging system for technical writings.

  > "Indite is an amazing way to share code ideas with the world."

--------------------------------------------------------------------------------

 - Every article is a branch.
 - Skins are also branches.
 - Skins and articles can be written and tested entirely offline.
 - Initial content is rendered by server and sent to client as pre-rendered HTML.
 - Once client has copy of JS code and git repo, it can render everything locally.
 - A chrome or firefox app can also consume the git format and allow reading and publishing.
 - Various runtimes for code can be added (parsers, interpreters, syscalls).

Since all the content is modular and in git branches, then other sites using this
same software can share.  Suppose I write this great node.js runtime for my blog
that lets me embed and run node.js snippets in my blog.  You could clone just that
part of my public git repo and have the same functionality in your site without
having to copy all my other data.

## Contents of Master Index

 - README.md - A human readable file describing this repository's format and purpose.
 - indite.json - Configuration of the site.  Including the skin and list of articles.

```js
{
  url: "http://howtonode.org/",
  skin: "light",
  articles: {
    "object-graphs": {
      title: "Object Graphs",
      date: 1381171051272,
      author: "Tim Caswell",
      summary: "...",
      skin: "dark"
    }
  }
}
```

## Contents of an Article

 - README.md - the main prose as well as links to plugin instances.

Raw code snippets associated with this article are also in this branch.

## Contents of a Skin

A skin contains static resources as well as templates.

## Contents of a Runtime

A runtime contains a code parser, an interpreter, and mappings to sandbox system
calls for interactivity.
