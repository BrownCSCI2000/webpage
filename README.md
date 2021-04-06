# CSCI 1430 Website

This is the repository for the [course website of CSCI 1430: Introduction to Computer Vision](https://cs.brown.edu/courses/csci1430/).

The [Brown CS course link](https://cs.brown.edu/courses/csci1430/) redirects to a GitHub Pages deployment of this repository.

## Updating and Adding Content

Almost all of the website content is written in [markdown](https://en.wikipedia.org/wiki/Markdown). Each markdown file (`*.md`) has a corresponding `index.html` that loads the markdown and renders it into html. See `js/markdown2html.js` for implementation of this markdown to html conversion.

To edit a page on the website, find the corresponding markdown file and add your changes. Your updates will automatically appear on the website after they are commited to the `main` branch.

To add a new page to the website, create a new directory and add a new markdown and `index.html` file to that directory. Use the guides saved under `resources/` as a template. Any images or files that you would like to embed into the new page can be saved in the new directory and relatively linked in the markdown file.

### LaTeX

The `markdown2html` script supports [LaTeX](https://www.latex-project.org/) both inline and as blocks. To use an equation block, do `$$...$$` in markdown. To use an inline equation, do `\\(...\\)` in markdown.

**Note:** `\` is an escape character in markdown, so to type something that would be `\\` in normal LaTeX, you would actually need to type `\\\\` in the markdown file. Below are some things to keep in mind:
- type `\\\\` in markdown to get `\\` in LaTeX
- type `\\(` in markdown to get `\(` in LaTeX
- type `\\)` in markdown to get `\)` in LaTeX

A good example of using LaTeX in markdown is `proj5_cameras/proj5.md`.

## Updating Staff Section of Homepage

The staff section of the homepage is created upon page load by the function defined in `js/staff.js`, which pulls staff data from `staff.csv` and creates the appropriate entries in the staff section.

To update a staff member's information (e.g. name, pronouns, fun fact, images), just update `staff.csv` (you can use a spreadsheet application like Microsoft Excel or Google Sheets) and make sure that the images are saved correctly in the `staff_images` directly. 

Currently, all images are manually cropped to **squares of 300x300 pixels** to minimize load times and ensure consistent appearance on the website.

## Running the Website Locally

Any local server will work. For example, Python's `http.server` works great:

```bash
# run this in root directory of repo
python3 -m http.server
```
