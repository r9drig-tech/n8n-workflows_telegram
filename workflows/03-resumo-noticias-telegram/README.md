# 📱 Workflow 03 — Resumo de Notícias Diário via Telegram + Groq (Gratuito)

Workflow que acessa uma lista de sites diariamente ao meio-dia, resume cada notícia com **Groq LLaMA 3.3 70B** (100% gratuito) e envia tudo em uma única mensagem formatada direto no Telegram.

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

## ⚙️ Configuração

### 1. Credenciais necessárias

| Credencial | Como obter | Custo |
|---|---|---|
| **Groq API Key** | [console.groq.com/keys](https://console.groq.com/keys) | ✅ 100% Gratuito |
| **Telegram Bot Token** | @BotFather no Telegram | ✅ Gratuito |

### 2. Configurar Groq no n8n
- Settings → Credentials → Add → **Header Auth**
- **Name:** `Authorization`
- **Value:** `Bearer SUA_GROQ_API_KEY`
- Vincule ao node **"Groq - Resumir Notícia"**

### 3. Configurar Telegram no n8n
- Settings → Credentials → Add → **Telegram**
- Cole o token do bot
- Vincule ao node **"Enviar Telegram"**

### 4. Chat ID já configurado: `1546115301`

### 5. Personalizar os links
No node **"Lista de Links"**, edite o array:
```json
["https://g1.globo.com", "https://www.infomoney.com.br", "https://tecnoblog.net"]
```

---

## 💡 Por que Groq?
- ✅ 100% gratuito — 14.400 req/dia no free tier
- ✅ Extremamente rápido
- ✅ LLaMA 3.3 70B é excelente para resumos em português
- ✅ Sem cartão de crédito necessário

---

## 📲 Exemplo de mensagem no Telegram

```
📰 Resumo de Notícias
Quinta-feira, 15 de maio de 2026

━━━━━━━━━━━━━━━━
🔗 g1.globo.com

*TÍTULO:* Banco Central mantém Selic em 10,5%
*RESUMO:* O Comitê de Política Monetária...

━━━━━━━━━━━━━━━━
Gerado automaticamente pelo seu workflow n8n ⚡
```

---

## 📄 Arquivo
- [`workflow.json`](./workflow.json) — Importe diretamente no n8n
