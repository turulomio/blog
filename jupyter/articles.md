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

```python
import os
from IPython.display import display, Markdown

articles_dir = "articles"
articles = [f for f in os.listdir(articles_dir) if f.endswith(".md")]

markdown_output = "## Article List\n\n"
for article in sorted(articles):
    title = os.path.splitext(article)[0]
    link = f"articles/{title}"
    markdown_output += f"* [{title}]({link}.html)\n"

display(Markdown(markdown_output))
```
