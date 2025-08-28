# Sistemas especialistas
## Método fraco
mecanismo de busca de uso geral que procurava reunir passos elementares de raciocínio para encontrar soluções completas. Embora gerais, não podiam ter aumento de escala para instâncias grandes ou difíceis. "Podemos dizer que, para resolver um problema difícil, praticamente é necessário já saber a resposta."<sup>[^1] </sup>
Para resolver o problema de inferir a estrutura molecular a partir das informações fornecidas por um espectrômetro de massa,  Ed Feigenbaum, Bruce Buchanan e Joshua Lederberg desenvolveram o programa DENDRAL em 1969. A entrada do programa consiste na fórmula elementar da molécula e o espectro de massa que fornece as massas dos diversos fragmentos da molécula quando ela é bombardeada por um feixe de elétrons. O problema abordado pelo DENDRAL é intratável mesmo para moléculas de tamanho moderado, e em consulta com especialistas em química analítica a equipe descobriu que eles trabalhavam buscando por padrões conhecidos de picos no espectro que sugerissem subestruturas comuns na molécula.
O DENDRAL se tornou importante pois representou o primeiro sistema bem-sucedido de conhecimento intensivo: sua habilidade derivava de um grande número de regras de propósito específico, sendo poderoso não porque incorporava conhecimento relevante do tema na forma de princípios básicos mas sim "receitas de bolo" eficientes.
## Fator de certeza
MYCIN, um sistema de diagnóstico de infecções no sangue, se diferenciava do DENDRAL de duas maneiras importantes: Primeiro, não haviam modelos teóricos gerais a partir do qual regras pudessem ser deduzidas; Segundo, as regras incorporadas ao MYCIN tinham que refletir a incerteza associada ao conhecimento médico, levando à implementação de um cálcul de icnerteza chamado fatores de certeza.
 

# Sistemas Nebulosos / Fuzzy
## Sets Fuzzy
Elementos de um set podem pertencer a vários graus variáveis de pertencimento. Ao contrário da teoria de sets convencional, num set fuzzy podemos aplicar conceitos como "baixa renda" ou "alta inflação" e "pequeno erro de aproximação", conceitos os quais a quantificação convencional de sim/não não são aplicáveis – ou quando aplicáveis se mostram superficiais e restritivos. <sup>[^2]</sup>
O conceito de um Set Fuzzy foi definido por Zadeh (1965) de forma simples: Um set fuzzy A captura seus elementos ao designa-los com graus variáveis de pertencimento, quanto maior o grau de pertencimento  A(x), maior é o nível de pertencimento do elemento ao set A.
Diferentemente do conceito de Sets tradicional , os sets Fuzzy oferecem transições suaves entre os limites de campos A e B de maneira ideal à captura de noções de pertencimento parcial.
Os sets fuzzy surgem de maneiras fundamentalmente diferentes quando se trata de formulação e resolução de problemas:
	Explicito: 
		Conceitos básicos e de certa forma génericos usados na lingua e descrição da realidade. Tempo de espera **curto**, Dataset **grande**, Velocidade **alta**.
	Implícito:
		Conceitos mais complexos e inerentemente multifacetados aonde sets fuzzy podem ser incorporados na descrição formal e quantificação de problemas, mas ainda assim não de maneira tão instantânea. Carro **preferido**, **estabilidade** do sistema, economia **forte**. Esses conceitos e classificadores são evidentemente multifacetados e podem involver um número de descritores essenciais que quando juntos são efetivos em refletir a noção do que se tem em mente. Um "carro **preferido**" por exemplo: Pode involver diversos fatores como manutenção, confiabilidade, economia.
Em um modelamento Fuzzy, enquanto ainda nos preocupamos com acurácia do modelo resultante, a interpretabilidade e transparência se tornam de igual ou as vezes maior relevância. Em áreas únicas de aplicações, sets Fuzzy formam um alicerce metodologico e entregam a configuração algoritmica necessária: em modelagens fuzzy nas quais se inicia com coleções de granulos de informações (fuzzy sets) e se constrói um modelo como uma rede de associações entre eles.

## Interpretação dos sets Fuzzy

A ideia de "fuzziness" é conceitualmente e formalmente diferente do conceito de probabilidade, visto que características como "alto" e "baixo" são imprecisas enquanto que características mais comuns na probabilidade como "cara" e "coroa" (no caso clássico de um lançamento de moeda) são mais bem definidos. Enquanto que sets fuzzy são funções de pertencimento (membership functions) – mapeamentos de um dado universo sendo discutido relativo ao intervalo analisado – probabilidade se trata de funções cujo mapeamento é um set de subgrupos de um grupo. A teoria dos Set Fuzzy assume que o universo sendo analisado é bem definido e seus elementos são atribuídos a classes na forma de uma escala numérica.
## Funções de pertencimento
### 1. Funções de pertencimento triangulares
Modelos mais simples possiveis quando se trata de graduar o pertencimento, visto que eles são definidos inteiramente por apenas três parâmetros. 
$$ 
A(x, a, m, b) =
\begin{cases}
0, & \text{if } x \leq a \\
\frac{x - a}{m - a}, & \text{if } x \in [a, m) \\
\frac{b - x}{b - m}, & \text{if } x \in [m, b] \\
0, & \text{if } x \geq b
\end{cases}
$$
	a = Mínimo;
	b = Máximo;
	m = Valor Modal 
![[Pasted image 20250826175317.png]]
A sensibilidade da função triangular – O quanto alterações nas entradas da função alteram a saída (valor de pertencimento) – pode ser medida ao calcularmos sua derivada, que nos permite concluir que a sensibilidade é constante.
### 2. Funções de Pertencimento Trapezoidal

### 3. Funções de T-Pertencimento

### 4. Funções de S-Pertencimento

### 5. Funções de Pertencimento Gaussiano

### 6. Funções de Pertencimento Exponential-Like

## Números Fuzzy E Intervalos
Modelagem de quantidades imprecisas e captura do conceito inato de numeros aproximados ("entre dois e três", "mais que 10", "mais ou menos 5").
Quantidades fuzzy sumarizam dados númericos ao categorizar linguisticamente sets fuzzy cujo universo é os números reais. Uma variável pode ser caracterizada por valores impreciso mas ter um significado preciso; quando limites não são claramente definidos as quantidades se tornam números fuzzy ou intervalos, visto que nesses casos ambos são quantidade com significado preciso mas com valores imprecisos.

Na maioria dos casos práticos, parâmetros de modelos são apenas as estimativas devido à falta de informação, dados ou dificuldade/custo de obter os valores precisos. Em modelos de otimização clássicos, dados incertos são substituidos pelas médias dos seus adjacentes, mas na otimização dos modelos fuzzy o uso de dados granulares (aproximados) e subjetivos é permitido. Desta forma, as decisões tomadas são mais robustas, o modelo se torna mais crível e os custos de processamento de dados são reduzidos.

## Variáveis Linguísticas
Quando se trata de temperaturas, termos como "confortável" podem ser tratados como uma forma de sumarizar informação na forma de granulação, visto que este termo é usado pra aproximar uma caracterização de fenômenos complexos ou mal-definidos. Assim, usa-se sets fuzzy para mapear termos finitos para uma escala linguística cujos prórpios valores são sets fuzzy. Partindo da ideia de que sets fuzzy servem para represnetar coleções e conjuntos com limites incertos através de funções de pertencimento, podemos afirmar que os sets fuzzy provém meios de integrar quantidades númericas e linguísticas ao ligar computação com palavras e computação granular.

Por fim, podemos definir "Variáveis linguísticas" como sendo uma variavel cujos valores são sets fuzzy. Formalmente Variáveis Linguísticas são caracterizadas por um quinteto ${X, T(X), \mathbb{X}, G }$
	X : Nome da Variavel
	T(X): Termo de X cujos elementos são as os rótulos L dos valores linguísticos de X
	G - A gramática que gera os rótulos de X
	M - Regra semântica que designa a cada rótulo L pertencente à T(X) um significado cuja realização é um set fuzzy do conjunto universo $\mathbb{X}$ cuja variável base é x.
![[Pasted image 20250826190902.png]]
Quando se trata de variáveis linguísticas, um valor "positivo" pode ser visto como um set composto por {"concordo", " concordo muito ", "Indiferente","Discordo", "Discordo Muito"}

## Modelagem de um Sistema Fuzzy
Distinguimos três componentes funcionais de um modelo aonde cada um possui objetivos bem definidos:
1. Interface de entrada (Input Interface) : 
	Coleção de Sets Fuzzy e Relações Fuzzy que ligam o modelo ao seu núcleo processador e ao mundo exterior
2. Núcleo Processador: 
	Toda a computação à nivel dos fuzzy sets 
3. Interface de Saída:
	Converte o resultado do processamento granular em formatos aceitaveis pelo ambiente de modelagem

Modelos baseados em regras dotadods de modelos locais formando suas conclusões são comumente chamados de Fuzzy Funcional ou Modelos Fuzzy Takagi-Sugeno e são governados pela formula :
Se $X{_1}$ é $A{_i}$ e $X{_2}$ é $B{_i}$ e ... então $y$ é $f{_i}(x,a{_i})$
Aonde $f{_i}(x,a{_i})$ é o modelo local multivariavel; $x = [x{_1}, x{_2}, ..., x{_n}]^T$  é o vetor de variaveis base $X{_1}, X{_2}, ..., X{_n}$ ; e $a{_i}$ é um vetor de parâmetros $a{_i} = [a{_i,_1}, a{_i,_2},..., a{_i,_n}]^T$ 
## Modelos Fuzzy Tabulares
São formados por tabelas de relacionamento entre as variaveis do sistema granulados por sets fuzzy. Dados dois sets fuzzy A e B de entrada, e um set fuzzy de saída C, construímos uma tabela de relacionamentos ao associar os sets A e B com as saídas C. 
Em casos nos quais temos multiplos sets de entrada, o resultado é tabelas multidimensionais. A vantagem evidente deste tipo de modelo é sua legibilidade; a desvantagem reside no fato de não termos mecanismos de mapeamento direto. Desta forma, não há mecanismos de transformar entradas em suas respectivas saídas, ademais, a legibilidade do modelo pode ser substancialmente impactada pelo aumento do número de variáveis.
![[Pasted image 20250827201346.png]]
## Sistemas Baseados em Regras
Altamente modulares e facilmente e expansíveis devido ao fato de serem compostos por uma família de regras ("se – então") aonde sets fuzzy ocorrem nas condições e conclusões. O formato padrão é :
Se $condição{_1}$ é $A$ e $condição{_2}$ é $B$ e ... $condição{_n}$ é $W$ então $conclusão$ é $Z$ 
Aonde A, B, até Z são sets fuzzy definidos nos espaços de entrada e saída correspondentes. As `condições` do `Se` são chamadas de regras antecedentes enquanto as `conclusão` do `então` são chamadas de regras.
## Modelos Fuzzy Relacionais E Memórias Associativas

## Árvores de Decisão Fuzzy
## Redes Neurais Fuzzy
## Rede de Unidades de Processamento Fuzzy

## Verificação e Validação de Modelos Fuzzy

[^1] : RUSSELL, Stuart J; NORVIG, Peter. **Inteligência artificial:** uma abordagem moderna. 4. Rio de Janeiro: GEN LTC, 2022. 1 recurso online.
[^2] : W. Pedrycz and F. Gomide, Fuzzy Systems Engineering: Towards Human-Centric Computing, IEEE Press/Wiley International, 2007;




[^1]: 
