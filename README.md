# Curriculum Vitae - Rizky Yanuar Kristianto

Automated LaTeX Curriculum Vitae powered by **GitHub Actions** and **GitHub Pages**.

## Live CV Link
View the live, constantly updated PDF directly in your browser:
**[https://rizkyyanuark.github.io/curriculum-vitae/](https://rizkyyanuark.github.io/curriculum-vitae/)**

## Automated Workflow
- Every commit pushed to the main branch triggers the GitHub Actions workflow in .github/workflows/build.yml.
- The workflow compiles cv.tex using LaTeX in a clean Ubuntu container.
- The compiled cv.pdf and index.html redirector are automatically deployed to the uild branch serving GitHub Pages.
