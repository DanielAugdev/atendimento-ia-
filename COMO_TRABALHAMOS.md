# Como trabalhamos neste projeto

Este projeto foi desenvolvido por **Daniel**, que está construindo sua base em Java, com uma IA (Claude) como **professora, revisora e parceira técnica**.

> A IA aumenta minha capacidade de programar. Ela não substitui minha capacidade de pensar, resolver problemas e explicar o que desenvolvi.

Este arquivo existe para deixar claro, de forma transparente, **quem decide, quem escreve e quem valida** cada parte do código.

---

## 1. Papéis

| Quem | Responsabilidade |
|---|---|
| **Daniel** | Fazer a primeira tentativa, decidir o escopo, escrever e entender o código, testar, revisar e fazer os commits |
| **IA (Claude)** | Explicar conceitos, dar pistas, planejar etapas, revisar o código e apontar erros e melhorias |

A responsabilidade final pelo código é sempre minha.

---

## 2. Os dois modos de trabalho

### Modo Mentor (aprender)
Usado para estudar um conceito novo, resolver um exercício ou entender um erro.
A IA explica em linguagem acessível, faz perguntas e dá pistas progressivas. **Não entrega a solução completa** e não reescreve o projeto.

### Modo Desenvolvedor (construir)
Usado quando já entendo o problema e quero planejar, implementar, revisar ou testar uma funcionalidade.
A IA analisa a estrutura, explica quais arquivos pretende modificar e por quê, faz mudanças pequenas e **aguarda minha revisão** antes de avançar.

### Qual modo em cada etapa

| Etapa | Conteúdo | Modo |
|---|---|---|
| 1 | Modelo do domínio (classes e enums) | Desenvolvedor |
| 2 | Atendimento por palavras-chave no console | Desenvolvedor |
| 3 | Base de conhecimento (`List`, `Map`) | Mentor → Desenvolvedor |
| 4 | Salvar conversas em arquivo | Mentor → Desenvolvedor |
| 5 | Integração com a IA via API (HTTP e JSON) | Mentor → Desenvolvedor |
| 6 | Transbordo para atendente humano | Desenvolvedor |
| 7 | Testes com JUnit | Mentor → Desenvolvedor |
| 8 | README e demonstração em vídeo | Desenvolvedor |

---

## 3. Fluxo de cada funcionalidade

1. **Planejamento:** apresento o objetivo e a IA analisa a estrutura e propõe etapas. Nenhum arquivo é alterado.
2. **Aprovação:** leio o plano, tiro dúvidas e aprovo somente o que faz sentido.
3. **Implementação gradual:** uma etapa por vez, com poucos arquivos alterados, e eu reviso cada mudança.
4. **Testes:** cenários normais, entradas inválidas, casos extremos e resultado esperado. Uma funcionalidade só é considerada pronta depois de testada.
5. **Revisão técnica:** legibilidade, organização, tratamento de erros e manutenção, com os problemas priorizados antes de corrigir.
6. **Registro:** atualizo a documentação, anoto o que aprendi e faço um commit com mensagem clara.

---

## 4. Regras que seguimos

- Não aceito código que eu não consiga explicar.
- Não aceito mudanças enormes de uma só vez.
- Faço uma tentativa própria antes de pedir ajuda, mesmo que não consiga terminar. Registro o que tentei e onde travei.
- Uso o Git como ponto de segurança: reviso o `git diff` e faço commits antes de mudanças grandes.
- Teste de verdade: código que parece correto não é necessariamente código que funciona.
- **Nunca** publico senhas, tokens ou chaves de API no repositório. Credenciais ficam em variáveis de ambiente ou em arquivo local ignorado pelo Git.

---

## 5. Checklist antes de aceitar uma alteração

- [ ] Consigo explicar o que esse código faz?
- [ ] Entendo por que essa abordagem foi escolhida?
- [ ] Sei como executar e testar a funcionalidade?
- [ ] Consigo identificar pelo menos alguns possíveis erros?
- [ ] Sei quais arquivos foram modificados e por quê?
- [ ] Consigo explicar a mudança para outra pessoa?

---

## 6. Diário de aprendizado

Registro aqui, a cada etapa concluída, o que fiz e aprendi.

| Data | Etapa | Modo | O que fiz | O que aprendi | Dificuldade / onde travei |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 7. Decisões técnicas

Registro aqui as decisões importantes e o motivo de cada uma.

| Data | Decisão | Motivo | Alternativas consideradas |
|---|---|---|---|
| | | | |
| | | | |
