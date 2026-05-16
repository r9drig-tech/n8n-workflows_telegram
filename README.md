# 🤖 n8n Workflow — Resumo de Notícias via Telegram

> Workflow n8n que resume notícias diariamente e envia para o Telegram usando **Groq LLaMA 3.3** (100% gratuito).  
> Desenvolvido por **Rodrigo Salgado** — Analista de Dados & IA em transição para Engenheiro de Dados.

---

## 📋 Workflow

| # | Workflow | Descrição | Tecnologias |
|---|----------|-----------|-------------|
| 03 | [Resumo de Notícias via Telegram](./workflows/03-resumo-noticias-telegram/) | Acessa lista de sites, resume com Groq LLaMA 3.3 (gratuito) e envia mensagem formatada no Telegram diariamente | Schedule · HTTP · Groq LLaMA · Telegram |

---

## 🔁 Fluxo

```
⏰ Schedule (12h)
    └─▶ 📋 Lista de Links
            └─▶ 🔀 Separar Links
                    └─▶ 🌐 HTTP Request (busca HTML)
                            └─▶ 🧹 Limpar HTML
                                    └─▶ 🦙 Groq LLaMA 3.3 70B (gratuito!)
                                            └─▶ 📝 Formatar Resultado
                                                    └─▶ 💬 Montar Mensagem
                                                            └─▶ 📲 Telegram
```

---

## 🛠️ Tecnologias Utilizadas

- **[n8n](https://n8n.io/)** — Plataforma de automação low-code
- **[Groq LLaMA 3.3 70B](https://groq.com/)** — IA gratuita para resumo de notícias (14.400 req/dia free)
- **[Telegram Bot API](https://core.telegram.org/bots/api)** — Envio de mensagens via bot

---

## 🚀 Como Usar

### Pré-requisitos
- Conta no [n8n.io](https://n8n.io/) (cloud ou self-hosted)
- API Key do [Groq](https://console.groq.com/keys) — gratuito, sem cartão
- Bot no Telegram criado via [@BotFather](https://t.me/BotFather)

### Importar o Workflow
1. Acesse seu n8n
2. Clique em **"New Workflow"** → **"..."** → **"Import from JSON"**
3. Cole o conteúdo do arquivo [`workflow.json`](./workflows/03-resumo-noticias-telegram/workflow.json)
4. Configure as credenciais conforme o [README do workflow](./workflows/03-resumo-noticias-telegram/README.md)
5. Ative o workflow ✅

---

## ⚙️ Credenciais Necessárias

| Credencial | Como obter | Custo |
|---|---|---|
| **Groq API Key** | [console.groq.com/keys](https://console.groq.com/keys) | ✅ 100% Gratuito |
| **Telegram Bot Token** | [@BotFather](https://t.me/BotFather) no Telegram | ✅ Gratuito |

---

## 📲 Exemplo de Mensagem no Telegram

```
📰 Resumo de Notícias
Quinta-feira, 15 de maio de 2026

━━━━━━━━━━━━━━━━
🔗 g1.globo.com

*TÍTULO:* Banco Central anuncia nova política
*RESUMO:* O Banco Central do Brasil decidiu...

━━━━━━━━━━━━━━━━
🔗 tecnoblog.net

*TÍTULO:* Nova atualização do Android chega ao Brasil
*RESUMO:* O Google liberou hoje...

━━━━━━━━━━━━━━━━
Gerado automaticamente pelo seu workflow n8n ⚡
```

---

## 📁 Estrutura do Repositório

```
n8n-workflows_telegram/
├── README.md
└── workflows/
    └── 03-resumo-noticias-telegram/
        ├── workflow.json     ← importe no n8n
        └── README.md         ← instruções detalhadas
```

---

## 👨‍💻 Sobre o Autor

**Rodrigo Salgado**  
Analista de Power BI, Dados & IA | Em transição para Engenheiro de Dados & IA

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/SEU-PERFIL)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/r9drig-tech)

---

⭐ Se este repositório foi útil, deixe uma estrela!
