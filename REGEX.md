## Expressão Regular - RegEx ##
---
`/<...><busca><...>/<...>` - Estrutura base

`g` - Traga todas as referências da busca feita.

`i` - Ignore o Case Sensitive.

`^` - Busca iniciando pelo termo informado posteriormente.

`$` - Busca finalizando com o termo informado anteriormente.

`()` - Realiza um funcao de busca.

`|` - Dentro dos `()` Ou.

---
Exemplo: Banana R$ 10.00.

### `/a/` ###

busca pela primeira ocorrência da letra `a`. 

resultado: B`a`nana R$ 10.00.


### `/a/g` ###

o `g` faz com que a busca seja por todas as ocorrências da letra `a`.

resultado: B`a`n`a`n`a` R$ 10.00.

### `/b/gi` ###

o `g` busca todas as ocorrências.

o `i` ignora o case senstive, sem ele o resultado seria nenhum valor.

resultado: `B`anana R$ 10.00.

### `/^b/gi` ###

O `^` indica que quero começar com aquela letra. No caso palavras que iniciam com a letra `b`.

resultado: `B`anana R$ 10.00.

### `/^b$/gi` ###

O `$` indica que a string da busca foi finalizada. Match exato. No caso ele buscar a palavra que inicia com `b` e finaliza logo em seguida, ou seja, apenas o `b` exato. 

resultado: nada.

### `/\$/gi` ###

O `\` contra barra é usado quando quero buscar por um símbolo protegido, ou seja, no caso o `$` indica final da string de busca, porém pode contar no meu texto. 

resultado: Banana R`$` 10.00.

### `/(b|a)/gi` ###

Os parenteses `()` indicam um agrupamento de caracteres e o pipe `|` indicam a condição `OU`. Ou seja, busca a letra `b` ou `a`. 

resultado: `Ba`n`a`n`a` R$ 10.00.


Vamos alterar o exemplo para um texto para facilitar o entendimento de alguns recursos avançados do RegEx.

Exemplo: Bananada é um doce de banana com bastante banana. Nas Bananeiras do Brasil, um dos maiores produtores, estão em ótima safra. 

### `/banana(da){0,1}/gi` ###

