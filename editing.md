# Editing the content of the static site
The Chinatown History Directory site is generated from a set of framework pages, some of which dynamically draw in data from Wikibase. The process of editing the site thus involves three steps:
1. Knowing what file in the repository contains the framework for the page you want to edit
2. Making changes (carefully!) to that framework page and committing them in GitHub
3. Regenerating the site

Those first two things are fairly easy and are documented below. Step 3 requires one of the site administrators to initiate the process for regenerating the site and deploying the new version onto the publication server.

## Components of the static site

The editable files are all in the templates directory. Within that directory, almost all of the editable content of the site is in one of the following subdirectories:

* en: this contains the static HTML pages that form the English-language portion of the site
* zh: this contains the static HTML pages that form the Chinese-language portion of the site
* generic: this contains the template files for dynamically generated pages of the site (e.g. the list of collections, the individual collection pages, etc.)

The dynamically generated pages contain a mix of HTML code, static content, and dynamic code that draws in data from other pages and from Wikibase. You can recognize the dynamic code because it is enclosed within pairs of curly brackets ({{ }}). 

To make a change to one of thes pages, you'll need to identify the page to be edited; you can usually figure this out by looking at the URL for the page, and matching the filename to the corresponding file in GitHub.

## Editing process

When editing the template files, follow these guidelines:
1. To edit the actual words on the page, focus on the content of the existing HTML elements: e.g. the text inside &lt;p&gt; elements, &lt;h1&gt; elements, etc.
2. If it's necessary to change the structure of the page (for instance, to add a heading, or change a heading level, or make something into a list), you can edit the HTML markup itself, or add further HTML markup. Be cautious about *changing* or *removing* markup, to make sure that you don't change any of the dynamic template code. 
3. After making your change to one or more files, write a brief commit message describing the change(s), and commit your change to GitHub.
4. Once you've made and committed all of the changes necessary, contact Patrick Murray-John or the Data Engineer, who can regenerate the site and upload the results to the DSG server. 

Specific files that may be useful to edit:
* the About page: templates/en/about.html and templates/zh/about.html
* the Data Models page: templates/en/data_model.html and templates/zh/data_model.html
* the Credits page: templates/en/credits.html and templates/zh/credits.html
* the Collections index page (both languages): generic/collections_index.html
* the Organizations index page (both languages): generic/org_index.html
* the People index page (both languages): generic/people_index.html

