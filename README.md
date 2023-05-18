**********NATIVE_ARRAY_FUNCTION**********

````count()```` = mostra a qtd de items no array;

funcão q pega  a diferença entre dois arrays e gera um novo com os itens do primeiro array q ñ estao no segundo

````array_diff()```` => recebe dois parâmetros o array inicial e dps o que iremos comparar

````array_filter()```` => filtra algo no array, recebe o array e um callback que será nosso filtro.
ela precisa retornar true or false, se for true, automaticamente, nosso items do array já estraão filtrados no array alvo, sem a necessidade de ter um ````array_push()````;

```array_map()``` => percorre nosso array, como o nome já diz "map", mapeia algo, ele recebe doi parâmetros: 1º a função callback e o segundo o próprio array. é usada para aplicar uma função a cada elemento de um ou mais arrays, retornando um novo array contendo os resultados.

```array_pop()``` => remove o último item do nosso array.
```array_shift()``` => remove o primeiro item do nosso array;

```in_array()``` => serve pra buscar algo no array, primeiro parâmetro é o que vamos buscar e o segundo o nosso próprio array. Podemos usá-la dentro de um if, por exemplo. Esse tipo de função retorna apenas se tem algo ou não.

````
<?php
$numbers = [10,20,24,91,18];

if(in_array(24, $numbers)) {
    echo "We found it";
} else 
    echo "Try it again!";
````

```array_search``` além de dize se tem algo ou não, ira retornar a posição; Exemplo

```
<?php
$name = [
    'joao',
    'hugo',
    'cowboy',
    'ana',
    'rosane'
];

$pos = array_search('hugo', $name);

echo $pos;
// 1
```

```sort()``` => função para ordenar um array, seja de string ou numbers.

```
<?php
$name = [
    'joao',
    'hugo',
    'cowboy',
    'ana',
    'rosane'
];

sort($name);

print_r($name);

// Neste caso, ele irá retornar o array em ordem alfabética.

podeos fazer do último para o primero:
rsort($name)
```

vele lembrar que qunado usamos isso, a chave do nosso array tbm é alterada, por exemplo a chave do item 4 é 4, se usarmos a função ``rsort($name)`` ele passa a ser o item 0 de chave 0;
Para eviatar isso, usamos o 
``asort($name)`` ele muda a ordem e mantém as key do array;

se quiser usar do útlimo para o primeiro: ``arsort($name)``;

Assim como a função ````explode```` é usada para dividir uma string em um array de substrings com base em um delimitador especificado. Temo a função ``implode``,  que de mesmo modo trabalha, porém, com ela, podemos transformar um array em string;


*****************************************