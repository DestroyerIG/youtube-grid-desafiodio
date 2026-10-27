# PlayDev · Listagem de vídeos com CSS Grid

Projeto do desafio de Grid Layout da trilha Front-End da [DIO](https://www.dio.co). A proposta era construir a página de listagem de vídeos do YouTube usando apenas HTML e CSS, com foco em CSS Grid.

Em vez de copiar a marca original, mantive a identidade própria **PlayDev**, uma plataforma fictícia de vídeos sobre desenvolvimento web, com paleta em azul-petróleo escuro e destaque âmbar. Este projeto é a continuação do [desafio de Flexbox](https://github.com/DestroyerIG/youtube-flexbox-desafiodio), reconstruído com Grid.

> Substitua esta linha por um print da página (por exemplo, `![Prévia do projeto](./preview.png)`).

## Referência

Design base no Figma: [Desafio de Grid - DIO](https://www.figma.com/file/KknwioExyqKD3D2eSVFrcW/Desafio-Grid---DIO?node-id=0%3A1)

## O que foi construído

- **Layout da página** com áreas nomeadas: cabeçalho, menu lateral e conteúdo
- **Cabeçalho fixo** com logo, busca centralizada e ações do usuário
- **Menu lateral** fixo, que some em telas pequenas
- **Barra de filtros** com rolagem horizontal
- **Grade de vídeos** responsiva, com um vídeo em destaque que ocupa 2 colunas e 2 linhas em telas grandes
- **Miniaturas** feitas só com CSS (gradientes)

## Como o Grid foi usado

| Parte da página | Técnica |
| --- | --- |
| Estrutura geral | `grid-template-columns`, `grid-template-rows` e `grid-template-areas` com `header`, `sidebar` e `main` |
| Cabeçalho | 3 colunas (`220px minmax(0, 1fr) 220px`) e `justify-self: center` na busca |
| Campo de busca | `grid-template-columns: 1fr 64px` |
| Menu lateral | coluna única com `align-content: start` e `gap` |
| Item do menu | `grid-template-columns: 24px 1fr` (ícone + texto) |
| Filtros | `grid-auto-flow: column` e `grid-auto-columns: max-content` |
| Grade de vídeos | `repeat(auto-fill, minmax(260px, 1fr))` e `gap` |
| Vídeo em destaque | `grid-column: span 2` e `grid-row: span 2` |
| Preenchimento de buracos | `grid-auto-flow: dense` |
| Card de vídeo | `grid-template-rows: auto 1fr` (miniatura + informações) |
| Info do vídeo | `grid-template-columns: 36px minmax(0, 1fr)` |
| Centralização | `place-items: center` nas miniaturas, avatares e botões |
| Responsivo | `@media` que redefine `grid-template-areas` sem o menu lateral |

Também foram praticados `position: sticky`, `aspect-ratio`, variáveis CSS e `@media` queries.

## Estrutura do projeto

```
youtube-grid/
├── index.html
├── style.css
└── README.md
```

## Como rodar

Não há dependências. Basta clonar o repositório e abrir o `index.html` no navegador:

```bash
git clone https://github.com/DestroyerIG/youtube-grid-desafiodio.git
cd youtube-grid-desafiodio
```

## Possíveis melhorias

- Menu lateral recolhível em telas pequenas
- Tema claro e escuro
- Dados dos vídeos carregados com JavaScript
- Página de reprodução de vídeo

## Autor

**Itallo Gabriel**

- GitHub: [DestroyerIG](https://github.com/DestroyerIG)
- LinkedIn: [itallogoncalves](https://www.linkedin.com/in/itallogoncalves)
