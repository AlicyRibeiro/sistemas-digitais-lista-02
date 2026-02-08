
## 4) Dados o datapath e a FSM de alto nível abaixo, responda os itens a seguir

a) Apresente a tabela verdade e o circuito do bloco de controle (considere codificação binária)

b) Mostre a FSM do bloco de controle, com os devidos sinais de controle e valores.

---

## a) Derivação dos Sinais

### Estado 0 (T = D)

Para selecionar D, T_s deve ser 0. Para carregar T, T_reg deve ser 1.  
A operação BoostL = RawL é executada, então BoostL_ld = 1 e BoostH_ld = 0.  
O próximo estado é 1.

### Estado 1 (T = T + 5)

Para selecionar T + 5, T_s deve ser 1. Para carregar T, T_reg deve ser 1.  
A operação BoostH = RawH é executada, então BoostH_ld = 1 e BoostL_ld = 0.  
O próximo estado é 0.

---

## Tabela Verdade

| Estado Atual (p0) | Próximo Estado (n0) | T_s | T_reg | BoostL_ld | BoostH_ld |
|-------------------|---------------------|-----|--------|------------|------------|
| 0                 | 1                   | 0   | 1      | 1          | 0          |
| 1                 | 0                   | 1   | 1      | 0          | 1          |

---

## Equações lógicas

n0 = ¬p0  
T_s = p0  
T_reg = 1  
BoostL_ld = ¬p0  
BoostH_ld = p0

---

## Circuito

![Circuito da Questão 2.30 - item a](figuras/Questão3.15.jpeg)
