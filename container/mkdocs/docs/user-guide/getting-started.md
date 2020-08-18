# Getting started

After reading the article "Doku-Freuden" by Jan Mahn in the current c't, I'm changing my GitHub Pages user site to MkDocs.

??? note "A hint"
    Keyword `note`
    Here follows the contents of the box.
    Indented per Tab.
    ```
    Code in box
    ```

!!! danger "A hazard"
    Keyword `danger`
    You have to be careful here!

!!! example "An example"
    Keyword `example`

# Deploying your docs
```
mkdocs gh-deploy --config-file container/mkdocs/mkdocs.yml --remote-branch master
```