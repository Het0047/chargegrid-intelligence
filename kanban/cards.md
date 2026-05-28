# Quadro Kanban — Sprint 06

> Documento de referência da equipe. Reflete o estado inicial do quadro Kanban criado no GitHub Projects.

## Colunas

| Coluna | Significado |
|---|---|
| 📋 **Backlog** | Tarefas mapeadas mas ainda não iniciadas |
| 🔵 **A Fazer** | Próximas a serem trabalhadas na sprint atual |
| 🟡 **Em Andamento** | Em execução agora |
| 🟣 **Em Revisão** | Concluídas, aguardando revisão pelos pares |
| 🟢 **Concluído** | Aceitas e finalizadas |

## Cards

Cada card abaixo deve ser criado como um item no GitHub Projects. Os campos `Responsável`, `Fase` e `Prioridade` podem ser configurados como *custom fields* do board.

---

### 🟢 Fase 1 — Estruturação e Planejamento

#### Card 1.1 · Criar quadro Kanban público
- **Responsável**: Herbert
- **Fase**: 1
- **Prioridade**: Alta
- **Descrição**: criar o board no GitHub Projects associado ao repositório, configurar as 5 colunas (Backlog / A Fazer / Em Andamento / Em Revisão / Concluído) e garantir que o acesso esteja público.
- **Critérios de aceitação**:
  - [ ] Board criado e visível sem login
  - [ ] 5 colunas configuradas
  - [ ] Link do board adicionado ao README

#### Card 1.2 · Migrar tarefas da Sprint para o board
- **Responsável**: Herbert
- **Fase**: 1
- **Prioridade**: Alta
- **Descrição**: criar um card no board para cada uma das tarefas mapeadas nas Fases 1, 2 e 3, distribuir entre os responsáveis e definir prioridades.
- **Critérios de aceitação**:
  - [ ] Todos os cards criados
  - [ ] Cada card tem responsável e fase atribuídos
  - [ ] Cards iniciais movidos para "A Fazer"

#### Card 1.3 · Estruturar repositório no GitHub
- **Responsável**: Herbert
- **Fase**: 1
- **Prioridade**: Alta
- **Descrição**: criar o repositório público, subir a estrutura inicial (README, .gitignore, LICENSE, pastas src/, data/, docs/) e configurar branch protection se necessário.
- **Critérios de aceitação**:
  - [ ] Repositório público criado
  - [ ] Estrutura de pastas no padrão definido
  - [ ] README inicial com descrição, equipe e links
  - [ ] LICENSE adicionada

---

### 🔵 Fase 2 — Desenvolvimento da PoC

#### Card 2.1 · Definir escopo da PoC
- **Responsável**: Renan_Mano
- **Fase**: 2
- **Prioridade**: Alta
- **Descrição**: documentar o que entra e o que fica de fora do escopo da prova de conceito. Definir os cenários de teste que serão demonstrados no vídeo.
- **Critérios de aceitação**:
  - [ ] Escopo documentado em `docs/arquitetura.md`
  - [ ] Pelo menos 2 cenários de teste descritos

#### Card 2.2 · Implementar núcleo de gerenciamento de demanda
- **Responsável**: Renan_Mano
- **Fase**: 2
- **Prioridade**: Alta
- **Descrição**: implementar a lógica que distribui a potência disponível entre as sessões concorrentes, respeitando limites da rede.
- **Critérios de aceitação**:
  - [ ] Módulo `grid_manager.py` implementado
  - [ ] Função principal recebe sessões + capacidade e retorna alocação
  - [ ] Teste manual passa para os cenários definidos

#### Card 2.3 · Implementar engine de tarifação dinâmica
- **Responsável**: Renan_Mano
- **Fase**: 2
- **Prioridade**: Média
- **Descrição**: implementar o cálculo de tarifa conforme faixa horária (ponta / intermediária / fora-ponta).
- **Critérios de aceitação**:
  - [ ] Módulo `tariff_engine.py` implementado
  - [ ] Faixas horárias parametrizáveis
  - [ ] Custo calculado por sessão

#### Card 2.4 · Implementar lógica de prioridade
- **Responsável**: Renan_Mano
- **Fase**: 2
- **Prioridade**: Média
- **Descrição**: definir como cada sessão recebe uma prioridade (regras + opcional camada de IA simples).
- **Critérios de aceitação**:
  - [ ] Módulo `priority_logic.py` implementado
  - [ ] Documentação das regras em `docs/arquitetura.md`

#### Card 2.5 · Integrar tudo no main.py
- **Responsável**: Renan_Mano
- **Fase**: 2
- **Prioridade**: Alta
- **Descrição**: integrar os módulos, criar entrada de dados (CSV ou sintética) e gerar saída visualizável (tabela ou gráfico).
- **Critérios de aceitação**:
  - [ ] `python src/main.py` roda sem erro
  - [ ] Saída demonstra alocação + custo por sessão
  - [ ] README de execução atualizado

---

### 🟣 Fase 3 — Documentação e Entrega

#### Card 3.1 · Roteirizar vídeo
- **Responsável**: Biel
- **Fase**: 3
- **Prioridade**: Alta
- **Descrição**: escrever o roteiro do vídeo de até 5 minutos, com tempos por seção. Base em `docs/roteiro-video.md`.
- **Critérios de aceitação**:
  - [ ] Roteiro completo
  - [ ] Revisado pela equipe

#### Card 3.2 · Gravar e editar vídeo
- **Responsável**: Biel
- **Fase**: 3
- **Prioridade**: Alta
- **Descrição**: gravar a apresentação seguindo o roteiro, editar para caber em 5 minutos e publicar no YouTube.
- **Critérios de aceitação**:
  - [ ] Vídeo gravado
  - [ ] Editado dentro de 5 min
  - [ ] Publicado no YouTube (não-listado ou público)

#### Card 3.3 · Atualizar README final
- **Responsável**: Biel
- **Fase**: 3
- **Prioridade**: Alta
- **Descrição**: atualizar o README do GitHub com a descrição final da solução, diagrama de arquitetura, instruções reais de execução e links de Kanban e vídeo.
- **Critérios de aceitação**:
  - [ ] Descrição alinhada com a PoC final
  - [ ] Instruções de execução testadas
  - [ ] Todos os links preenchidos

#### Card 3.4 · Consolidar entregáveis e gerar `entrega_sprint_2.txt`
- **Responsável**: Biel
- **Fase**: 3
- **Prioridade**: Alta
- **Descrição**: criar o arquivo `.txt` final com nomes, RMs e os 3 links (YouTube, GitHub, Kanban).
- **Critérios de aceitação**:
  - [ ] Todos os RMs preenchidos
  - [ ] 3 links funcionais
  - [ ] Arquivo enviado no formato pedido

---

## Distribuição visual inicial sugerida do board

```
📋 BACKLOG        🔵 A FAZER          🟡 EM ANDAMENTO   🟣 EM REVISÃO   🟢 CONCLUÍDO
                  2.1 escopo PoC      1.1 Kanban
                  2.2 grid manager    1.3 repositório
                  2.3 tarifação
                  2.4 prioridade
                  2.5 integração
                  3.1 roteiro
                  3.2 gravação
                  3.3 README final
                  3.4 .txt entrega                       1.2 migrar tarefas
```

Conforme as tarefas avançarem, os responsáveis movem seus cards.
