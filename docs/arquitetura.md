# Arquitetura — ChargeGrid Intelligence

> **Status**: rascunho inicial. A ser detalhado pelo responsável da Fase 2 conforme a PoC for implementada.

## 1. Visão geral

O ChargeGrid Intelligence é organizado em três camadas lógicas:

1. **Camada de Entrada** — recebe os dados das sessões de carga, demanda atual da rede, tarifa horária vigente e nível de prioridade de cada veículo.
2. **Núcleo de Decisão** — aplica a lógica de priorização e tarifação para decidir como distribuir a potência disponível.
3. **Camada de Saída** — retorna as decisões: potência alocada por sessão, custo estimado e ordem de atendimento na fila.

## 2. Fluxo principal

```
[Sessão de carga chega] 
        │
        ▼
[Verifica disponibilidade da rede]
        │
        ▼
[Consulta tarifa horária]
        │
        ▼
[Calcula prioridade do EV]
        │
        ▼
[Núcleo de Decisão aloca potência]
        │
        ▼
[Atualiza fila + registra sessão]
        │
        ▼
[Retorna decisão para o ponto de recarga]
```

## 3. Componentes principais (a detalhar)

- **`src/grid_manager.py`** — gerencia o estado da rede e a demanda agregada.
- **`src/tariff_engine.py`** — calcula a tarifa vigente conforme a faixa horária.
- **`src/priority_logic.py`** — define a prioridade de cada sessão (regras + opcional IA).
- **`src/session_scheduler.py`** — orquestra a fila e a alocação de potência.
- **`src/main.py`** — ponto de entrada da PoC, executa a simulação.

## 4. Dados de entrada

A PoC pode reaproveitar a base preparada na Sprint 04 (`fase1-base_de_dados-final.csv`) como histórico de sessões para simulação, ou gerar dados sintéticos para os cenários de teste.

## 5. Decisões em aberto

- [ ] Definir formato de entrada (CSV, JSON, API)
- [ ] Definir se a camada de IA será implementada ou se ficará só com regras
- [ ] Definir os cenários de teste que aparecerão no vídeo da Fase 3
