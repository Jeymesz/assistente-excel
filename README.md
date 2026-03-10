# 📊 Excel IA — Assistente de Fórmulas com IA

Assistente de IA especializado em Excel com biblioteca de fórmulas integrada. Funciona como um painel lateral direto no Excel.

---

## 🚀 Como publicar no GitHub Pages

### Passo 1 — Criar o repositório

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"**
3. Nome: `excel-ia`
4. Marque como **Public**
5. Clique em **"Create repository"**

### Passo 2 — Subir os arquivos

Você pode usar o método mais simples (arrastar e soltar):

1. Na página do repositório, clique em **"uploading an existing file"**
2. Arraste os arquivos `index.html` e `manifest.xml`
3. Clique em **"Commit changes"**

### Passo 3 — Ativar o GitHub Pages

1. No repositório, clique em **Settings** (engrenagem)
2. No menu lateral, clique em **Pages**
3. Em "Source", selecione **Deploy from a branch**
4. Em "Branch", selecione **main** e pasta **/ (root)**
5. Clique em **Save**
6. Aguarde ~2 minutos. Sua URL será:
   ```
   https://SEU_USUARIO.github.io/excel-ia
   ```

### Passo 4 — Atualizar o manifest.xml

Abra o `manifest.xml` e substitua **todas** as ocorrências de:
```
SEU_USUARIO
```
pelo seu nome de usuário real do GitHub. Depois suba o arquivo atualizado.

---

## 🔧 Instalar no Excel

### Excel Desktop (Windows)

1. Baixe o arquivo `manifest.xml`
2. Mova-o para uma pasta compartilhada (ex: `C:\Suplementos\`)
3. No Excel: **Arquivo → Opções → Central de Confiabilidade → Configurações → Catálogos de Suplementos Confiáveis**
4. Em "URL do Catálogo", cole o caminho da pasta e clique em **Adicionar**
5. Marque **"Mostrar no Menu"** e clique em **OK**
6. Reinicie o Excel
7. Vá em **Inserir → Suplementos → Meus Suplementos** → selecione **Excel IA**

### Excel Desktop (Mac)

1. Baixe o `manifest.xml`
2. Copie para: `~/Library/Containers/com.microsoft.Excel/Data/Documents/wef/`
   (crie a pasta `wef` se não existir)
3. Reinicie o Excel
4. Vá em **Ferramentas → Suplementos do Excel** → selecione **Excel IA**

### Excel Online (Navegador)

1. Abra qualquer planilha no [Excel Online](https://office.com)
2. Vá em **Inserir → Suplementos → Carregar Suplemento**
3. Clique em **"Carregar Meu Suplemento"**
4. Selecione o arquivo `manifest.xml`
5. O painel do Excel IA vai aparecer na barra lateral ✅

---

## 🔑 Configurar a chave API

Para o assistente de IA funcionar, você precisa de uma chave da Anthropic:

1. Acesse [console.anthropic.com](https://console.anthropic.com)
2. Crie uma conta (há créditos gratuitos para começar)
3. Vá em **API Keys** → **Create Key**
4. Copie a chave (começa com `sk-ant-...`)
5. No painel do Excel IA, cole a chave no campo **"Chave API Anthropic"** e clique em **Salvar**

> ⚠️ A chave é salva apenas no seu navegador (localStorage). Ela nunca é enviada para nenhum servidor além da Anthropic.

---

## ✨ Funcionalidades

- 💬 **Chat IA** — Tire dúvidas, peça fórmulas, descreva seu problema
- 📋 **Biblioteca** — 50+ fórmulas com sintaxe, descrição e exemplos
- 🔍 **Busca e filtro** por categoria
- 🔗 **Integração direta** — clique em qualquer fórmula para perguntar à IA

---

## 🛠️ Personalizar

Para adicionar suas próprias fórmulas, edite o array `FORMULAS` no `index.html`:

```javascript
{ name:"MINHAFORMULA", cat:"Categoria", syntax:"=MINHAFORMULA(...)", desc:"Descrição.", ex:"=MINHAFORMULA(A1)" },
```

---

## 📄 Licença

MIT — Livre para usar e modificar.
