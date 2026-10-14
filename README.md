# aws-threat-detection

Detecção e resposta a incidentes na nuvem. O projeto configura alarmes de segurança em uma conta AWS, provoca eventos suspeitos de forma controlada, confirma que os alarmes disparam e fecha com um relatório de incidente no formato que a área usa.

> Projeto 6 de 7 do laboratório [sentinelatech](https://github.com/sentinelatech). Área: **detecção em nuvem**. Continua o [aws-account-baseline](https://github.com/sentinelatech/aws-account-baseline).

## Por que isso importa em segurança

Ter a conta endurecida não basta: é preciso perceber quando algo sai do esperado. Montar a trilha de detecção (registro → regra → alerta) e conduzir a resposta é o trabalho de quem cuida de segurança em nuvem.

## Objetivo

Ligar alarmes para três situações de risco em uma conta AWS, testá-los com eventos controlados e documentar um incidente do começo ao fim: detecção, análise, contenção e lições.

## Estrutura

```
docs/especificacao.md   escopo e critério de aceite
docs/deteccoes.md       os alarmes, o que cada um cobre e por quê
relatorio/              o relatório de incidente, com linha do tempo
evidencias/             prints e trechos de log (conta ocultada)
```

## Alarmes

Login da conta root · mudança em política IAM · abertura de um security group para `0.0.0.0/0`. Montados com CloudTrail → EventBridge → SNS (aviso por e-mail).

## Custo

Cabe no plano gratuito. CloudTrail, EventBridge e SNS para este volume ficam em centavos. O GuardDuty tem teste grátis de 30 dias no plano pago; use só se quiser estender o projeto e lembre de desligar. Mantenha o alerta de orçamento do projeto 3 ligado.

## Resultado

<!-- Preencher ao fim -->

## Aviso

Todos os eventos são provocados por você, na sua própria conta de laboratório. Nenhuma conta ou serviço de terceiros é tocado. Credenciais e ID da conta não são versionados.
