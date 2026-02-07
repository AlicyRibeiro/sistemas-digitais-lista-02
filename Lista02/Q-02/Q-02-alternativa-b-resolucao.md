
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

## 2 b) Maior atraso de 10 ns e o menor de 6 ns

O circuito deve ter múltiplos caminhos, com o mais longo demorando 10 ns e o mais curto,  
6 ns.

### Caminho Longo (10 ns)

Atraso de portas = 10 ns - 1 ns (fio) = 9 ns.

Circuito:  
( (A XOR B) XOR C ) NAND D

Atraso:  
2.5 ns (XOR) + 2.5 ns (XOR) + 2 ns (NAND) = 7 ns.

Para chegar a 9 ns, podemos usar:  
( ( (A NAND B) NOR C ) XOR D) XNOR E.

Atraso =  
2 ns + 2 ns + 2.5 ns + 2.5 ns = 9 ns.

### Caminho Curto (6 ns)

Atraso de portas = 6 ns - 1 ns (fio) = 5 ns.

Circuito:  
(X XOR Y)

Atraso:  
2.5 ns.

Para chegar a 5 ns, usa-se:  
(X XOR Y) XOR Z.

Atraso =  
2.5 ns + 2.5 ns = 5 ns.

---

## Ciruito

![Circuito da Questão 2.30 - item a](figuras/alternatica-b.png)
