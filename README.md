# Oficina "IA para gestores escolares" (Humus Educação, 5/11/2026): versão 3

Versão construída a partir da proposta apresentada aos cursistas (pasta `perfil do publico`), com o design e a preparação prévia da versão 2.

## Princípios desta versão

- **Um roteiro por atividade**, em PDF e Word: o que você vai fazer e aprender, fluxograma, materiais, passo a passo, prompts com [colchetes], personalização, variações opcionais e dicas para gestores.
- **Roteiros independentes**: nenhum roteiro depende de outro nem recapitula etapas anteriores. Horários só na página (`index.html`), nunca nos documentos.
- **Práticas com escolha**: a pessoa escolhe um roteiro e faz a sequência completa; as variações vêm depois.
- **Um único conjunto de pastas para a formação inteira**, em duas versões com os mesmos nomes: `escola_EXEMPLO_horizonte` (tudo preenchido, escola fictícia) e `escola_MODELO_para_preencher` (só a estrutura).

## Estrutura

| Pasta | Conteúdo |
|---|---|
| `index.html`, `assets/` | Página da oficina. Programação com horários em `assets/app.js` (lista `BLOCOS`); links de formulários e ZIP em `assets/config.js`. |
| `roteiros/` | 18 roteiros: 00 preparação · 01 acolhida · 02 fundamentos · 03 ética e matriz · 04 documento da escola · 05A/05B/05C Prática 1 · 06A/06B/06C Prática 2 · 07A–07D Prática 3 · 08 laboratório · 09 governança · 10 fechamento |
| `materiais/escola_EXEMPLO_horizonte/` | 01 perfil · 02 tom de voz · 03 identidade visual · 04 normas · 05 projetos · 06 pedagógico · 07 assistentes · 08 checklists (com documentos de teste e gabarito) · 09 riscos e governança · 10 produções de exemplo · 11 gestão e indicadores (planilha fictícia agregada) |
| `materiais/escola_MODELO_para_preencher/` | As mesmas 11 pastas, com modelos em branco |
| `apoio/` | Normativas (8 PDFs), política institucional editável, quadro comparativo, orientações de preparação e NotebookLM, vídeos, slides de fundamentos, formulários de diagnóstico e avaliação (atualizados para as etapas da v3), checklist de anonimização |

## Programação (só na página)

| Hora | Atividade | Roteiro |
|---|---|---|
| 9h | Acolhida e diagnóstico | 01 |
| 9h30 | Fundamentos, panorama e cultura de dados | 02 |
| 10h20 | Ética, inclusão e matriz de riscos | 03 |
| 11h10 | Documento da escola | 04 |
| 11h40 | Prática 1 | 05A, 05B ou 05C |
| 14h | Prática 2 | 06A ou 06B; demonstração 06C |
| 14h40 | Prática 3 | 07A, 07B, 07C ou 07D |
| 15h20 | Laboratório individual | 08 |
| 16h | Governança e gestão de mudança | 09 |
| 16h40 | Fechamento | 10 |

## Ajustes de prioridade alta (após a análise crítica)

- Links de pastas: cada pasta de `materiais/` e `apoio/` tem um `index.html` com a lista de arquivos (o GitHub Pages não lista diretórios). Se acrescentar arquivos, gere de novo essas listas.
- Critério de dados de crianças corrigido no checklist LGPD (base legal adequada e melhor interesse; consentimento específico quando for essa a base).
- Catálogo de situações: 19 (e não 21).
- Roteiros práticos com o quadro "Como priorizar" (essencial, aprofundar, atalho, desafio) e passos marcados.
- Quadro "Se você usar outra plataforma" (ChatGPT, Gemini, Manus, NotebookLM) nas práticas, no laboratório e na demonstração.
- `apoio/normativas_recortes/`: versões curtas para anexar à IA.
- Novo roteiro 05C (indicadores e relatório para a mantenedora) e pasta 11.

## Verificação dos itens pesquisados

Resultado em `analise_critica/verificacao_itens_pesquisa`. Corrigidos: slide do caso de Newark (fontes NYT jun. 2023 e CNN ago. 2023), critério do ECA Digital (arts. 1º, 22 e 26; vigência 17/03/2026), nome Gemini Notebook, limites de ChatGPT, Claude e Gemini nos quadros por plataforma. Quadro comparativo (`apoio/`) atualizado em 29/10/2026: Gemini Notebook, Manus independente da Meta, limites de projetos e criação de arquivos. Em 29/10/2026: caso de Newark revisado com a reportagem completa (R7, tradução do NYT) e catálogo de situações de risco com a coluna "Por que é risco". Ainda parciais: limites dos planos gratuitos (ensaiar antes do dia) e créditos do Manus.

## Prompts e guia de introdução (29/10/2026)

- Toda caixa de prompt traz "O que você vai obter" (o produto e para quê) e "Anexe ou cite" (arquivo, pasta ou "mesma conversa").
- Prompts que iniciam uma produção pedem que a IA não invente e pergunte quando faltar informação; revisores marcam "não verificável".
- `apoio/fundamentos/guia_introducao_tela_da_ia`: infográficos da tela de uma IA (conversa, modelo, esforço, texto ou voz, modo, anexos, projetos, conectores, plugins, artefato) e das extensões de navegador, com dicas para escrever prompts. Os infográficos também estão em PNG para projetar.

## Pendências

1. Criar os formulários (diagnóstico e avaliação) com `apoio/diagnostico_formularios` e colar os links em `assets/config.js`.
2. Ensaiar os prompts das práticas em conta gratuita para calibrar tempos.
3. Os vídeos de preparação (v2) citam o caso da rematrícula e trilhas; regravar se possível.
4. Slides de fundamentos revisados (23 slides): sem horário, título da oficina atualizado, slide "O percurso do dia" e caso de Newark em dois slides (o caso, com capa e link da matéria do R7, e qual foi o problema).

## Como regenerar o kit (ZIP)

Na pasta `HUMUS_Gestores_v3`: `zip -r kit_oficina_ia_gestores_v3.zip roteiros materiais apoio -x "*.mp4" "*.srt" ".*"`
