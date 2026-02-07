# Lista 02 – Sistemas Digitais

Este repositório contém as resoluções da **Lista de Exercícios 02** da disciplina de **Sistemas Digitais**, com foco em projeto e análise de circuitos digitais em nível RTL (*Register Transfer Level*).

As soluções exploram tanto aspectos **teóricos** quanto **práticos** do projeto de hardware, incluindo análise temporal, projeto de FSMs, datapath e mapeamento em arquiteturas do tipo FPGA.

---

##  Informações da Disciplina

- **Universidade:** Universidade Federal do Ceará (UFC) — Campus Quixadá  
- **Disciplina:** Sistemas Digitais  

---

##  Tópicos Abordados

Esta lista de exercícios foca no design de hardware em um nível mais prático e abstrato, cobrindo os seguintes tópicos:

- **Arquitetura de FPGAs**  
  Implementação de circuitos em uma arquitetura customizada, configurando **CLBs (Configurable Logic Blocks)**, **LUTs (Look-Up Tables)** e **matrizes de chaveamento (Switch Matrix)**.

- **Análise de Tempo (Timing)**  
  Projeto de circuitos lógicos que atendem a restrições específicas de desempenho, como **frequência máxima de clock** e **atrasos de propagação**.

- **Projeto de Datapath e Bloco de Controle**  
  Conversão de **Máquinas de Estados Finitos (FSMs)** de alto nível em circuitos de **bloco de controle** e **datapaths** correspondentes.

- **Codificação de Estados**  
  Implementação de FSMs utilizando diferentes esquemas de codificação, como **binário** e **one-hot**.

- **Análise de Caminho Crítico**  
  Cálculo dos caminhos de **maior (crítico)** e **menor atraso** em circuitos síncronos.

---

##  Questões Resolvidas

Abaixo estão listadas as soluções desenvolvidas para cada questão da lista.

>  *Cada solução pode estar documentada em um arquivo `.md` separado, contendo explicações, tabelas, diagramas e análises.*

---

### Questão 1 — Implementação em FPGA

- **Descrição:**  
  Projeto de um circuito customizado que atende a um conjunto de restrições (5 entradas, 2 saídas, mínimo de 2 FFs, etc.) e seu mapeamento para a arquitetura FPGA 2-CLB fornecida.

- **Solução:**
  
  [Link para a Solução Q1.md](Lista02/Q-01/Q-01-resolucao.md)


---

### Questão 2 — Projeto com Restrições de Tempo

- **Descrição:**  
  Elaboração de três circuitos distintos (a, b e c) que operam dentro de restrições específicas de tempo, com base em uma tabela de atrasos de portas lógicas (AND, OR, XOR, etc.).

- **Soluções:**
  - **2a)** Frequência máxima = 200 MHz — [Link para a Solução Q2a.md](Lista02/Q-02/Q-02-alternativa-a-resolucao.md)
  - **2b)** Atraso de caminho entre 6 ns e 10 ns — [Link para a Solução Q2b.md](Lista02/Q-02/Q-02-alternativa-b-resolucao.md)  
  - **2c)** Frequência ≥ 275 MHz (usando XOR e NAND) — [Link para a Solução Q2c.md](Lista02/Q-02/Q-02-alternativa-c-resolucao.md)

---

### Questão 3 — Datapath e Controle (Codificação One-Hot)

- **Descrição:**  
  Construção da tabela-verdade e da FSM do bloco de controle para um datapath, utilizando codificação **one-hot** (Qe = 01, R = 10).

- **Solução:**  
  `[Link para a Solução Q3.md]`

---

### Questão 4 — Datapath e Controle (Codificação Binária)

- **Descrição:**  
  Apresentação da tabela-verdade e do circuito do bloco de controle para um segundo datapath, utilizando **codificação binária padrão**.

- **Solução:**  
  `[Link para a Solução Q4.md]`

---

### Questão 5 — Mapeamento de Bloco de Controle para FPGA

- **Descrição:**  
  Demonstração de como um bloco de controle (registrador de estado + lógica combinacional) pode ser implementado em uma arquitetura FPGA baseada em **LUTs 3×1** e matrizes de interconexão.

- **Solução:**  
  `[Link para a Solução Q5.md]`

---

### Questão 6 — Análise de Caminho Crítico (Geral)

- **Descrição:**  
  Cálculo do tempo e da frequência dos caminhos de **maior (crítico)** e **menor atraso** para os circuitos das questões anteriores, considerando novos parâmetros de atraso (portas lógicas = 1 ns, datapath = 3 ns).

- **Solução:**  
  `[Link para a Solução Q6.md]`
