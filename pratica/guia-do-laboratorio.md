# Laboratório · Diagnóstico da Vitrine

**Em grupo · 40 minutos · entrega: a ficha preenchida e as 3 atividades do grupo no mapa de calor**

## Material

- `projeto-vitrine.md`: o contexto do projeto (time, números, como o trabalho anda).
- `atividades-de-qa.md`: as 12 atividades de QA da Vitrine.
- `ficha-diagnostico.csv`: a ficha do grupo. Abre no Excel ou no Google Sheets (separador `;`).

## Passo a passo

### 1 · Ler o projeto · 5 min
Leiam `projeto-vitrine.md`. Combinem quem anota na ficha.

Se o grupo quiser, acrescente até duas atividades do dia a dia de vocês nas linhas G1 e G2. Descrevam a atividade, não o projeto: nada de nome de cliente, sistema interno ou dado real.

### 2 · Dor e oportunidade · 8 min
Para cada atividade, de 1 a 3:
- **Dor hoje:** quanto ela pesa no trabalho do time (tempo, retrabalho, atraso).
- **Oportunidade para IA:** quanto a IA poderia ajudar, pelo que vocês viram no M1.

### 3 · Nível de autonomia · 8 min
Para cada atividade, o nível que vocês dariam à IA:

| Nível | Nome | O que significa |
|---|---|---|
| 1 | Human-only | A IA não participa. |
| 2 | AI-assisted | A pessoa faz; a IA sugere, resume, aponta. |
| 3 | AI-generated + Human-approved | A IA faz; nada sai sem uma pessoa aprovar. |
| 4 | AI-autonomous | A IA faz e o resultado segue sem aprovação humana. |

### 4 · Custo do erro · 12 min
Para cada atividade com nível 2 ou mais:
- **Se a IA errar, o que acontece?** Seja concreto: quem é afetado, quanto custa. Use os números de `projeto-vitrine.md`.
- **Quem percebe e quando?** Na revisão? No teste? O cliente, em produção?
- **Probabilidade de erro (1-3)** e **Impacto (1-3)**. **Risco = P × I** (de 1 a 9).

Uma ajuda: o mesmo erro custa mais quanto mais alto o nível de autonomia, porque há menos chance de alguém pegar antes do cliente.

### 5 · Decidir · 5 min
Para cada atividade: **usar**, **usar com guardrail** ou **não usar**, com uma frase de porquê.

### 6 · Levar ao mapa de calor · 2 min
Escolham e anotem:
- as **3 atividades de maior dor**;
- as **3 de maior oportunidade**;
- as **3 de maior risco**.

Um representante do grupo fala as três listas para o mapa de calor da turma.

## Para guardar

A ficha volta no encontro 6, quando o grupo desenha os guardrails mínimos para as atividades mais arriscadas e escreve uma proposta de experimento. Salvem com o nome do grupo.
