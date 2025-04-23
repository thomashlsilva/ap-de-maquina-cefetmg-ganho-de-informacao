
# Atividade: Cálculo de Ganho de Informação

## Descrição

Este projeto implementa algoritmos fundamentais para a construção de árvores de decisão em Machine Learning, com foco em:

- Cálculo da entropia de um conjunto de dados.
- Cálculo do ganho de informação para atributos categóricos, numéricos e booleanos (com discretização).
- Testes automatizados para validação das implementações.

---

## Conceitos Implementados

### 1. `entropia()`
Calcula a entropia da variável de classe com base nas proporções dos valores, utilizando logaritmo binário.

### 2. `ganho_informacao_condicional()`
Calcula o ganho de informação condicional para um valor específico de um atributo.

### 3. `ganho_informacao()`
Retorna o ganho de informação total de um atributo, considerando todos os seus valores (ponderado).  
Suporta atributos:
- Categóricos
- Numéricos
- Booleanos (com discretização)

---

## Testes

O arquivo `tests.py` (fornecido pelo professor) valida:

- A entropia para cada coluna.
- O ganho de informação condicional por valor.
- O ganho de informação total por atributo.

Resultado: Todos os testes passam com precisão de até 3 casas decimais.

---

## Exemplo de Uso

```python
import pandas as pd
from ganho_informacao import ganho_informacao

# DataFrame de exemplo
df = pd.DataFrame({
    "Temperatura": ["Quente", "Quente", "Fria", "Fria"],
    "JogarTenis": ["Não", "Não", "Sim", "Sim"]
})

# Cálculo do ganho de informação
print(ganho_informacao(df, "JogarTenis", "Temperatura"))
```

---

## Instruções de Execução

### Instalação de Dependências

Certifique-se de ter o Python e os pacotes necessários instalados:

```bash
apt-get install python3 jupyter python3-pip
pip install -r requirements.txt
```

Atenção: Evite usar `sudo` com o pip.

---

### Executando o Jupyter Notebook

```bash
jupyter notebook
```

Abra o notebook fornecido chamado "Análise de Atributos usando InfoGain" e siga as instruções no arquivo.

---

## Créditos

Atividade desenvolvida para a disciplina de Machine Learning do CEFET-MG, Campus Nova Gameleira.

Material baseado nas aulas do professor Daniel Hasan Dalip.
