# Fundamentos da Eletricidade: Grandezas Básicas

Este guia explica os quatro pilares da eletricidade utilizando a **Analogia Hidráulica** (comparando o fluxo de elétrons com o fluxo de água em canos).

---

## 1. Tensão Elétrica (Voltage)
**O que é:** É a "pressão" que empurra os elétrons. Sem ela, não há movimento ordenado. Pense na altura de uma caixa d'água: quanto mais alta, maior a pressão para a água descer.

* **Símbolo da Variável:** $V$ (ou $U$)
* **Unidade de Medida:** Volts (V)
* **Fórmula Principal:** $V = R \cdot I$

---

## 2. Corrente Elétrica (Current)
**O que é:** É o fluxo real de elétrons passando por um condutor. É a "vazão" da eletricidade. No cano, seria a quantidade de litros de água que passa por segundo.

* **Símbolo da Variável:** $I$
* **Unidade de Medida:** Ampères (A)
* **Fórmula Principal:** $I = \frac{V}{R}$

---

## 3. Resistência (Resistance)
**O que é:** É a oposição à passagem da corrente. Materiais ou componentes que dificultam o movimento dos elétrons. No cano, imagine um estreitamento ou uma sujeira que dificulta a passagem da água.

* **Símbolo da Variável:** $R$
* **Unidade de Medida:** Ohms ($\Omega$)
* **Fórmula Principal:** $R = \frac{V}{I}$

---

## 4. Potência (Power)
**O que é:** É o trabalho realizado por segundo. Indica quanta energia está sendo convertida em luz, calor ou movimento. É o "resultado final" (ex: o brilho da lâmpada ou o calor do chuveiro).

* **Símbolo da Variável:** $P$
* **Unidade de Medida:** Watts (W)
* **Fórmulas Principais:** * $P = V \cdot I$ (Básica)
    * $P = R \cdot I^2$ (Quando você tem resistência e corrente)
    * $P = \frac{V^2}{R}$ (Quando você tem tensão e resistência)

---

## Resumo em Tabela

| Grandeza | Analogia | Símbolo | Unidade | Fórmula |
| :--- | :--- | :---: | :--- | :--- |
| **Tensão** | Pressão da água | $V$ | Volts (V) | $V = R \cdot I$ |
| **Corrente** | Fluxo/Vazão | $I$ | Ampères (A) | $I = V / R$ |
| **Resistência** | Estreitamento do cano | $R$ | Ohms ($\Omega$) | $R = V / I$ |
| **Potência** | Força da turbina | $P$ | Watts (W) | $P = V \cdot I$ |

> **Dica de Estudo:** Lembre-se do triângulo da Lei de Ohm. Para achar uma variável, basta "esconder" ela com o dedo e ver o que sobra da fórmula $V = R \cdot I$.

---

## Macetes de Proporcionalidade

Para entender como um componente afeta o outro sem precisar fazer conta toda hora, guarde estas regras:

### A Tensão e a Corrente são "Amigas" (Proporcionais)
* **Dica:** Se você aumentar a Tensão ($V$) e manter a mesma Resistência, a Corrente ($I$) **sobe** junto.
* *Exemplo:* Se você ligar uma lâmpada de 12V em uma bateria de 24V, a corrente dobra (e a lâmpada provavelmente queima).

### A Resistência e a Corrente são "Inimigas" (Inversamente Proporcionais)
* **Dica:** Quanto **maior** a Resistência ($R$), **menor** será a Corrente ($I$).
* *Analogia:* Se o cano for muito estreito (muita resistência), passa pouca água (pouca corrente).

### O Macete do Triângulo (Lei de Ohm)
Desenhe um triângulo com o $V$ no topo e $R$ e $I$ na base:
```text
      [ V ]
     /     \
    [R] * [I]
