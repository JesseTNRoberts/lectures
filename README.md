# Lectures

Jesse Roberts's lecture and talk decks, with their companion notebooks. Served by GitHub Pages
(deploy from branch `main`, root) at https://www.jessetnroberts.com/lectures/.

There is no build and no staging. A commit to `main`, including a save from Slidewright, is live
in about a minute.

| What | Where |
| --- | --- |
| Course lectures | `<COURSE>/<name>-slides.html` and `<COURSE>/<name>-notebook.ipynb` |
| General talks | `talks/` |

Each deck carries `<meta name="slidewright-source" content="github:JesseTNRoberts/lectures@main:<path>">`
so Slidewright saves edits back here. Update it if a deck is renamed or moved.

The lecture library on the main site (`_teaching/*.md` in the site repo) links to these files as
`/lectures/<path>`. Adding a deck here does not list it there, add the session to the course file too.

Never create a `/lectures/` folder in the main site repo, it would collide with this site.
