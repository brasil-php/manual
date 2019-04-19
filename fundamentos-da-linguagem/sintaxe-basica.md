---
description: >-
  Este tópico apresenta a sintaxe básica da linguagem e descreve o processo de
  interpretação, comentários, operadores de fluxo e etc.
---

# Sintaxe Básica

## PHP tags

Quando o PHP interpreta um arquivo ele procura pelas tags de abertura e fechamento, `<?php` e `?>`, que dizem ao PHP para iniciar ou parar a interpretação do código entre elas. Quando criamos um arquivo que será processado pelo interpretador precisamos usar. esses dois identificadores para designar que o trecho será executado pelo interpretador ou simplesmente impresso.

> A abordagem de interpretação que o PHP usa permite que a linguagem seja para diversos tipos de documentos, pois tudo que está fora dessas tags é ignorado pelo interpretador do PHP e escrito como texto. Embora o PHP seja muito comum na impressão de páginas HTML, graças à sua estratégia de interpretação ele pode ser usado para diversas outras finalidades.

```php
<?php
echo "Isto é PHP";
// o script termina aqui, sem tag de fechamento PHP
```

> Isto é PHP

Embora fosse uma prática comum não é mais recomendado usar o fechamento caso você não vá produzir alguma nova saída de texto. Se quiser saber mais sobre isso a [PSR-2](https://www.php-fig.org/psr/psr-2) trata sobre esse assunto.

{% hint style="warning" %}
Não use o fechamento do PHP como último caractere do arquivo
{% endhint %}

Quando combinamos trechos que são apenas texto e PHP temos o seguinte resultado

```php
<?php
echo "Isto é PHP";
?>
Isto não é
<?php
echo "Isto também é PHP";
```

> Isto é PHP  
> Isto não é  
> Isto também é PHP

O PHP também permite a tag curta _&lt;?_ \(cujo uso é desencorajado pois essa opção está disponível somente quando habilitada na diretiva [short\_open\_tag](https://www.php.net/manual/pt_BR/ini.core.php#ini.short-open-tag) no arquivo de configuração `php.ini`, ou quando o PHP tiver sido compilado com a opção **--enable-short-tags** \).

{% hint style="info" %}
A tag `<?=` sempre está disponível, independente do da configuração [short\_open\_tag](https://php.net/short_open_tag) do `.ini`, à partir da versão 5.4
{% endhint %}

{% hint style="danger" %}
As tags ASP &lt;%, %&gt;, &lt;%= e a script tag &lt;script language="php"&gt; foram removidos do PHP na versão 7
{% endhint %}

## Instruções

Como no C ou Perl, o PHP requer que as instruções sejam terminadas com um ponto-e-vírgula \(`;`\) ao final de cada comando. A tag de fechamento de um bloco de código PHP automaticamente implica em um ponto-e-vírgula, ou seja, não é preciso ter um ponto-e-vírgula terminando a última linha de um bloco PHP. A tag de fechamento do bloco irá incluir uma nova linha logo após, se estiver presente.

```php
<?php
echo 'Isto é '; echo 'um teste';
?>
<?php echo 'Isto será impresso' ?>

<?php echo 'Nós omitimos a última tag de fechamento';
```

> Isto é um teste  
> Isto será impresso  
>   
> Nós omitimos a última tag de fechamento

{% hint style="info" %}
É possível colocar vários comandos em uma mesma linha separados por `;`, mas isto, geralmente, não é considerado uma boa prática
{% endhint %}

## Comentários

A sintaxe de comentários no PHP é compatível com o estilo 'C', 'C++' e do Unix shell \(estilo Perl\).

### Comentário de linha

Um comentário de linha vai informar ao interpretador que ele pode ignorar tudo o que estiver escrito à partir dele seguindo até o final da linha em que ele foi declarado ou até encontrar a tag de fechamento \(`?>`\). Os operadores para comentários de linha são `//` e `#`.

```php
<?php
// estilo de comentário de uma linha em c++
echo 'Isto é um teste'; // comentário no final da linha
// echo 'Instrução ignorada';
echo 'Um teste final'; # estilo shell
```

> Isto é um teste  
> Um teste final

### Comentário de bloco

Os comentários de bloco são usados para informar ao interpretador que ele deve ignorar trechos de código. Para iniciar a área que será ignorada usamos `/*` e para finalizar usamos `*/`.

```php
<?php
echo 'Isto é um teste'/* comentário de bloco */;
/* este é um comentário de múltiplas linhas
echo "Esse echo não vai aparecer";
ainda outra linha de comentário */
echo /* comentário de bloco */'Um teste final';
```

> Isto é um teste  
> Um teste final

### Comentário de documentação

É comum de vermos um comentário de bloco que inicia com `/**` ao invés do `/*`. Esta variação do comentário de bloco costuma é usada para documentar recursos do código. Esses comentários são baseados no [PHP Doc](https://docs.phpdoc.org/references/phpdoc/index.html) e nos permitem descrever com algumas marcações informações sobre o recurso documentado.

{% hint style="info" %}
Podemos recuperar os comentários de documentação em tempo de execução usando Reflection, um exemplo é a [`ReflectionClass::getDocComment`](https://www.php.net/manual/en/reflectionclass.getdoccomment.php) que pode ser usada para pegar os `docblock` da declaração de uma classe
{% endhint %}

### Comentários e tags curtas

Quando estamos usando a sintaxe de tags curtas podemos omitir usar comentários de linha ou de blocos.

```php
<?php echo 'Isto é um teste'; ?>
<?php // echo 'Isto é um teste'; ?>
<?php # echo 'Instrução ignorada'; ?>
<?php /* echo 'Um teste final'; */ ?>
<?php
echo 'Um teste final';
?>
```

> Isto é um teste  
> Um teste final

## Trabalhando com HTML

