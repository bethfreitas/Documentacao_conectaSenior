# Ficha de Inscriçao

{% file src=".gitbook/assets/Ficha_Inscriçao_A3.pdf" %}

# Prompt 01 — Atualizar o preparativo para a banca sem perder o contexto

> **Uso:** copie o texto da seção **Prompt para copiar** e envie a qualquer IA junto com o arquivo `Preparativo_Banca_Apresentacao_Conecta_Senior.md` atualizado. Anexe, se houver, outros documentos oficiais do projeto.
>
> **Objetivo:** acrescentar novos tópicos, perguntas, respostas e argumentos para a banca **sem apagar, reescrever ou contradizer silenciosamente** o material existente.

## Prompt para copiar

```text
Você atuará como revisor e organizador da documentação de apresentação do projeto Conecta Sênior.

TAREFA
Atualize o arquivo Markdown "Preparativo_Banca_Apresentacao_Conecta_Senior.md" com novos preparativos para a banca, preservando integralmente as informações e a linha de raciocínio já documentadas.

CONTEXTO DO PROJETO
O Conecta Sênior é uma plataforma de empregabilidade voltada a profissionais com 60 anos ou mais e empresas. A proposta contempla perfis profissionais, vagas e candidaturas, acessibilidade e apoio de IA para tradução de experiências em competências, recomendações e preparação para entrevistas. A arquitetura proposta inclui React/Vite/Atomic Design, API Go, banco de dados e armazenamento KV. O uso de IA deve respeitar a autonomia do usuário, a LGPD, a inclusão e a supervisão humana. Para detalhes, prevalecem os documentos anexados, e não este resumo.

INSTRUÇÕES OBRIGATÓRIAS
1. Leia o Markdown atual por inteiro antes de acrescentar conteúdo. Ele é a fonte primária do estado da documentação.
2. Preserve títulos, numeração, ordem, informações, tabelas, exemplos, referências e afirmações existentes. Não apague, resuma, substitua ou reescreva trechos por conta própria.
3. Acrescente somente informações novas e úteis, evitando duplicações. Priorize uma seção claramente identificada, como "Novos preparativos para a banca — [tema]", ou novas subseções em local coerente, sem alterar o conteúdo anterior.
4. Antes de incorporar uma novidade, classifique-a como: (a) informação confirmada em documento fornecido, (b) proposta/hipótese a validar, ou (c) pergunta provável da banca com resposta sugerida.
5. Nunca apresente funcionalidades planejadas como já implementadas. Não invente resultados de testes, parcerias, números, decisões técnicas, cronogramas ou evidências.
6. Se surgir conflito com o documento existente, NÃO sobrescreva: crie o tópico "Pontos a validar ou decidir", explicando a divergência e sua origem.
7. Mantenha o padrão de linguagem do Conecta Sênior: português brasileiro, texto claro, seções organizadas, conteúdo direto, acessível e adequado à apresentação acadêmica.
8. Sempre que possível, proponha respostas objetivas para perguntas difíceis da banca: problema, evidências, público, diferenciais, riscos, IA, acessibilidade, LGPD, arquitetura, MVP e validação.
9. Cite a seção ou o documento de origem quando usar informações fornecidas. Não crie fontes bibliográficas ou links inexistentes.
10. Não divulgue informações pessoais, credenciais, tokens ou dados confidenciais contidos em possíveis anexos.

DADOS DE ENTRADA
- Markdown atual: [ANEXAR OU COLAR A VERSÃO MAIS RECENTE]
- Tema(s) ou dúvidas que quero acrescentar: [INFORMAR]
- Documentos adicionais, se houver: [ANEXAR OU INFORMAR "NENHUM"]

ENTREGA
A. Devolva o Markdown COMPLETO atualizado, em formato .md, preservando o texto anterior e acrescentando apenas o necessário.
B. Ao final do documento, acrescente uma seção "Histórico de atualizações do preparativo" com data informada, tema adicionado e descrição breve da alteração, sem apagar registros anteriores. Caso a data não tenha sido fornecida ou esteja indisponível, solicite-a; não invente.
C. Fora do arquivo, apresente um resumo sucinto do que foi adicionado e dos pontos que precisam de validação.
D. Se não conseguir acessar o arquivo original, NÃO reconstrua o documento de memória: solicite o arquivo atual.
```

## Como usar

1. Anexe a **última versão** de `Preparativo_Banca_Apresentacao_Conecta_Senior.md`.
2. Cole o prompt e informe a novidade desejada (por exemplo: “adicione perguntas sobre viés do matching de vagas e respostas para a banca”).
3. Confira o resumo das alterações, os itens a validar e o documento final antes de substituir a versão no Git.
4. Registre o uso no histórico de IA com o **Prompt 02**.

> **Importante:** o prompt estabelece um procedimento, mas não garante que uma IA tenha acesso a versões anteriores ou que cumpra todas as regras sem revisão humana. Faça o diff do PR antes de aprovar alterações.

---------------------------------------------------------------------------------------------------------------------------

# Prompt 02 — Registrar uso de IA e histórico para atualização do projeto

> **Uso:** envie este prompt ao final de **cada sessão de trabalho com uma IA**. Ele solicita informações de autoria e a parte do histórico relevante para o projeto e gera uma entrada Markdown para um registro contínuo.
>
> **Arquivo de destino sugerido:** `Historico_de_Uso_de_IA_Conecta_Senior.md` (um registro cronológico separado dos preparativos da banca).

## Prompt para copiar

```text
Você é o responsável por documentar de forma auditável e objetiva as interações de IA utilizadas no projeto Conecta Sênior.

OBJETIVO
Ao final desta sessão, produzir um registro em Markdown para atualizar o arquivo "Historico_de_Uso_de_IA_Conecta_Senior.md". O registro deverá mostrar QUEM utilizou a IA, QUAL IA foi utilizada, QUANDO foi utilizada, O QUE foi solicitado, QUAL resultado foi produzido e COMO isso afeta a documentação do projeto.

PASSO 1 — SOLICITAÇÃO OBRIGATÓRIA
Antes de gerar o registro, peça as informações ausentes:
- Nome de quem utilizou a IA (obrigatório).
- Nome da IA e, se conhecido, o modelo/versão (obrigatório).
- Data da interação no formato AAAA-MM-DD e, se pertinente, horário/fuso (obrigatório).
- Histórico da conversa ou exportação/transcrição da sessão (obrigatório para afirmar cobertura completa).
- Nome dos arquivos criados ou alterados e, se houver, link do PR/commit (opcional).

Se o histórico já estiver disponível integralmente nesta conversa, utilize-o. Se não estiver, solicite que a pessoa cole ou anexe o histórico. NÃO alegue acesso automático a conversas de outras contas, outras IAs, sessões anteriores ou arquivos não fornecidos. Se o histórico vier incompleto, registre "Histórico parcial" e descreva quais partes estão disponíveis. Não preencha os dados obrigatórios por suposição; mantenha o registro pendente até recebê-los.

PASSO 2 — ORGANIZAÇÃO DO HISTÓRICO
Com base APENAS no histórico realmente fornecido ou acessível:
1. Identifique os objetivos e pedidos feitos à IA.
2. Resuma, em ordem cronológica, as decisões, dúvidas e respostas relevantes para o Conecta Sênior.
3. Registre separadamente propostas de IA, decisões confirmadas pela equipe, atividades executadas e pendências. Se uma decisão não estiver explícita no histórico, não a trate como aprovada.
4. Liste arquivos Markdown, códigos, imagens, pesquisas ou outros artefatos efetivamente gerados, quando houver evidência deles.
5. Identifique se o material impacta a apresentação à banca, requisitos, funcionalidades, arquitetura, IA, acessibilidade, ética, privacidade ou segurança.
6. Não invente mensagens, citações, links, datas ou resultados. Se necessário, assinale "Não informado".
7. Não replique senhas, tokens, dados pessoais sensíveis, currículos privados, áudios de usuários ou informações sigilosas. Faça um resumo seguro, e só inclua trechos literais se forem indispensáveis e autorizados.

PASSO 3 — FORMATO DA ENTRADA EM MARKDOWN
Produza uma entrada com a seguinte estrutura:

## [AAAA-MM-DD] — [Nome da pessoa] — [IA/modelo]

| Campo | Registro |
|---|---|
| Responsável | [Nome informado] |
| IA utilizada | [Ferramenta e modelo, se conhecido] |
| Data | [AAAA-MM-DD] |
| Histórico consultado | [Completo / Parcial, indicando escopo] |
| Documentos ou PR relacionados | [Nomes/links, se disponíveis] |
| Objetivo da sessão | [Resumo curto] |

### Solicitações realizadas
- [Principais solicitações em ordem cronológica]

### Contribuições e resultados da IA
- [O que foi sugerido ou produzido; não confundir sugestão com implementação]

### Decisões confirmadas pela equipe
- [Somente decisões explicitamente registradas; caso contrário, "Nenhuma decisão confirmada neste histórico"]

### Impacto nos documentos do Conecta Sênior
- [Arquivo/seção afetados e tipo de atualização recomendada]

### Pendências e itens a validar
- [Dúvidas, inconsistências, checagens e próximos passos]

### Referência ao histórico
- [Arquivo de exportação, anexo, ID de registro ou indicação de que o histórico foi apresentado na conversa]

PASSO 4 — ATUALIZAÇÃO SEGURA DO REGISTRO
- Se eu anexar o arquivo "Historico_de_Uso_de_IA_Conecta_Senior.md", preserve todas as entradas anteriores e acrescente esta entrada no final, sem apagar ou reescrever registros.
- Se o arquivo ainda não existir, crie um novo Markdown com o título "# Histórico de Uso de Inteligência Artificial — Conecta Sênior", uma breve descrição da finalidade do registro e a primeira entrada.
- Se a sessão ou o histórico já tiver sido registrado, sinalize possível duplicidade e peça orientação antes de duplicar a entrada.
- Não altere automaticamente os outros documentos do projeto: descreva o impacto e proponha mudanças para revisão da equipe.
- Gere o conteúdo completo do arquivo .md atualizado e disponibilize-o para download se o ambiente permitir; caso contrário, forneça Markdown pronto para copiar.

ENTREGA FINAL
1. Arquivo Markdown completo do histórico de uso de IA, com as entradas anteriores preservadas.
2. Resumo das mudanças e pendências.
3. Aviso explícito quando o histórico fornecido for parcial ou quando dados obrigatórios ainda estiverem faltando.
```

## Como usar

1. Ao terminar uma conversa com qualquer IA, cole o prompt **na mesma conversa**, para aproveitar o contexto disponível.
2. Informe seu nome, a IA/modelo e a data. Se estiver utilizando outra conta ou a IA não puder recuperar o início da conversa, anexe uma exportação ou cole o histórico.
3. Anexe o `Historico_de_Uso_de_IA_Conecta_Senior.md` mais recente para acrescentar o novo registro, em vez de substituir registros antigos.
4. Revise o registro, retire informações confidenciais e inclua o arquivo no Git junto com o PR.

## Estrutura recomendada no repositório

```text
Conecta-Senior/
├── Preparativo_Banca_Apresentacao_Conecta_Senior.md
├── Historico_de_Uso_de_IA_Conecta_Senior.md
└── prompts/
    ├── Prompt_01_Atualizar_Preparativo_Banca_Conecta_Senior.md
    └── Prompt_02_Registro_de_Uso_e_Historico_de_IA_Conecta_Senior.md
```

> **Observação:** a execução é **manual por sessão**. Este prompt não ativa coleta automática nem permite que uma IA acesse, por conta própria, o histórico de outra ferramenta. Para consistência entre sessões, a equipe precisa seguir o processo e anexar os arquivos atualizados.


