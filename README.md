![Pure CSS Components Logo](logo-pcc.jpg "Pure CSS Components")

# Sass - Let's Go! :running:

## Preparando o ambiente
> Ambiente Linux - Ubunto
### Instalando o Ruby :gem:
```sh
  `sudo apt-get install ruby`
```
Para conferir se foi instalado com êxito, basta executar o comando: `ruby --version`. Se aparecer a versão, então deu certo :)

### Instalando o Sass :zap:
```sh
  ## Principal
  `sudo gem install sass`
  
  ## Gem's importantes
  `sudo gem install compass`
  `sudo gem install ruby-sass`
  `sudo gem install listen`
```
> Note: Caso queria ver se o Sass foi instalado com êxito, basta usas `sass --version`. Caso apareça a versão, deu certo!

## Utilizando o Sass
- Compilando o arquivo Sass: `sass arquivo.scss:arquivo.css`. Será transformado no arquivo css;
- Dando um 'Watch' (Assistindo as alterações automaticamente): `sass --watch arquivo.scss:arquivo.css`. Assim não precisa compilar toda alteração.

> Note: Os comandos de utilização do Sass precisam ser dado dentro da pasta onde está o arquivo css.
