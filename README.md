 Conversor Duplo de Voltagem (9V para 5V e 3.3V) - V1

Este projeto consiste num conversor duplo de tensão utilizando reguladores lineares para rebaixar uma entrada de **9V** para duas saídas estáveis: **5V** (via conector USB-A) e **3.3V** (via terminal de parafusos). É ideal para alimentar placas de desenvolvimento como Arduino e ESP32.

## Dados Teóricos de Potência e Temperatura

Abaixo encontram-se os cálculos efetuados para analisar o comportamento térmico dos reguladores sob diferentes condições de carga, considerando uma **Temperatura Ambiente de 25°C**:

### Regulador de 5V (LM7805)

| Vi (V) | Vo (V) | I (A) | P (W) | Rθja (°C/W) | Rθjc (°C/W) | Ttnu (°C) | Ttcom (°C) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 9 | 5 | 0.5 | 2.0 | 50 | 21 | 125 | 78 |
| 9 | 5 | 0.8 | 3.2 | 50 | 21 | 185 | 109.8 |
| 9 | 5 | 0.5 | 2.0 | 50 | 16 | 125 | 68 |
| 9 | 5 | 0.8 | 3.2 | 50 | 16 | 185 | 93.8 |

### Regulador de 3.3V (LD1117V33)

| Vi (V) | Vo (V) | I (A) | P (W) | Rθja (°C/W) | Rθjc (°C/W) | Ttnu (°C) | Ttcom (°C) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 5 | 3.3 | 0.3 | 0.51 | 50 | 16 | 50.5 | 35.965 |
| 9 | 3.3 | 0.3 | 1.71 | 50 | 16 | 110.5 | 61.765 |
| 5 | 3.3 | 0.3 | 0.51 | 50 | 21 | 50.5 | 38.515 |
| 9 | 3.3 | 0.3 | 1.71 | 50 | 21 | 110.5 | 70.315 |

*Nota: **Ttnu** representa a temperatura estimada do componente sem dissipador (nú), e **Ttcom** com  dissipador térmico externo. 
