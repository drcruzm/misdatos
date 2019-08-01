## Welcome to GitHub Pages

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

You can use the [editor on GitHub](https://github.com/drcruzm/misdatos/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/drcruzm/misdatos/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

# 💡Análisis de Normalidad: evaluación R

| **Objetivo**<br>**Outcomes** | En base al box plot de una serie de datos determinar si la serie se ajustan a una distribución Normal . |
| ---------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Datos**                    | Serie de datos abalon:  https://drvcruz.s3.us-east-2.amazonaws.com/abalone.csv                          |
| **Prezi**                    |                                                                                                         |
| **Relacionado**              | - Box plots <br>- Prueba de Shapiro                                                                     |
| **Paquetes**                 | # install.packages("lattice")<br># install.packages("DAAG")<br># install.packages("moments")            |
| **R codes**                  | https://drvcruz.s3.us-east-2.amazonaws.com/Limpio.Rmd                                                   |

## Definiciones Generales
    ```{r setup, include=FALSE}
    knitr::opts_chunk$set(echo = TRUE)
    setwd("C:/Users/Dr.Victor/Dropbox/R code")
    dir()
    ```
## Lectura
    ```{r}
    
    abalone1 <- read.table("https://drvcruz.s3.us-east-2.amazonaws.com/abalone.csv", header = T, sep = ",", dec=".")
    head(abalone1)
    ```
    
