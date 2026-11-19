# Lectures

Jesse Roberts's lecture and talk decks, with their companion notebooks. Served by GitHub Pages
(deploy from branch `main`, root) at https://www.jessetnroberts.com/lectures/.

There is no build and no staging. A commit to `main`, including a save from Slidewright, is live
in about a minute.

| What | Where |
| --- | --- |
| Course lectures | `<COURSE>/<name>-slides.html` and `<COURSE>/<name>-notebook.ipynb` |
| General talks and guest lectures (no course) | `talks/` or `misc/`, listed under `MISC:` in `lectures.yml` (shown as Miscellaneous on the site) |

Each deck carries `<meta name="slidewright-source" content="github:JesseTNRoberts/lectures@main:<path>">`
so Slidewright saves edits back here. Update it if a deck is renamed or moved.

## Adding a lecture

1. Commit the deck (and notebook) to `<COURSE>/`.
2. Add an entry to that course's list in `lectures.yml` (copy one that's there), for example

   ```yaml
   AI4200:
     - week: 12
       session: 1
       title: Lecture title
       topics: [topic one, topic two]
       slides: AI4200/week12.1-slides.html
       notebook: AI4200/week12.1-notebook.ipynb
   ```

   Optional fields are `date` (YYYY-MM-DD), `pdf`, `video`, `note`, `readings` (title, authors,
   year, venue, url), `demos` and `models`. The course id (`AI4200`) must match `course_id` in the
   site's `_teaching/` file. Put quotes around a title or topic that contains a colon or `#`, or a
   topic that contains a comma.

The Teaching page and course pages read `lectures.yml` in the browser, so the lecture shows up
within a minute of the push. The site's next build also bakes it into the pages (for search engines
and visitors without JavaScript). A broken `lectures.yml` (usually bad indentation) makes site builds
fail until it's fixed. The site that's already up stays up.

Never create a `/lectures/` folder in the main site repo, it would collide with this site.
