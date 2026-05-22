🎮 Análise Exploratória — Steam Games Dataset
Autor: Pedro Lima Zampier de Andrade  
Atividade: Trabalho realizado para a aula de Ciência de Dados  
Arquivo principal: `steam_analysis_colab.ipynb
---
📌 Sobre o projeto
Este projeto apresenta uma análise exploratória de dados (EDA) sobre jogos da plataforma Steam, utilizando o dataset público Steam Games Dataset. O objetivo da atividade é investigar padrões relacionados a preço, popularidade, avaliações dos usuários, gêneros, DLCs e qualidade percebida dos jogos.
A análise foi desenvolvida originalmente no Google Colab e organizada em perguntas analíticas, gráficos e insights de negócio.
---
📂 Dataset utilizado
O dataset contém informações detalhadas sobre jogos da Steam, incluindo:
Nome do jogo
Data de lançamento
Preço em dólar
Estimativa de donos/jogadores
Avaliações positivas e negativas
Taxa de aprovação
Quantidade de DLCs
Gêneros e categorias
Desenvolvedores e publicadoras
Idiomas suportados
Plataformas compatíveis
Tempo médio e mediano de jogo
Recomendações e conquistas
O carregamento do dataset é feito diretamente via `kagglehub`, a partir do arquivo `games.csv`.
---
🧰 Tecnologias e bibliotecas
O projeto utiliza as seguintes bibliotecas Python:
```python
pandas
numpy
matplotlib
seaborn
kagglehub
```
Essas bibliotecas são usadas para carregamento dos dados, limpeza, criação de novas variáveis, análise estatística e geração dos gráficos.
---
🧹 Etapas da análise
1. Setup
Instalação e importação das bibliotecas necessárias para executar a análise.
2. Carregamento do dataset
O dataset é carregado por meio da biblioteca `kagglehub`, utilizando o arquivo `games.csv`.
3. Limpeza e feature engineering
Nesta etapa são criadas novas variáveis para facilitar a análise, como:
`Year`: ano de lançamento do jogo
`Owners_est`: estimativa numérica de donos do jogo
`Total_reviews`: total de avaliações recebidas
`Approval_rate`: percentual de avaliações positivas
`Is_free`: identifica se o jogo é gratuito
`Price_band`: faixa de preço do jogo
---
❓ Perguntas analisadas
O projeto foi estruturado em 6 perguntas principais:
1. Qual o preço mediano por gênero na Steam?
Analisa quais gêneros possuem maior e menor preço mediano considerando apenas jogos pagos.
2. Qual a distribuição de preços e proporção entre jogos pagos e gratuitos?
Compara jogos free-to-play e pagos, além de mostrar média e mediana dos preços dos jogos pagos.
3. Quais são os gêneros dominantes na Steam?
Identifica os gêneros mais frequentes no catálogo analisado.
4. Existe relação entre preço e avaliação dos usuários?
Analisa a aprovação dos jogos por faixa de preço e observa a dispersão entre preço e percentual de reviews positivas.
5. Qual o efeito do volume de DLCs na satisfação do público?
Compara a taxa mediana de aprovação entre jogos sem DLCs, com poucas DLCs, volume moderado e modelo live-service.
6. Qual o perfil dos jogos com alta aprovação?
Classifica jogos com pelo menos 100 avaliações em níveis de qualidade e compara a distribuição com o preço mediano.
---
📊 Principais insights
A base analisada possui grande presença de jogos gratuitos, com os jogos pagos representando uma parcela menor do catálogo.
Jogos pagos apresentam concentração de preços em torno de valores medianos próximos a US$ 50.
Jogos com preços mais baixos tendem a apresentar aprovação ligeiramente maior.
Jogos com poucos DLCs apresentam melhor mediana de aprovação, enquanto volumes muito altos de DLCs não aumentam necessariamente a satisfação.
A maioria dos jogos com 100 ou mais avaliações está nas categorias positivas ou aclamadas.
Jogos mais bem avaliados conseguem sustentar preços medianos mais altos.
---
▶️ Como executar
Opção 1 — Google Colab
Abra o arquivo `steam_analysis_colab.py` ou o notebook correspondente no Google Colab.
Execute as células em ordem.
Caso o Kaggle solicite autenticação, gere um token em sua conta Kaggle e faça upload do arquivo `kaggle.json`.
Opção 2 — Ambiente local
Instale as dependências:
```bash
pip install pandas numpy matplotlib seaborn kagglehub
```
Execute o arquivo Python:
```bash
python steam_analysis_colab.py
```
> Observação: o arquivo foi gerado a partir de um notebook do Google Colab, portanto algumas células e comandos podem precisar de adaptação para execução local.
---
📁 Estrutura esperada
```text
.
├── steam_analysis_colab.py
└── README.md
└──Steam Analysis Deck _standalone_.html
```
---
🎯 Objetivo acadêmico
Este trabalho foi desenvolvido como atividade da disciplina de Ciência de Dados, com foco em aplicar conceitos de análise exploratória, tratamento de dados, visualização de informações e interpretação de resultados.
---
👤 Autor
Pedro Lima Zampier de Andrade
