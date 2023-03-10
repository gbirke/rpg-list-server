# RPG PDF rulebooks server environment

This is an NGinX configuration plus PHP thumbnail generator to host my RPG
rulebooks, together with https://github.com/gbirke/astro-rpg-list

It contains an NGinX configuration for serving my PDF files as well as
generating thumbnails for then with the help of a PHP script and
ImageMagick.

## Document roots and path aliases in the NGinX configuration

The NGinX configuration expects four file system paths to exist:

- `/site/` - The static site that shows the collection of games, generated from
	Markdown metadata files.
- `/pdf/` - Path to the documents linked from the site
- `/thumbnail-srv/` - The PHP thumbnail generator for the files in
	`/pdf/`.
- `/thumbnails/` - The generated thumbnails

NGinX will map these file system paths to the following URL paths:

|File system |URL |
|---|---|
|`/site/` | `/` (root) |
|`/pdf/` |`/PDFs/` |
|`/thumbnails/` |`/thumbnails/` |



