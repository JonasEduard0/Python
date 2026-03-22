```md
# 🐍 Python

## 📌 Símbolos e tipos básicos

`str` — texto / palavras  
`int` — número inteiro  
`float` — número decimal  
`bool` — `True` ou `False`  

`and` — todas as condições precisam ser `True`  
`or` — pelo menos uma condição precisa ser `True`  
`!=` — diferente  
`==` — igual  
`<` — menor  
`>` — maior  
`=` — recebe valor  
`<=` — menor ou igual  
`>=` — maior ou igual  
`%` — resto da divisão  
`#` — comentário no código  
`**` — potência  
`+=` — `a = a + b`  
`in` — verifica se um valor ou trecho está contido em outro

---

## 📦 Variáveis

`type(variavel)` — mostra o tipo da variável (`int`, `str`, `float`, etc.)

`variavel = int(input("Digite o número: "))` — pede um valor, converte para inteiro e guarda na variável.  
Também pode ser feito com `int`, `float`, `bool` e `str`.

---

## 🖨️ Prints

`print("""Eu  
estou    programando""")` — imprime respeitando quebra de linha e espaçamento.

`print("\n")` — pula uma linha.

`print("numero =", numero)` — imprime a frase `"numero ="` e depois o valor da variável `numero`.

---

## 🛠️ Comandos importantes

`.format()` — insere valores dentro de uma string.

`print('A soma entre {} e {} vale {}'.format(n1, n2, s))` — o primeiro `{}` recebe `n1`, o segundo recebe `n2` e o terceiro recebe `s`.

`print(f'A soma entre {n1} e {n2} vale {s}')` — forma mais atual de inserir valores em strings.

`format` e `f-string` podem ser usados para tratar strings, mostrar cálculos, valores formatados, etc.

`n.isnumeric()` — retorna `True` se a string contém apenas caracteres numéricos. Existem vários métodos parecidos: `islower`, `isupper`, `isalpha`, `isalnum`, etc.

`{:.2f}` — mostra a quantidade de casas decimais escolhida.

`end=''` — faz o próximo `print` continuar na mesma linha.

`del(variavel)` — deleta a variável.

### Exemplo

`n1 = int(input('Digite um valor: '))`  
`n2 = int(input('Digite outro: '))`  
`s = n1 + n2`  
`print('A soma entre {} e {} vale {}'.format(n1, n2, s))`  
`print(f'A soma entre {n1} e {n2} vale {s}')`

`n = input('Digite um valor: ')`  
`print(n.isnumeric())`

---

## 🔀 If statement / Estrutura condicional simples, composta e aninhada

`if nome == 'Jonas':` — estrutura condicional simples.  
Se a variável `nome` tiver o valor `'Jonas'`, o bloco será executado.

`elif nome == 'Lucas':` — estrutura condicional aninhada. Pode ter quantos `elif` quiser. Economiza vários `if`.

`else:` — estrutura condicional composta. Executa se nenhuma condição anterior for verdadeira.

### Exemplo

`if nome == 'Jonas':`  
`    print('Meu nome')`

`elif nome == 'Lucas':`  
`    print('Nome do professor')`

`else:`  
`    print('Nome normal')`

---

## 📚 Módulos

`import math` — importa todas as funções da biblioteca `math`.

`from math import sqrt, factorial` — importa apenas `sqrt` e `factorial` da biblioteca `math`.

### Exemplo

`num = int(input('Numero 1: '))`  
`raiz = math.sqrt(num)`

Existe biblioteca para quase tudo e elas podem ser importadas para o Python.

---

## 📦 Bibliotecas / pacotes importantes

`math` — `ceil`, `floor`, `trunc`, `pow`, `sqrt`, `factorial`  
`random` — `randint`: escolhe um número inteiro aleatório entre os valores informados, ex: `random.randint(1, 10)`  
`pygame` — voltado para jogos, possui recursos como mixer de áudio  
`datetime` — relacionado a datas  
`time` — `sleep(1)`: pausa o código pelo número de segundos desejado

---

## 🔤 Tratamento de strings

`variavel = 'Curso em Vídeo Python'`

`variavel[9:13:2]` — pega do caractere 9 até o 12, de 2 em 2.  
Resultado: `vd`

`variavel[15:]` — do caractere 15 até o final.

`len(variavel)` — tamanho da string.

`variavel.count('o', 0, 13)` — conta quantos `'o'` existem do índice 0 até o 12.

`variavel.find('deo')` — mostra a posição onde começa `'deo'`. Retorna `-1` se não existir.

`'Curso' in variavel` — `True` se `'Curso'` estiver na string.

`variavel.replace('Python', 'Android')` — substitui `'Python'` por `'Android'`.

`variavel.upper()` / `variavel.lower()` — coloca tudo em maiúsculo ou minúsculo.

`variavel.capitalize()` — deixa tudo minúsculo, mas com a primeira letra maiúscula.

`variavel.title()` — coloca a primeira letra de cada palavra em maiúsculo.

`variavel.strip()` — remove espaços desnecessários no começo e no fim.

`variavel.split()` — divide a string em palavras e guarda em uma lista.

`variavel.count('x')` — quantas vezes o caractere ou trecho aparece.

> `sort()` não é método de string. É usado em listas.

---

## 🎨 Cores no terminal

`\033[0;30;40m`

Estrutura:

- primeiro número: estilo
- segundo número: cor do texto
- terceiro número: background

### Estilos mais usados

`0` — sem estilo  
`1` — negrito  
`4` — sublinhado  
`7` — inverte texto com background

### Cores do texto

`30` a `37` — respectivamente: branco, vermelho, verde, amarelo, azul, roxo, ciano, cinza

### Cores do background

Mesma ordem das cores do texto, mas de `40` a `47`.

### Exemplo

`print('\033[1;31;40mOlá mundo!')` — imprime com estilo, cor do texto e background.

`print('\033[1;31;40mOlá mundo!\033[m')` — limita a cor apenas a essa frase.

---

## 🔁 Laço / Estrutura de repetição

### For

No terceiro valor do `range`, pode colocar qualquer número. Assim, a contagem será feita pulando esse número de casas.

`for variavel in range(0, 10):` — vai de `0` até `9`.

### Exemplo

`for variavel in range(0, 10):`  
`    print('Oi')`

`for variavel in range(10, 0, -1):`  
`    print(variavel)`

`i = int(input('I: '))`  
`f = int(input('F: '))`  
`p = int(input('P: '))`  
`for c in range(i, f, p):`  
`    print(c)`

`S = 0`  
`for c in range(0, 10):`  
`    n = int(input('Valor: '))`  
`    s += n`  
`print('Soma = {}'.format(s))`

### While

`contador = 0` — enquanto o contador estiver abaixo de `5`, o bloco será executado.

`while contador < 5:`  
`    print('Palavra')`  
`    contador += 1`

#### Com `break`

`conta = 0`  
`while conta < 10:`  
`    conta += 1`  
`    if conta == 6:`  
`        break`

Quando `conta` chegar a `6`, o laço para.

#### Com `continue`

`conta = 0`  
`while conta < 10:`  
`    conta += 1`  
`    if conta == 6:`  
`        continue`

Quando `conta` chegar a `6`, ele pula o restante daquela volta e vai para a próxima.

---

## 🧩 Variáveis compostas

Podem guardar vários valores e interagir entre si.

### Tuplas

São imutáveis.

`lanche = ('h', 's', 'p', 'u')`

`print(lanche[0:3])` — mostra `'h', 's', 'p'`; o índice `3` não entra.

`for variavel in lanche:`  
`    print(variavel)`

### Listas

Parecidas com tuplas, mas mutáveis. Usam `[]`.

`lanche.remove('p')` — remove `'p'`  
`lanche.append('o')` — adiciona `'o'`

### Dicionários `{}`

São estruturas com chaves e valores personalizados.

`dados = {'nome': 'Pedro', 'idade': 25}`

- `keys()` — chaves
- `values()` — valores
- `items()` — chave + valor

`print(dados.values())`  
`print(dados.items())`

`dados['sexo'] = 'M'` — adiciona a chave `sexo` com valor `'M'`.

`del dados['idade']` — deleta a chave `idade`.

---

## ⚙️ Função

Você cria uma função para executar uma ação sempre que quiser chamá-la.

### Exemplo

`def linha():`  
`    print('-' * 30)`

`print('Parte de cima')`  
`linha()`  
`print('Parte de baixo')`

Sempre que a função `linha()` for chamada, será executada.

### Com parâmetros

`def titulo(txt):`  
`    print('-' * 30)`  
`    print(txt)`  
`    print('-' * 30)`

`titulo('Curso em Vídeo')`  
`titulo('Python é bom')`

### Parâmetro opcional

`def soma(a, b=0):` — `b=0` é parâmetro opcional.  
`    s = a + b`  
`    print(s)`

`*args` pode ser usado quando a função receber vários valores.

`def soma(a=0, b=0, c=0):`  
`    s = a + b + c`  
`    return s`

`r = soma(3, 2, 5)`  
`r2 = soma(1, 7)`  
`r3 = soma(4)`

`return` retorna o valor para ser guardado em uma variável.

---

## ❓ Interactive Help

`help()` — exibe o manual interativo.  
`help(modulo)` — mostra informações sobre um módulo, função ou comando.

---

## ⚠️ Exceção / Erro

`try` — tenta executar o bloco.  
`except` — executa se der erro.  
`else` — executa se não der erro.  
`finally` — executa em qualquer caso.

### Exemplo

`try:`  
`    a = int(input('Numerador: '))`  
`    b = int(input('Denominador: '))`  
`    r = a / b`

`except Exception as erro:`  
`    print(f'Houve um problema! Ele é {erro.__class__}')`

`else:`  
`    print(f'O resultado é {r}')`

`finally:`  
`    print('Volte sempre!')`

Se `b` receber `0`, dará erro. Com esse comando, você pode tratar o erro e exibir uma mensagem.
```
