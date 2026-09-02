<div align="center">

# Dashboard Studio

**Monte o painel, escreva as perguntas de negócio, saia com a especificação pronta para a IA construir.**

[![arquivo único](https://img.shields.io/badge/arquivo_%C3%BAnico-index.html-93003C?style=flat-square)](index.html)
![sem build](https://img.shields.io/badge/build-nenhum-2E7D32?style=flat-square)
![dependências](https://img.shields.io/badge/depend%C3%AAncias-0-2E7D32?style=flat-square)
![componentes](https://img.shields.io/badge/cat%C3%A1logo-194_componentes-0F1B2D?style=flat-square)
![saídas](https://img.shields.io/badge/sa%C3%ADdas-4_documentos-0F1B2D?style=flat-square)
![offline](https://img.shields.io/badge/offline-100%25-0F1B2D?style=flat-square)
![pt-BR](https://img.shields.io/badge/idioma-pt--BR-3F444B?style=flat-square)

</div>

---

Escolha o esqueleto da página, arraste componentes de um catálogo de 194 peças, ajuste o UI kit e defina as perguntas que o painel precisa responder. O documento se reescreve a cada clique — no fim você copia (ou baixa) um briefing que um modelo de IA transforma em HTML funcionando.

Tudo em um `index.html` de 326 KB: HTML, CSS e JS inline, 195 previews desenhados em SVG à mão. Nada de CDN, fonte remota, servidor ou instalação.

## Índice

- [Começar](#começar)
- [Os dois modos](#os-dois-modos)
- [As quatro saídas](#as-quatro-saídas)
- [Catálogo](#catálogo)
- [UI kit](#ui-kit)
- [Revisão do painel](#revisão-do-painel)
- [Atalhos](#atalhos)
- [Arquivo do projeto](#arquivo-do-projeto)
- [Ligar um design system](#ligar-um-design-system)
- [Mapa do código](#mapa-do-código)

## Começar

```
Abra index.html no navegador.
```

Sem `npm install`, sem servidor local, sem rede. Funciona por `file://`.

## Os dois modos

Alternados pelos botões no topo da tela.

### 🖥️ UI do dashboard

O canvas. Escolha um esqueleto de página, encaixe componentes nas 8 áreas fixas (barra superior, lateral, filtros, trilha, rodapé, sobreposições…) e organize o corpo em seções com 6 layouts de coluna — `1`, `2`, `3`, `4`, `2-1`, `1-2`. Arraste do painel esquerdo ou clique para inserir; cada componente entra uma vez só.

Cada peça no canvas tem inspetor próprio: título, nota de instrução, métrica ou campo, filtros, período, tom, tamanho e moldura. Some-se a isso 12 comportamentos globais (filtro cruzado, drill-down, tooltip sincronizado, estado na URL, alertas por limite, acessibilidade reforçada…).

### 💡 Design de negócio

Antes de desenhar, decidir. Cada pergunta é um bloco com 15 campos — o que é medido, a fórmula, a decisão que apoia, quem decide, meta, limite de alerta, frequência, cortes, fonte do dado, prioridade `P0`/`P1`/`P2`, componentes que respondem e notas de armadilha.

11 templates prontos partem do problema real: receita, churn, conversão de funil, ticket médio, SLA, ocupação, custo unitário, NPS, inadimplência, estoque e produtividade. Os botões **Copiar Markdown** e **Baixar .md** no topo da aba geram um documento a parte, independente da especificação visual.

## As quatro saídas

O documento vive ao lado do canvas e se reescreve na hora. `Baixar .md` salva o que está visível; `Copiar especificação` manda para a área de transferência.

| Aba | Arquivo | O que contém |
| --- | --- | --- |
| **Especificação** | `especificacao-dashboard.md` | O briefing completo: contexto, tokens, estrutura do template, ficha de cada componente, comportamentos e checklist. ~14 KB já vazio. |
| **UI kit** | `ui-kit.md` | Só os tokens, para colar em Figma, `tailwind.config` ou variáveis CSS. |
| **Perguntas de negócio** | `perguntas-de-negocio.md` | Índice das perguntas + um bloco por pergunta, com meta, alerta, decisão e componentes. |
| **JSON** | `estrutura-dashboard.json` | A estrutura inteira, legível por máquina — kit, seções, widgets e o nó `negocio`. |

O botão **Bruto** alterna entre o Markdown renderizado e o texto puro. Clicar num código como `K-02` dentro do documento abre aquele bloco no inspetor.

## Catálogo

194 componentes em 19 famílias, cada um com preview em SVG e uma ficha técnica que entra na especificação (anatomia, dados esperados, interações, estados, acessibilidade, responsividade, tokens e um "não faça").

<details>
<summary><strong>Ver as 19 famílias</strong></summary>

| Família | Peças |
| --- | --: |
| Estrutura da página | 9 |
| Navegação | 9 |
| Elementos de página | 12 |
| Detalhe, entidade e colaboração | 12 |
| Cards de indicador e big numbers | 14 |
| Gráficos de barras | 18 |
| Linhas e áreas | 17 |
| Proporção e composição | 10 |
| Dispersão e distribuição | 7 |
| Heatmaps e matrizes | 5 |
| Mapas | 8 |
| Fluxo, hierarquia e tempo | 5 |
| Medidores | 3 |
| Tabelas e listas | 10 |
| Filtros e controles | 10 |
| Filtros avançados | 15 |
| Calendário e tempo | 8 |
| Carregamento e animações | 12 |
| Interações, estados e detalhes | 10 |

</details>

## UI kit

11 grupos de decisão visual, 47 opções, cada uma com amostra de cor e o parágrafo que vai para a especificação:

**Tema visual** · **Paleta dos dados** · **Tipografia** · **Densidade** · **Cantos e bordas** · **Profundidade** · **Claro ou escuro** · **Como desenhar os gráficos** · **Base de CSS** · **Dados de exemplo** · **Detalhamento da especificação**

A escolha vira um bloco `:root` de variáveis CSS na aba **UI kit**, pronto para copiar literalmente.

## Revisão do painel

O ícone de lista na barra do painel abre a auditoria: 20 regras que apontam o que falta antes de gerar o código, em três severidades — gráfico circular em excesso, tabela sem ordenação, série temporal sem comparação, ausência de estado vazio ou de erro, widget sem métrica, pergunta `P0` sem meta ou decisão. Cada aviso traz o componente que resolve.

## Atalhos

| Tecla | Ação |
| --- | --- |
| `Ctrl+Z` | Desfazer |
| `Ctrl+Shift+Z` · `Ctrl+Y` | Refazer |
| `Ctrl+C` · `Ctrl+V` | Copiar e colar o widget selecionado |
| `Delete` | Remover o widget selecionado |
| `Ctrl+B` | Ocultar ou mostrar o painel lateral |
| `Esc` | Fechar o modal, sair do campo de texto |

O painel lateral é redimensionável pela borda; duplo clique restaura a largura padrão.

## Arquivo do projeto

Em **Configurações do kit → Arquivo do projeto**: `Exportar .json` salva estrutura, kit, comportamentos, notas e perguntas em `dashboard-studio-projeto.json`; `Importar` reabre; `Começar do zero` limpa tudo.

> [!IMPORTANT]
> Não há salvamento automático — nada de `localStorage`. Fechar a aba sem exportar perde o trabalho.

## Ligar um design system

O topo tem uma faixa de atalhos para kits prontos, vazia por padrão. Abra o `index.html` num editor, procure por `const HUB=` (linha 1652) e preencha:

```js
const HUB=[
  {id:'meu-ds', n:'Nome no card', d:'Descrição curta',
   sw:['#F4F6F9','#1B4FE0','#0F1B2D'], tema:'corporativo',
   href:'https://link-do-seu-design-system'},
];
```

Com `href`, o card vira link e abre em nova aba. Sem `href`, o card aplica o kit correspondente aqui mesmo — os campos `tema`, `modo`, `tipo`, `cantos`, `paleta`, `profundidade` e `densidade` mapeiam os grupos do UI kit. As três cores de `sw` são só a amostra visual.

## Mapa do código

Um arquivo, 3.063 linhas, organizado por comentários de faixa:

| Linhas | Bloco |
| --: | --- |
| 7–628 | CSS — hub, painel, documento, preview de Markdown, modal |
| 630–729 | Markup — cabeçalho, painel, `main#biz`, `main#stage`, modal |
| 731–764 | Primitivas de desenho SVG |
| 765–889 | Os 195 previews |
| 890–1026 | Catálogo (`SECTIONS`) |
| 1027–1610 | Direção visual (`STYLE`), previews ricos, componentes extras |
| 1611–1652 | Comportamentos globais e hub |
| 1653–1759 | Fichas por família (`DETAIL`), ícones, tokens |
| 1760–2487 | Estado, palco ao vivo, regras de inserção, painel |
| 2488–2523 | Revisão (`review`) |
| 2524–2880 | Saídas (`buildSpec`, `buildKit`, `buildJSON`), copiar, baixar, painel redimensionável |
| 2881–3060 | Design de negócio e `buildBiz` |

---

<div align="center">
<sub>Feito para ser aberto, editado e entregue. Um arquivo, nada mais.</sub>
</div>
