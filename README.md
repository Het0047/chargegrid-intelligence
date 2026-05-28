# ChargeGrid Intelligence

> **Sprint 06 — GoodWe Challenge** · Prova de Conceito (PoC) para gerenciamento inteligente de demanda em pontos de recarga de veículos elétricos.

[![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

---

## 📋 Sobre o Projeto

O **ChargeGrid Intelligence** é uma prova de conceito desenvolvida no contexto do *GoodWe Challenge* (FIAP) para demonstrar como uma camada de inteligência pode otimizar o gerenciamento de demanda, a tarifação dinâmica e a interoperabilidade em uma rede de pontos de recarga de veículos elétricos (EV).

A solução simula o comportamento de um conjunto de carregadores conectados a uma mesma rede elétrica, aplicando regras de priorização e tarifação variável para distribuir a carga de forma eficiente, evitando picos de demanda e aproveitando janelas de menor custo energético.

> ⚠️ **Status**: este repositório está em construção como parte da Sprint 06. Consulte a aba *Projects* para acompanhar o progresso.

---

## 🎯 Conceitos-chave integrados

| Conceito | Como aparece na PoC |
|---|---|
| **Gerenciamento de demanda** | Algoritmo de priorização que distribui potência disponível entre sessões concorrentes |
| **Tarifação dinâmica** | Modelo de preço por faixa horária (ponta / intermediária / fora-ponta) |
| **Interoperabilidade** | Estrutura de dados compatível com padrão OCPP-like para sessões de carga |
| **Inteligência (IA / regras)** | Lógica de decisão baseada em prioridade, histórico de consumo e disponibilidade de rede |

---

## 🏗️ Arquitetura

```
┌─────────────────────────────────────────────────────────┐
│                  ChargeGrid Intelligence                │
├─────────────────────────────────────────────────────────┤
│                                                         │
│   [ Entradas ]                  [ Saídas ]              │
│   • Sessões de carga ──┐                                │
│   • Demanda da rede    ├──► [ Núcleo de Decisão ] ──►   │
│   • Tarifa horária     │                                │
│   • Prioridade do EV ──┘    ┌──────────────────┐        │
│                             │ • Potência aloc. │        │
│                             │ • Custo estimado │        │
│                             │ • Fila / ordem   │        │
│                             └──────────────────┘        │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

(*Diagrama detalhado em [`docs/arquitetura.md`](docs/arquitetura.md) — a ser preenchido pelo responsável da Fase 2.*)

---

## 📂 Estrutura do repositório

```
chargegrid-intelligence/
├── README.md                  # este arquivo
├── LICENSE                    # licença MIT
├── .gitignore                 # arquivos ignorados pelo Git
├── requirements.txt           # dependências Python
│
├── src/                       # código-fonte da PoC
│   └── (a ser preenchido pela Fase 2)
│
├── data/                      # bases de dados / inputs simulados
│   └── README.md              # documentação dos datasets usados
│
├── docs/                      # documentação técnica
│   ├── arquitetura.md         # diagrama e fluxo do sistema
│   ├── decisoes-tecnicas.md   # registro de decisões (ADRs)
│   └── roteiro-video.md       # roteiro do vídeo (Fase 3)
│
└── kanban/                    # backup do estado do Kanban
    └── cards.md               # lista de cards (referência)
```

---

## 🚀 Como executar (placeholder)

> A ser detalhado pelo responsável da Fase 2 quando a PoC estiver implementada.

```bash
# 1. Clonar o repositório
git clone https://github.com/<usuario>/chargegrid-intelligence.git
cd chargegrid-intelligence

# 2. Instalar dependências
pip install -r requirements.txt

# 3. Executar a PoC
python src/main.py
```

---

## 👥 Equipe

| Nome | RM | Responsabilidade na Sprint 06 |
|---|---|---|
| Herbert Richers | RM_______ | Fase 1 — Kanban + estrutura do repo |
| Renan_Mano | RM_______ | Fase 2 — Núcleo da Prova de Conceito |
| Furin | RM_______ | (a definir) |
| Biel Santos | RM_______ | Fase 3 — Documentação, vídeo e entrega |

> 📝 **TODO Herbert**: preencher os RMs reais antes da entrega final.

---

## 🔗 Links do projeto

- **Repositório**: (este)
- **Kanban (GitHub Projects)**: [https://github.com/users/Het0047/projects/2](https://github.com/users/Het0047/projects/2)
- **Vídeo de apresentação (YouTube)**: a preencher pela Fase 3

---

## 📅 Cronograma

| Fase | Descrição | Responsável | Entrega |
|---|---|---|---|
| 1 | Kanban + estrutura inicial do repo | Herbert | em andamento |
| 2 | Desenvolvimento da PoC | Renan_Mano | aguardando Fase 1 |
| 3 | Documentação, vídeo e entrega final | Biel Santos | 15/06 |

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja [`LICENSE`](LICENSE) para detalhes.

---

*Projeto desenvolvido como parte da Sprint 06 — GoodWe Challenge na FIAP (2026).*
