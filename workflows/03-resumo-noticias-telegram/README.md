# 📱 Workflow 03 — Resumo de Notícias Diário via Telegram

Workflow que acessa uma lista de sites diariamente ao meio-dia, resume cada notícia com ChatGPT (GPT-4o) e envia tudo em uma única mensagem formatada direto no Telegram.

---

## 🔁 Fluxo

```
⏰ Schedule (12h)
    └─▶ 📋 Lista de Links
            └─▶ 🔀 Separar Links
                    └─▶ 🌐 HTTP Request
                            └─▶ 🧹 Limpar HTML
                                    └─▶ 🤖 ChatGPT GPT-4o
                                            └─▶ 📝 Formatar Resultado
                                                    └─▶ 💬 Montar Mensagem
                                                            └─▶ 📲 Telegram
```

---

## ⚙️ Configuração

### 1. Credenciais necessárias

| Credencial | Como configurar |
|---|---|
| **OpenAI API Key** | n8n → Credentials → OpenAI |
| **Telegram Bot Token** | n8n → Credentials → Telegram → Bot Token: `8932768214:AAFuO_1gidu_kZpELV4JlrqQUy5AiA2vMx8` |

### 2. Configurar credencial Telegram no n8n

1. Vá em **Settings → Credentials → Add Credential**
2. Busque **Telegram**
3. Cole o token do bot
4. Salve e vincule ao node **"Enviar Telegram"**

### 3. Chat ID já configurado
O workflow já está configurado com o Chat ID `1546115301`.

### 4. Personalizar os links
No node **"Lista de Links"**, edite o array com seus sites preferidos:
```json
["https://g1.globo.com", "https://www.infomoney.com.br", "https://tecnoblog.net"]
```

---

## 📲 Exemplo de Mensagem no Telegram

```
📰 Resumo de Notícias
Quinta-feira, 15 de maio de 2026

━━━━━━━━━━━━━━━━
🔗 Fonte: g1.globo.com

TÍTULO: Banco Central mantém Selic em 10,5%
RESUMO: O Comitê de Política Monetária decidiu...

━━━━━━━━━━━━━━━━
🔗 Fonte: infomoney.com.br
...

━━━━━━━━━━━━━━━━
Gerado automaticamente pelo seu workflow n8n ⚡
```

---

## 📄 Arquivo

- [`workflow.json`](./workflow.json) — Importe diretamente no n8n
