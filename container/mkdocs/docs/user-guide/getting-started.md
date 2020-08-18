# Getting started

Read [Mahn, J. (2020) Doku-Freuden](https://www.heise.de/select/ct/2020/18/2000809371395242374) (in German).  
(I'm changing my GitHub Pages user site to MkDocs.)

??? note "pyenv version"
    ```shell
    $ pyenv version
    3.8.5
    ```

```shell
pip install mkdocs
```

To use the popular [Material](https://squidfunk.github.io/mkdocs-material/) theme, load this too via pip:

```shell
pip install mkdocs-material
```

## Pack everything into a container

Put the entire documentation into a container to be sure that the software will find identical conditions on all developer machines and on the server – identical dependencies, MkDocs plug-ins and Python versions for example.

## Build a multistage image

Read [Mahn, J. (2019) Raketenstufenbau](https://www.heise.de/select/ct/2019/3/1548578276157318) (in German).

## Deploy the docs

```shell
mkdocs gh-deploy --config-file container/mkdocs/mkdocs.yml --remote-branch master
```

!!! danger "A hazard"
Never edit files in the master branch of the pages repository by hand if using the `gh-deploy` command because you will lose your work the next time you run the command.

[Organization and User Pages](https://www.mkdocs.org/user-guide/deploying-your-docs/)
