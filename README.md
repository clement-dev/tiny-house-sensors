[![Website perso.crans.org](https://img.shields.io/website-up-down-green-red/http/perso.crans.org.svg)](https://tinyhousesensors.herokuapp.com/)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)

# Lowtech Lab - Interface pour les capteurs de la Tiny House 🏕

## Démarrer le projet 🚀

### Local  💻
```bash
npm i
sh macos_start.sh
```
Accéder à l'url: localhost:1880 

### Docker DEV 🐳

```bash
docker build --no-cache -t <username/tag:version> .
docker run -it <username/tag:version>  
```
## Documentation 📚

### Description 🙋🏽

La documentation est rédigée en format Markdown dans le répertoire ``~/Docs/src/``, il est possible d'en exporter le contenu dans de nombreux formats. 
```bash
pandoc [OPTIONS] [FILES]
Input formats:  docbook, haddock, html, json, latex, markdown, markdown_github,
                markdown_mmd, markdown_phpextra, markdown_strict, mediawiki,
                native, opml, rst, textile
Output formats: asciidoc, beamer, context, docbook, docx, dzslides, epub, epub3,
                fb2, html, html5, json, latex, man, markdown, markdown_github,
                markdown_mmd, markdown_phpextra, markdown_strict, mediawiki,
                native, odt, opendocument, opml, org, pdf*, plain, revealjs,
                rst, rtf, s5, slideous, slidy, texinfo, textile
                [*for pdf output, use latex or beamer and -o FILENAME.pdf
```

### Générer la documentation ✍️

#### PDF
```bash
docker build --no-cache -t <username/tag:version> .
docker run -v `pwd`:/source <username/tag:version> -f markdown -t latex src/*.md -o documentation-tiny.pdf
```
*Si il y a un problème avec les caractères UNICODES des emojis*
```bash
docker build --no-cache -t <username/tag:version> .
docker run -v `pwd`:/source <username/tag:version> -f markdown -t latex --latex-engine=xelatex src/*.md -o documentation-tiny.pdf
```

#### HTML
```bash
docker build --no-cache -t <username/tag:version> .
docker run -v `pwd`:/source <username/tag:version> -f markdown -t html5 src/*.md -o documentation-tiny.html
```

## Contributions 👩🏻‍🌾👨🏻‍🌾

Le dossier mocks contient les mocks au format .json qui simulent les données des capteurs transmises via MQTT. 