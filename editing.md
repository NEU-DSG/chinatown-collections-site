# Editing the content of the static site
The Chinatown History Directory site is generated from a set of framework pages which dynamically draw in data from Wikibase. The process of editing the site thus involves three steps:
1. Knowing what file in the repository contains the framework for the page you want to edit
2. Making changes (carefully!) to that framework page and committing them in GitHub
3. Regenerating the site

Those first two things are fairly easy and are documented below. Step 3 requires one of the site administrators to initiate the process for regenerating the site and deploying the new version onto the publication server.

When editing the template files, focus on the HTML contentL e.g. inside <p> elements, <h1> elements, etc.

Specific files that are useful to edit:
* en/about.html
* en/credits.html
* en/data_model.html
