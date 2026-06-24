# Nobel Tintas – Landing Page com Painel de Edição

## Como publicar (passo a passo)

### 1. Criar conta gratuita no Netlify
Acesse https://netlify.com e crie uma conta (pode usar o login com Google ou e-mail).

### 2. Criar repositório no GitHub
- Acesse https://github.com e crie uma conta gratuita (se não tiver)
- Crie um repositório chamado `nobel-tintas`
- Envie todos os arquivos desta pasta para o repositório

### 3. Conectar ao Netlify
- No Netlify, clique em "Add new site" → "Import an existing project"
- Escolha GitHub e selecione o repositório `nobel-tintas`
- Clique em "Deploy site"
- Em alguns segundos o site estará no ar (ex: https://nobel-tintas.netlify.app)

### 4. Ativar o painel de edição (Netlify Identity + CMS)
- No painel do Netlify, vá em **Site settings → Identity → Enable Identity**
- Em **Registration**, selecione **Invite only**
- Em **Services → Git Gateway**, clique em **Enable Git Gateway**
- Vá em **Identity → Invite users** e convide seu e-mail
- Você receberá um e-mail para criar sua senha de acesso

### 5. Acessar o painel de edição
Após configurar, acesse:
```
https://SEU-SITE.netlify.app/admin
```
Faça login com o e-mail e senha criados.

---

## O que você pode editar pelo painel (/admin)

- Slogan e descrição da empresa (Hero)
- Texto da seção "Sobre a empresa"
- **Número de WhatsApp de cada loja** ✅
- Endereço e horário de cada unidade ✅
- Mensagem padrão enviada ao clicar no WhatsApp ✅

---

## Estrutura dos arquivos

```
nobel-tintas/
├── index.html          ← Página principal (site)
├── netlify.toml        ← Configuração do Netlify
├── admin/
│   ├── index.html      ← Painel de edição (/admin)
│   └── config.yml      ← Campos editáveis pelo painel
└── public/
    └── dados.json      ← Dados editáveis (WhatsApp, endereços, textos)
```

---

## Alterar dados manualmente (sem painel)

Abra o arquivo `public/dados.json` e edite os campos:
- `"whatsapp"`: número com DDI+DDD, sem espaços (ex: `"5581991234567"`)
- `"endereco"`: endereço completo da loja
- `"horario"`: separar as linhas com `|`

Salve e envie ao GitHub — o Netlify atualiza automaticamente.
