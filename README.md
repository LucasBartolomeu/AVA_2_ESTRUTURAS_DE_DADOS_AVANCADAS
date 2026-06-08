# 🔍 Busca Binária em C — Vetor Dinâmico Ordenado

> Atividade prática para aprendizado do algoritmo de **Busca Binária**, implementada em linguagem C com um vetor dinâmico sempre ordenado e menu interativo.

---

## 📚 Sobre o Projeto

Este programa foi desenvolvido como **atividade prática** da disciplina de Estruturas de Dados Avançadas, com o objetivo de demonstrar na prática o funcionamento do algoritmo de **Busca Binária** — um dos algoritmos de pesquisa mais eficientes da ciência da computação.

A proposta é simples: o usuário gerencia um vetor de inteiros através de um menu, e todas as operações de busca e remoção utilizam o algoritmo de busca binária, explorando sua eficiência em comparação à busca linear.

---

## 🧠 Conceito: O que é Busca Binária?

A **Busca Binária** é um algoritmo de pesquisa que funciona sobre **vetores ordenados**. A cada iteração, ele divide o espaço de busca ao meio, comparando o valor central com o alvo:

```
Vetor: [ 3, 7, 12, 18, 25, 31, 44 ]
Busca pelo valor: 25

Passo 1 → meio = 18  →  25 > 18  →  busca na metade direita
Passo 2 → meio = 31  →  25 < 31  →  busca na metade esquerda
Passo 3 → meio = 25  →  ENCONTRADO na posição 4 ✓
```

| Algoritmo       | Complexidade de Busca |
|-----------------|-----------------------|
| Busca Linear    | O(n)                  |
| **Busca Binária** | **O(log n)**        |

> ⚠️ **Requisito fundamental:** o vetor **deve estar ordenado** para que a busca binária funcione corretamente. Por isso, este programa reordena o vetor automaticamente a cada inserção.

---

## ⚙️ Funcionalidades

| Opção | Função              | Descrição                                                  |
|-------|---------------------|------------------------------------------------------------|
| `1`   | Inserir elemento    | Adiciona um inteiro ao vetor e reordena automaticamente    |
| `2`   | Remover elemento    | Localiza via busca binária e remove o elemento             |
| `3`   | Buscar elemento     | Pesquisa um valor usando busca binária e retorna a posição |
| `4`   | Apresentar elementos| Exibe todos os elementos do vetor na tela                  |
| `0`   | Encerrar programa   | Finaliza a execução                                        |

---

## 🗂️ Estrutura do Código

```
busca-binaria/
│
├── busca_binaria.c     # Código-fonte principal
└── README.md           # Documentação do projeto
```

### Funções implementadas

```c
void ordenar()            // Ordena o vetor com Selection Sort
void inserir()            // Insere um elemento e mantém a ordem
void apresentar()         // Exibe os elementos do vetor
int  buscaBinaria(valor)  // Retorna o índice do valor ou -1
void buscar()             // Interface de busca para o usuário
void remover()            // Remove um elemento pelo valor
```

---

## 🚀 Como Compilar e Executar

### Pré-requisitos

- Compilador GCC instalado  
- Terminal (Linux/macOS) ou MinGW/WSL (Windows)

### Compilação

```bash
gcc busca_binaria.c -o busca_binaria
```

### Execução

```bash
./busca_binaria
```

### Exemplo de uso

```
============================
MENU - BUSCA BINARIA
============================
1 - Inserir elemento
2 - Remover elemento
3 - Buscar elemento
4 - Apresentar elementos
0 - Encerrar programa
Escolha uma opção: 1

Digite o valor para inserir: 42
Valor inserido com sucesso!
```

---

## 📌 Detalhes de Implementação

- **Tamanho máximo do vetor:** 100 elementos (`#define MAX 100`)
- **Ordenação:** Selection Sort aplicado após cada inserção, garantindo que o vetor esteja sempre pronto para a busca binária
- **Remoção:** após localizar o elemento via busca binária, os elementos seguintes são deslocados para preencher o espaço

---

## 🎯 Objetivo de Aprendizado

Ao estudar e executar este programa, espera-se que o estudante seja capaz de:

- [x] Compreender a lógica de divisão e conquista da busca binária
- [x] Entender por que o vetor precisa estar ordenado
- [x] Comparar a eficiência entre busca linear e binária
- [x] Visualizar a integração entre ordenação e pesquisa em vetores
