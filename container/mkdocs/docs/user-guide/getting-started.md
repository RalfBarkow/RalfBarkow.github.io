# Get started

Read [Mahn, J. (2020) Doku-Freuden](https://www.heise.de/select/ct/2020/18/2000809371395242374) (in German).  
(I'm changing my GitHub Pages' user site to MkDocs.)

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
Regarding Organization and User Pages, the [mkdocs documentation](https://www.mkdocs.org/user-guide/deploying-your-docs/#organization-and-user-pages) recommends to work with copies of 2 repositories on our local system. For example, consider the following file structure:
```
my-project/
    mkdocs.yml
    docs/
orgname.github.io/
```
After making and verifying updates to your project you need to change directories to the orgname.github.io repository and call the mkdocs gh-deploy command from there:
```shell
cd ../orgname.github.io/
mkdocs gh-deploy --config-file ../my-project/mkdocs.yml --remote-branch master
```
Deviating from this, I want to work with only one repository, as described by Jan Mahn. 
```shell
cd RalfBarkow.github.io
mkdocs gh-deploy --config-file container/mkdocs/mkdocs.yml --remote-branch master
```
