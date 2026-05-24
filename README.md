# Análise Exploratória de Dados — Steam Games Dataset

Este projeto apresenta uma análise exploratória de dados (EDA) detalhada sobre o catálogo de jogos da plataforma Steam, investigando dinâmicas de mercado, precificação e o comportamento dos usuários.

## Descrição do Projeto

O script realiza uma investigação analítica completa dividida em etapas estruturadas, incluindo:

* **Ingestão automatizada de dados** diretamente da API do Kaggle.
* **Limpeza e Engenharia de Features** para segmentação temporal e financeira.
* **Tratamento de dados categóricos** complexos (múltiplos gêneros e plataformas).
* **Análise Estatística** focada em correlações entre preço, volume de DLCs e aceitação do público.
* **Visualização Gráfica Avançada** com distribuições, dispersões e cruzamentos de variáveis.
* **Geração de Insights de Negócio** voltados para o mercado de games.

## Objetivos

* Identificar os gêneros dominantes e os padrões de preço mediano no catálogo da Steam.
* Mapear a proporção real entre jogos *Free-to-Play* e títulos pagos.
* Avaliar o impacto direto de faixas de preço na percepção de qualidade do público.
* Analisar se estratégias de múltiplos DLCs (*Live-Service*) afetam positivamente ou negativamente a satisfação dos usuários.
* Traçar o perfil socioeconômico e mercadológico dos jogos considerados "Aclamados".

## Estrutura do Projeto

```text
steam-games-analysis/
│
├── steam_analysis_colab.py               # Script principal da análise (convertido do Colab)
├── Steam Analysis Deck _standalone_.html  # Deck de apresentação interativo
└── README.md                             # Documentação do projeto

```

## Tecnologias Utilizadas

* **Python 3.8+**
* **Pandas** — Manipulação, limpeza e estruturação dos dados.
* **NumPy** — Operações matemáticas e computação vetorizada.
* **Matplotlib** — Construção da base dos gráficos e customizações de layout.
* **Seaborn** — Visualizações estatísticas e plots complexos de dispersão e densidade.
* **Kagglehub** — Integração e download direto do dataset público.

---

## Como Executar o Projeto

### Execução via Google Colab

1. Faça o upload do arquivo `steam_analysis_colab.py` ou copie o código para um novo notebook no Google Colab.
2. Execute as células em ordem sequencial (`Shift + Enter`).
3. **Nota sobre Autenticação:** O pacote `kagglehub` baixará o arquivo `games.csv` automaticamente. Caso o Kaggle solicite suas credenciais, faça o upload do seu token pessoal (`kaggle.json`) gerado na sua conta da plataforma.

---

## Dados Utilizados & Engenharia de Features

O carregamento inicial extrai o arquivo `games.csv` bruto. Para viabilizar as respostas analíticas, foram construídas e tratadas as seguintes variáveis:

| Variável Criada | Tipo de Dado | Descrição / Objetivo |
| --- | --- | --- |
| `Year` | Inteiro | Extração do ano de lançamento a partir da data original. |
| `Owners_est` | Numérico (Float) | Conversão da string de estimativa de donos para um valor numérico calculável. |
| `Total_reviews` | Inteiro | Somatório de avaliações positivas e negativas (`positive` + `negative`). |
| `Approval_rate` | Percentual (Float) | Razão de análises positivas sobre o total: (Positivas / Total) * 100. |
| `Is_free` | Booleano | Identificação binária de jogos gratuitos (*True*/*False*). |
| `Price_band` | Categórico | Agrupamento dos preços dos jogos em faixas de valor específicas. |

---

## Perguntas Analíticas Respondidas

O escopo do projeto foi delimitado para solucionar 6 problemas de negócio:

1. **Precificação por Gênero:** Qual o preço mediano praticado por nicho de mercado (considerando apenas títulos pagos)?
2. **Dinâmica Free-to-Play:** Qual a real proporção de jogos gratuitos no catálogo e como se distribuem os preços dos jogos pagos?
3. **Saturação do Catálogo:** Quais gêneros dominam massivamente a quantidade de lançamentos na plataforma?
4. **Valor vs. Percepção:** Existe correlação matemática ou dispersão óbvia entre o preço cobrado e a taxa de aprovação dos usuários?
5. **Impacto dos DLCs:** A estratégia de fragmentar o jogo em múltiplos conteúdos adicionais satura ou melhora a satisfação da comunidade?
6. **O Perfil da Alta Qualidade:** Jogos aclamados pela crítica popular sustentam preços medianos de venda superiores aos demais?

## Resultados e Insights de Negócio

* **Predomínio de Gratuitos:** A base histórica possui volumosa presença de jogos *Free-to-Play*, servindo como estratégia principal de aquisição de usuários.
* **Ancoragem de Preço:** O mercado de jogos pagos consolida faixas de preço em torno de valores medianos próximos a **US$ 50**, mostrando barreiras psicológicas tradicionais de precificação.
* **Sensibilidade ao Preço:** Jogos posicionados em faixas de preço mais baixas apresentam taxas de aprovação sutilmente superiores, indicando menor tolerância a falhas em jogos caros.
* **O Limite dos DLCs:** Títulos com um volume moderado de DLCs mantêm bons índices de aprovação. No entanto, o modelo agressivo de *Live-Service* (centenas de conteúdos adicionais) gera desgaste, não convertendo necessariamente em satisfação do público.
* **Prêmio por Qualidade:** Há validação de valor em jogos bem avaliados; títulos classificados como "Aclamados" (com mais de 100 reviews) conseguem sustentar preços medianos significativamente superiores.

---

## Conceitos de Ciência de Dados Abordados

* Análise Exploratória de Dados (EDA)
* Engenharia de Variáveis (*Feature Engineering*)
* Estatística Descritiva (Média, Mediana, Quartis e Distribuições)
* Visualização de Dados com foco em Storytelling
* Segmentação de Mercado e Análise de Cohorts por Faixas de Preço

---

## Currículo e Critérios Acadêmicos Atendidos

Este projeto compõe a avaliação prática da disciplina de Ciência de Dados, validando competências essenciais do ciclo de vida dos dados: desde a coleta automatizada, passando pelo tratamento de dados inconsistentes, até a comunicação visual e analítica dos resultados gerados.

---

## Autor

**Pedro Lima Zampier de Andrade**

* **Instituição:** UniCEUB
* **Curso:** Bacharelado em Ciência de Dados e Machine Learning
* **GitHub:** [@OPedroZampier](https://github.com/OPedroZampier/)

*Última atualização: Maio de 2026*

*Status do Projeto: Concluído / Funcional*
