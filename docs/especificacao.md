# Especificação — aws-threat-detection

**Semana:** 21/11 a 27/11/2026
**Entrega final:** alarmes configurados + relatório de incidente

## Contexto

A conta AWS já está endurecida (projeto 3). Agora o time quer saber quando algo perigoso acontece. Você vai montar os alarmes, testá-los provocando os eventos e, a partir de um deles, escrever um relatório de incidente completo.

## Escopo

1. **Registrar** — garantir CloudTrail ativo e entregando eventos ao EventBridge.
2. **Alarmar** — três regras no EventBridge que notificam por SNS: login da root, alteração de política IAM, abertura de security group para `0.0.0.0/0`.
3. **Testar** — provocar cada evento, de forma controlada, na sua conta, e confirmar o aviso.
4. **Responder** — escolher um dos eventos e tratá-lo como incidente real: linha do tempo, o que foi afetado, como conter, o que fazer para não repetir.

## Critério de aceite

- [ ] Os três alarmes ativos e testados (evidência do aviso recebido)
- [ ] Como cada alarme funciona, documentado em `docs/deteccoes.md`
- [ ] Relatório de incidente com linha do tempo, impacto, contenção e lições
- [ ] Evidências com o ID da conta ocultado
- [ ] README com o resultado em uma linha

## Fora de escopo

Qualquer conta que não seja a sua de laboratório. Serviços pagos sem teste grátis.

## Fases (issues da semana)

| Dia | Fase | Entrega do dia |
|---|---|---|
| Sáb 21/11 | Conferir CloudTrail e EventBridge (dia leve) | Eventos chegando ao EventBridge |
| Dom 22/11 | Alarme 1: login da root (dia leve) | Regra + aviso por SNS testado |
| Seg 23/11 | Alarme 2: mudança de política IAM | Regra testada |
| Ter 24/11 | Alarme 3: security group aberto | Regra testada |
| Qua 25/11 | Documentar as detecções | `docs/deteccoes.md` |
| Qui 26/11 | Conduzir o incidente | Relatório de incidente em rascunho |
| Sex 27/11 | Fechamento | Relatório final e README |
