# Lista 02 - Sistemas Digitais 

Este repositório contém as resoluções da **Lista de Exercícios 02** da disciplina de Sistemas Digitais.

## Informações da Disciplina

* **Universidade:** Universidade Federal do Ceará (UFC) - Campus Quixadá 
* **Disciplina:** Sistemas Digitais p/ Computadores 

## Tópicos Abordados

Esta lista de exercícios foca no design de hardware em um nível mais prático e abstrato, cobrindo os seguintes tópicos:

* **Arquitetura de FPGAs:** Implementação de circuitos em uma arquitetura customizada, configurando CLBs (Configurable Logic Blocks), LUTs (Look-Up Tables) e matrizes de chaveamento (Switch Matrix)[cite: 2, 130].
* [cite_start]**Análise de Tempo (Timing):** Projeto de circuitos lógicos que atendem a restrições específicas de desempenho, como frequência máxima de clock e atrasos de propagação[cite: 48, 53, 54, 55].
* [cite_start]**Projeto de Datapath e Bloco de Controle:** Conversão de Máquinas de Estados Finitos (FSMs) de alto nível em circuitos de bloco de controle e datapaths correspondentes[cite: 56, 97].
* [cite_start]**Codificação de Estados:** Implementação de FSMs usando diferentes esquemas de codificação, como binário e "one-hot"[cite: 57, 98].
* [cite_start]**Análise de Caminho Crítico:** Cálculo dos caminhos de maior e menor atraso em circuitos síncronos[cite: 140].

## Questões Resolvidas

Abaixo estão as soluções detalhadas para cada questão da lista.

*(Você pode criar arquivos `.md` separados para cada solução e linká-los aqui)*

### Questão 1: Implementação em FPGA

* [cite_start]**Descrição:** Projetar um circuito customizado que atenda a um conjunto de restrições (5 entradas, 2 saídas, min. 2 FFs, etc.) e mapeá-lo para a arquitetura FPGA 2-CLB fornecida[cite: 2, 3, 4, 5, 6, 7].
* **Solução:** `[Link para a Solução Q1.md]`

### Questão 2: Projeto com Restrições de Tempo

* [cite_start]**Descrição:** Elaborar três circuitos diferentes (a, b, c) que operem dentro de restrições de tempo específicas, com base em uma tabela de atraso de portas (AND, OR, XOR, etc.)[cite: 48, 49, 50, 52].
* **Soluções:**
    * [cite_start]**2a) Frequência Máxima = 200 MHz**[cite: 53]: `[Link para a Solução Q2a.md]`
    * [cite_start]**2b) Atraso de Caminho entre 6ns e 10ns**[cite: 54]: `[Link para a Solução Q2b.md]`
    * [cite_start]**2c) Frequência >= 275 MHz (c/ XOR e NAND)**[cite: 55]: `[Link para a Solução Q2c.md]`

### Questão 3: Datapath e Controle (One-Hot)

* [cite_start]**Descrição:** Apresentar a tabela-verdade e a FSM do bloco de controle para um datapath, usando a codificação "one-hot" (Qe=01, R=10)[cite: 56, 57].
* **Solução:** `[Link para a Solução Q3.md]`

### Questão 4: Datapath e Controle (Binário)

* [cite_start]**Descrição:** Apresentar a tabela-verdade e o circuito do bloco de controle para um segundo datapath, usando a codificação binária padrão[cite: 97, 98, 99].
* **Solução:** `[Link para a Solução Q4.md]`

### Questão 5: Mapeamento de Bloco de Controle para FPGA

* [cite_start]**Descrição:** Mostrar como um bloco de controle (State Register + lógica) seria implementado em uma arquitetura de FPGA que usa LUTs 3x1 e matrizes de interconexão[cite: 130, 131].
* **Solução:** `[Link para a Solução Q5.md]`

### Questão 6: Análise de Caminho Crítico (Geral)

* [cite_start]**Descrição:** Calcular o tempo e a frequência dos caminhos de maior (crítico) e menor atraso para os circuitos projetados nas questões anteriores, usando novos parâmetros de atraso (portas lógicas=1ns, datapath=3ns)[cite: 140, 141, 142].
* **Solução:** `[Link para a Solução Q6.md]`
