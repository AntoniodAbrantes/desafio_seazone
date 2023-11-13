# Análise de Dados - Desafio Seazone

## Descrição do Desafio
O desafio consiste em analisar os dados de "details" e "rating" de anúncios no Booking para responder a uma série de perguntas.

## Início do Desafio
Criei um diretório no GitHub para futuros commits. Utilizei o VSCode para fazer o upload dos arquivos e criei um Jupyter Notebook para análise dos dados. Os dados foram carregados nas variáveis "df_Details" e "df_Ratings". Como os dados em CSV não estavam sendo lidos corretamente, converti para xlsx para uma manipulação mais fluida e precisa, sem erros.

## Análise dos Dados
Iniciei a análise importando a biblioteca pandas em Python. Criei os DataFrames e utilizei df.head() para visualização dos dados e início da limpeza. Removi todos os zeros na coluna 'number_of_ratings' para evitar interferências futuras nas análises. Realizei a concatenação das tabelas para trabalhar com dados conjuntos e exportei para o Excel para uma verificação mais detalhada.

Utilizei a função duplicated() e sum() para identificar e remover dados duplicados na coluna 'hotel_id'. Ao analisar no Excel, identifiquei IDs não duplicados que precisavam ser excluídos devido à presença das palavras 'excluir' ou 'teste' no nome. Realizei a exclusão e replicação no 'hotel_name'. Percebi também cidades não preenchidas, optando por preenchê-las manualmente link por link para uma resposta mais concreta à terceira pergunta.

## Questões Respondidas
1. **Ordene as cidades em ordem crescente de número de listings:**
   - Hidrolândia: 0; Praia do Rosa: 0; Trancoso: 0; ... Balneário Camboriú: 20; Florianópolis: 207.

2. **Ordene as cidades em ordem decrescente de metros quadrados:**
   - Florianópolis: 19447.64; Itapema: 2158.80; Porto Seguro: 2019.26; ... Águas Brancas: 30.00; Hidrolândia: 0.00; Praia do Rosa: 0.00.

3. **Quais cidades têm mais avaliações?**
   - Anitápolis: 78.0; Urubici: 1.0; ... Florianópolis: 3270.0.

4. **Quais cidades têm a maior média de avaliações? E a menor média?**
   - Cidade com a maior média: Brasília - Média: 10.0.
   - Cidade com a menor média: Urubici - Média: 4.0.
     - *Explicação:* A quantidade de anúncios em Florianópolis contribui para uma média mais baixa, contrastando com Brasília, que, apesar de ter poucos anúncios, ostenta notas altas. Dessa forma, Brasília conquistou a primeira posição devido às excelentes avaliações de seus poucos anúncios. Por outro lado, em Urubici, apesar do reduzido número de anúncios, a média de avaliações não é positiva.

5. **Existem correlações entre as características de um anúncio e a sua localização?**
   - Certamente, todas as características de um imóvel influenciam em sua avaliação, incluindo a localização. Mesmo que o imóvel apresente excelentes comodidades, limpeza, entre outros, com avaliações positivas, a distância em relação ao centro ou a alguns pontos turísticos pode impactar negativamente em sua taxa de ocupação, possivelmente aquém do desejado.

6. **Existem relações entre a nota do anúncio e os recursos disponíveis no imóvel?**
   - Ao explorar a matriz de correlação, destaquei algumas relações interessantes. Há uma forte correlação positiva entre 'Comodidades' e a avaliação total ('Total'). Isso sugere que os hóspedes valorizam propriedades com boas comodidades. Além disso, há correlação positiva entre 'Limpeza', 'Conforto' e 'Custo-benefício' com a avaliação total. Manter o local limpo, confortável e com uma boa relação custo-benefício pode influenciar positivamente nas avaliações totais dos hóspedes.

7. **Existe alguma relação entre a nota recebida e a localização?**
   - Ao

 examinar a interação entre a nota do anúncio e sua localização, alguns insights se destacam. A localização é crucial para notas mais altas, mas outras características, como comodidades, limpeza e conforto, também desempenham papéis importantes. Uma localização excepcional pode, até certo ponto, compensar deficiências em outras áreas, resultando em uma nota geral mais positiva.

8. **O que pode ser inferido sobre as notas dos imóveis?**
   - As notas refletem a importância da localização, mas também destacam a necessidade de uma abordagem equilibrada para atender às diversas expectativas dos hóspedes. Imóveis bem localizados tendem a receber notas mais altas, mas características específicas, como comodidades, limpeza, conforto e custo-benefício, também influenciam. Uma excelente localização pode, em certa medida, compensar avaliações menos favoráveis em outras categorias.

9. **Quais são os anúncios críticos?**
   - Anúncios com avaliações consistentemente baixas são considerados críticos, indicando problemas significativos que afetam a satisfação dos hóspedes.

10. **Outras Análises Criativas:**
   - Se eu tivesse dados completos, utilizaria a biblioteca nltk para identificar palavras mais frequentes nos anúncios, revelando o que os hóspedes geralmente buscam. Analisaria características mais comuns e bem avaliadas em diferentes cidades para identificar padrões locais. Também realizaria uma análise de feedback negativo para melhorar áreas nos apartamentos.

11. **Design de Dashboard:**
   - [Link para o Dashboard]

12. **Outras Informações Relacionadas:**
   - Consideraria incluir dados demográficos dos hóspedes, dados climáticos, avaliações em outras plataformas, preços médios e taxas de ocupação dos imóveis. Dados econômicos locais e histórico de manutenção dos imóveis também seriam relevantes.

13. **Como Melhorar as Notas:**
   - Investir em comodidades bem avaliadas, garantir serviços de limpeza eficientes, destacar pontos turísticos próximos, oferecer promoções especiais e resolver proativamente problemas são sugestões para melhorar as notas dos imóveis.

## Conclusão
A análise fornece insights valiosos sobre os anúncios no Booking, destacando a importância da localização e de características específicas para as avaliações dos hóspedes. A abordagem equilibrada, considerando diversos aspectos, é crucial para melhorar a satisfação do cliente e, consequentemente, as notas recebidas.
