# Projeto Vitrine · contexto para o diagnóstico

> A Vitrine é uma loja online fictícia, criada para o curso IA para QA. Nenhum número, pessoa ou incidente deste arquivo vem de cliente ou de projeto real.

## A loja

- Loja online de casa e decoração, com site e app para Android e iOS.
- Pagamento por cartão de crédito, Pix e boleto.
- Status de um pedido: **Aguardando pagamento → Pago → Em separação → Enviado → Entregue**. Um pedido também pode passar para **Cancelado**.
- Cupons de desconto criados pelo marketing e aplicados pelo cliente no checkout.

## Os números do negócio

| Indicador | Valor |
|---|---|
| Pedidos por dia | 1.200 |
| Ticket médio | R$ 180,00 |
| Frete médio | R$ 18,00 |
| Pedidos com cupom percentual | 30% |
| Pedidos cancelados pelo app | 4% |
| Pico do ano | Black Friday: 4 vezes o volume de um dia normal |

## O time

| Papel | Quantas pessoas | Como usa IA hoje |
|---|---|---|
| Dev do time Checkout | 2 | Claude Code no dia a dia; cerca de 60% dos PRs têm código gerado por IA |
| Dev do time Pós-venda | 2 | Claude Code para escrever código e testes unitários |
| PO | 1 | Escreve as histórias; às vezes pede ao chat para "completar os critérios de aceite" |
| QA | 2 | Uso pontual: chat para escrever casos de teste e resumir bugs |

## Como o trabalho anda

- Sprint de 2 semanas. Deploy em produção toda terça-feira.
- Regressão manual do checkout antes de cada deploy: cerca de 3 horas de uma pessoa de QA.
- Escrever os casos de teste de uma história nova: cerca de 2 horas de uma pessoa de QA.
- O PO responde dúvidas de regra no canal do time; as respostas ficam espalhadas nas conversas.
- No último trimestre, 7 bugs chegaram à produção (2 de severidade Alta).
- Desde que os devs passaram a usar IA, o número de PRs por semana dobrou. A fila de revisão de QA também.

## O que o time já tem escrito

- Histórias: **US-01** (cupom de desconto), **US-02** (cancelar pedido pelo app), **US-03** (montar o carrinho e escolher a entrega).
- Critério de severidade do time (Crítica, Alta, Média, Baixa).
- Bugs triados no encontro 2: BUG-101 a BUG-109.
- A loja de homologação usada no encontro 4 (`vitrine-loja.html`).

## Um custo de erro que já aconteceu (exemplo para a conta)

O BUG-101 (cupom percentual também desconta o frete) tira, em média, 10% do frete de cada pedido com cupom percentual:

- pedidos por dia com cupom percentual: 1.200 × 30% = **360**
- perda por pedido: 10% × R$ 18,00 = **R$ 1,80**
- perda por dia: 360 × R$ 1,80 = **R$ 648,00**
- perda por mês (30 dias): **R$ 19.440,00**; numa semana de Black Friday, 4 vezes mais por dia.

Um bug "pequeno" por pedido, multiplicado pelo volume, deixa de ser pequeno. É essa conta que o diagnóstico de hoje pede para fazer.
