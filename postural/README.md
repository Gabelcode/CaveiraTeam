# 💀 CAVEIRA TEAM - Análise Postural Privada

Sistema seguro de análise postural integrado com Claude API. Login privado, análise de fotos e export de dados em Markdown/TXT.

---

## 🔐 Credenciais Padrão

**Email:** `gaujo.caveira@gmail.com`  
**Senha:** `CaveiraPosto2025!`

⚠️ **IMPORTANTE:** Mude essas credenciais antes de ir ao ar! Veja seção "Customização" abaixo.

---

## 🚀 Deploy no Vercel (Rápido)

### Passo 1: Preparar no GitHub

```bash
# Clone seu repositório ou crie uma pasta nova
mkdir caveira-postural
cd caveira-postural
git init

# Copie os arquivos
cp caveira-postural-app.html index.html
cp vercel.json vercel.json

# Commit
git add .
git commit -m "Initial commit: Caveira Team Postural Analysis"
git branch -M main
git remote add origin https://github.com/seu-usuario/caveira-postural.git
git push -u origin main
```

### Passo 2: Deploy no Vercel

1. Acesse [vercel.com](https://vercel.com)
2. Clique "New Project"
3. Selecione seu repositório GitHub
4. Deixe as configurações padrão
5. Clique "Deploy"

**Pronto!** Seu app estará no ar em ~2 minutos.

---

## 🛠️ Customização

### Alterar Credenciais de Login

Abra `caveira-postural-app.html` e procure por:

```javascript
// CONFIG
const MASTER_EMAIL = 'gaujo.caveira@gmail.com';
const MASTER_PASSWORD = 'CaveiraPosto2025!';
```

Substitua pelos seus valores:

```javascript
const MASTER_EMAIL = 'seu-email@gmail.com';
const MASTER_PASSWORD = 'SuaSenhaSegura123!';
```

**Depois:** Faça `git push` e o Vercel atualiza automaticamente.

---

### Alterar Esteticamente (Cores, Fontes, etc)

As variáveis CSS estão no topo do arquivo:

```css
:root {
    --color-primary: #0A0A0A;      /* Preto */
    --color-accent: #C8102E;       /* Vermelho Caveira */
    --color-light: #F0EDE8;        /* Branco */
    --color-dark: #1a1a1a;         /* Cinza escuro */
    --color-border: #333;          /* Bordas */
}
```

Personalize conforme quiser. Salve e faça `git push`.

---

## 📋 Como Usar

### 1. Fazer Login
- Email e senha (conforme configurado)
- Sessão fica salva no navegador (localStorage)

### 2. Analisar Postura
- Envie 1 até 3 fotos (frontal, lateral, posterior)
- Digite nome do aluno
- Clique "Analisar Postura"
- Aguarde análise via Claude API

### 3. Visualizar Resultados
- Alterações posturais identificadas
- Classificação de gravidade
- Explicações técnicas e didáticas
- Compensações previstas
- Resumo clínico

### 4. Exportar Dados
- **Baixar MD:** Markdown (para arquivos, edição)
- **Baixar TXT:** Texto puro (para impressão, email)

---

## 🔗 Integração com Seu Site

### Opção 1: Iframe (Recomendado)

Se seu site tem uma página `/avaliacoes`:

```html
<iframe 
  src="https://caveira-postural.vercel.app" 
  style="width: 100%; height: 100vh; border: none;"
></iframe>
```

### Opção 2: Link Direto

Coloque um botão no seu site:

```html
<a href="https://caveira-postural.vercel.app" target="_blank">
  Acessar Análise Postural
</a>
```

### Opção 3: Domínio Customizado

No Vercel dashboard:
1. Vá para "Settings" do projeto
2. "Domains"
3. Adicione seu domínio (ex: `postural.seusite.com`)

---

## 🔐 Segurança

✅ **Autenticação local** (sem servidor, apenas localStorage)
✅ **HTTPS automático** (Vercel fornece)
✅ **Sem armazenamento permanente** (dados só na memória/download)
✅ **Claude API** com chave gerenciada pelo Vercel

⚠️ **NÃO compartilhe** a URL pública com pessoas não autorizadas. O login é simples intencionalemente (pode ser melhorado com Firebase/Auth0 se necessário).

---

## 🐛 Troubleshooting

### "Erro ao analisar. Tente novamente."
- Verifique conexão com internet
- Verifique se as fotos são válidas (JPG, PNG)
- Espere alguns segundos e tente novamente

### "Email ou senha incorretos"
- Verifique as credenciais configuradas
- Limpe cache/cookies (Ctrl+Shift+Delete)
- Tente incógnito

### App não carrega no Vercel
- Verifique se o arquivo está nomeado como `index.html` ou `caveira-postural-app.html`
- Verifique `vercel.json`
- Redeploy manualmente no dashboard Vercel

---

## 📊 Próximos Passos (Opcional)

Se quiser expandir:

1. **Banco de Dados:** Salvar histórico de análises (Firebase, Supabase)
2. **Múltiplos Usuários:** Sistema de alunos com permissões
3. **Mapa de Exercícios:** Integrar prescrição de treino
4. **API de Webhooks:** Notificar alunos automaticamente

---

## 🎯 Suporte

Dúvidas sobre o app? 

- Verifique este README
- Cheque console do navegador (F12 → Console)
- Contate Caveira Team

---

**Caveira Team** • Análise Postural Premium • 💀👊🏴‍☠️
