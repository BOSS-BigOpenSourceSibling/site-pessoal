# Template para o seu site pessoal!

Este repositório é um esqueleto para te ajudar a construir o seu site pessoal como quiser.

## Como?

### Criando o seu repositório

Crie o seu fork desse repositório para ter sua própria cópia. Vá até configurações e renomeie o nome do repositório: pode ser seu nome mesmo!

Depois de renomear, volte para o submenu `Code` no GitHub, clique no botão verde com o ícone de Download com o nome `Code` e copie a URL do seu fork.

Faça o clone do seu repositório no terminal:

```sh
git clone <url que você copiou>
```

### Instalando as dependências

Esse repositório usa o [Jekyll](https://jekyllrb.com/), uma gem [Ruby](https://www.ruby-lang.org/pt/) que permite criarmos sites estáticos que possui uma série de plug-ins e templates!

Vamos começar instalando o Ruby. Para instalar, encontre o seu sistema operacional abaixo e rode o comando indicado:

**Ubuntu, Debian ou Mint:**
```sh
sudo apt-get install ruby-full
```

**Arch Linux ou Manjaro:**
```sh
sudo pacman -S ruby
```

**macOS:**
```sh
brew install ruby
```

Se você estiver usando o Windows, use o [RubyInstaller](https://rubyinstaller.org/) para instalar o ruby.

Para outros sistemas ou distribuições, [leia aqui](https://www.ruby-lang.org/pt/documentation/installation).

Depois de instalado o ruby, instale as dependências ruby do projeto:

```sh
cd nome-do-projeto # navegue para a pasta que você clonou anteriormente
bundle install
```

### Rodando o servidor

Se tudo tiver corrido bem, agora é só rodar o servidor:

```sh
bundle exec jekyll serve
```

Abra o navegador e vá até o http://localhost:4000/site-pessoal/ para ver ao vivo!

### Fazendo minhas alterações

Comece pelo arquivo de configuração `_config.yml`. Altere como desejar para colocar seu nome, uma descrição sobre você, seu twitter (se você não tiver basta apagar a linha) e o seu usuário do Github. No campo `baseurl` preencha com `/nome-do-seu-repositório`.

Depois, altere também o arquivo `defaults.yml` que está na pasta `_data`.

Altere o conteúdo da página principal no arquivo `index.md` para deixar do seu jeito :D Se você estiver confortável com HTML e CSS, pode usar também!

Modifique livremente conforme você gostar! Este projeto usa o tema [Jekyll theme yat](https://github.com/jeffreytse/jekyll-theme-yat), você pode olhar o repositório do tema para ter mais ideias do que você pode fazer.

### Publicando

#### Configuração

Para publicar, você precisa conceder ao GitHub uma autorização de modificação. Isso pode não ser fácil da primeira vez que você for fazer, mas depois que você aprende fica tranquilo!

No Github, visite [este link](https://github.com/settings/tokens). Clique em `Generate new token`. O campo `Note` não importa, coloque o que quiser nele. Marque os campos `repo` e os sub-itens e `workflow` nele.

Clique no botão ao final da página para gerar e **copie o código token gerado** (algo parecido com `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`).

Vá ao seu repositório. Clique na aba `Settings`. No submenu, selecione `Secrets`.

Clique no botão `New repository secret`. O nome que você vai preencher precisa ser exatamente `GH_TOKEN`. No campo **Value**, cole o token que você acabou de gerar e salve suas alterações.

#### Fazendo o seu commit!

Reveja todos os arquivos alterados e revise quais você gostaria de adicionar:

```sh
git status
```

Adicione os arquivos que você quer enviar para o repositório.

```sh
git add nome-do-arquivo-1 nome-do-arquivo-2 nome-do-arquivo-3
```

**Dica:** Se você quiser adicionar todos os arquivos alterados, em vez de escrever todos nominalmente, você pode rodar apenas `git add .`!

Crie seu commit e dê um nome a ele:

```sh
git commit -m "Nome do seu commit!" # pode ser algo como: Adicionando minhas novas configurações
```

Envie suas modificações para o Github:

```sh
git push origin main
```

Agora é só esperar! O Github vai rodar a integração e publicar sua página em alguns minutos. Você poderá encontrá-la se você for em `Settings`, clicar no submenu `Pages` e clicar no link onde você pode verr que o seu site está publicado.