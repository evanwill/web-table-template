# web-table-template

**Project in process. Not working!**

A simple template to publish an interactive web table from a Google Sheet or CSV file.

## Add Your Sheet

See ["docs/set-up-web-table.md"](docs/set-up-web-table.md).

## Template Basics

The site is based on [bootstrap5-template](https://github.com/thecdil/bootstrap-template), a basic template repository to create a [Bootstrap 5](https://getbootstrap.com/) site using Jekyll on GitHub Pages (or where every you want to host it). 
The layout is based on the [Bootstrap starter template example](https://getbootstrap.com/docs/5.1/examples/) with a navbar, search box (using lunr.js), and footer.

There are several builtin options to start customizing the site.

### Get Started 

- Click green "Use this template" button to make a copy of the code in your own repository (alternatively, use Import or manually copy files)
- Edit `_config.yml` with your site information
- In your new repository visit "Settings" > "Pages" to activate GitHub Pages
- Edit and create pages in the "pages" folder (probably in Markdown). Use each page's yaml front matter to populate the navbar:
    - `title` will appear as h1 at top of the page content.
    - `nav` if this option has a value, it will appear in the navbar as link to this page.
    - `nav_order` navbar items will be sorted using this number. 
- Use "includes" to simplify adding Bootstrap features to Markdown pages (see comments in the "_include/" files for instructions).

See [docs/create-website.md](https://github.com/thecdil/bootstrap5-template/blob/main/docs/create-website.md) for more details.

### Customize 

- Tweak base variables in `assets/css/custom.scss` (text color, link color, container size)
- Tweak bootstrap theme colors using `_data/theme-colors.csv` (add a css color in the color column next to the BS color-class to override, or create a new class name. This will generate btn-, text-, and bg- classes.)
- Add custom CSS to `_sass/_custom.scss` (content of `_sass/_template.scss` relates to template components)
- Use Bootstrap to customize `_layouts/` and `_includes/template/`.

## Template Assets

Included in assets/lib folder:

- [Bootstrap](https://getbootstrap.com/docs/5.1/getting-started/introduction/) v5.1
- [Bootstrap Icons](https://icons.getbootstrap.com/) v1.7.1
- [lunr.js](https://lunrjs.com/) v2.3.9
- [lazysizes](https://github.com/aFarkas/lazysizes) v5.3.2
- [DataTables](https://www.datatables.net/) v1.11.3, with concatenated jQuery 3, Buttons, HTML5 Export, JSZip, Print view.
- [PapaParse](https://github.com/mholt/PapaParse) v5.0.2
