| Tag | Competência esperada                             |
| --- | ------------------------------------------------ |
| [B] | Explicar e reconhecer                            |
| [I] | Implementar, interpretar e comparar              |
| [A] | Analisar mecanismos, limitações e trade-offs     |
| [P] | Demonstrar em um sistema reproduzível e operável |

### 2. Fundamentos e interfaces
### Formulação do problema

- [ ] [B] Diferenciar chatbot, assistente, copiloto, workflow e agente.

- [ ] [I] Identificar a tarefa real, não apenas a interface conversacional.

- [ ] [I] Definir usuários, entradas, saídas e critérios de sucesso.

- [ ] [I] Identificar quando usar regras, busca, SQL ou ML clássico em vez de LLM.

- [ ] [I] Distinguir geração, extração, classificação, transformação e execução de ações.

- [ ] [I] Definir tolerância a erros e necessidade de revisão humana.

- [ ] [I] Definir requisitos de latência, disponibilidade, privacidade e custo.

- [ ] [A] Identificar riscos de automatizar decisões ou ações incorretas.

- [ ] [P] Criar um baseline sem LLM quando viável.

- [ ] [P] Documentar o problema e os critérios de aceitação antes da implementação.

### Fundamentos de LLMs

- [ ] [B] Explicar geração autoregressiva e previsão de tokens.

- [ ] [B] Diferenciar modelo base e modelo ajustado para instruções.

- [ ] [I] Diferenciar pré-treinamento, continued pretraining e fine-tuning.

- [ ] [I] Conhecer supervised fine-tuning e treinamento por preferências.

- [ ] [I] Diferenciar conhecimento nos pesos de informação fornecida em contexto.

- [ ] [I] Diferenciar modelos de geração, embedding e reranking.

- [ ] [I] Diferenciar modelos textuais e multimodais.

- [ ] [I] Entender limitações de factualidade, atualização e consistência.

- [ ] [A] Distinguir fluência linguística de correção verificável.

- [ ] [A] Investigar sensibilidade a idioma, domínio e formato da tarefa.

- [ ] [P] Avaliar capacidades no problema concreto em vez de depender apenas de benchmarks públicos.

### Seleção de modelos

- [ ] [I] Comparar modelos por qualidade na tarefa.

- [ ] [I] Comparar custo de entrada, saída e infraestrutura.

- [ ] [I] Comparar latência, throughput e limites de uso.

- [ ] [I] Verificar suporte a contexto longo, ferramentas e saídas estruturadas.

- [ ] [I] Verificar modalidades e idiomas suportados.

- [ ] [I] Diferenciar modelos proprietários, de pesos abertos e efetivamente open source.

- [ ] [A] Avaliar dependência de fornecedor e portabilidade.

- [ ] [A] Avaliar licenciamento, hospedagem e restrições de uso.

- [ ] [P] Criar uma matriz de seleção baseada em avaliações próprias.

- [ ] [P] Registrar versão e configuração do modelo escolhido.

### Tokens e tokenização

- [ ] [B] Diferenciar caracteres, palavras, tokens e subwords.

- [ ] [I] Conhecer BPE, WordPiece e tokenização Unigram.

- [ ] [I] Identificar tokens especiais e formatos de conversação.

- [ ] [I] Contar tokens com o tokenizador correto.

- [ ] [I] Diferenciar orçamento de entrada e de saída.

- [ ] [I] Contabilizar mensagens, documentos e definições de ferramentas.

- [ ] [I] Avaliar tokenização de português, código e dados estruturados.

- [ ] [A] Investigar truncamento e seus efeitos.

- [ ] [P] Implementar limites e políticas explícitas para entradas grandes.

- [ ] [P] Registrar uso real de tokens por tarefa.

### Consumo de APIs e SDKs

- [ ] [I] Autenticar chamadas sem expor segredos.

- [ ] [I] Trabalhar com mensagens e papéis suportados pelo provedor.

- [ ] [I] Usar chamadas síncronas, assíncronas e streaming.

- [ ] [I] Interpretar finish reasons, erros e consumo de tokens.

- [ ] [I] Configurar timeouts e cancelamento.

- [ ] [I] Tratar rate limits e indisponibilidade.

- [ ] [A] Implementar retries com backoff e jitter.

- [ ] [A] Evitar retries que dupliquem ações externas.

- [ ] [P] Criar uma camada de adaptação entre a aplicação e os provedores.

- [ ] [P] Testar troca de fornecedor sem presumir comportamento equivalente.

- [ ] [P] Distinguir resposta incompleta de resposta válida.

### Geração e parâmetros de inferência

- [ ] [I] Entender temperature, top-p e limites de saída.

- [ ] [I] Diferenciar configurações para extração e geração criativa.

- [ ] [I] Trabalhar com sequências de parada quando suportadas.

- [ ] [A] Investigar variabilidade entre execuções.

- [ ] [A] Não tratar temperature zero como garantia universal de determinismo.

- [ ] [P] Definir configurações por tarefa e avaliá-las.

- [ ] [P] Registrar parâmetros junto dos resultados.

### Prompt engineering

- [ ] [B] Construir instruções claras e contextualizadas.

- [ ] [I] Usar zero-shot e few-shot prompting.

- [ ] [I] Selecionar exemplos representativos, incluindo casos difíceis.

- [ ] [I] Separar instruções, dados e formato de saída.

- [ ] [I] Usar delimitadores e estrutura consistente.

- [ ] [I] Explicitar critérios de resposta e condições de abstinência.

- [ ] [I] Decompor tarefas complexas quando isso melhorar os resultados.

- [ ] [A] Investigar sensibilidade à ordem e formulação dos exemplos.

- [ ] [A] Evitar depender de supostas “palavras mágicas”.

- [ ] [P] Versionar prompts.

- [ ] [P] Manter testes de regressão.

- [ ] [P] Avaliar alterações antes de colocá-las em produção.

### Saídas estruturadas

- [ ] [I] Definir schemas para respostas.

- [ ] [I] Usar JSON Schema e validação com ferramentas como Pydantic.

- [ ] [I] Diferenciar JSON sintaticamente válido de dados semanticamente corretos.

- [ ] [I] Definir campos obrigatórios, enums e limites.

- [ ] [I] Tratar recusas, campos ausentes e saídas interrompidas.

- [ ] [A] Comparar geração restringida, validação posterior e reparo.

- [ ] [P] Validar a resposta antes de executar lógica de negócio.

- [ ] [P] Limitar ciclos de correção.

- [ ] [P] Testar casos adversos e valores inesperados.

### Engenharia de contexto

O contexto deve ser selecionado e mantido segundo sua utilidade; simplesmente preencher a janela não é o objetivo. A engenharia de contexto inclui seleção, carregamento sob demanda e compactação.

- [ ] [I] Definir o que entra no contexto de cada chamada.

- [ ] [I] Priorizar instruções, tarefa, evidências e estado necessário.

- [ ] [I] Separar informações confiáveis de conteúdo externo.

- [ ] [I] Gerenciar histórico por relevância, não apenas por recência.

- [ ] [I] Usar resumos e compactação.

- [ ] [A] Investigar perda de informação durante a compactação.

- [ ] [A] Avaliar posição, redundância e conflito entre informações.

- [ ] [A] Comparar contexto longo com recuperação seletiva.

- [ ] [P] Criar políticas de orçamento de tokens.

- [ ] [P] Preservar fatos críticos e identificadores ao resumir.

- [ ] [P] Carregar dados sob demanda quando apropriado.

### Memória e estado

- [ ] [I] Diferenciar histórico, estado operacional e memória persistente.

- [ ] [I] Diferenciar memória por sessão e por usuário.

- [ ] [I] Armazenar preferências com origem e data.

- [ ] [A] Definir políticas de atualização, expiração e esquecimento.

- [ ] [A] Resolver informações contraditórias.

- [ ] [A] Não tratar resumos gerados como fonte infalível.

- [ ] [P] Permitir correção e exclusão.

- [ ] [P] Isolar memória entre usuários e organizações.

- [ ] [P] Avaliar recuperação de memória separadamente da geração.

### 3. Dados, busca e RAG
### Representações e embeddings

- [ ] [B] Explicar representações vetoriais densas e esparsas.

- [ ] [I] Diferenciar embeddings de tokens, sentenças, documentos e modalidades.

- [ ] [I] Usar embeddings para busca, agrupamento e classificação.

- [ ] [I] Comparar cosine similarity, produto interno e distância euclidiana.

- [ ] [I] Entender o efeito da normalização dos vetores.

- [ ] [A] Distinguir proximidade semântica de verdade, relevância ou autorização.

- [ ] [A] Investigar efeitos de idioma, domínio e comprimento.

- [ ] [A] Entender modelos com representações distintas para consulta e documento.

- [ ] [P] Avaliar embeddings com consultas representativas.

- [ ] [P] Versionar modelo, dimensão, normalização e configuração.

### Modelos de embedding

- [ ] [I] Integrar modelos por API, incluindo OpenAI.

- [ ] [I] Executar modelos locais disponíveis no ecossistema Hugging Face.

- [ ] [I] Usar bibliotecas como Sentence Transformers.

- [ ] [I] Respeitar limites de entrada e instruções específicas do modelo.

- [ ] [I] Processar embeddings em lotes.

- [ ] [A] Comparar embeddings gerais, especializados e multilíngues.

- [ ] [A] Conhecer modelos sparse e multi-vector.

- [ ] [P] Medir custo, latência e qualidade de recuperação.

- [ ] [P] Não misturar vetores de espaços incompatíveis.

- [ ] [P] Planejar reindexação quando o modelo mudar.

### Ingestão e parsing

- [ ] [I] Ler PDF, HTML, Markdown, DOCX e formatos estruturados.

- [ ] [I] Diferenciar PDF textual e documento digitalizado.

- [ ] [I] Aplicar OCR quando necessário.

- [ ] [I] Preservar títulos, seções, tabelas e listas.

- [ ] [I] Remover ruído sem apagar informação relevante.

- [ ] [I] Extrair metadados de origem, data, versão e permissões.

- [ ] [A] Investigar erros de ordem de leitura.

- [ ] [A] Tratar documentos com imagens e layout complexo.

- [ ] [P] Manter rastreabilidade até o documento original.

- [ ] [P] Implementar validação da extração.

- [ ] [P] Quarentenar arquivos inválidos ou suspeitos.

### Chunking

- [ ] [I] Comparar divisão por caracteres, tokens e estrutura documental.

- [ ] [I] Implementar divisão recursiva.

- [ ] [I] Definir tamanho e sobreposição.

- [ ] [I] Preservar títulos e contexto local.

- [ ] [A] Comparar chunking semântico e estrutural.

- [ ] [A] Construir relações parent–child.

- [ ] [A] Tratar tabelas, código e seções que não podem ser separadas arbitrariamente.

- [ ] [P] Avaliar chunking pela qualidade de recuperação e resposta.

- [ ] [P] Evitar escolha de tamanho sem experimento.

- [ ] [P] Registrar a estratégia junto da versão do índice.

### Fundamentos de informação e busca

- [ ] [I] Diferenciar busca lexical e semântica.

- [ ] [I] Entender índices invertidos e BM25.

- [ ] [I] Entender busca exata e aproximada por vizinhos.

- [ ] [A] Estudar HNSW, IVF e quantização de vetores.

- [ ] [A] Comparar recall, latência, memória e custo de construção.

- [ ] [A] Investigar impacto dos filtros na recuperação.

- [ ] [P] Medir qualidade com consultas e relevâncias de referência.

- [ ] [P] Evitar avaliar o mecanismo apenas com exemplos escolhidos manualmente.

### Bancos e índices vetoriais

- [ ] [I] Diferenciar biblioteca de índice vetorial e banco vetorial.

- [ ] [I] Criar coleções, schemas e índices.

- [ ] [I] Implementar upsert, busca, atualização e exclusão.

- [ ] [I] Trabalhar com IDs estáveis e metadados.

- [ ] [I] Aplicar filtros por usuário, organização e documento.

- [ ] [A] Avaliar consistência, durabilidade e atualização.

- [ ] [A] Planejar particionamento, replicação e backup.

- [ ] [P] Integrar uma opção como Milvus, Pinecone ou MongoDB Atlas Vector Search.

- [ ] [P] Comparar alternativas como PostgreSQL com pgvector.

- [ ] [P] Conhecer FAISS como opção de indexação, sem confundi-lo com um banco completo.

- [ ] [P] Selecionar tecnologia por requisitos, não por popularidade.

### Ciclo de vida dos documentos

- [ ] [I] Identificar documentos novos, alterados e removidos.

- [ ] [I] Usar hashes e IDs para evitar duplicação.

- [ ] [I] Atualizar índices incrementalmente.

- [ ] [A] Propagar exclusão para chunks, vetores, caches e artefatos derivados.

- [ ] [A] Gerenciar versões e datas de validade.

- [ ] [P] Implementar reprocessamento idempotente.

- [ ] [P] Monitorar atraso entre origem e índice.

- [ ] [P] Testar migrações de esquema e reindexação.

### RAG básico

O fluxo central é recuperar evidências, acrescentá-las ao contexto e gerar uma resposta; avaliar a recuperação e verificar as citações são partes do sistema, não etapas opcionais.

- [ ] [B] Explicar retrieval, augmentation e generation.

- [ ] [I] Construir um pipeline RAG mínimo.

- [ ] [I] Definir consultas, número de resultados e orçamento de contexto.

- [ ] [I] Inserir documentos com identificadores de origem.

- [ ] [I] Orientar respostas fundamentadas nas evidências.

- [ ] [I] Definir comportamento quando não há evidência suficiente.

- [ ] [P] Retornar citações verificáveis.

- [ ] [P] Separar falhas de recuperação e falhas de geração.

- [ ] [P] Comparar com busca simples e com uso direto do modelo.

### Recuperação avançada

- [ ] [I] Implementar busca híbrida.

- [ ] [I] Combinar resultados com métodos como reciprocal rank fusion.

- [ ] [I] Aplicar reranking.

- [ ] [A] Comparar rerankers cross-encoder e alternativas.

- [ ] [A] Usar query rewriting em perguntas conversacionais.

- [ ] [A] Implementar decomposição de consultas.

- [ ] [A] Avaliar multi-query retrieval e expansão de consultas.

- [ ] [A] Conhecer HyDE e seus riscos.

- [ ] [A] Recuperar vizinhos e contexto de chunks.

- [ ] [A] Aplicar diversificação de resultados.

- [ ] [P] Medir o ganho de cada etapa por ablação.

- [ ] [P] Avaliar custo e latência adicionais.

### Montagem do contexto e resposta

- [ ] [I] Deduplicar evidências recuperadas.

- [ ] [I] Ordenar e selecionar trechos sob orçamento de tokens.

- [ ] [I] Preservar relação entre evidência e origem.

- [ ] [I] Diferenciar citação existente de citação que realmente sustenta a afirmação.

- [ ] [A] Resolver versões conflitantes e fontes desatualizadas.

- [ ] [A] Avaliar extração direta versus síntese.

- [ ] [A] Usar compressão contextual sem perder fatos críticos.

- [ ] [P] Verificar afirmações importantes contra as evidências.

- [ ] [P] Evitar inventar fonte, página ou trecho.

- [ ] [P] Explicitar insuficiência ou conflito de informações.

### RAG especializado

- [ ] [A] Estudar hierarchical retrieval.

- [ ] [A] Estudar GraphRAG e recuperação por relações.

- [ ] [A] Estudar recuperação multimodal.

- [ ] [A] Estudar recuperação iterativa ou agentic retrieval.

- [ ] [A] Estudar busca federada em fontes diferentes.

- [ ] [A] Integrar dados estruturados e documentos.

- [ ] [P] Comparar cada estratégia com RAG simples.

- [ ] [P] Justificar o ganho antes de aumentar a complexidade.

### Dados estruturados e text-to-SQL

- [ ] [I] Fornecer schema e significado das tabelas.

- [ ] [I] Diferenciar geração de SQL e execução de SQL.

- [ ] [I] Validar sintaxe, tabelas e colunas.

- [ ] [A] Restringir consultas por permissões e políticas.

- [ ] [A] Controlar custo, tempo e quantidade de resultados.

- [ ] [P] Usar acesso somente leitura quando suficiente.

- [ ] [P] Executar em ambiente controlado.

- [ ] [P] Verificar se a consulta responde à pergunta real.

- [ ] [P] Separar erro de consulta de erro de interpretação do resultado.

### 4. Ferramentas, agentes e adaptação
### Tool calling

- [ ] [B] Diferenciar gerar texto e solicitar execução de ferramenta.

- [ ] [I] Definir nome, descrição, argumentos e schema.

- [ ] [I] Validar argumentos antes da execução.

- [ ] [I] Retornar resultados estruturados.

- [ ] [I] Tratar erro, timeout e resultado vazio.

- [ ] [A] Projetar ferramentas com responsabilidade bem delimitada.

- [ ] [A] Evitar respostas excessivas que consumam o contexto.

- [ ] [P] Testar seleção correta da ferramenta.

- [ ] [P] Separar ferramentas de leitura e escrita.

- [ ] [P] Exigir autorização antes de ações sensíveis.

A qualidade das ferramentas depende tanto da implementação quanto de descrições, contratos e resultados úteis. Paginação, filtros e limites de resposta ajudam a controlar o contexto consumido.

### Workflows determinísticos

- [ ] [I] Implementar encadeamento de etapas.

- [ ] [I] Implementar roteamento por tarefa.

- [ ] [I] Implementar execução paralela quando apropriada.

- [ ] [I] Separar etapas determinísticas de decisões do modelo.

- [ ] [A] Modelar estados, transições e condições de parada.

- [ ] [A] Implementar validação e revisão de resultados.

- [ ] [P] Persistir estado para retomada.

- [ ] [P] Garantir idempotência de etapas repetíveis.

- [ ] [P] Preferir fluxo previsível quando ele resolve o problema.

### Agentes

- [ ] [B] Explicar o ciclo observar, decidir, agir e verificar.

- [ ] [I] Construir um agente com poucas ferramentas.

- [ ] [I] Diferenciar decisão do modelo e autorização do sistema.

- [ ] [I] Definir orçamento de passos, tokens, tempo e custo.

- [ ] [I] Definir critérios verificáveis de conclusão.

- [ ] [A] Investigar loops, repetição e deriva de objetivo.

- [ ] [A] Avaliar planejamento e replanning.

- [ ] [A] Avaliar necessidade de autonomia em cada tarefa.

- [ ] [P] Observar resultados reais das ferramentas.

- [ ] [P] Permitir cancelamento e intervenção humana.

- [ ] [P] Testar falhas durante a execução.

A recomendação de começar simples é importante: arquiteturas agentic devem ser adicionadas quando prompts ou workflows mais simples não resolvem a tarefa, e não como escolha automática.

### Sistemas multiagentes

- [ ] [A] Diferenciar especialização útil de divisão artificial.

- [ ] [A] Definir responsabilidades, contratos e limites por agente.

- [ ] [A] Modelar coordenação e compartilhamento de estado.

- [ ] [A] Investigar duplicação de trabalho e mensagens contraditórias.

- [ ] [A] Controlar permissões de cada agente.

- [ ] [P] Medir custo e latência totais.

- [ ] [P] Comparar com agente único e workflow.

- [ ] [P] Evitar tratar consenso entre agentes como garantia de verdade.

### Protocolos e interoperabilidade

- [ ] [I] Entender contratos entre clientes, servidores e ferramentas.

- [ ] [I] Conhecer MCP para integração de ferramentas e recursos.

- [ ] [I] Diferenciar descoberta de capacidade e autorização de acesso.

- [ ] [A] Investigar identidade, transporte e fronteiras de confiança.

- [ ] [A] Versionar schemas e preservar compatibilidade.

- [ ] [P] Validar servidores e ferramentas antes de disponibilizá-los.

- [ ] [P] Não presumir que um protocolo elimina riscos de segurança.

### Frameworks e orquestração

- [ ] [I] Implementar um fluxo sem framework para compreender os componentes.

- [ ] [I] Conhecer ferramentas como LangChain, LangGraph ou LlamaIndex.

- [ ] [I] Diferenciar abstrações de retrieval, estado e execução.

- [ ] [A] Avaliar dependências e comportamento oculto.

- [ ] [A] Investigar retries e persistência implementados pelo framework.

- [ ] [P] Inspecionar prompts e chamadas efetivamente executados.

- [ ] [P] Evitar acoplamento desnecessário.

- [ ] [P] Selecionar framework apenas quando seus benefícios justificarem o custo.

### Adaptação do modelo

- [ ] [I] Diferenciar prompting, RAG, fine-tuning e treinamento do zero.

- [ ] [I] Escolher adaptação conforme a origem da falha.

- [ ] [I] Construir dados de treinamento consistentes.

- [ ] [A] Diferenciar ajuste de comportamento e atualização de conhecimento.

- [ ] [A] Conhecer SFT, LoRA e treinamento por preferências.

- [ ] [A] Investigar contaminação entre treino e avaliação.

- [ ] [P] Avaliar o modelo antes e depois da adaptação.

- [ ] [P] Manter capacidades gerais que ainda são necessárias.

- [ ] [P] Aprofundar implementação e otimização no checklist de Deep Learning.

### Inferência própria

- [ ] [I] Diferenciar API gerenciada e hospedagem própria.

- [ ] [I] Estimar memória de pesos e KV cache.

- [ ] [I] Entender prefill e decoding.

- [ ] [A] Estudar batching e continuous batching.

- [ ] [A] Estudar prefix caching.

- [ ] [A] Conhecer quantização e speculative decoding.

- [ ] [A] Conhecer paralelismo para inferência.

- [ ] [P] Avaliar runtimes como vLLM ou alternativas compatíveis.

- [ ] [P] Medir throughput, tempo até o primeiro token e latência total.

- [ ] [P] Comparar custo total com serviço gerenciado.

### Sistemas multimodais

- [ ] [I] Integrar texto, imagem, áudio e documentos.

- [ ] [I] Definir pré-processamento por modalidade.

- [ ] [I] Preservar sincronização e origem das informações.

- [ ] [A] Avaliar OCR versus compreensão visual direta.

- [ ] [A] Avaliar recuperação multimodal.

- [ ] [P] Testar ausência, corrupção e conflito entre modalidades.

- [ ] [P] Validar grounding de respostas em elementos visuais ou sonoros.

### 5. Avaliação, segurança e produção
### Arquitetura da aplicação

- [ ] [I] Separar interface, regras de negócio, modelos e acesso a dados.

- [ ] [I] Definir contratos entre componentes.

- [ ] [I] Modelar fluxo de dados e fronteiras de confiança.

- [ ] [I] Identificar componentes com estado.

- [ ] [A] Escolher processamento síncrono, assíncrono ou por filas.

- [ ] [A] Planejar tarefas longas e retomada.

- [ ] [P] Produzir diagramas de componentes e sequências.

- [ ] [P] Registrar decisões arquiteturais e alternativas rejeitadas.

- [ ] [P] Evitar transformar todo componente em microserviço sem necessidade.

### Avaliação end-to-end

- [ ] [I] Construir um conjunto representativo de tarefas.

- [ ] [I] Incluir casos comuns, difíceis, ambíguos e sem resposta.

- [ ] [I] Definir critérios objetivos por tarefa.

- [ ] [I] Avaliar qualidade, custo e latência juntos.

- [ ] [A] Separar métricas automáticas e julgamento humano.

- [ ] [A] Investigar variabilidade entre execuções.

- [ ] [P] Versionar datasets e rubricas de avaliação.

- [ ] [P] Executar testes de regressão antes de mudanças.

- [ ] [P] Avaliar o sistema completo, não apenas a resposta do modelo isolado.

### Avaliação de RAG

- [ ] [I] Medir recall@k, precision@k e métricas de ranking apropriadas.

- [ ] [I] Verificar se a evidência necessária foi recuperada.

- [ ] [I] Avaliar relevância e suficiência do contexto.

- [ ] [I] Avaliar correção e completude da resposta.

- [ ] [I] Avaliar fidelidade às fontes.

- [ ] [I] Avaliar suporte das citações.

- [ ] [A] Distinguir falha de parsing, indexação, retrieval e geração.

- [ ] [P] Fazer ablações de chunking, embeddings, busca e reranking.

- [ ] [P] Medir desempenho em perguntas sem evidência disponível.

### LLM-as-a-judge

- [ ] [I] Construir rubricas explícitas para avaliadores.

- [ ] [I] Comparar avaliação absoluta e pareada.

- [ ] [A] Investigar viés de posição, estilo e extensão.

- [ ] [A] Comparar julgamentos com anotadores humanos.

- [ ] [A] Evitar usar julgamento automático como verdade definitiva.

- [ ] [P] Versionar modelo avaliador e prompt.

- [ ] [P] Auditar amostras de discordância.

- [ ] [P] Separar avaliador de critérios determinísticos verificáveis.

### Avaliação de agentes

- [ ] [I] Medir conclusão real da tarefa.

- [ ] [I] Avaliar escolha de ferramentas e argumentos.

- [ ] [I] Avaliar sequência de ações e respeito a permissões.

- [ ] [A] Investigar loops e ações desnecessárias.

- [ ] [A] Avaliar recuperação após erros externos.

- [ ] [P] Usar ambientes de teste sem efeitos reais.

- [ ] [P] Medir custo por tarefa concluída com sucesso.

- [ ] [P] Testar cancelamento, retomada e intervenção humana.

### Segurança de LLMs

Os riscos não se limitam a respostas incorretas. A OWASP destaca classes como prompt injection, exposição de informações, agência excessiva e tratamento inadequado das saídas.

- [ ] [B] Explicar prompt injection direta e indireta.

- [ ] [I] Tratar documentos e resultados de ferramentas como conteúdo não confiável.

- [ ] [I] Separar instruções do sistema de dados externos.

- [ ] [I] Aplicar privilégio mínimo.

- [ ] [I] Validar saídas antes de usá-las em código, HTML, SQL ou comandos.

- [ ] [A] Investigar exfiltração por ferramentas e URLs.

- [ ] [A] Investigar envenenamento de documentos e memória.

- [ ] [A] Investigar riscos de dependências, modelos e servidores externos.

- [ ] [P] Não armazenar segredos no prompt como mecanismo de proteção.

- [ ] [P] Controlar acesso fora do modelo.

- [ ] [P] Construir testes adversariais e red teaming.

- [ ] [P] Implementar defesa em profundidade.

### Autorização e ações externas

- [ ] [I] Autenticar o usuário que solicita a ação.

- [ ] [I] Validar acesso ao recurso e ao escopo da ação.

- [ ] [I] Separar recomendação, preparação e execução.

- [ ] [A] Vincular aprovação ao alvo e conteúdo exatos.

- [ ] [A] Prevenir substituição do alvo depois da aprovação.

- [ ] [P] Exigir confirmação para ações sensíveis.

- [ ] [P] Implementar idempotência.

- [ ] [P] Registrar quem solicitou, aprovou e executou.

- [ ] [P] Definir compensação ou rollback quando possível.

### Privacidade e isolamento

- [ ] [I] Classificar informações pessoais e sensíveis.

- [ ] [I] Minimizar dados enviados a provedores.

- [ ] [I] Avaliar retenção e políticas contratuais.

- [ ] [A] Aplicar isolamento por usuário e organização.

- [ ] [A] Garantir permissões durante retrieval, não apenas após a resposta.

- [ ] [P] Testar vazamento entre tenants.

- [ ] [P] Sanitizar logs e traces.

- [ ] [P] Propagar correção e exclusão para artefatos derivados.

- [ ] [P] Avaliar requisitos de LGPD com apoio jurídico quando necessário.

### Confiabilidade

- [ ] [I] Definir timeouts e budgets por etapa.

- [ ] [I] Implementar circuit breakers e limites de concorrência.

- [ ] [I] Definir fallback por tipo de falha.

- [ ] [A] Evitar trocar silenciosamente para um modelo incapaz da tarefa.

- [ ] [A] Distinguir degradação aceitável de resposta insegura.

- [ ] [P] Testar indisponibilidade de modelo, banco e ferramenta.

- [ ] [P] Implementar cancelamento de tarefas.

- [ ] [P] Evitar duplicação de ações em retries.

- [ ] [P] Definir comportamento seguro quando dependências falham.

### Observabilidade

- [ ] [I] Registrar chamadas, duração e status.

- [ ] [I] Medir tokens e custos por etapa.

- [ ] [I] Registrar versão de modelo, prompt e índice.

- [ ] [I] Correlacionar uma tarefa com suas chamadas internas.

- [ ] [A] Inspecionar traces de retrieval e tool calling.

- [ ] [P] Proteger dados sensíveis nos registros.

- [ ] [P] Criar dashboards e alertas.

- [ ] [P] Registrar feedback e incidentes.

- [ ] [P] Permitir reprodução controlada de falhas.

### Otimização de custo e latência

- [ ] [I] Calcular custo por requisição e por tarefa bem-sucedida.

- [ ] [I] Medir latência de cada componente.

- [ ] [I] Reduzir chamadas e contexto desnecessários.

- [ ] [I] Usar caching com política de validade.

- [ ] [A] Avaliar cache exato e semântico.

- [ ] [A] Avaliar roteamento entre modelos de capacidades diferentes.

- [ ] [A] Paralelizar etapas independentes.

- [ ] [A] Investigar custos de retries e loops agentic.

- [ ] [P] Impor limites por usuário e organização.

- [ ] [P] Avaliar ganhos sem degradar segurança ou qualidade.

### Deploy e ciclo de vida

- [ ] [P] Versionar código, prompts, schemas e configurações.

- [ ] [P] Gerenciar segredos fora do código.

- [ ] [P] Criar ambientes separados de desenvolvimento, teste e produção.

- [ ] [P] Automatizar avaliações no CI/CD.

- [ ] [P] Usar rollout gradual quando adequado.

- [ ] [P] Planejar migração de modelos e índices.

- [ ] [P] Implementar rollback.

- [ ] [P] Monitorar mudanças de comportamento dos provedores.

- [ ] [P] Definir critérios de atualização e descontinuação.

### Governança e documentação

- [ ] [P] Documentar finalidade, usuários e limitações.

- [ ] [P] Registrar procedência e licença das fontes.

- [ ] [P] Definir responsáveis por incidentes.

- [ ] [P] Documentar critérios de aprovação de mudanças.

- [ ] [P] Manter inventário de modelos, provedores e dependências.

- [ ] [P] Definir supervisão humana.

- [ ] [P] Documentar riscos residuais.

- [ ] [P] Não apresentar o sistema como infalível ou autônomo além do que foi demonstrado.

Evidências de domínio

Para cada bloco, só considere domínio quando conseguir:

Explicar a decisão arquitetural sem depender do nome da ferramenta.

Implementar uma versão mínima funcional.

Comparar com uma alternativa mais simples.

Medir resultados e custos.

Mostrar um caso de falha.

Implementar uma mitigação.

Registrar limitações e trade-offs.