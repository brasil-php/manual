---
description: Variáveis e "variáveis variáveis"
---

# Variáveis

## Variáveis

O PHP possui o que é geralmente chamado de tipagem dinâmica. Em resumo o PHP não obriga que você defina o tipo da variável em sua declaração, e nem que você declare uma variável para que ela seja usada, ela pode simplesmente ser declarada em qualquer lugar de seu código. Voltando aos tipos, uma mesma variável pode assumir qualquer tipagem, isso vai ser determinado pelo tipo de dado que esta sendo assimilado a ela na execução.

```php
$variavel = "Meu Nome";
echo gettype($variavel); // Res: string
$variavel = 1990;
echo gettype($variavel); // Res: integer
$variavel = 12.2;
echo gettype($variavel); // Res: double
$variavel = array("nome" => "Seu nome");
echo gettype($variavel); // Res: array

// Conheça mais sobre a função gettype em:
// https://www.php.net/manual/pt_BR/function.gettype.php
```

Como o exemplo acima, a mesma variável toma para si a tipagem de seu valor, por isso o terma "tipagem dinâmica". 

## "Variáveis variáveis"

"Variáveis variáveis" é um termo usado para definir a prática de usar o valor `string` de uma variável que coincida com o nome de uma outra variável no mesmo escopo através de um `$` antes do `$` que já existe normalmente no nome da variável para acessar o conteúdo dela.

```php
$outraVariavel = 10;
$variavel = 'outraVariavel';
echo $$outraVariavel; // 10
```

Esta prática pode ser útil em momentos em que você precise acessar dinâmicante o valor de uma variável.

{% hint style="danger" %}
Essa abordagem pode gerar fluxos que dificultam a leitura do algoritmo. Use com moderação.
{% endhint %}

