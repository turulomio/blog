---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Articles

```{code-cell} ipython3
from pathlib import Path
from IPython.display import display, Markdown

# Genera una lista de enlaces a los artículos en el directorio 'articles/'
# La ruta debe ser relativa al directorio 'jupyter/', donde se ejecuta el build.
articles_path = Path("../articles")
# The link needs to be a valid Markdown link pointing to the generated HTML file.
article_links = [f"* [{p.stem.replace('_', ' ').title()}]({p.with_suffix('.html')})" for p in sorted(articles_path.glob("*.md"))]
markdown_list = "\n".join(article_links)
display(Markdown(markdown_list))
```
