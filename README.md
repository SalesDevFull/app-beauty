# Fio a Fio (nome provisório)

App de agenda, sinal no Pix e no cartão, caixa e clientes para estúdios de cílios, sobrancelhas e unhas.

Este projeto começou como uma cópia do **Degradê** (app de barbearias, repositório `JS-Barber-APP`) e foi adaptado para o ramo de beleza. A adaptação mexeu no visual, nos textos e também nos recursos do dia a dia de uma lash designer ou designer de sobrancelhas.

- App: https://app-beauty.pages.dev
- Banco: Supabase `app-beauty` (região São Paulo), separado do Degradê

## O que tem de próprio do ramo

**Retorno e manutenção.** Cada serviço tem "volta em (dias)", por exemplo 21 dias para a manutenção de cílios. No Início aparece o card "Hora da manutenção", com as clientes cujo prazo está chegando e um botão para convidar pelo WhatsApp. Ao fechar a comanda, a profissional já pode marcar a próxima manutenção na hora.

**Ficha de saúde (anamnese).** No agendamento online, a cliente responde perguntas sobre alergia (cola, látex, henna), problema nos olhos, lente de contato, gravidez, tratamento de pele, micose ou ferida nas unhas e reação anterior, e declara que as informações são verdadeiras. A ficha fica salva na cliente. A agenda mostra um alerta "⚠ Ficha de saúde" antes do atendimento. A dona pode ligar ou desligar a ficha em Gestão → Estúdio.

**Ficha técnica.** Na ficha da cliente ficam a técnica, a curvatura, a espessura, os tamanhos, a cola, a cor e, para unhas, o formato e o esmalte usados, para repetir o mesmo resultado na manutenção.

**Regras do estúdio.** A dona escreve as regras (tolerância de atraso, remarcação, vir sem maquiagem), e a cliente precisa aceitar antes de agendar.

**Cuidados pós-procedimento.** Ao fechar a comanda, um botão manda pelo WhatsApp o texto de cuidados que a dona configurou.

**Descrição dos serviços.** Cada serviço pode ter uma explicação curta, que aparece na página de agendamento.

**Serviços prontos.** Um estúdio novo já começa com fio a fio, volume brasileiro, volume russo, manutenção, lash lifting, design de sobrancelha, henna e brow lamination. Em Gestão → Serviços, a dona adiciona de uma vez os pacotes de Cílios, Sobrancelhas ou Unhas (manicure, pedicure, esmaltação em gel, banho de gel, alongamento em gel e em fibra, manutenção e remoção), com preço, duração e prazo de volta sugeridos.

**Fotos de antes e depois.** Na ficha da cliente, a equipe tira fotos de antes e de depois (até 24 por cliente). Elas ficam num armazenamento privado: só quem é do estúdio vê, por links que expiram em 1 hora. Quando a cliente é apagada, as fotos são apagadas junto.

**Estoque.** Em Gestão → Estoque ficam os materiais de uso no estúdio (cola, fios, henna, gel…) e os produtos à venda (sérum, kit de manutenção…).
- Estoque mínimo por item, com o aviso "repor" e uma lista de compras para copiar ou mandar no WhatsApp.
- Validade do item lacrado e "dura depois de aberto" (a cola de cílios vale de 4 a 6 semanas aberta). O botão "Abri um novo hoje" calcula quando vence.
- "Gasta por atendimento": quanto cada serviço consome de cada material. O app dá baixa sozinho ao fechar a comanda.
- "Chegou compra" soma ao estoque, atualiza o custo e pode lançar a despesa.
- Produtos à venda aparecem na comanda e saem do estoque quando são vendidos.
- Pacotes de materiais comuns de Cílios, Sobrancelhas e Unhas, e um card de alerta no Início.

## Visual

- Tons nude e rosé, com tema claro por padrão e tema escuro opcional
- Títulos em Playfair Display e texto em DM Sans
- Emblema de olho fechado com cílios, e ícones novos
- Textos adaptados: estúdio, profissional, "a cliente", "Em atendimento"

## Herdado do Degradê

Agenda por profissional, sinal no Pix/cartão pelo Mercado Pago de cada estúdio, comandas e caixa, metas, vales, equipe com acesso próprio, lembretes por notificação, página pública de agendamento, termos e privacidade, e painel administrativo com planos.

## Estado

- [x] Projeto próprio no Supabase, com banco e funções publicados
- [x] Publicação no Cloudflare Pages
- [x] Nome, cores, ícone e textos do ramo de beleza
- [x] Manutenção, ficha de saúde, ficha técnica, regras e cuidados
- [x] Mercado Pago (aplicação própria "Fio a Fio", segredos no Supabase, conexão testada)
- [ ] Planos e chave Pix no painel administrativo
- [x] Fotos de antes e depois na ficha da cliente (privadas)
- [x] Serviços de unhas e pergunta de unhas na ficha de saúde
- [x] Estoque de materiais e produtos, com validade, mínimo e baixa automática
- [ ] Revisar `docs/INSTALACAO.md`, que ainda fala em barbearia

O guia técnico herdado do Degradê está em `docs/INSTALACAO.md`.
