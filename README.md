# Desafio Excel – Classificação de Perfil de Investidor

## 📄 Descrição

Este projeto foi desenvolvido como parte de um desafio para aplicação de **fórmulas e formatação condicional no Excel**. O objetivo principal é identificar o **perfil de investidor** com base no **tempo de investimento** informado em uma tabela de cenários.

## 📊 Estrutura da Planilha

A planilha contém uma tabela com os seguintes dados:

- **Cenários:** Pergunta "Quanto em X meses?"
- **Patrimônio Acumulado:** Valor projetado ao final do período.
- **Rendimento:** Valor total do rendimento obtido no período.

### Exemplo de dados:

| Cenários              | Patrimônio Acumulado | Rendimento  |
|-----------------------|----------------------|-------------|
| Quanto em 24 meses?   | R$ 2.547,41          | R$ 157,18   |
| Quanto em 60 meses?   | R$ 7.007,57          | R$ 432,37   |
| Quanto em 120 meses?  | R$ 16.540,01         | R$ 1.020,52 |
| Quanto em 240 meses?  | R$ 47.146,18         | R$ 2.908,92 |
| Quanto em 360 meses?  | R$ 103.780,81        | R$ 6.403,28 |

---

## 🧠 Lógica Implementada

### 🎯 Classificação do Perfil do Investidor (na célula `D32`):

- **Conservador** → até 24 meses
- **Moderado** → entre 60 e 120 meses
- **Agressivo** → entre 240 e 360 meses

A célula `D32` analisa a quantidade de meses informada e retorna o perfil do investidor, usando a fórmula:

```excel
=SE(D18<=24;"Conservador";
 SE(E(D18>=25;D18<=120);"Moderado";
 SE(E(D18>=121;D18<=360);"Agressivo";"")))
```

# 🎨 Formatação Condicional
Foi aplicada formatação condicional à célula D32 para representar visualmente o perfil de investidor:

Conservador: Verde claro

Moderado: Amarelo

Agressivo: Vermelho

# ✅ Objetivo da Planilha
Permitir que o usuário insira um tempo de investimento e veja automaticamente:

O perfil correspondente (com cor visual)

Os valores de patrimônio e rendimento esperados para cada cenário

# 🛠️ Tecnologias
Microsoft Excel

Fórmulas: SE, E, OU, PROCURAR

Formatação condicional baseada em texto

# 📁 Arquivo
[📊 Download do arquivo desafio-excel.xlsx](./desafio-excel.xlsx)
