<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rounded&color=0:fbcfe8,100:f9a8d4&height=170&section=header&text=Elei%C3%A7%C3%B5es%202022&fontSize=48&fontColor=831843&fontAlignY=42&desc=Checkpoint%20de%20Data%20Science%20%C2%B7%20FIAP&descSize=16&descAlignY=68" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Quicksand&weight=600&size=19&pause=1400&color=DB2777&center=true&vCenter=true&width=620&lines=Estat%C3%ADstica+descritiva+com+Python;Presidente+e+Governador%2C+1%C2%BA+e+2%C2%BA+turno;Como+o+Brasil+votou+em+2022" />

<br>

<a href="./eda_eleicoes_2022.ipynb">Ver o notebook</a>

</div>

<br>

### Sobre o projeto

Análise exploratória dos dados oficiais do TSE sobre as **Eleições 2022**, feita como checkpoint de Data Science do curso de Engenharia de Software da FIAP. O recorte são os cargos de **Presidente e Governador**, os únicos que tiveram 2º turno, o que permite comparar os dois turnos.

A pergunta que guia o trabalho: **como o Brasil votou, quem foi às urnas, como o voto se dividiu e em quem?**

<br>

### Os dados

Base *Brazil Elections 2022* (Kaggle), com dados oficiais do TSE. Usamos os 4 arquivos e juntamos os dois tipos numa tabela só:

| | 1º turno | 2º turno |
|:---|:---|:---|
| **Por zona** (quem votou: aptos, comparecimento, brancos e nulos) | `detalhe_votacao.csv` | `detalhe_votacao_2_turno.csv` |
| **Por candidato** (em quem votou) | `votacao_candidato.csv` | `votacao_candidato_2_turno.csv` |

São **21.658 registros de zonas** e **140.620 registros de candidatos**, em 5.613 municípios, nos 27 estados e no exterior.

<br>

### O que o notebook faz

| Etapa | Conteúdo |
|:---|:---|
| Preparação | Limpeza, testes de consistência (votos dos candidatos batem com os votos válidos) e criação de taxas de comparecimento, abstenção, brancos e nulos |
| Tendência central | Média, mediana e moda |
| Dispersão | Variância, desvio-padrão, coeficiente de variação e quartis |
| Distribuição | Histogramas, assimetria e curtose, com e sem o exterior |
| Correlação | Pearson, gráficos de dispersão e comparação entre os turnos |
| Segmentação | Região, estado, turno, cargo e situação do candidato |
| Outliers | IQR e Z-Score, com estudo de caso |
| Storytelling | Síntese dos achados, limitações e próximos passos |

<br>

### Principais achados

- **O comparecimento é parecido em todo o país:** média de 78,3%, com metade das zonas entre 75,9% e 82,3%.
- **O voto nulo é o que mais varia** e depende do cargo: 6,98% para Governador contra 2,67% para Presidente no 1º turno.
- **O exterior distorce a distribuição:** comparecimento de 35,9%. Sem ele, o histograma vira quase uma curva normal.
- **A eleição presidencial foi dividida por região:** a mediana de votos do candidato eleito no 2º turno foi de 77,3% no Nordeste e 39,9% no Sul.
- **Quase ninguém mudou de lado entre os turnos:** correlação de 0,995 entre o 1º e o 2º turno, zona a zona.
- **Paradoxo de Simpson:** a correlação entre votos do eleito e voto nulo é positiva no Brasil todo, mas inverte dentro do Nordeste e do Sudeste.
- **Sergipe teve 36,6% de votos nulos para Governador:** o candidato mais votado teve o registro negado e seus votos foram anulados.

<br>

<div align="center">
  <img src="docs/share-vencedor-por-regiao.png" width="48%" />
  &nbsp;
  <img src="docs/comparecimento-por-estado.png" width="48%" />
</div>

<br>

### Tecnologias

<div align="center">
  <img src="https://skillicons.dev/icons?i=python&theme=light" />
  <br>
  <sub>Python · pandas · NumPy · Matplotlib · Google Colab</sub>
</div>

<br>

### Como executar

1. Baixe os 4 arquivos CSV da base *Brazil Elections 2022* no Kaggle.
2. Abra o `eda_eleicoes_2022.ipynb` no Google Colab e envie os arquivos para a pasta `/content`, no mesmo caminho usado na primeira célula de código.
3. Execute as células em ordem.

<br>

### Equipe

<div align="center">

Camile Silva &nbsp;·&nbsp; Gustavo Ferreira &nbsp;·&nbsp; Lucas Caetano &nbsp;·&nbsp; Marco Conte &nbsp;·&nbsp; Sofia Rodrigues

</div>

<img src="https://capsule-render.vercel.app/api?type=rounded&color=0:fbcfe8,100:f9a8d4&height=60&section=footer" width="100%" />
