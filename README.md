# Atendimento IA

Sistema de atendimento feito por inteligência artificial para clínicas, barbearias, restaurantes e outras empresas que atendem o público no dia a dia.

> 🚧 **Projeto em desenvolvimento.** Este repositório está na fase inicial (Etapa 0: estrutura e documentação). As funcionalidades abaixo descrevem o objetivo da versão 1 e serão entregues etapa por etapa.

## O problema

Pequenos negócios recebem as mesmas perguntas o dia inteiro: "Qual o horário de funcionamento?", "Quanto custa?", "Tem horário livre amanhã?". Responder tudo isso manualmente toma o tempo de quem deveria estar atendendo presencialmente, e o cliente que não recebe resposta rápida acaba procurando outro lugar.

## A proposta

Um atendente virtual que responde os clientes com base nas informações reais do negócio (horários, preços, perguntas frequentes) e, quando não souber responder ou o cliente pedir, passa a conversa para um atendente humano.

## Funcionalidades planejadas (versão 1)

- **Modelo do atendimento:** clientes, mensagens e conversas representados em classes.
- **Atendimento por regras:** respostas por palavras-chave no console, sem IA, como primeira versão.
- **Base de conhecimento:** FAQ, horários e preços guardados como dados, e não como texto fixo no código.
- **Histórico de conversas:** conversas salvas em arquivo, para não se perderem ao fechar o programa.
- **Integração com IA:** respostas geradas por uma API de IA, usando apenas os dados do negócio, sem inventar informações.
- **Transbordo para humano:** a conversa muda de status e a IA para de responder quando um atendente precisa assumir.
- **Testes automatizados:** regras principais validadas com JUnit.

## Status e roteiro

- [ ] Etapa 0: estrutura do repositório e README *(em andamento)*
- [ ] Etapa 1: modelo do domínio
- [ ] Etapa 2: atendimento por palavras-chave (console)
- [ ] Etapa 3: base de conhecimento
- [ ] Etapa 4: salvar conversas em arquivo
- [ ] Etapa 5: integração com a IA
- [ ] Etapa 6: transbordo para humano
- [ ] Etapa 7: testes
- [ ] Etapa 8: README final e demonstração

**Próximas versões:** API com Spring Boot, banco de dados PostgreSQL, integração com WhatsApp, Docker e CI com GitHub Actions.

## Tecnologias

- Java 25 (sem frameworks na versão 1)
- `HttpClient` nativo do Java, para a integração com a IA
- JUnit, para os testes
- Git e GitHub

## Como este projeto é desenvolvido

Este projeto é desenvolvido com o apoio de uma IA (Claude) como mentora e revisora, com regras claras sobre quem decide, quem escreve e quem valida o código. Os detalhes, o diário de aprendizado e as decisões técnicas estão em [COMO_TRABALHAMOS.md](COMO_TRABALHAMOS.md).

## Autor

**Daniel**: [GitHub](https://github.com/DanielAugdev)
