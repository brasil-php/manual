---
description: >-
  É muito comum usar o PHP na construção de documentos HTML para a criação de
  templates. É possível combinar código PHP com a sintaxe HTML para criar
  páginas dinâmicas.
---

# Trabalhando com HTML

Tudo o que estiver fora das tags PHP \(`<?php` e `?>`\) é ignorado pelo interpretador, o que permite arquivos PHP de conteúdo misto. Veja o trecho de código à seguir onde é combinado códigos HTML e PHP para gerar uma saída.

{% code-tabs %}
{% code-tabs-item title="index.php" %}
```php
<p>
Isto vai ser ignorado pelo PHP, 
mas estará no resultado do processamento deste documento.
</p>
<?php echo 'Este trecho será interpretado.'; ?>
<p>Este trecho também estará no resultado.</p>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

> &lt;p&gt;  
> Isto vai ser ignorado pelo PHP,   
> mas estará no resultado final do processamento deste documento.  
> &lt;/p&gt;  
> Este trecho será interpretado.  
> &lt;p&gt;Este trecho também estará no resultado final.&lt;/p&gt;



