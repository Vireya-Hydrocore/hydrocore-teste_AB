# 🧪 Teste A/B – Avaliação de Novo Fluxo de Interface

## 📋 Descrição do Projeto
Este notebook tem como objetivo **analisar estatisticamente o impacto de uma nova interface móvel** sobre o tempo médio de execução de uma tarefa.  
Foram comparados dois fluxos distintos:

- **Teste A:** versão atual (fluxo original)  
- **Teste B:** versão nova (com alterações de UX/UI)

A hipótese testada é se o novo fluxo (**B**) melhora a performance e reduz o tempo médio de execução da tarefa, mantendo a experiência do usuário.

---

## 🎯 Objetivo
Avaliar se há **diferença estatisticamente significativa** no tempo de conclusão da tarefa entre os dois fluxos utilizando **testes t de Student**.

---

## 🧠 Contexto e Coleta de Dados
Os dados foram coletados por meio da plataforma **Maze**, com 30 usuários testando cada fluxo (A e B).  
Cada participante executou a mesma tarefa sob condições controladas, e o **tempo (em segundos)** foi registrado automaticamente.

- Amostra A → fluxo atual  
- Amostra B → novo fluxo  
- Métrica → tempo de execução (segundos)

---

## 🧩 Estrutura do Notebook

O notebook está organizado nas seguintes seções:

1. **Importação de bibliotecas**
   ```python
   import math
   import numpy as np
   from scipy import stats

**Definição das amostras**
teste_a = [4.51, 3.31, 4.69, 5.3, ...]
teste_b = [6.14, 27.65, 11.19, 14.21, ...]

---

**Cálculo de médias e tamanhos das amostras**
Teste estatístico t de Student (amostras independentes)
t_stat, p_valor_bilateral = stats.ttest_ind(a, b, equal_var=False)
p_valor_unilateral = p_valor_bilateral / 2 if t_stat > 0 else 1 - (p_valor_bilateral / 2)

---

**Interpretação do resultado e conclusão sobre a hipótese nula**

## ⚙️ Requisitos
Para rodar o notebook, instale as dependências abaixo:
pip install numpy scipy jupyter

---

## ▶️ Como Executar
Abra o arquivo Teste_AB.ipynb no Jupyter Notebook ou VSCode com a extensão Jupyter.


Execute as células em sequência.


Os resultados dos testes (estatísticas t, p-valores e médias) serão exibidos nas saídas.

---

## 📈 Interpretação dos Resultados
O teste t avalia a significância estatística da diferença entre os fluxos A e B.

p < 0.05: diferença significativa → um fluxo é mais rápido que o outro.

p ≥ 0.05: diferença não significativa → o desempenho é estatisticamente igual.

---

## 🧾 Conclusão
O notebook fornece uma análise clara e quantitativa do desempenho entre os fluxos de interface, permitindo embasar decisões de design e UX com evidências estatísticas.

📚 Tecnologias Utilizadas


Python 3.x

NumPy

SciPy

Jupyter Notebook


## 🧠 Tecnologias Utilizadas

- **Python 3.x**
- **NumPy**
- **SciPy**
- **Jupyter Notebook**

---

## ✍️ Autor

**Guilherme Costa**  
Estudante do Instituto Germinare Tech  
💼 Interesse em dados, IA e aplicações sustentáveis  
📅 2025

