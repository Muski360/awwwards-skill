# Auditoria e evolução da Awwwards Skill

Registro de 13 de novembro de 2026. A linha de base é o commit `8e8033c`. O foco principal da evolução é Claude e Codex; os demais clientes permanecem secundários. Este documento registra evidências e avaliações da skill e não integra seu percurso normal de execução.

## Linha de base

Foram lidos os dez arquivos de conteúdo e a configuração `.gitignore`, vazia. A skill não possui código executável, manifesto de pacotes ou dependências obrigatórias; as bibliotecas citadas são opções de implementação para projetos atendidos.

| Material | Palavras | Bytes |
| --- | ---: | ---: |
| `SKILL.md` | 1.153 | 8.891 |
| Sete referências | 5.839 | 42.370 |
| Entrada e referências | 6.992 | 51.261 |
| README e metadata | 737 | 7.157 |
| Repositório, sem `.git` | 7.729 | 58.418 |

As palavras foram contadas por ocorrências de `\S+` nos arquivos completos, incluindo frontmatter e tabelas; bytes correspondem ao tamanho dos arquivos. Esses números não são tokens. As verificações da linha de base passaram: `quick_validate.py` retornou `Skill is valid!`; 31 links e âncoras relativos foram verificados sem falhas; a working tree estava limpa.

## Diagnóstico e evidências

| Prioridade | Achado na linha de base | Evidência e limite |
| --- | --- | --- |
| P1 | A pesquisa externa pode ser dispensada antes de definir uma direção ambiciosa. | `SKILL.md:66` e `references/external-references.md:8` condicionam a pesquisa à percepção de necessidade. Nos três ensaios independentes, os agentes leram o guia e nenhum pesquisou externamente. |
| P1 | O fluxo desenvolve um candidato antes de contrastar direções. | `SKILL.md:68` pede um candidato e o compara sobretudo com uma solução estática ou nenhuma adição. O guia de identidade passa da evidência para uma tese sem uma comparação explícita de organizações possíveis. Isso é uma lacuna de instrução, não prova de incapacidade dos modelos. |
| P1 | O repertório mais concreto concentra mecanismos e efeitos. | As sete entradas do catálogo priorizam motion, WebGL, transições, cursor, parallax, texto animado e menu, com forte presença de React/Next. Exemplos de composição, tipografia e fontes do próprio domínio não recebem portas de pesquisa equivalentes. |
| P2 | Há redundância e uma ambiguidade de escopo. | Disposições, comparação com baseline, substituição de marca e revisão do momento mais fraco se repetem entre guias. `SKILL.md:78` manda concluir toda a experiência, enquanto o modo de mudança estreita limita o escopo. |
| P2 | Falta um registro verificável de evolução. | Não havia avaliações versionadas. O README apresentava quatro banners repetidos como placeholders de antes/depois, identificados como tais; não eram resultados demonstrados. |

A estrutura da skill já era válida e já defendia liberdade estética, adaptação ao contexto e acessibilidade. O diagnóstico não sustenta uma reescrita para corrigir suposta incompatibilidade estrutural com modelos recentes. A hipótese de ancoragem criativa é sustentada pela concentração de exemplos e pelas saídas observadas, mas não isola o efeito da skill de prompts, modelos, preferências e decisões anteriores de cada projeto.

### Projetos fornecidos pelo usuário

| Projeto | Evidência inspecionada | Conclusão permitida |
| --- | --- | --- |
| [MegaDex](https://megadex.pages.dev) | HTML, CSS, JavaScript, arquivo de fonte e captura desktop de 1.440 × 1.000. | Abertura em duas colunas, título condensado muito grande à esquerda, cartas à direita, fundo claro quente e acento. Acervo, filtros, álbum, progresso, armazenamento local e backup dão função própria ao projeto. |
| [Portfólio MUSKI360](https://portfolio-muski360.muski.workers.dev) | HTML, CSS, JavaScript, fonte, captura desktop de 1.440 × 1.000, página inteira e viewport móvel de 390 × 844. | A abertura compartilha a relação título/objeto, usando nome e disquete. Biografia, formação, projetos, retrato e controle de rotação são específicos do portfólio. |
| [Kernel](https://github.com/Muski360/Kernel) | Documentação, estilos, componentes e dependências, no commit `f0eefceecff8e84aa1cb66eefada855acd669829`. | Papel/tinta/verde, hero em duas colunas e mostrador contextual estão no código. A [auditoria do projeto](https://github.com/Muski360/Kernel/blob/f0eefceecff8e84aa1cb66eefada855acd669829/docs/auditoria-site.md#L3) registra uso da skill para refinamento e preservação dessas escolhas preexistentes. O deploy indicado retornou 404 nesta inspeção. |
| [orbt](https://github.com/Muski360/orbt) | Documentação visual, componentes, estilos e dependências pelo GitHub. | A [direção documentada](https://github.com/Muski360/orbt/blob/main/docs/visual-identity.md) define brutalismo, papel/tinta/lima e Geist; a abertura combina título e Kanban real. Não foi encontrado deploy público nem atribuição documental à skill. Isso não contradiz o uso informado pelo usuário. |

As tabelas `name` das fontes do [MegaDex](https://megadex.pages.dev/assets/display-BKzMuPgK.woff2) e do [portfólio](https://portfolio-muski360.muski.workers.dev/fonts/BarlowCondensed-ExtraBold.woff2), inspecionadas com `fontTools`, identificam a mesma família e face: **Barlow Condensed ExtraBold**, PostScript `BarlowCondensed-ExtraBold`. Os arquivos diferem em tamanho e hash; não são bytes idênticos. As capturas confirmam a proximidade compositiva, além da coincidência tipográfica. Essa evidência justifica testar alternativas de linguagem sem proibir a estética empregada.

Não houve auditoria completa de acessibilidade, medição de performance ou execução das suítes desses projetos. Estilos e código não demonstram, por si, qualidade de execução no navegador. O comportamento de orbt e Kernel permaneceu sem verificação renderizada.

## Contrato das mudanças

| Problema | Mudança e responsabilidade |
| --- | --- |
| Pesquisa facultativa e escolha precoce | A entrada determina pesquisa antes da escolha para novas direções e transformações ambiciosas; o guia de pesquisa define descoberta, evidência, adaptação e momento de parar. Ajustes estreitos mantêm proporcionalidade. |
| Catálogo domina o método | O método de pesquisa fica separado de [referências técnicas condicionais](../references/reference-catalog.md). Os sete pontos existentes são preservados com alertas úteis, sem virarem um stack padrão. |
| Repertório e exemplos semelhantes | O guia de identidade orienta o contraste entre hipóteses contextuais; os exemplos demonstram decisões e relações diferentes, sem fornecer temas, paletas ou fontes prontas para cada segmento. |
| Repetição e escopo | Auditoria concentra achados, disposições e prioridade; avaliação concentra aceitação e comparação; motion preserva invariantes técnicos. A entrada limita conclusão a rotas e estados afetados pelo trabalho autorizado. |
| Ausência de antes/depois verificável | README e metadata refletem o novo fluxo. Este registro guarda briefs, resultados, métricas e limitações; não é uma referência carregada durante a criação normal de sites. |

Preservar fatos e direitos dos materiais, semântica, teclado/foco, contraste, composição responsiva, reduced motion, alternativas à interação, recuperação de falhas, interrupção de animações e limpeza de recursos. Atmosfera e experimentação continuam justificativas possíveis para movimento sofisticado; simplificação não equivale a remover expressividade.

## Protocolo dos ensaios conceituais

1. Executar cada brief em um agente independente, com o mesmo texto e a versão da skill em avaliação. Não fornecer esta auditoria, saídas anteriores ou uma direção desejada ao agente.
2. Pedir uma direção resolvida em até 350 palavras, com abertura/percurso, tipografia/cor/mídia, interação/movimento e mobile/falhas. Registrar arquivos realmente lidos, fontes abertas, ferramentas usadas, alternativas consideradas e inferências. Os materiais descritos no brief são hipotéticos; não foram anexados arquivos de mídia.
3. Avaliar adequação ao público e propósito, diversidade entre conceitos, uso efetivo de pesquisa, autonomia, escopo e preservação de caminhos acessíveis. Cor, fonte ou troca do objeto focal, isoladamente, não demonstram diversidade de organização da experiência.
4. Comparar decisões e rastros de execução, sem impor um tema esperado a cada segmento. Investigar uma convergência quando não houver justificativa contextual; corrigir a instrução responsável e repetir o caso afetado, em vez de adicionar uma proibição geral.
5. Separar conceito de implementação. Estes ensaios não demonstram aparência renderizada, acessibilidade, performance nem superioridade estatística. Registrar cliente/modelo quando identificado; não declarar execução em Claude sem tê-la realizado.

### Brief 1 — Cooperativa de sementes

Texto exato do pedido submetido:

```text
Use $awwwards-skill em modo conceito para uma cooperativa regional de sementes crioulas. O site deve ajudar agricultores a encontrar variedades adequadas à sua região e época, entender a procedência e solicitar reserva. Há um catálogo real com dados de cultivo, fotos documentais de sementes e produtores e relatos autorizados. O público inclui agricultores usando celulares modestos com conexão instável. Não há identidade visual definida. Queremos um resultado original, legível e ambicioso, sem inventar alegações.
```

### Brief 2 — Festival experimental

Texto exato do pedido submetido:

```text
Use $awwwards-skill em modo conceito para um festival independente de música experimental que ocupa diferentes espaços de uma cidade. Público: frequentadores curiosos que precisam descobrir artistas, comparar horários e planejar sua visita; parte acessa durante o evento em celular. Material disponível: gravações autorizadas, retratos muito diferentes entre si, programação com cruzamentos de horário, mapas dos espaços e textos curatoriais. Sem identidade visual definida. Queremos experiência ambiciosa, original e funcional; áudio apenas por iniciativa da pessoa.
```

### Brief 3 — Instrumentos ópticos industriais

Texto exato do pedido submetido:

```text
Use $awwwards-skill em modo conceito para uma fabricante B2B de instrumentos ópticos de inspeção industrial. Público: engenheiros e compradores comparando faixas de medição, integração, precisão documentada e custo operacional; devem solicitar avaliação de uma amostra. Material: desenhos dimensionais, fotos macro dos resultados de inspeção, vídeos de bancada, fichas técnicas, CAD e casos autorizados. Sem direção visual definida. O site deve transmitir capacidade técnica e criar uma experiência original e visualmente ambiciosa, sem inventar números ou desempenho.
```

## Resultados da linha de base

Os três ensaios foram executados por agentes independentes disponibilizados no ambiente Codex, antes das alterações. As descrições abaixo são **sínteses fiéis das respostas**, não transcrições integrais. Não houve implementação, inspeção dos materiais hipotéticos nem pesquisa externa.

| Ensaio | Direção e decisões produzidas | Rastro e limite |
| --- | --- | --- |
| Sementes | “Índice de campo”: fotografia de sementes em aproximadamente metade da abertura, título e seleção de região/época ao lado; faixas editoriais, procedência e reserva. Georgia com sans do sistema; branco, tinta quase preta e azul. No celular, seleção antes da foto. | Leu entrada, identidade e pesquisa. Comparou abertura cinematográfica/exploração espacial com composição estática; escolheu o índice por conteúdo e conexão limitada. Não abriu fontes externas. |
| Festival | “Partitura urbana”: faixas por espaço e intervalos por apresentação; abertura com horários reais e retrato amplo. Artista → áudio voluntário → apresentação → plano, com conflitos explícitos. Grotesca, numerais tabulares, papel/grafite/amarelo ácido; lista cronológica no celular. | Leu entrada, identidade, pesquisa e motion. Comparou atlas, cartazes e partitura. Não abriu fontes externas. Consulta offline foi proposta, sem implementação ou verificação de atualização. |
| Indústria | “Da superfície à evidência”: macro ampla com recorte ampliado, promessa e ação ao lado; detalhe associado a desenho/ficha em coluna estável. Sans editorial, dados mono, mineral/grafite/âmbar; detalhes numerados no celular. | Leu entrada, identidade, pesquisa e motion. Comparou catálogo estático, 3D e passagem de escala. Não abriu fontes externas. Associações documentais e custo técnico permaneceram inferidos. |

Houve diferenciação funcional e os três agentes mencionaram alternativas. O resultado não permite afirmar que a skill sempre gera o mesmo site. Entretanto, **zero de três** ensaios realizou pesquisa externa, mesmo lendo o guia, e dois repetiram a relação de imagem ampla com conteúdo adjacente. Isso sustenta a revisão do acionamento de pesquisa e da comparação de organizações visuais; não estabelece que qualquer composição compartilhada seja inadequada.

## Resultados após as mudanças

Os mesmos três pedidos foram repetidos em agentes novos e independentes deste ambiente Codex, sem acesso ao README, a este registro, ao histórico ou às respostas anteriores. Os agentes receberam a entrada revisada e carregaram referências conforme sua necessidade. Os três leram somente entrada, pesquisa e identidade; nenhum precisou carregar o catálogo técnico ou toda a coleção. As sínteses abaixo descrevem respostas efetivamente produzidas.

| Ensaio | Direção produzida e diferença estrutural | Pesquisa executada e limite |
| --- | --- | --- |
| Sementes | “Almanaque de cultivo”: entrada por local/época, régua sazonal com meses escritos e resultados em faixas; procedência e relatos acompanham a variedade. Contrapôs entrada documental de cultivo à entrada por retratos/relatos. Georgia, fonte de sistema, marfim/carvão/azul. Mobile põe filtros antes de imagens; reserva distingue solicitação de confirmação. | Abriu cartilha de sementes e guia sazonal. Usou a relação região/época para estruturar dados, sem transferir recomendações de cultivo. Capturas falharam ou retornaram apenas referência textual; a direção foi declarada provisória. |
| Festival | “Partitura da cidade”: abertura em trilhas curatoriais desencontradas; programação com eixo temporal compartilhado, conflitos e “Minha visita”. Contrapôs rádio-revista sequencial à comparação de simultaneidades. Grotesca estreita, texto neutro, fundo claro/tinta/vermelho; retratos conservam diferenças. No celular, sequência por horário e vistas específicas de comparação/mapa. | Inspecionou visualmente uma página do programa oficial Nuits sonores, renderizada em PNG temporário; leu a programação Unsound Osaka como texto. Transferiu o eixo comum de horários, sem copiar textura ou verde da referência. |
| Indústria | “A superfície como evidência”: macro quase integral com margem documental; seleção correlaciona desenho, região, imagem e documento da mesma amostra; comparação técnica vem depois. Contrapôs filme da máquina seguido de catálogo à correlação de evidências. Títulos estreitos, numerais tabulares, mineral/grafite/âmbar. Mobile usa sequência de representações e comparação de dois modelos. | Inspecionou visualmente duas páginas de nota técnica ZEISS, renderizadas em PNG; leu páginas oficiais de serviços e submissão de componentes. Transferiu relações entre representações, condições e escalas, sem atribuir capacidades ZEISS à fabricante hipotética. |

### Fontes e rastreabilidade dos ensaios revisados

| Ensaio | Fonte aberta | Evidência usada |
| --- | --- | --- |
| Sementes | [Cartilha Casa da Semente, 2022](https://ciorganicos.com.br/wp-content/uploads/2017/10/cartilha-sementes-crioulos-2022-Publicacao-22.pdf) | Leitura textual da página impressa 3: ficha de variedade e dados por região/época. A tentativa de captura retornou 403; não houve inspeção visual. |
| Sementes | [Guia sazonal Real Seeds](https://realseeds.co.uk/summersowing.pdf) e [página principal](https://realseeds.co.uk/) | Leitura de seleção por época e de notas/calendários de cultivo. A captura do PDF retornou referência textual, sem imagem utilizável. Outro PDF, de Sementes Crioulas — Caém, excedeu o limite de abertura com 16.697.085 bytes; não foi contado como fonte inspecionada. |
| Festival | [Programa oficial Nuits sonores 2025](https://nuits-sonores.com/wp-content/uploads/2025/05/Timetable-Nuits-sonores-2025-en-un-clin-doeil_01.pdf) | Página 1 inspecionada visualmente em PNG: horas compartilhadas e colunas por palco tornam simultaneidades comparáveis. |
| Festival | [Unsound Osaka — programação](https://unsound.jp/events/september-6-creative-center/) | Texto extraído de programação por palco e acesso a mapa/participação; aparência não observada. Awwwards retornou timeout. |
| Indústria | [ZEISS — nota técnica de correlação, agosto de 2017](https://asset-downloads.zeiss.com/catalogs/download/mic/27cf2242-faf4-4d4b-94a6-3d2b0ad672f7/EN_wp_Smartzoom-SEM-correlation.pdf) | Páginas 3–4 inspecionadas visualmente em PNG: macros, legendas, escalas e representações da mesma PCB sob condições diferentes. Fonte de relações documentais, não de recomendações tecnológicas atuais. |
| Indústria | [ZEISS — medição óptica](https://www.zeiss.com/metrology/en/services/zeiss-measurement-services/optical-measurement-services.html) e [serviços de metrologia](https://www.zeiss.com/metrology/us/services/zeiss-measurement-services.html) | Leitura textual de aplicações, CAD/documentação e apresentação de componentes/desenhos para avaliação; aparência e comportamento não inspecionados. |

Os três agentes usaram comandos locais de leitura e ferramentas de busca/abertura web. Festival e indústria recorreram a Python/urllib/PyMuPDF e `view_image` para observar PDFs quando a ferramenta de screenshot não forneceu imagem utilizável. Os artefatos foram produzidos fora do repositório. Nenhum dos três implementou um site ou alterou a skill.

### Comparação e limites

Pesquisa externa passou de **0/3 para 3/3** ensaios; **2/3** obtiveram observação visual de referências, e o terceiro declarou evidência textual. Os três contrastaram alternativas e decidiram sem pedir ao usuário uma votação.

As propostas diferem na organização: seleção agrícola ligada ao calendário e à procedência; descoberta cultural associada à simultaneidade e à visita; investigação técnica por correlação de representações e comparação documentada. Isso vai além de trocar o objeto focal. Entretanto, sementes e indústria mantiveram ideias próximas de suas respostas anteriores, e os três conceitos revisados ainda usam base clara, tinta escura e acento. Festival e indústria também propõem títulos estreitos. A pesquisa melhorou a fundamentação; não demonstrou, por si só, uma transformação estética consistente nem eliminou todos os hábitos dos modelos.

Uma avaliação independente dos três conceitos, sem acesso à skill, à auditoria ou aos outros agentes, confirmou diferenças de intenção estrutural e adequação às tarefas. Ressalvou que trilhas desencontradas podem dificultar leitura no festival, e que a macro dominante pode atrasar a consulta técnica na indústria. Também identificou aproximação potencial entre suas bases claras e títulos estreitos. Seu parecer distingue diversidade de intenção de diversidade visual executada; essas ressalvas não foram transformadas em proibições gerais na skill.

O conjunto é exploratório: uma execução por brief/versão, com materiais hipotéticos e sem controle estatístico de variação entre agentes. Os pedidos de projeto foram idênticos; os invólucros de avaliação solicitaram leitura restrita e relato de ferramentas, com diferenças de redação. Não se deve atribuir todo resultado exclusivamente à mudança da skill. Nenhum conceito foi renderizado; não há medição de qualidade visual, acessibilidade, performance ou fidelidade aos assets reais. A família/versão exata do modelo não foi capturada; não houve execução em Claude.

### Controles de escopo e autorização

Um agente independente executou os três pedidos abaixo sem consultar auditoria, README, histórico ou resultados dos outros ensaios.

| Controle e pedido | Resultado executado |
| --- | --- |
| Edição estreita: “Ajustar apenas o padding de `.action` para 16px em telas até 600px; preservar desktop e demais propriedades.” Fixture temporária com HTML e CSS fora do repositório. | Alterou somente o valor mobile de 12px para 16px. Asserts do agente e verificação independente do integrador confirmaram um único byte alterado, regra desktop intacta e nenhum arquivo extra na fixture. Sem pesquisa ou redesign; CSS não foi renderizado. |
| Conceito de arquivo comunitário de histórias orais com acesso à rede indisponível neste ensaio e nenhum material anexado. | A restrição de rede foi simulada pelo protocolo; nenhuma ferramenta de rede foi usada. Propôs provisoriamente um índice textual e contrastou um atlas dependente de metadados ainda desconhecidos. Não inventou fontes consultadas nem criou arquivos. |
| Exposição tipográfica com brutalismo explicitamente solicitado: papel, preto, verde ácido, títulos pesados e formas duras; sem pesquisa externa neste ensaio. | Preservou a direção pedida, com composição tipográfica e navegação acessível propostas. Declarou a falta de materiais e de verificações; não substituiu o estilo por uma preferência da skill. Nenhum arquivo criado. |

Os dois controles conceituais verificam decisões relatadas, não acessibilidade implementada ou falhas reais de infraestrutura. O controle de CSS verifica limite de edição; não substitui teste visual de breakpoints.

## Antes/depois de contexto e revisão

Métricas reproduzidas com `git show 8e8033c:<arquivo>` e leitura UTF-8 dos arquivos atuais. Palavras usam separação por whitespace, equivalente a `\S+`; bytes usam o conteúdo bruto. Não há tokenizador instalado identificado para esta medição, portanto os valores não são chamados de tokens.

| Conjunto | Palavras antes → depois | Bytes antes → depois | Interpretação |
| --- | ---: | ---: | --- |
| Entrada | 1.153 → 870 | 8.891 → 6.593 | −24,5% de palavras; fluxo mais curto e explícito. |
| Entrada + identidade + pesquisa | 3.194 → 2.165 | 23.991 → 15.982 | −32,2% de palavras no mesmo percurso de três arquivos; o catálogo deixou de vir junto com o método. |
| Entrada + todas as referências | 6.992 → 6.254 | 51.261 → 46.565 | −10,6% de palavras, incluindo o novo catálogo condicional. |
| Pacote sem este registro de avaliação | 7.729 → 7.137 | 58.418 → 54.247 | README/metadata incluídos; −7,7% de palavras. O registro de avaliação acrescenta documentação fora do contexto normal. |

A entrada perdeu o perfil de nove campos e a enumeração de efeitos; contexto e limites permanecem, com formação da direção detalhada no guia de identidade. O exemplo costeiro foi removido para reduzir ancoragem. O catálogo passou a carregar somente quando seu mecanismo for pertinente, preservando os sete repositórios e alertas sobre dependências, APIs privadas, licença, input e falhas. Auditoria mantém disposições e prioridade; avaliação recebe comparação e transferibilidade; SLOP mantém sinais sem repetir uma revisão inteira. O guia de motion preservou todo o conteúdo técnico, alterando somente a referência ao nome do fluxo. README e metadata foram alinhados e os banners de antes/depois foram retirados.

Verificações executadas: `quick_validate.py` passou; validação UTF-8, frontmatter e metadata de invocação passou; 43 links/âncoras internos passaram; os sete repositórios GitHub foram conferidos como preservados; comparação do guia de motion confirmou apenas a troca de terminologia; `git diff --check` passou. Uma revisão independente do diff e dos guias conectados não encontrou regressão material. A revisão não equivale a execução da skill em Claude ou a construção de sites reais.

## Fontes de orientação consultadas

As fontes abaixo foram abertas durante a auditoria. Sustentam carregamento progressivo, instruções concisas, liberdade proporcional à tarefa e avaliação por execução; não certificam a qualidade desta skill.

| Fonte primária | Uso nesta evolução |
| --- | --- |
| [Agent Skills — Specification](https://agentskills.io/specification) | Contrato do pacote, frontmatter e referências sob demanda. |
| [Agent Skills — Best practices](https://agentskills.io/skill-creation/best-practices) | Contexto útil, concisão e refinamento com execução real. |
| [Agent Skills — Evaluating skill output quality](https://agentskills.io/skill-creation/evaluating-skills) | Briefs realistas, comparação com baseline e limites da avaliação. |
| [Claude — Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) | Liberdade de decisão, carregamento progressivo e necessidade de testar os modelos efetivamente utilizados. |
| [OpenAI — Build skills](https://learn.chatgpt.com/docs/build-skills.md) | Estrutura portável, descoberta e carregamento progressivo no Codex. |

Awwwards retornou timeout e a página inicial de Codrops retornou 403 na ferramenta web durante a auditoria; repositórios GitHub de exemplos permaneceram acessíveis. Esses resultados de acesso não foram tratados como inspeção visual das galerias.
