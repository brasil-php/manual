---
description: >-
  PHP é uma linguagem de programação que possui uma sintaxe simples e dinâmica.
  Com ela podemos criar sites e serviços para a web com uma ampla variedade de
  recursos disponíveis.
---

# Apresentando o PHP

## O que é PHP?

PHP, que significa "PHP: Hypertext Preprocessor", é uma linguagem de programação de ampla utilização, interpretada, que é especialmente interessante para desenvolvimento para a web e pode ser mesclada dentro do código HTML e outros tipos de documentos. A sintaxe da linguagem lembra C, Java e Perl, e é fácil de aprender. O objetivo principal da linguagem é permitir a desenvolvedores escreverem páginas que serão geradas dinamicamente rapidamente, mas você pode fazer muito mais do que isso com PHP.

## Pra que serve o PHP?

Como pode ser visto no próximo tópico o PHP foi criado inicialmente para produzir páginas pessoais em HTML, mas isso já mudou a muitos anos. Atualmente o PHP é amplamente usado não só na confecção de páginas HTML, mas também na criação de **API**s e **WebService**s ****em geral gerando saídas em formatos de dados apropriados como **JSON** e **XML**. Também é comum ver o PHP em **Bots** e rotinas que rodam no lado do servidor como **Queues** e **WebHooks**. Há ainda implementações de ferramentas que usam PHP de forma **assíncrona** abrindo portas para **Chats** e comunicações em **Realtime** através de sockets.

PHP acabou se tornando uma boa opção para uma linguagem de template, mas não parou por ai e correntemente pode ser usado em diversos tipos de aplicações e finalidades.

## A trajetória do PHP

A primeira versão do PHP foi escrita na linguagem de programação C por Rasmus Lerdorf em 1994 para uso no monitoramento de seu currículo on-line e informações pessoais. Por esse motivo, PHP originalmente significava "Personal Home Page". Lerdorf combinou PHP com seu próprio Form Interpreter, lançando a combinação publicamente como PHP/FI \(geralmente referido como PHP 2.0\) em 8 de junho de 1995.

Dois programadores, Zeev Suraski e Andi Gutmans \(que viriam a criar a Zend\), reconstruíram o núcleo do PHP, lançando o resultado atualizado como PHP/FI 2 em 1997. Neste momento, a sigla foi formalmente alterada para PHP: "HyperText Preprocessor" \(este é um exemplo de acrônimo recursivo: onde o próprio acrônimo está em sua própria definição\).

Estas primeiras versões do PHP eram uma espécie de simplificações das estratégias de programação para a web usadas na época como CGI e/ou Perl . Em 1998, o PHP 3 foi lançado, e já não era apenas uma abstração para criar páginas HTML usando Shell, Bash ou Perl, tornando-se a primeira versão amplamente utilizada.

Cerca de dois anos depois, em maio de 2000, o PHP 4 foi lançado com um novo núcleo conhecido como o Zend Engine 1.0. Esta nova versão apresentava maior velocidade e confiabilidade em relação ao PHP 3. Em termos de recursos, o PHP 4 adicionou referências, o tipo Boolean, suporte COM no Windows, buffer de saída, muitas novas funções de array, programação orientada a objeto expandida, inclusão da biblioteca PCRE, e mais. ‌

O PHP 5 foi lançado em julho de 2004, com o motor Zend atualizado. Como uma das versões mais robustas até então o PHP 5 foi amplamente utilizado no mundo todo e levou o PHP à ser responsável por mais de 70% dos recursos da web. Em algumas pesquisas esse índice chegou à mais de 80% deixando clara a hegemonia do PHP nas aplicações para internet.

Em dezembro de 2015 foi lançada o PHP 7. Esta versão foi liderada principalmente por Dmitry Stogov, Xinchen Hui e Nikita Popov e foi uma reescrita completa do core da linguagem. As implementações feitas no PHP 7 colocaram o PHP de volta no topo das opções de linguagens para a web já que trouxeram um ganho de performance muito grande e correções de problemas críticos.

## Documentação oficial

É possível encontrar muita documentação na internet, em videos, forums e grupos do telegram, mas sem dúvida, a melhor que você poderá encontrar será o seu próprio manual online, traduzido em diversas linguás.

[https://www.php.net/manual/pt\_BR](https://www.php.net/manual/pt_BR/)

## Curadoria

{% embed url="https://phptherightway.com" caption="Uma referência às boas práticas no PHP" %}

{% embed url="https://github.com/ziadoz/awesome-php" caption="Repositório com uma curadoria de recursos para PHP" %}

{% embed url="https://getcomposer.org" caption="Composer é o gerenciador de dependências mais usado no PHP" %}

{% embed url="https://www.php.net/manual/pt\_BR" caption="Documentação do PHP" %}

{% embed url="http://cursoemvideo.com" caption="Plataforma de ensino que possui vários cursos de PHP gratuitos" %}

{% embed url="https://packagist.org" caption="Um dos repositórios de pacotes para projetos PHP mais usado" %}

{% embed url="https://medium.com/php-brasil" caption="Blog de posts da nossa comunidade" %}

## Interface de linha de comando

O PHP é um motor de interpretação e tem uma interface de linha de comando que pode ser usada em diversos cenários. Para fazer uso do CLI é preciso ter o PHP instalado no dispositivo e expor o caminho de instalação nas variáveis de ambiente. Dessa forma é possível executar as instruções pelo terminal usando o comando `php`. No bloco de código abaixo temos um exemplo de uso do comando `php` usando a opção `-h` para mostrar o menu de ajuda \(a letra _h_ vem de _help_\).

```text
$ php -h
Usage: php [options] [-f] <file> [--] [args...]
   php [options] -r <code> [--] [args...]
   php [options] [-B <begin_code>] -R <code> [-E <end_code>] [--] [args...]
   php [options] [-B <begin_code>] -F <file> [-E <end_code>] [--] [args...]
   php [options] -S <addr>:<port> [-t docroot] [router]
   php [options] -- [args...]
   php [options] -a

  -a               Run as interactive shell
  -c <path>|<file> Look for php.ini file in this directory
  -n               No configuration (ini) files will be used
  -d foo[=bar]     Define INI entry foo with value 'bar'
  -e               Generate extended information for debugger/profiler
  -f <file>        Parse and execute <file>.
  -h               This help
  -i               PHP information
  -l               Syntax check only (lint)
  -m               Show compiled in modules
  -r <code>        Run PHP <code> without using script tags <?..?>
  -B <begin_code>  Run PHP <begin_code> before processing input lines
  -R <code>        Run PHP <code> for every input line
  -F <file>        Parse and execute <file> for every input line
  -E <end_code>    Run PHP <end_code> after processing all input lines
  -H               Hide any passed arguments from external tools.
  -S <addr>:<port> Run with built-in web server.
  -t <docroot>     Specify document root <docroot> for built-in web server.
  -s               Output HTML syntax highlighted source.
  -v               Version number
  -w               Output source with stripped comments and whitespace.
  -z <file>        Load Zend extension <file>.

  args...          Arguments passed to script. Use -- args when first argument
                   starts with - or script is read from stdin

  --ini            Show configuration file names

  --rf <name>      Show information about function <name>.
  --rc <name>      Show information about class <name>.
  --re <name>      Show information about extension <name>.
  --rz <name>      Show information about Zend extension <name>.
  --ri <name>      Show configuration for extension <name>.

```

### Exemplos de uso

Vamos listar alguns de uso da interface de linha de comando do PHP. Esta seção é meramente informativa e tem como objetivo demonstrar o poder do PHP como interface de linha de comando.

{% hint style="info" %}
Os códigos PHP usados no exemplo são explicados na seção [Fundamentos da Linguagem](fundamentos-da-linguagem/)
{% endhint %}

#### Executar arquivos

É possível executar um arquivo usando a linha de comando, basta digitar o comando como o exemplo abaixo.

```text
$ php index.php
```

Imaginando que o conteúdo do arquivo `index.php` seja o que está logo abaixo a saída no terminal será a que tem no bloco subsequente ao que mostra o conteúdo do arquivo `index.php`.

{% code-tabs %}
{% code-tabs-item title="index.php" %}
```php
<?php
echo "Vamos executar PHP no terminal?", PHP_EOL;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

> Vamos executar PHP no terminal

#### Console interativo

Usando a opção `-a` o PHP é iniciado um terminal interativo onde você pode executar comandos PHP e ter a saída no próprio console.

```text
$ php -a
```

![Exemplo de uso da fun&#xE7;&#xE3;o var\_dump no terminal interativo](.gitbook/assets/image%20%281%29.png)

{% hint style="success" %}
Para conhecer mais sobre o uso do PHP no terminal leia a seção [Usando o PHP no terminal](usando-o-php-no-terminal.md)
{% endhint %}

## PHP e o HTTP

Loren ipsum

