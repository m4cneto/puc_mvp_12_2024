# MVP de Ciência de Dados

## Descrição do Projeto

Este projeto tem como objetivo principal prever o preço de casas com base em suas características utilizando técnicas de machine learning. O projeto foi desenvolvido como um MVP (Mínimo Produto Viável) para demonstrar a aplicação de modelos de regressão em problemas do mundo real.

## Etapas do Projeto

1. **Importação das Bibliotecas:**
   - Foram utilizadas bibliotecas como `pandas`, `numpy`, `matplotlib`, `seaborn` e ferramentas da biblioteca `scikit-learn` para manipulação de dados, visualização e modelagem.

2. **Definição do Problema:**
   - O problema consiste em prever o preço de casas com base em variáveis explicativas como número de quartos, tamanho do lote, entre outras.

3. **Carregamento dos Dados:**
   - O dataset utilizado foi obtido a partir de um repositório público no GitHub. [Dataset](https://raw.githubusercontent.com/m4cneto/puc_mvp_12_2024/refs/heads/main/boston.csv).

4. **Análise Exploratória dos Dados:**
   - Análise inicial para compreender a estrutura dos dados e verificar valores ausentes ou inconsistências.
   - Estatísticas descritivas foram geradas para entender as distribuições e possíveis outliers.

5. **Preparação dos Dados:**
   - Remoção de valores ausentes e normalização das variáveis para padronizar a escala.
   - Separação das variáveis entre conjuntos de treino e teste.

6. **Seleção de Features:**
   - Foram selecionadas as 10 melhores features usando o método `SelectKBest` com base na correlação estatística.

7. **Modelagem:**
   - Dois modelos foram treinados: Regressão Linear (baseline) e Random Forest.
   - Ambos os modelos foram avaliados para medir sua performance inicial.

8. **Otimização de Hiperparâmetros:**
   - Foi realizada uma busca em grade para ajustar os hiperparâmetros do Random Forest, visando melhorar seu desempenho.

9. **Avaliação dos Modelos:**
   - Métricas utilizadas: MSE (Mean Squared Error) e R² (coeficiente de determinação).
   - Comparou-se o desempenho dos modelos antes e depois da otimização.

10. **Conclusão:**
    - Foi apresentado o desempenho final dos modelos e discutidos os resultados obtidos.

## Requisitos para Execução

- Python 3.7 ou superior.
- Bibliotecas necessárias:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`

Para instalar as dependências, execute:
```bash
pip install -r requirements.txt
```

## Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu_usuario/mvp_ciencia_dados.git
   ```

2. Navegue até o diretório do projeto:
   ```bash
   cd mvp_ciencia_dados
   ```

3. Abra o notebook no Jupyter ou Google Colab e execute as células sequencialmente.

## Estrutura do Projeto

- `notebook/`: Contém o notebook principal do projeto.
- `data/`: Diretório para armazenar o dataset utilizado.
- `README.md`: Documento descritivo do projeto.
- `requirements.txt`: Lista de dependências necessárias.

## Resultados

- A Regressão Linear apresentou MSE e R² moderados, sendo utilizada como baseline.
- O Random Forest superou a Regressão Linear e mostrou melhores resultados após a otimização.
- Detalhes completos estão documentados no notebook.

## Licença

Este projeto é licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

