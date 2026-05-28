# Guia Passo-a-Passo — Fase 1 (Herbert)

> Este guia te leva do zero até a Fase 1 entregue. Cada passo é independente e tem um critério de "feito".

---

## ✅ Checklist final da Fase 1

Você terá feito a Fase 1 quando tiver:

- [ ] Um **repositório público no GitHub** com a estrutura inicial subida
- [ ] Um **GitHub Project público** (Kanban) ligado ao repo, com colunas e cards criados
- [ ] O **link do Kanban no README** do repositório
- [ ] Tudo isso pronto pro Renan começar a Fase 2

---

## Passo 1 · Criar o repositório no GitHub (5 min)

1. Acesse https://github.com/new
2. **Repository name**: `chargegrid-intelligence`
3. **Description**: `Sprint 06 - GoodWe Challenge: Prova de Conceito para gerenciamento inteligente de demanda em pontos de recarga EV.`
4. Marque **Public** (precisa ser público pro Kanban ser acessível pelos professores)
5. **NÃO** marque "Add a README" / "Add .gitignore" / "Choose a license" — você vai subir isso manualmente
6. Clique em **Create repository**

✅ **Pronto** quando: a URL `https://github.com/<seu-usuario>/chargegrid-intelligence` abre uma página vazia "Quick setup".

---

## Passo 2 · Subir a estrutura inicial (5 min)

Você tem duas opções. Escolha a que for mais confortável.

### Opção A — Pelo navegador (mais fácil, sem terminal)

1. Na página do repositório vazio, clique em **"uploading an existing file"**
2. Arraste todos os arquivos e pastas que eu te entreguei (README.md, .gitignore, LICENSE, requirements.txt, src/, docs/, data/, kanban/)
3. Escreva o commit message: `Estrutura inicial do projeto`
4. Clique em **Commit changes**

### Opção B — Por terminal (Git)

```bash
# Na pasta onde você descompactou os arquivos:
cd caminho/para/chargegrid-intelligence
git init
git add .
git commit -m "Estrutura inicial do projeto"
git branch -M main
git remote add origin https://github.com/<seu-usuario>/chargegrid-intelligence.git
git push -u origin main
```

✅ **Pronto** quando: a página do repositório mostra a árvore de pastas (README, src, docs, data, kanban, etc).

---

## Passo 3 · Criar o GitHub Project (Kanban) (10 min)

1. Na página do repositório, clique na aba **Projects** (no topo, do lado de Issues / Pull requests)
2. Clique em **"Link a project"** → **"New project"**
3. Escolha o template **"Board"** (formato Kanban)
4. **Project name**: `ChargeGrid Sprint 06 - Kanban`
5. Clique em **Create project**

### Tornar o Project público

GitHub Projects criados a partir de um repo público herdam a visibilidade do repo. Pra confirmar:

1. No Project, clique nos três pontinhos `...` no canto superior direito → **Settings**
2. Em **Visibility**, confirme que está como **Public**

### Configurar as colunas

O template Board já vem com `Todo`, `In Progress`, `Done`. Vamos ajustar pra 5 colunas:

1. Renomeie `Todo` para **A Fazer** (clique no nome da coluna)
2. Renomeie `In Progress` para **Em Andamento**
3. Renomeie `Done` para **Concluído**
4. Clique no `+` à esquerda de "A Fazer" e adicione uma coluna **Backlog**
5. Adicione outra coluna **Em Revisão** entre "Em Andamento" e "Concluído"

Ordem final: `Backlog · A Fazer · Em Andamento · Em Revisão · Concluído`

✅ **Pronto** quando: o board tem as 5 colunas na ordem acima.

---

## Passo 4 · Criar os cards (15 min)

Abra o arquivo `kanban/cards.md` do repositório — ele tem **todos os 12 cards** já redigidos. Pra cada card:

1. Na coluna desejada do board, clique em **`+ Add item`**
2. Cole o título do card (ex: `Card 1.1 · Criar quadro Kanban público`)
3. Aperte Enter
4. Clique no card que acabou de criar pra abrir os detalhes
5. Cole a descrição completa do card (do `cards.md`) no campo de descrição
6. Salve

### Distribuição sugerida no board inicial

| Coluna | Cards |
|---|---|
| **Backlog** | (vazio por enquanto) |
| **A Fazer** | 2.1, 2.2, 2.3, 2.4, 2.5, 3.1, 3.2, 3.3, 3.4 |
| **Em Andamento** | 1.1, 1.3 |
| **Em Revisão** | (vazio) |
| **Concluído** | 1.2 (porque você está fazendo agora) |

> Dica: quando você terminar de criar todos os cards, mova o `1.1` e `1.3` pra **Concluído** também — porque a esta altura você já vai ter feito as duas coisas (Kanban criado + repo estruturado). Só sobra o `1.2` (migrar cards) que você terá acabado de finalizar.

✅ **Pronto** quando: os 12 cards estão criados e distribuídos nas colunas.

---

## Passo 5 · Atualizar o README com o link do Kanban (2 min)

1. No board do Project, copie a URL (algo como `https://github.com/users/<seu-usuario>/projects/N`)
2. Abra o arquivo `README.md` no repositório
3. Procure a linha: `- **Kanban (GitHub Projects)**: a preencher após criação`
4. Substitua por: `- **Kanban (GitHub Projects)**: <cole a URL aqui>`
5. Commit a mudança (mensagem: `docs: adicionar link do Kanban ao README`)

✅ **Pronto** quando: o link do Kanban no README leva pro board público.

---

## Passo 6 · Avisar a equipe (1 min)

Mande no grupo:

> Pessoal, terminei a Fase 1 ✅
> Repo: `<link do GitHub>`
> Kanban: `<link do Projects>`
> @Renan, os cards da Fase 2 já estão criados no board, pode começar.
> @Biel, o roteiro inicial já está em `docs/roteiro-video.md`.

---

## Tempo total estimado: ~40 minutos

Se travar em algum passo, me chama que eu te ajudo.
