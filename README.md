![](logo-sass.png "Logo Sass")

# Sass - Let's Go! :running:

## Preparando o ambiente
> Ambiente Linux
### Instalando o Dart-Sass :zap:
>Note: Não foi utilizado o Ruby, por está descontinuado, segundo o Próprio site. Por isso utilizamos o Dart-Sass.

1) Acesse o [Repositório Dart-Sass](https://github.com/sass/dart-sass/releases/tag/1.28.0) no github;
2) Baixe o arquivo que esteja de acordo com o seu computador (**Na aba Assets**);
3) No terminal acesse o arquivo `.bashrc`, usando o seguinte comando:
```sh 
  `~/getit .bashrc`
```
4) Com o **.bashrc** aberto, na última linha digite o seguinte comando: `export PATH="your-dir:$PATH"`, onde o **your-dir** é o diretório da pasta que você salvou o arquivo dart-sass que você baixou.
```sh 
  #Exemplo
  `export PATH="~/Documentos/dart-sass:$PATH"`
  
  **Depois Salve o arquivo e feche-o. Reinicie também o terminal**
```
5) Por fim verifique se tudo foi instalado com exito. Execute o comando `sass --version` no terminal. Se aparecer a versão, deu tudo certo :)

> Caso queira instalar no Windows ou no Mac, acesse o [Path de instalação](https://katiek2.github.io/path-doc/), com todas as intruções.

### Instalando com o Node.js (via npm)
É uma opção também instalar via npm, se você usa o node.js.
```sh 
  #Execute o comando
  `npm install -g sass`
```
## Utilizando o Sass
- Compilando o arquivo Sass: `sass arquivo.scss:arquivo.css`. Será transformado no arquivo css;
- Dando um 'Watch' (Assistindo as alterações automaticamente): `sass --watch arquivo.scss:arquivo.css`. Assim não precisa compilar toda alteração.

### Mixin e Variáveis

### Variável
```sh
  #Criando uma variável
  `$nome-da-variavel: #fff`;
  
  -- Utilizando
  Basta substituir o valor que você deseja, pela variável.
```

#### Mixin
O mixin é uma forma de unir várias propriedades em um só elemento, para economizar código. Observe: 
```sh 
  # Criando um Mixin
  @mixin nome-do-mixin($valor) {
    -webkit-border-radius: $valor;
    border-radius: $valor;
  }
  
  # Utilizando o mixin
  @include nome-do-mixin(0.3em);
  
  # A utilização de valor pode ser opcional.
  # Mas ajuda para elementos que necessitam de diferentes valores, mas que tem a mesma propriedade. 
  # Neste caso você pode colocar na criação do mixin, um valor padrão e no elemento que tenha o valor diferente, passar o valor q deseja.
  
  #Exemplo:
   -- Criação
  `@mixin nome-do-mixin($valor:0.3em){ }`
  
   -- Chamada de valor diferente
   `@include nome-do-mixin(50px)`
  
```


> Note: Os comandos de utilização do Sass precisam ser dado dentro da pasta onde está o arquivo css.

### Aninhamento
![Veja aqui](Aninhamento.md) a explicação e uso do Aninhamento (Nexting)
