# Portfolio Assignment Instructions

This is a template for you to start building your professional portfolio. It is also part of your journey at MAE and will be reviewed, as needed, by your instructor and the Undergraduate Program Office.

## Getting Started

1. This is your personal copy of the portfolio template repository. It was created automatically when you accepted the Assignment through the GitHub Classroom link you were provided.
2. Start by cloning your repository to your local machine:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

## Personalizing Your Portfolio

### Homepage
- `index.md`: Replace the placeholder text with a welcome or pitch paragraph about yourself.
- `assets/images/profile-pic.jpg`: Replace the placeholder with a portrait of yourself.

### Projects
- In the `_projects` folder: Use the provided example pages (e.g., `2022-trig-analysis.md`) to build one page per project.
- Each project has a main (square) project image, set in the page's top matter by the `image` variable.
- All images are in `assets/images`. Delete the ones you don't need.
- It is useful to name the page with a leading date. This will determine the order of projects on your main portfolio gallery.
- You can also develop another ordering by naming the projects with some numerical prefix.
- The example project pages show you how to include code and images in the portfolio page.
- Refer to the Jekyll Markdown documentation for other formatting tips

### CV
- `assets/CV.pdf`: Replace this placeholder with your own PDF CV.

### Color Schemes

The provided template comes with multiple color schemes. To choose a scheme:

1. Open the `_config.yml` file.
2. Look for the `color_scheme` setting.
3. Change the value to the desired skin name. Refer to the inline comment in `_config.yml` for available skin options.


Example:
```yaml
skin: aqua
```

## Running the Site Locally

Once you made your changes, or at any time you wish to, you can test your changes locally, by running this terminal command:

```bash
bundle exec jekyll serve
```

## Publishing your Portfolio to the Web

Once everything looks good, commit and push your changes:

```bash
git add .
git commit -m "<Commit Edit>"
git push origin main
```

Your portfolio will be live at:

```php
https://<your-username>.github.io/<your-repo>/
```

## Using Other Jekyll Themes

You can customize your portfolio by using other Jekyll themes. Here are some good places to find themes:

- [Start Bootstrap](https://startbootstrap.com/themes/jekyll/)
- [Jekyll Themes](https://jekyllthemes.io/)
- [Jekyll Theme](http://jekylltheme.org/)
- [Jekyll Themes on GitHub](https://github.com/topics/jekyll-theme)

Follow the theme's installation and customization instructions as needed to fit your portfolio content.
