# TCC — Apoio à decisão na produtividade leiteira

Projeto de Trabalho de Conclusão de Curso em Ciência da Computação que utiliza dados reais de duas propriedades leiteiras para desenvolver um modelo de Inteligência Artificial voltado ao apoio à tomada de decisão na produtividade leiteira.

O trabalho utiliza Python, Jupyter Notebook e Pandas para organização e análise dos dados, e scikit-learn para Machine Learning. O experimento de modelagem foi concluído e está documentado em `notebooks/02_harmonizacao_e_machine_learning.ipynb`.

## Status do projeto

- Preparação das bases das duas propriedades: concluída.
- Harmonização das bases e das variáveis: concluída.
- Treinamento, comparação dos modelos e ajuste de hiperparâmetros: concluídos.
- Modelo final experimental: Gradient Boosting no cenário C2 (`C2_lactacao`), selecionado com base na validação cruzada agrupada por animal sobre o conjunto de treinamento.
- Avaliação final no conjunto de teste reservado: concluída.
- Próxima etapa: preparação do modelo de implantação, integração com PostgreSQL e desenvolvimento da aplicação.

O modelo final experimental apresentou MAE de 3,685 kg, RMSE de 5,075 kg e R² de 0,749 no conjunto de teste, composto por 189 controles de 37 animais. Esses resultados estão registrados no notebook. O modelo avaliado foi preservado separadamente da futura versão de implantação.

## Organização do projeto

```text
TCC/
├── dados/
│   ├── originais/
│   │   ├── cerqueira_cesar/
│   │   └── uenp/
│   └── processados/
├── notebooks/
├── modelos/
├── src/
├── resultados/
│   ├── tabelas/
│   ├── graficos/
│   └── modelos/
├── requirements.txt
├── .gitignore
└── README.md
```

- `dados/`: reúne os dados utilizados no projeto.
- `dados/originais/`: armazena os arquivos reais recebidos, preservando-os sem alterações.
- `dados/originais/cerqueira_cesar/`: dados originais da propriedade de Cerqueira César.
- `dados/originais/uenp/`: dados originais da propriedade da UENP.
- `dados/processados/`: armazena as versões tratadas dos dados utilizadas no experimento.
- `notebooks/`: reúne os notebooks de preparação, harmonização e modelagem.
- `modelos/`: armazena o modelo final experimental avaliado e seus metadados, conforme o salvamento registrado no notebook.
- `src/`: destinada aos módulos e scripts Python reutilizáveis.
- `resultados/`: reúne as saídas produzidas pelas análises e pela modelagem, incluindo as previsões do teste e a importância das variáveis exportadas pelo notebook.
- `resultados/tabelas/`: destinada às tabelas de resultados.
- `resultados/graficos/`: destinada aos gráficos gerados.
- `resultados/modelos/`: pasta prevista na estrutura inicial; o modelo final experimental foi salvo em `modelos/`.
- `requirements.txt`: lista as dependências do projeto.
- `.gitignore`: impede o versionamento do ambiente virtual, caches Python, arquivos temporários do Jupyter e arquivos de sistema.
