
## 2) Para cada item a seguir elabore um circuito que atenda às restrições estabelecidas

Os atrasos das portas lógicas são mostrados na tabela abaixo. Considere que o atraso somado de todos os fios de um mesmo caminho é sempre igual a **1 ns**. Utilize os FFs que julgar necessários.

### Portas e atrasos

| Portas           | Atraso |
|------------------|--------|
| AND, OR, NOT     | 1 ns   |
| NAND, NOR        | 2 ns   |
| XOR, XNOR        | 2,5 ns |

### Itens

a) Frequência máxima = 200 MHz  
b) Maior atraso de 10 ns e o menor de 6 ns  
c) Frequência máxima >= 275 MHz, usando no mínimo 1 XOR e 1 NAND  

---
## c) Frequência máxima >= 275 MHz, usando no mínimo 1 XOR e 1 NAND

Tmin = 1/ 275 MHz ≈ 3,64 ns.  

Tportas + 1 ns ≤ 3,64 ns ⇒ Tportas ≤ 2,64 ns.

Como TXOR = 2,5 ns e TNAND = 2 ns, eles devem estar em caminhos paralelos.

### Circuito Proposto

Um circuito com dois flip-flops.

**Caminho 1:**  
Uma porta NAND alimenta o primeiro FF.  
Atraso total:  
TNAND + Tfios = 2 ns + 1 ns = 3 ns (f ≈ 333 MHz).

**Caminho 2:**  
Uma porta XOR alimenta o segundo FF.  
Atraso total:  
TXOR + Tfios = 2,5 ns + 1 ns = 3,5 ns (f ≈ 286 MHz).

O caminho crítico do circuito é 3,5 ns, resultando em Fmax ≈ 286 MHz, que satisfaz a condição.

---

## Ciruito

![Circuito da Questão 2.30 - item a](figuras/alternatica-c.png)
