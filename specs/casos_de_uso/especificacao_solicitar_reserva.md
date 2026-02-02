## UC02 – Solicitar Reserva

**Objetivo**  
Permitir que o cliente solicite a reserva de brinquedos.

**Requisitos**  
RF004

**Atores**  
Cliente Final

**Condição de Entrada**  
O ator visualizou brinquedos disponíveis.

### Fluxo Principal
1. O ator seleciona um brinquedo.
2. Informa o cliente, descrição, valor do aluguel, data de inicio do pedido, data de inicio da locação, data de fim da locação e local do evento.
3. Confirma a solicitação.
4. O sistema registra a reserva como *Aguardando aprovação*.
5. O sistema envia notificação ao cliente.

### Fluxos Alternativos
- **A1 – Reserva de múltiplos brinquedos**
  1. O ator adiciona outros brinquedos.
  2. O sistema recalcula o valor total.

### Fluxos de Exceção
- **E1 – Brinquedo indisponível**
  - O sistema impede a solicitação.