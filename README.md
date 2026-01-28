# Nucleus Email Template

Template de e-mail marketing para Nucleus, compatível com todos os principais clientes de e-mail.

## Estrutura

- `index.html` - Arquivo HTML principal do e-mail
- `images/` - Pasta contendo todas as imagens do template
- `vercel.json` - Configuração para deploy na Vercel

## Deploy na Vercel

### Opção 1: Via Vercel CLI (Recomendado)

1. Instale a Vercel CLI globalmente:
```bash
npm i -g vercel
```

2. No diretório do projeto, execute:
```bash
cd "/Users/danielsnows/Documents/Danyll Goodman/Nucleus/Emails"
vercel
```

3. Siga as instruções no terminal para fazer login e configurar o projeto.

4. Para fazer deploy em produção:
```bash
vercel --prod
```

### Opção 2: Via Interface Web da Vercel

1. Acesse [vercel.com](https://vercel.com) e faça login
2. Clique em "Add New Project"
3. Se o projeto estiver no GitHub/GitLab/Bitbucket, importe o repositório
4. Ou use "Deploy" e arraste a pasta do projeto
5. Configure o projeto e clique em "Deploy"

### Opção 3: Via GitHub (Recomendado para produção)

1. Crie um repositório no GitHub
2. Inicialize o Git no projeto:
```bash
cd "/Users/danielsnows/Documents/Danyll Goodman/Nucleus/Emails"
git init
git add .
git commit -m "Initial commit: Nucleus email template"
git branch -M main
git remote add origin <URL_DO_SEU_REPOSITORIO>
git push -u origin main
```

3. Na Vercel, conecte o repositório GitHub
4. A Vercel fará deploy automático a cada push

## Acessando o Site

Após o deploy, você receberá uma URL no formato:
- Preview: `https://nucleus-emails-xxxxx.vercel.app`
- Produção: `https://nucleus-emails.vercel.app` (ou domínio customizado)

## Notas

- As imagens estão em caminhos relativos (`images/`), funcionando perfeitamente na Vercel
- O arquivo `index.html` será servido como página principal
- Todos os arquivos estáticos serão servidos automaticamente pela Vercel
