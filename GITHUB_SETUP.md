# Passo a Passo: Enviar Código para GitHub

## Pré-requisitos
- Conta no GitHub criada
- Git instalado no seu computador

## Passo 1: Criar Repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique no botão **"+"** no canto superior direito
3. Selecione **"New repository"**
4. Preencha:
   - **Repository name**: `nucleus-emails` (ou outro nome de sua preferência)
   - **Description**: "Email templates for Nucleus marketing campaigns"
   - **Visibility**: Escolha **Public** ou **Private**
   - **NÃO marque** "Initialize this repository with a README" (já temos arquivos)
5. Clique em **"Create repository"**

## Passo 2: Copiar a URL do Repositório

Após criar o repositório, o GitHub mostrará uma página com instruções. Você verá uma URL como:
```
https://github.com/SEU-USUARIO/nucleus-emails.git
```
**Copie essa URL** - você vai precisar dela no próximo passo.

## Passo 3: Inicializar Git e Fazer Commit Local

Abra o terminal e execute os seguintes comandos:

```bash
# Navegar para a pasta do projeto
cd "/Users/danielsnows/Documents/Danyll Goodman/Nucleus/Emails"

# Inicializar repositório Git
git init

# Adicionar todos os arquivos ao staging
git add .

# Fazer o primeiro commit
git commit -m "Initial commit: Email 1 - Welcome template"
```

## Passo 4: Conectar ao Repositório Remoto e Fazer Push

```bash
# Adicionar o repositório remoto (substitua SEU-USUARIO pela sua URL)
git remote add origin https://github.com/SEU-USUARIO/nucleus-emails.git

# Renomear branch para main (padrão atual)
git branch -M main

# Fazer push para o GitHub
git push -u origin main
```

## Passo 5: Verificar no GitHub

1. Acesse seu repositório no GitHub
2. Você deve ver todos os arquivos:
   - `email-1-welcome.html`
   - `index.html`
   - `images/` (pasta com todas as imagens)
   - `vercel.json`
   - `README.md`
   - etc.

## Comandos Úteis para o Futuro

### Fazer commit de mudanças:
```bash
git add .
git commit -m "Descrição das mudanças"
git push
```

### Ver status dos arquivos:
```bash
git status
```

### Ver histórico de commits:
```bash
git log
```

## Nota sobre Autenticação

Se você encontrar erro de autenticação ao fazer `git push`, você pode precisar:

1. **Usar Personal Access Token** (recomendado):
   - Vá em GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Gere um novo token com permissões `repo`
   - Use o token como senha quando solicitado

2. **Ou configurar SSH** (mais seguro a longo prazo):
   - Siga o guia: https://docs.github.com/en/authentication/connecting-to-github-with-ssh

## Arquivos que Serão Ignorados (já configurado no .gitignore)

- `node_modules/` - Dependências do npm
- `.vercel/` - Configurações locais da Vercel
- `*.log` - Arquivos de log
