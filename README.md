# Sistemas especialistas
## Método fraco
mecanismo de busca de uso geral que procurava reunir passos elementares de raciocínio para encontrar soluções completas. Embora gerais, não podiam ter aumento de escala para instâncias grandes ou difíceis. "Podemos dizer que, para resolver um problema difícil, praticamente é necessário já saber a resposta."<sup>[^1] </sup>
Para resolver o problema de inferir a estrutura molecular a partir das informações fornecidas por um espectrômetro de massa,  Ed Feigenbaum, Bruce Buchanan e Joshua Lederberg desenvolveram o programa DENDRAL em 1969. A entrada do programa consiste na fórmula elementar da molécula e o espectro de massa que fornece as massas dos diversos fragmentos da molécula quando ela é bombardeada por um feixe de elétrons. O problema abordado pelo DENDRAL é intratável mesmo para moléculas de tamanho moderado, e em consulta com especialistas em química analítica a equipe descobriu que eles trabalhavam buscando por padrões conhecidos de picos no espectro que sugerissem subestruturas comuns na molécula.
O DENDRAL se tornou importante pois representou o primeiro sistema bem-sucedido de conhecimento intensivo: sua habilidade derivava de um grande número de regras de propósito específico, sendo poderoso não porque incorporava conhecimento relevante do tema na forma de princípios básicos mas sim "receitas de bolo" eficientes.
## Fator de certeza
MYCIN, um sistema de diagnóstico de infecções no sangue, se diferenciava do DENDRAL de duas maneiras importantes: Primeiro, não haviam modelos teóricos gerais a partir do qual regras pudessem ser deduzidas; Segundo, as regras incorporadas ao MYCIN tinham que refletir a incerteza associada ao conhecimento médico, levando à implementação de um cálcul de icnerteza chamado fatores de certeza.
 

# Sistemas Nebulosos / Fuzzy
## Sets Fuzzy
Elementos de um set podem pertencer a vários graus variáveis de pertencimento. Ao contrário da teoria de sets convencional, num set fuzzy podemos aplicar conceitos como "baixa renda" ou "alta inflação" e "pequeno erro de aproximação", conceitos os quais a quantificação convencional de sim/não não são aplicáveis – ou quando aplicáveis se mostram superficiais e restritivos. [^2]
O conceito de um Set Fuzzy foi definido por Zadeh (1965) de forma simples: Um set fuzzy A captura seus elementos ao designa-los com graus variáveis de pertencimento, quanto maior o grau de pertencimento  A(x), maior é o nível de pertencimento do elemento ao set A.
Diferentemente do conceito de Sets tradicional , os sets Fuzzy oferecem transições suaves entre os limites de campos A e B de maneira ideal à captura de noções de pertencimento parcial.
Os sets fuzzy surgem de maneiras fundamentalmente diferentes quando se trata de formulação e resolução de problemas:
	Explicito: 
		Conceitos básicos e de certa forma génericos usados na lingua e descrição da realidade. Tempo de espera **curto**, Dataset **grande**, Velocidade **alta**.
	Implícito:
		Conceitos mais complexos e inerentemente multifacetados aonde sets fuzzy podem ser incorporados na descrição formal e quantificação de problemas, mas ainda assim não de maneira tão instantânea. Carro **preferido**, **estabilidade** do sistema, economia **forte**. Esses conceitos e classificadores são evidentemente multifacetados e podem involver um número de descritores essenciais que quando juntos são efetivos em refletir a noção do que se tem em mente. Um "carro **preferido**" por exemplo: Pode involver diversos fatores como manutenção, confiabilidade, economia.
Em um modelamento Fuzzy, enquanto ainda nos preocupamos com acurácia do modelo resultante, a interpretabilidade e transparência se tornam de igual ou as vezes maior relevância. Em áreas únicas de aplicações, sets Fuzzy formam um alicerce metodologico e entregam a configuração algoritmica necessária: em modelagens fuzzy nas quais se inicia com coleções de granulos de informações (fuzzy sets) e se constrói um modelo como uma rede de associações entre eles.

## Interpretação dos sets Fuzzy




[^1] : RUSSELL, Stuart J; NORVIG, Peter. **Inteligência artificial:** uma abordagem moderna. 4. Rio de Janeiro: GEN LTC, 2022. 1 recurso online.
[^2] : W. Pedrycz and F. Gomide, Fuzzy Systems Engineering: Towards Human-Centric Computing, IEEE Press/Wiley International, 2007;




[^1]: 
