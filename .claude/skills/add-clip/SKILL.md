---
name: add-clip
description: Add one of my published stories to the Clips section of my site. Use when I run /add-clip with a link to a story, or ask to add a clip or story to the site.
argument-hint: <link to story>
---

# Add a clip

I'll give you a link to one of my stories. Add it to the Clips section of `index.html`.

## 1. Get the headline, outlet and date from the story

- Open the link (with WebFetch or a browser) and find:
  - **Headline:** copy it exactly as published, character for character, including capitalization and punctuation. Never rewrite, shorten, summarize or "clean up" the headline. Use the story's own headline on the page, not the shorter title a browser tab or social preview might show. If the two differ and you can't tell which is the published headline, ask me.
  - **Outlet:** the name of the publication.
  - **Date:** the date the story was published, as shown on the page.
- If you can't open the link, or any of the three is missing or unclear, **stop and ask me** for the headline, outlet and date. Don't guess, and don't fill in anything from memory or search results.

## 2. Add it to the page

- In `index.html`, find `<ul class="clips">` inside `<section id="clips">`.
- Add a new `<li>` as the **first item** in that list, so the newest story is at the top:

  ```html
  <li>
    <a href="STORY URL">HEADLINE</a><br>
    <span class="clip-outlet">OUTLET · DATE</span>
  </li>
  ```

- Use the link exactly as I gave it. Escape `&`, `<` and `>` in the headline as HTML entities, without changing the words.
- If the placeholder item (`<li class="todo">[CLIPS GO HERE …]</li>`) is still there, remove it.
- Don't change anything else on the page.

## 3. Publish it

- Commit the change straight to `main` with a message like `Add clip: HEADLINE`, then push to `origin main` so the site updates. Don't use another branch or open a pull request.

## 4. Tell me what you added

In plain words, tell me the headline, outlet and date you added, exactly as they now appear on the site, plus the link. Say that the live site can take a minute or two to update.
