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

### Placeholder
O placeholder é uma maneira mais performática de reutilizar códigos que são repetidos. Diferente do mixin, ele não repete o códico e sim une todas as classes que usam o mesmo código em um só lugar.

```sh 
  # Sintaxe
  %nome-do-placeholder {
    propriedades:
  }

  # Exemplo
  %sombra-padrao {
    -webkit-box-shadow:0 2px 6.65px 0.35px;
    box-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
  }

  #chamada para uso
  @extend %sombra-padrao;

  #resultado esperado
  `contato button, .plano button, .destaque button` {
  -webkit-box-shadow: 0 2px 6.65px 0.35px;
  box-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
}
```

