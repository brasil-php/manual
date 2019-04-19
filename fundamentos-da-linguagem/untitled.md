---
description: Variáveis e "variáveis variáveis"
---

# Variáveis

## Variáveis



## "Variáveis variáveis"

"Variáveis variáveis" é um termo usado para definir a prática de usar o valor `string` de uma variável que coincida com o nome de uma outra variável no mesmo escopo através de um `$` antes do `$` que já existe normalmente no nome da variável para acessar o conteúdo dela.

```php
$outraVariavel = 10;
$variavel = 'outraVariavel';
echo $$outraVariavel; // 10
```

Esta prática pode ser útil em momentos em que você precise acessar dinamitante o valor de uma variável.

{% hint style="danger" %}
Essa abordagem pode gerar fluxos que dificultam a leitura do algoritmo. Use com moderação.
{% endhint %}

