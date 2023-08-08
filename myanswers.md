# AULA 4

1. 

a) Os nomes de variáveis são escritos em snakecase, letras minusculas, deve iniciar com um _ (há uma convenção de que variáveis iniciadas por _ são variáveis descartáveis) ou uma letra (não são permitidos iniciar com números) e não podem haver escape characters como !?espaço no centro do nome da variável. Ao nomear o importante é ter um nome claro e curto e ser um substantivo simples ou um substantivo adjetivado.

b) constantes são escritas totalmente em letras maíusculas e devem ter um nome que demonstre clareza no seu papel ou utilidade.

c) métodos são escritos todo em minúsculo em snakecase, separando palavras por _ e devem representar ações. O ideal é uma escolha clara de verbos. um ! no final do método explicita que este é um método destrutivo, que altera o objeto inicial e ? que é um método que retorna um valor boolean, estes portanto fazem verificações.

d) interrogações explicitam que o método retorna um valor booleano, true ou false, 0 ou 1.

e) métodos destrutivos que alteram o objeto recebido, não retornam uma cópia modificada.

f) operadores aritmeticos no ruby são métodos, já que tudo é um objeto, as operações estão presentes como métodos e podem ser feitas com 1.+(1) que resultará em 2. É um fun fact interessante que remonta a conhecimentos teóricos de compiladores e linguagens de programação

g) operações entre inteiro e inteiro resultam em um inteiro, entre float e inteiro em float e float float em float

h) o cast no ruby é feito por meio de um método no formato .to_<insira_a_inicial_do_tipo_do_objeto> por exemplo .to_s para string, .to_i para inteiro, .to_f para float.

i) a conversão de float para inteiro não arredonda, apenas remove a flutuação e fica com a parte inteira do valor. Ex: 5.6.to_i = 5

j) os métodos .even? e .odd? retornam true para a verificação e falso para negativo.

k) o método .methods em um objeto retorna uma lista de todos os métodos disponíveis para uso desse objeto

l) string literals é o nome dado para cadeias de texto (strings) delimitadas por aspas simples ''. Essas strings são mais performáticas já que não apresentam utilidades extras como interpolação. A recomendação é utilizá-las quando o valor não será alterado no decorrer do código.

m) escape characters são uma forma de representar caracteres que normalmente são interpretados pela linguagem de uma forma literal. Por exemplo, espaço é \s, tabulação é \t, para representar uma contrabarra \\ 

n) \\, \b, \n, \s, \t, \' e \"

o) interpolação é o nome dado à operação de substituição de um valor de uma variável dentro de outro contexto, no caso do ruby em uma string. A sintaxe utilizada é "logo à frente vem uma variavel interpolada #{variavel}".

p) aspas duplas permitem interpolação, aspas simples não. Devido essa funcionalidade, caso não haja uma interpolação, uma alteração na string no decorrer do código de forma variável, utiliza-se aspas simples.

q) podemos usar o operador aritmetico + com strings como 'eu' + ' voce', ou usar o << (shovel) com 'eu' << ' voce' ou usar o metodo concat com 'eu'.concat ' voce', o interessante é que dá pra usar concat em cadeia

r) 

    1. basta acessar com um valor numerico como batata = 'batata' e batata[0] = b

    2. também dá pra pegar varios index de uma vez como batata[0..2] = bat

    3. se você usar valores negativos ele conta ao contrário. começa do -1, no caso batata[-1] = a

    4. o intervalo com dois pontos é um intervalo inclusivo, inclui o ultimo valor.

    5. é um intervalo exclusivo, não inclui o ultimo valor 

    6. o método .capitalize coloca a inicial da string em maiuscula entao tipo 'thiago'.capitalize retorna 'Thiago' mantendo o valor anterior e 'thiago.capitalize!' retorna 'Thiago' alterando a string de entrada.

    7. dá pra fazer .include('substring')?

    8. dá pra fazer .uppercase com ! ou sem.

    9. .downcase com ! ou sem.

    10. .empty? retorna vazio para ''. 

    11. .lenght

    12. .sub " ", "-"

    13. .gsub " ", "-"

    14. 

    15. .delete" "

    16. 

    17. .to_s

s) Simbolos são identificados no ruby. O seu motivo de existência é que elas ocuparão sempre o mesmo endereço de memória e serão sempre o mesmo objeto em todo e qualquer escopo de código. Normalmente são utilizadas como chaves para hashs

t) exponenciação em ruby é feita utilizando o operador ** como 2**3 = 8

u) enquanto strings são armazenadas na memoria mesmo que exista outra string com o mesmo valor repetido, simbolos são únicos e imutáveis em toda execução do código.

v) 

1. false

2. true

3. true

w) São valores true ou false True ou False, 0 ou 1, que estão para sim ou não, positivo ou negativo. São muito úteis para representar um estado ou fazer uma verificação de valor.

x) o valor nil em Ruby é quando não há valor nenhum armazenado, não há nada.

y) Operadores de assignment são atalhos sintaticos para operações aritmeticas destrutivas, ou atribuições. Há um para cada operação aritmetica: += -= /= *= **=, o padrãozao =, os insanos |= que faz operação bitwise for de x |= 0b1100 e atribui a x, &= realiza bitwise and e atribui a x, ||= só atribui o valor da direita à variavel à esquerda se e somente se x for nil ou false, &&= atribui somente se x for true e >>= realiza deslocamento à direita e <<=realiza deslocamento à esquerda.

2. Variáveis são identificadores para espaços de memória que serão preenchidos com uma variedade de valores durante qualquer uma das execuções do código.

3. 

a) variaveis sao escritas em snakecase em letras minusculas separadas por _ sendo substantivos ou substantivos adjetivados que deixem claro o papel e utilidade daquela variavel no sistema

b) snake case

c) em outras linguagens é comum existir a sintaxe int a,b = 1. No ruby como não há força de tipagem, as variaveis também não são escritas com a,b=1. Isso é a sintaxe reservada para outro tipo de ação. No ruby as variaveis são atribuidas varias de uma vez fazendo atribuições em sequencia, o correto seria: a=b=1.

d) desestruturação é como se faz a atribuição quebrando outro valor. Isso funciona pra strings, arrays, hashs, até objetos (é o que é feito quando voce faz |variavel| do). a,b = "abc" resultara em a= "a" e b="b".

e) a,b = b,a resulta em a= "b" e b = "a".