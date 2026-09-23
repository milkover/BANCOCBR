# Banco de Questões CBR — Radiologia

Aplicativo web de estudo e revisão de radiologia com foco na prova anual do Colégio Brasileiro de Radiologia (CBR). O projeto foi pensado para funcionar totalmente no navegador, sem backend e sem dependências de build.

## O que inclui

- Banco de questões com cadastro manual
- Filtros por categoria
- Estudo por sorteio de questão
- Revisão automática de erros
- Estatísticas de desempenho
- Importação exata de JSON/CSV
- Parsing estrutural de PDF/DOCX
- Geração grounded a partir de material de estudo
- Persistência em localStorage
- Tema claro/escuro
- Layout responsivo para celular

## Estrutura do repositório

- `index.html`: aplicação completa em um único arquivo
- `README.md`: instruções de uso e publicação

## Como rodar localmente

1. Abra o arquivo `index.html` diretamente no navegador, ou
2. Serva a pasta localmente com um servidor estático simples, por exemplo:

```bash
cd /caminho/para/BANCOCBR
python3 -m http.server 8000
```

Depois acesse:

```text
http://localhost:8000/
```

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. No terminal, rode:

```bash
git init
git add .
git commit -m "Primeiro commit"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
git push -u origin main
```

3. No GitHub, vá em `Settings` → `Pages`.
4. Em `Build and deployment`, selecione:
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/root`
5. Salve.
6. O site ficará disponível em algo como:

```text
https://SEU_USUARIO.github.io/SEU_REPO/
```

## Observações importantes

- Todo o banco é salvo no navegador via `localStorage`.
- Nenhum dado é enviado para servidor, então o uso é local ao dispositivo.
- A geração por IA é implementada como uma funcionalidade grounded no material fornecido, com revisão obrigatória antes de estudar as questões geradas.
- Para importação de PDF/DOCX, o navegador extrai texto localmente usando `pdf.js` e `mammoth.js` via CDN.

## Desenvolvimento futuro

As melhorias futuras listadas na especificação podem ser adicionadas progressivamente, mas a versão atual já está organizada para uso funcional e publicação como página web estática.
