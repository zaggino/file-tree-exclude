# Brackets File Tree Exclude

Brackets extension for excluding folders and files from the file tree, find in files, and quick open.
This means that the files will be completely invisible to Brackets (and thankfully not count against the 30,000 file limit). 

This is great for cache folders, distribution/build folders and files, and package manager folders like `node_modules` and `bower_components`.

This is a rewrite of Jon Wolfe's extension - [file-tree-exclude](https://github.com/JonathanWolfe/file-tree-exclude).

## How to install

Use [brackets-npm-registry](https://github.com/zaggino/brackets-npm-registry)

## Configure

Exclusions are defined globally by default inside the Brackets preferences file (_Debug > Open preferences file_).

Append or edit your configuration options there. (See below for example of defaults)

**Or on a per project basis:**

Create a `.brackets.json` in project root (it may already exist) and add your settings there.

## Note

**Project config completely redefine exclusion rules from global config.**

## Configuration defaults

```JSON
{
	"brackets-file-tree-exclude.excludeList": [
		"(^|/)\.git($|/)",
        "(^|/)dist($|/)",
        "(^|/)bower_components($|/)",
        "(^|/)node_modules($|/)"
    ]
}
```

## How it Matches

Matches are done using JavaScript regexp's relatively to the current project root. Don't forget to escape special characters like dots.
