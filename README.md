# Roleta Super Premiado — Arena Praia Fabri

Roleta de brindes em HTML/CSS/JS puro (sem backend, sem dependências além de fontes do Google Fonts). Abra o `index.html` em qualquer navegador para rodar localmente, ou publique no GitHub Pages para ter um link público.

## Prêmios configurados
Grip, Hambúrguer, Camisa, Viseira, Boné, Cropped, Chaveiro, Copo Stanley, Toalhinha, Munhequeira, R$ 1,00.

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser público), por exemplo `roleta-arena-praia-fabri`.
2. Clone o repositório vazio ou aponte este projeto para ele:
   ```bash
   git init
   git add .
   git commit -m "Roleta Arena Praia Fabri"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/roleta-arena-praia-fabri.git
   git push -u origin main
   ```
3. No GitHub, vá em **Settings → Pages**.
4. Em "Source", selecione a branch `main` e a pasta `/ (root)`.
5. Salve. Em ~1 minuto o GitHub gera o link público, algo como:
   ```
   https://SEU_USUARIO.github.io/roleta-arena-praia-fabri/
   ```
6. Compartilhe esse link — qualquer pessoa pode acessar e girar a roleta pelo celular ou computador, sem precisar instalar nada.

## Editar prêmios ou textos

Abra o `index.html` e procure pelo array `prizes` dentro da tag `<script>`:

```js
const prizes = [
  { label:"Grip",         color:"#C9A227" },
  { label:"Hambúrguer",   color:"#3B2A1E" },
  ...
];
```

Basta editar os textos (`label`) ou adicionar/remover itens da lista. As cores alternam automaticamente entre dourado, marrom e verde.

## Observação importante

Esta é uma roleta **puramente visual/aleatória no navegador de cada pessoa** — não há banco de dados nem controle de quantos giros cada pessoa já fez, nem controle de estoque dos prêmios. Se for usar em uma promoção real com prêmios limitados, recomendo:
- Adicionar um formulário simples (nome/telefone) antes de girar, salvo em uma planilha (Google Sheets) ou banco de dados.
- Limitar a 1 giro por pessoa/dia.
- Registrar o resultado sorteado para conferência na hora da retirada do prêmio.

Posso ajudar a implementar isso com um pequeno backend (ex: Google Sheets API ou Firebase) se for do seu interesse.
Teste