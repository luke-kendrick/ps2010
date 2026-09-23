# PS2010 Workshop Code Book

Source for the new PS2010 workshop code book. It follows the 2025 site's Bookdown layout, with a blue theme.

## Edit and publish with RStudio

1. Clone this repository and open `ps2010.Rproj` in RStudio.
2. Install Bookdown if needed: `install.packages("bookdown")`.
3. Edit `index.Rmd` and the numbered chapter files. Add another `.Rmd` file for each workshop, with a level-one `#` heading; Bookdown includes root-level files in filename order.
4. Build from the project root in the R console:

   ```r
   bookdown::render_book("index.Rmd", "bookdown::bs4_book")
   ```

5. Preview `docs/index.html`. Commit the changed source **and** `docs/`, then push to `main`. GitHub Pages serves the already rendered HTML; GitHub does not run R.

On GitHub, set **Settings → Pages → Build and deployment → Deploy from a branch**; select **main** and **/docs**. The address will be <https://luke-kendrick.github.io/ps2010/>.

Change the theme colour in `_output.yml` and other visual details in `style.css`. The `docs/index.html` file included initially is a holding page; the first Bookdown render replaces it.
