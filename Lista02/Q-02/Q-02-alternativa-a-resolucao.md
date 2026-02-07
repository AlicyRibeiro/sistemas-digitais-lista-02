
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

## a) Frequência máxima = 200 MHz

O período mínimo do clock (Tmin) deve ser:  
Tmin = 1/ Fmax = 1/ 200 MHz = 5 ns

O atraso do caminho crítico (Tcritico) entre dois flip-flops deve ser ≤ Tmin.  
Tcritico = Tportas + Tfios ≤ 5 ns  
Tportas + 1 ns ≤ 5 ns ⇒ Tportas ≤ 4 ns

**Circuito Proposto:**  
Um caminho com uma porta AND (1 ns) seguida de uma porta XOR (2.5 ns).

**Lógica:**  
Saida <= (Entrada1 AND Entrada2) XOR Entrada3

Atraso das portas = 1 ns + 2.5 ns = 3.5 ns.  
Atraso total do caminho = 3.5 ns (portas) + 1 ns (fio) = 4.5 ns, que é menor que 5 ns.

---

## Circuito

![Circuito da Questão 2.30 - item a](figuras/alternatica-a.png)

