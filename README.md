Latex Docker Container
=====
This container helps compiling latex sources without the need to install all latex packages on your system. It is based on ubuntu:devel (artful) to use TeX Live 2017.

Gitlab CI
-----
The container can be used in connection with Gitlab CI using the following .gitlab-ci.yml as a starting point.
```yaml
image: friesischscott/latex-docker
build:
  script:
    - latexmk -pdf
  artifacts:
    paths:
      - "*.pdf"
```