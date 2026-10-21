# Patch Portuguese — Para The sims 2 (versao MAC OS X)

Iniciador compartilhável para a versão Mac do **The Sims 2 completo**, incluindo
as expansões instaladas no mesmo conjunto. O iniciador pede ao aplicativo do
jogo para carregar o idioma `Portuguese` sem substituir o aplicativo original,
sem alterar arquivos do sistema e sem incluir arquivos do jogo.

> Compatibilidade validada experimentalmente em um MacBook2,1 com Mac OS X Lion
> 10.7. O comportamento pode variar conforme a edição do jogo e os recursos de
> idioma instalados.

## O que este projeto faz

- instala um aplicativo separado chamado **Patch Portuguese**;
- abre o `The Sims 2.app` com o argumento `-l:Portuguese`;
- Voce tambem pode fazer isso manualmente pelo terminal com o codigo sem instalar o app : (open "/Applications/The Sims 2.localized/The Sims 2.app" --args "-l:Portuguese")
- mantém o jogo original intacto;
- funciona com instalações que já contenham os recursos de idioma em português;

O parâmetro foi testado na instalação usada no desenvolvimento. Se a instalação
de outra pessoa não tiver os recursos portugueses, o iniciador não consegue
criar a tradução sozinho e o jogo pode continuar em inglês.

## Instalação no Mac

### 1. Requisitos

- The Sims 2 para Mac instalado;
- expansões e Stuff Packs instalados, caso desejados;
- Mac OS X 10.7 ou posterior;
- acesso ao Terminal apenas para a instalação inicial.

### 2. Baixar o projeto

No Terminal:

```sh
git clone https://github.com/RafJaeger/The-Sims-2-Patch-Portugues-Mac-Version.git
cd The-Sims-2-Patch-Portugues-Mac-Version
```

### 3. Instalar o iniciador

```sh
sh macos/install.sh
```

Por padrão, ele instala somente o iniciador em:

```text
~/Applications/Patch Portuguese.app
```

Depois, abra essa aplicação pelo Finder ou execute:

```sh
open "$HOME/Applications/Patch Portuguese.app"
```

### 4. Se o jogo estiver em outro local

O iniciador procura automaticamente nos locais mais comuns. Para indicar o
caminho exato sem editar nenhum arquivo:

```sh
PATCH_PORTUGUESE_GAME_PATH="/caminho/The Sims 2.app" \
  open "$HOME/Applications/Patch Portuguese.app"
```

Exemplo para a instalação padrão usada nos testes:

```sh
PATCH_PORTUGUESE_GAME_PATH="/Applications/The Sims 2.localized/The Sims 2.app" \
  open "$HOME/Applications/Patch Portuguese.app"
```

## Instalação em `/Applications`

Se o usuário preferir deixar o iniciador junto dos outros aplicativos:

```sh
PATCH_PORTUGUESE_DEST="/Applications/Patch Portuguese.app" \
  sh macos/install.sh
```

## Como desfazer

Apague apenas o iniciador instalado. O jogo original não é modificado:

```sh
rm -rf "$HOME/Applications/Patch Portuguese.app"
```

Se ele foi instalado em `/Applications`, use o Finder ou remova somente:

```text
/Applications/Patch Portuguese.app
```

## Observações

Este repositório contém apenas código de inicialização e documentação. Cada
usuário deve fornecer sua própria cópia do jogo e seus próprios recursos de
idioma. O projeto não promete compatibilidade universal com todas as edições,
instaladores ou expansões.
