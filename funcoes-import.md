# Importar no SASS
O sass tem diversas funcionalidades para otimizar e deixar o nosso código ainda mais fácil de se trabalhar e fazer manutenção nele. 

Para nos ajudar nisso, podemos particionar o nosso código em diversos pequenos arquivos sass, da forma que acharmos melhor, e então depois importar essas partes no nosso arquivo principal SASS.

Veja o exemplo
```sh 
    @import "./helpers/variaveis";
    @import "./helpers/mixin";

    @import "./base/normalize";

    @import "./layout/geral"; #Eu posso ou não colocar a extensão se for arquivo sass
    @import "./layout/header";
    @import "./layout/destaque";
    @import "./layout/sobre";
    @import "./layout/planos";
    @import "./layout/blog";
    @import "./layout/contato";
    @import "./layout/footer";
```
Particionei o meu arquivo em diversos outros menores e assim posso ter uma facilidade maior na manutenção dele. 
> Note: Veja que não coloque a extensão *.scss*. Quando o arquivo é scss, não preciso colocar a extensão. Se for css, é necessário colocar.

# Funções no SASS
Ainda, para nos ajudar, o sass conta con diversas funções. Demontraremos duas delas aqui, que é a de deixar a cor mais escura e outra mais clara. 

```sh 
    $cor-padrao: darken(#c23e4b, 20%);
    $cor-auxiliar: lighten(#1e2c35, 50%);
```
`darken(cor, porcentagemDoEfeito)` - Deixa a cor mais esrura. Você determina a cor e a porcentagem de quanto quer que esta cor fique escura.

`lighten(cor, porcentagemDoEfeito)` - Deixa a cor mais clara. Você escolhe a cor e a porcentagem de quanto quer que ela tenha o efeito.
