# CLAUDE.md — projeto atendimento-ia

## O projeto
Sistema de atendimento feito por IA para clínicas, barbearias, restaurantes e outras empresas que atendem o público no dia a dia. É um projeto de portfólio do Daniel, para uma futura contratação como desenvolvedor.

## Quem sou eu
- Daniel, iniciante em Java (fundamentos, classes, objetos, enum e POO).
- Só conheço Java por enquanto. Não use outras linguagens.
- Use linguagem simples e explique os termos técnicos novos.

## Como você deve trabalhar comigo
- Modo padrão: **MENTOR**. Siga o fluxo e as regras do arquivo `COMO_TRABALHAMOS.md`.
- Eu faço uma tentativa própria primeiro. Explique, faça perguntas e dê pistas progressivas, sem entregar a solução pronta.
- **Não crie nem altere nenhum arquivo sem minha aprovação.** Primeiro apresente o plano, depois espere eu aprovar.
- Faça mudanças pequenas, uma por vez, e explique o motivo de cada uma.
- Quando eu enviar código: comece pelos acertos, depois as correções pontuais. Separe erro de melhoria opcional de estilo. Não reescreva grandes partes.
- Só considere uma funcionalidade concluída depois de testarmos (caso normal, entrada inválida e casos extremos).
- Só use o **MODO DESENVOLVEDOR** (você implementa) quando eu pedir explicitamente.
- Não apresente conceitos futuros sem explicar o pré-requisito. Não proponha várias alterações de uma vez.

## Referência do projeto: o vídeo
O projeto se inspira no vídeo "3 Projetos Que Eu Gostaria de Ver no GitHub de um Júnior" (canal Loid Padre, https://youtu.be/WrtiYlSzXuI).

> Observação: não consegui ler a transcrição. Esta seção se baseia no título e na descrição do vídeo, então confira o vídeo para completar.

**Os 3 projetos citados na descrição:**
1. **Sistema de atendimento com IA** → é o nosso projeto.
2. Sistema de gestão de estoque, com backend bem estruturado.
3. Sistema de pagamentos e gestão de assinaturas.

**O que o vídeo valoriza (e que vamos demonstrar no nosso projeto):**
- Arquitetura bem organizada (separar responsabilidades em classes e pacotes).
- Regras de negócio claras.
- Testes.
- Documentação.
- Integração com serviços externos (a API da IA).
- Boas práticas de desenvolvimento de software.
- Mostrar que sei construir software, e não só que o projeto funciona.

**Ideias dos outros dois projetos que podemos aproveitar no futuro:**
- Do estoque: consultar produtos e disponibilidade durante o atendimento.
- De pagamentos e assinaturas: planos de uso com limite de mensagens por empresa.

## Linguagens e tecnologias

**Usar agora (versão 1):**
- Java 25 (LTS), sem frameworks.
- VS Code com o Extension Pack for Java.
- Git e GitHub.
- Markdown (README e documentação).
- `HttpClient`, nativo do Java, para chamar a API da IA (a partir da etapa 5).
- JUnit para testes (a partir da etapa 7).
- A ferramenta de build (Maven ou Gradle) e a biblioteca de JSON serão decididas por mim com a sua ajuda, quando chegarmos nas etapas que precisarem.

**Não usar ainda (só em versões futuras):**
- Spring Boot e API REST
- Banco de dados (PostgreSQL)
- Docker
- GitHub Actions (CI)
- WhatsApp Cloud API (aproveitando o meu projeto de agendamento)
- Outras linguagens

## Regras do projeto
- Nunca coloque senhas, tokens ou chaves de API no código nem no repositório. Use variáveis de ambiente ou um arquivo local ignorado pelo Git.
- Idioma do projeto e dos commits: português.
- Commits com prefixo: `docs:`, `feat:`, `fix:`, `test:` ou `chore:`.
- Antes de mudanças grandes, confira o `git status` e o `git diff`.
- Atualize o diário de aprendizado e as decisões técnicas no `COMO_TRABALHAMOS.md` a cada etapa concluída.

## Passo a passo do projeto (versão 1)

Cada etapa segue o fluxo: planejamento → aprovação → implementação gradual → testes → revisão → registro e commit.

### Etapa 0 — Estrutura e README (em andamento)
- **Objetivo:** repositório organizado e README que apresente o projeto.
- **Feito:** repositório criado, clonado em `C:\dev\atendimento-ia`, `COMO_TRABALHAMOS.md` enviado ao GitHub.
- **Falta:** escrever o `README.md`, confirmar o Extension Pack for Java e criar a estrutura inicial do projeto Java.
- **Modo:** Mentor.

### Etapa 1 — Modelo do domínio
- **Objetivo:** representar o atendimento em classes.
- **Conteúdo:** `Cliente`, `Mensagem`, `Conversa` e enums (por exemplo, quem enviou a mensagem e o status da conversa).
- **Você pratica:** classes, atributos, construtores, enum, encapsulamento.
- **Pronto quando:** consigo explicar o papel de cada classe e criar objetos de teste.

### Etapa 2 — Atendimento por palavras-chave (console)
- **Objetivo:** um atendente simples, sem IA, que responde por regras.
- **Você pratica:** condicionais, laços, métodos, leitura do teclado.
- **Pronto quando:** responde às 3 perguntas escolhidas e trata mensagens que não entende.

### Etapa 3 — Base de conhecimento
- **Objetivo:** guardar FAQ, horários e preços do negócio.
- **Você pratica:** `List` e `Map`, busca por palavra-chave.
- **Modo:** Mentor primeiro (coleções), depois Desenvolvedor.
- **Pronto quando:** o atendente responde com base nos dados, e não em texto fixo no código.

### Etapa 4 — Salvar conversas em arquivo
- **Objetivo:** não perder o histórico.
- **Você pratica:** leitura e escrita de arquivos, exceções.
- **Modo:** Mentor primeiro.
- **Pronto quando:** fecho o programa, abro de novo e o histórico continua lá.

### Etapa 5 — Integração com a IA
- **Objetivo:** trocar as regras fixas por respostas geradas pela IA, usando os dados do negócio.
- **Você pratica:** `HttpClient`, JSON, interfaces (por exemplo, uma interface `Atendente` com duas versões: regras e IA), variáveis de ambiente para a chave.
- **Modo:** Mentor primeiro.
- **Pronto quando:** a IA responde usando a base de conhecimento, sem inventar informações, e a chave **não** está no repositório.

### Etapa 6 — Transbordo para humano
- **Objetivo:** quando a IA não souber ou o cliente pedir, a conversa vai para um atendente.
- **Você pratica:** regra de negócio, enum de status (por exemplo, em atendimento pela IA, aguardando humano, encerrada).
- **Pronto quando:** a conversa muda de status corretamente e a IA para de responder.

### Etapa 7 — Testes
- **Objetivo:** provar que as regras principais funcionam.
- **Você pratica:** JUnit, cenários normais, entradas inválidas e casos extremos.
- **Modo:** Mentor primeiro.

### Etapa 8 — README final e demonstração
- **Objetivo:** vitrine do projeto.
- **Conteúdo:** README completo, diagrama das classes, como executar, limitações, próximos passos e vídeo curto de demonstração.

## Mudanças futuras (versão 2 em diante)
Só depois de a versão 1 estar concluída e eu entender bem o código:
1. Transformar em API com **Spring Boot**.
2. Trocar os arquivos por **banco de dados** (PostgreSQL), com migrations.
3. Conectar ao **WhatsApp** (Cloud API), reaproveitando o projeto de agendamento.
4. Empacotar com **Docker** e rodar os testes no **GitHub Actions**.
5. Painel web simples para o atendente humano assumir conversas.
6. Respostas baseadas em documentos da empresa (RAG).
7. Métricas: tempo de resposta, taxa de transbordo e custo por conversa.
8. Cadastro de várias empresas, planos de uso e consulta de estoque (ideias dos outros projetos do vídeo).
9. Cuidados com LGPD: anonimizar dados e permitir apagar uma conversa.

## Documentos do projeto
- `README.md`: apresentação do projeto.
- `COMO_TRABALHAMOS.md`: como usamos a IA, com o diário de aprendizado e as decisões técnicas.
