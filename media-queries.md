# Media Queries - Sass
O media queries são 'pontos de quebras' (break points), que definem a execução do código Css para um determinado tamanho de tela.
Normalmente é utilizado para os layouts responsivos, onde se definem diversos pontos de quebras para cada dispositivo (mobile, descktop, tablet).

O Sass nos ajuda a organizar melhor esses pontos de quebras e deixar o código mais intuitivo e fácil de fazer manutenção. 

Mas o que fazer? O sass permite que o media querie seja declarado dentro da classe (tag) no qual você está fazendo a alteração. Veja:

```sh 
    header { 
        border-top: 5px solid $cor-padrao;
        background: rgba($cor-auxiliar, 0.8);
        height: 90px;
        width: 100%;
        position: absolute;

        `@media (max-width: 980px)` {
            height: auto;
            
            h1 {
            max-width: 50%;
            margin: 0 auto;

            img {
                max-width: 100%;
                margin: .5em auto;
                display: block;
            }#//fim do img
            }#//fim do h1
        }#//fim do media querie
    }#// fim do header 
``` 

Veja que foi possível, assim como fizemos no ainhamento, unir diversos filhos de um mesmo pai, dentro do *media querie*. (*h1* e *img* são filhos do *header*)

## Variáveis com @media querie
Para ainda deixar mais otimizado e dinâmico nosso código, podemos subistituir os pontos de quebras por variáveis. Veja:

**Declarando a variável**: `$mediaQ-mobile: "max-width:980px"`. Observe que foi necessário declarar como uma string, pois quando for passado para o @media, ele irá reconhecer.

**Passando o valor**

```sh 
    #Depois
    `@media #{nome-da-variavel}{

    }`
    #É preciso colocar nesta sintaxe para funcionar. Com o #{}, para concatenar.
```