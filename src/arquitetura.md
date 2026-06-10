# Escopo da Prova de Conceito (PoC) - ChargeGrid Intelligence

Este documento define os limites da Prova de Conceito para o sistema de gerenciamento de demanda e tarifação de recarga de VEs.

## 1. O que entra no escopo (In)
* **Gerenciamento de Demanda:** Lógica de distribuição de potência que respeita os limites da rede elétrica.
* **Tarifação Dinâmica:** Cálculo de custos baseados em faixas horárias (Ponta, Intermediária, Fora-ponta).
* **Lógica de Priorização:** Algoritmo que ordena a fila de carregamento dando prioridade aos veículos com menor nível de bateria.
* **Interface via Terminal:** Execução centralizada no script `main.py` com saída de dados visuais no console (tabela).

## 2. O que fica de fora do escopo (Out)
* Integração física com hardwares de carregadores reais (OCPP).
* Desenvolvimento de Interface Gráfica (Frontend/App).
* Banco de dados persistente (os testes rodarão em memória).

---

## Cenários de Teste (Para Demonstração no Vídeo)

Estes cenários foram desenhados para provar o funcionamento da PoC e serão demonstrados na execução do script.

### Cenário 1: Gerenciamento e Sobrecarga de Grid
* **Contexto:** 5 veículos se conectam simultaneamente demandando um total de energia superior à capacidade atual do grid (ex: 55kW solicitados vs 40kW disponíveis).
* **Resultado Esperado:** O sistema deve limitar a potência fornecida. Os veículos com bateria mais cheia terão sua potência alocada reduzida a zero ou a um valor mínimo, garantindo que o limite do grid (40kW) nunca seja ultrapassado, priorizando os de bateria mais baixa.

### Cenário 2: Variação de Tarifação por Horário
* **Contexto:** Uma sessão de carregamento é simulada em diferentes faixas de horário.
* **Resultado Esperado:** O sistema deve demonstrar que o custo por hora da mesma quantidade de kW alocados muda automaticamente dependendo se a simulação ocorre no horário de Ponta (ex: 19h) ou Fora-ponta (ex: 14h).