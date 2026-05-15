# 🤖 n8n Workflows — Automações com IA

> Coleção de workflows n8n para automação inteligente com IA, APIs e integrações.  
> Desenvolvido por **Rodrigo Salgado** — Analista de Dados & IA em transição para Engenheiro de Dados.

---

## 📋 Workflows Disponíveis

| # | Workflow | Descrição | Tecnologias |
|---|----------|-----------|-------------|
| 01 | [Resumo de Notícias por E-mail](./workflows/01-resumo-noticias-email/) | Acessa lista de sites, resume com ChatGPT e envia por e-mail diariamente | Schedule · HTTP · ChatGPT · Gmail |
| 02 | [Alerta de Ações com IA](./workflows/02-alerta-acoes-ia/) | Monitora cotações da B3, detecta variações e envia alertas com análise de sentimento | Alpha Vantage · Bing News · ChatGPT · Gmail · Sheets |
| 03 | [Resumo de Notícias via Telegram](./workflows/03-resumo-noticias-telegram/) | Resume notícias com ChatGPT e envia mensagem formatada no Telegram diariamente | Schedule · HTTP · ChatGPT · Telegram |

---

## 🛠️ Tecnologias Utilizadas

- **[n8n](https://n8n.io/)** — Plataforma de automação low-code
- **[OpenAI GPT-4o](https://openai.com/)** — Análise de sentimento e resumo de notícias
- **[Alpha Vantage API](https://www.alphavantage.co/)** — Cotações de ações em tempo real
- **[Bing News Search (RapidAPI)](https://rapidapi.com/microsoft-azure-org-microsoft-cognitive-services/api/bing-news-search1)** — Busca de notícias financeiras
- **[Telegram Bot API](https://core.telegram.org/bots/api)** — Envio de mensagens via bot
- **[Gmail API](https://developers.google.com/gmail)** — Envio de alertas formatados em HTML
- **[Google Sheets API](https://developers.google.com/sheets)** — Armazenamento e histórico de dados

---

## 🚀 Como Usar

### Pré-requisitos
- Conta no [n8n.io](https://n8n.io/) (cloud ou self-hosted)
- Credenciais configuradas (veja cada workflow para detalhes)

### Importar um Workflow
1. Acesse seu n8n
2. Clique em **"New Workflow"** → **"..."** → **"Import from JSON"**
3. Cole o conteúdo do arquivo `workflow.json` desejado
4. Configure as credenciais e variáveis conforme o README do workflow
5. Ative o workflow

---

## 📁 Estrutura do Repositório

```
n8n-workflows/
├── README.md
├── workflows/
│   ├── 01-resumo-noticias-email/
│   │   ├── workflow.json
│   │   └── README.md
│   ├── 02-alerta-acoes-ia/
│   │   ├── workflow.json
│   │   └── README.md
│   └── 03-resumo-noticias-telegram/
│       ├── workflow.json
│       └── README.md
```

---

## 👨‍💻 Sobre o Autor

**Rodrigo Salgado**  
Analista de Power BI, Dados & IA | Em transição para Engenheiro de Dados & IA

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/SEU-PERFIL)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/r9drig-tech)

---

## ⚠️ Aviso

Os workflows de análise financeira são para fins educacionais e de aprendizado.  
**Não constituem recomendação de investimento.**

---

⭐ Se este repositório foi útil, deixe uma estrela!
