# Aninhamento - sass
O aninhamento é uma forma de otimizar o seu código, agrupando elemtos filhos detro do seu pai. 

```sh 
    #Exemplo
    .menu-principal {
        position: absolute;
        right: 0;
        top: -.5em;
        font-size: 1.2em;
        font-weight: lighter;

        ul {
            padding-left: 0;
        }

        li {
            display: inline-block;
            width: 5em;
        }

        a {
            color: $cor-branca;
            text-decoration: none;
            &:hover {
            text-decoration: underline;
            }
        }
    }
```
Observe que na tag *a*, foi utilizado o código `&:hover`, onde o **&** está relacionado ao elemento que sofrerá a ação. Neste caso o *a*.

## Vantagens
Como vantagens o aninhamento ajuda na otimização do código e na manutenção do mesmo, tendo em vista que alterando o nome do elemento pai, todos os outros também serão alterados automaticamente. 

## Cuidados
Como boa prática, não é recomendado que se faça grande aninhamentos. Uma grande cascata de elementos deixa o código perder a performace.