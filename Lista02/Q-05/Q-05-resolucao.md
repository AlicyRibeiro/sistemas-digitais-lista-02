
## 5) Dado um FPGA onde os CLBs possuem LUTs 3x1 e matrizes de interconexão com 4 entradas e 4 saídas, mostre como ficaria a configuração do circuito do bloco de controle mostrado a seguir. Utilize quantos CLBs e matrizes quiser e faça as ligações entre os componentes da forma que  achar necessário.

![Circuito da Questão 2.30 - item a](figuras/questão5.jpeg)

---

## Implementação do Bloco de Controle em FPGA com LUTs 3x1 e Matrizes de Interconexão 4x4

Para implementar o bloco de controle proposto em um FPGA com LUTs 3x1 e matrizes de interconexão 4x4, a estratégia divide-se em **mapeamento lógico**, **programação de memória** e **roteamento de sinais**.

---

## 1. Mapeamento das Funções Lógicas

O circuito possui três entradas primárias ($b, p1, p0$) e gera três saídas: os próximos estados ($n1, n0$) e a saída do sistema ($z$).

Com base no diagrama de portas:

- **Próximo Estado $n1$**:  
  $n1 = (b \cdot p1) + (b \cdot p0)$

- **Próximo Estado $n0$**:  
  $n0 = (b \cdot \overline{p1} \cdot \overline{p0}) + (\overline{b} \cdot p0)$

- **Saída $z$**:  
  $z = p1$ (conexão direta / *pass-through*)

---

## 2. Configuração dos CLBs (LUTs 3x1)

Como cada saída de próximo estado depende de exatamente três variáveis, serão utilizados **dois CLBs**.

### CLB 1 — Saída $n1$

A LUT será programada com a função:  
$n1 = b \land (p1 \lor p0)$

| Endereço (b, p1, p0) | Saída n1 |
|----------------------|----------|
| 0 (000) até 4 (100)  | 0        |
| 5 (101)              | 1        |
| 6 (110)              | 1        |
| 7 (111)              | 1        |

**Conteúdo da Memória (Bitstream):**

    00000111


---

### CLB 2 — Saída $n0$

A LUT será programada com a função:  
$n0 = (b \cdot \overline{p1} \cdot \overline{p0}) \lor (\overline{b} \cdot p0)$

| Endereço (b, p1, p0) | Saída n0 |
|----------------------|----------|
| 0 (000)              | 0        |
| 1 (001)              | 1        |
| 2 (010)              | 0        |
| 3 (011)              | 1        |
| 4 (100)              | 1        |
| 5 (101)              | 0        |
| 6 (110) até 7 (111)  | 0        |

**Conteúdo da Memória (Bitstream):**

    01011000


---

## 3. Configuração da Matriz de Interconexão (4x4)

A matriz deve ser configurada para rotear os sinais de entrada e os sinais de *feedback* do registrador de estado para as entradas das LUTs.

| Entrada da Matriz | Sinal de Origem        | Destino (Saída da Matriz)                     |
|-------------------|------------------------|-----------------------------------------------|
| Entrada 0         | Sinal externo $b$      | Entrada $a2$ de ambos os CLBs                 |
| Entrada 1         | Feedback $p1$          | Entrada $a1$ de ambos os CLBs e saída $z$     |
| Entrada 2         | Feedback $p0$          | Entrada $a0$ de ambos os CLBs                 |
| Entrada 3         | (Não utilizado)        | —                                             |

---

## 4. Registradores e Saída $z$

- **Registrador de Estado**:  
  As saídas $n1$ e $n0$ das LUTs são conectadas às entradas dos *Flip-Flops* (FFs) internos dos CLBs, atualizando os sinais $p1$ e $p0$ no próximo ciclo de clock.

- **Saída $z$**:  
  Como $z$ corresponde diretamente ao sinal $p1$, ele é roteado da saída do registrador de estado para o pino de saída por meio da matriz de interconexão, sem a necessidade de uma terceira LUT.

---

## Conclusão

A configuração apresentada utiliza:
- **2 CLBs** para a lógica combinacional de próximo estado
- **1 matriz de interconexão** para o roteamento dos sinais

Essa solução respeita as limitações de **3 entradas por LUT** e **4 caminhos de roteamento** da matriz, implementando corretamente o bloco de controle no FPGA.

