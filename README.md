# 📊 Status Report Executivo — Integrações

Dashboard executivo para acompanhamento do portfólio de integrações. Gerado a partir do `data.json`, sem necessidade de código.

---

## 🗂️ Estrutura dos arquivos

```
/
├── index.html   → O dashboard (nunca precisa ser editado)
├── data.json    → Os dados (editado toda semana)
└── README.md    → Este guia
```

---

## 🚀 Publicando no GitHub Pages (primeira vez — ~10 minutos)

### Passo 1 — Criar uma conta no GitHub
Acesse [github.com](https://github.com) e crie uma conta gratuita (se ainda não tiver).

### Passo 2 — Criar um repositório
1. Clique no botão **"New"** (ou **"+"** no canto superior direito → *New repository*)
2. Dê um nome ao repositório, ex: `status-integracoes`
3. Deixe como **Public**
4. Clique em **"Create repository"**

### Passo 3 — Fazer upload dos arquivos
1. Na página do repositório recém-criado, clique em **"uploading an existing file"**
2. Arraste os três arquivos: `index.html`, `data.json` e `README.md`
3. Clique em **"Commit changes"**

### Passo 4 — Ativar o GitHub Pages
1. Clique na aba **"Settings"** do repositório
2. No menu lateral esquerdo, clique em **"Pages"**
3. Em *Source*, selecione **"Deploy from a branch"**
4. Em *Branch*, selecione **"main"** e pasta **"/ (root)"**
5. Clique em **"Save"**

### Passo 5 — Acessar o link
Após ~1 minuto, o GitHub Pages vai gerar o link:
```
https://SEU-USUARIO.github.io/status-integracoes/
```
Esse é o link que você compartilha com o board. ✅

---

## ✏️ Atualizando o dashboard toda semana

Você **nunca** precisa tocar no `index.html`. Só edite o `data.json`.

### Como editar pelo GitHub (sem instalar nada):
1. Acesse seu repositório no github.com
2. Clique no arquivo **`data.json`**
3. Clique no ícone de **lápis ✏️** (Edit this file)
4. Faça as alterações nos campos desejados
5. Clique em **"Commit changes"** → **"Commit changes"** (confirmar)
6. Em ~1 minuto o dashboard já reflete as mudanças 🎉

---

## 📝 Guia rápido do data.json

### Campos de cada parceiro:

| Campo | O que é | Exemplo |
|---|---|---|
| `nome` | Nome do parceiro | `"XP Investimentos"` |
| `status` | Badge de status | `"Em Dia"` / `"Aguardando"` / `"Em PRD"` |
| `progresso` | % da barra (0 a 100) | `75` |
| `descricao` | Texto do card | `"Reunião realizada, próximos passos definidos."` |
| `proximo_marco` | Texto do próximo passo | `"Aguardando assinatura do contrato."` |
| `label_marco` | *(Opcional)* Título da seção de marco | `"Status Final"` |

### Cores automáticas por status:

| Status contém... | Cor |
|---|---|
| `"Em Dia"` ou `"Em PRD"` | 🟢 Verde |
| `"HML"` ou `"Homolog"` | 🔵 Azul |
| `"Aguardando"` | 🟡 Âmbar |
| Qualquer outro | ⚫ Cinza |

### Para adicionar um novo parceiro:
Copie e cole o bloco abaixo dentro do array `parceiros` da fase correta:

```json
{
  "nome": "Nome do Banco",
  "status": "Em Dia",
  "progresso": 10,
  "descricao": "Descrição do status atual.",
  "proximo_marco": "Próximo passo esperado."
}
```

### Para mover um parceiro de fase:
Recorte o bloco do parceiro de uma fase e cole na fase de destino.

---

## 💬 Atualizando via Claude.ai (forma mais rápida)

Você pode me enviar as atualizações em linguagem natural toda semana e eu gero o `data.json` atualizado para você copiar e colar no GitHub:

> *"Semear avançou para 90%, contrato assinado. XP foi movida para Fase 2, progresso 20%."*

---

## 🔮 Próxima evolução: Favro

Quando os dados das integrações estiverem estruturados no Favro e você tiver acesso à API Key, o dashboard pode ser conectado diretamente — sem precisar editar o `data.json` manualmente. O `index.html` não precisará ser reescrito.
