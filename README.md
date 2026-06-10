# Alejandro's Academic Portfolio

This repository hosts my personal academic website, featuring my research portfolio, publications, blog, and professional history. The site is built using a customized, modern editorial version of the Jekyll `al-folio` theme.

---

## 🚀 Key Features & Customizations

- **Modern Editorial Layout**: Features a responsive, horizontal bio banner and inline social profiles for a premium academic look.
- **Tailored Typography & Palette**: Built using **Inter** (for body/sans-serif text) and **Lora** (for header/serif text), utilizing a professional steel-blue accent and sober alabaster (light) / deep slate (dark) theme values.
- **Research Interests**: Displayed using interactive capsule tags.
- **Publication Integration**: Automated citation layout generated directly from `_bibliography/papers.bib` with InspireHEP and arXiv linking.
- **Responsive Navigation**: Retains a clean, single-column main body flow with responsive top navigation headers.

---

## 🛠️ Local Development (Docker-based)

To avoid compiling native extensions locally and to ensure parity with the deployment environment, use the pre-packaged Docker container to run the development server:

```bash
docker run --name jekyll-dev --rm \
  -v $(pwd):/srv/jekyll \
  -p 8080:8080 \
  -p 35729:35729 \
  -e JEKYLL_ENV=development \
  amirpourmand/al-folio:v0.12.1 \
  bash -c "bundle install && /tmp/entry_point.sh"
```

Once running, the development server is available at: [http://localhost:8080](http://localhost:8080)

---

## 🤖 CI/CD Workflows

The repository uses automated GitHub Actions workflows to maintain code quality and deploy the website:

1. **Deploy site (`deploy.yml`)**: Compiles and publishes the site to GitHub Pages on every push to the `main` branch.
2. **Prettier code formatter (`prettier.yml`)**: Automates styling alignment to keep code clean and formatted.
3. **Check for broken links (`broken-links.yml`)**: Validates external links across the markdown repository content.
4. **Check for broken links on site (`broken-links-site.yml`)**: Automatically runs an offline link checker on the built site assets inside a container equipped with ImageMagick to verify relative path validity.

---

## 📜 License

This website template is open-source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
