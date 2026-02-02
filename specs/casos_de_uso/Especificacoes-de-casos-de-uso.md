# Especificação de Casos de Uso – SGBF
## Sistema Gerenciador de Brinquedos de Festa

---

## Legenda (Índice de Casos de Uso)

- [UC01 – Visualizar Brinquedos Disponíveis](#uc01--visualizar-brinquedos-disponíveis)
- [UC02 – Solicitar Reserva](#uc02--solicitar-reserva)
- [UC03 – Receber Notificações](#uc03--receber-notificações)
- [UC04 – Consultar Status do Pedido](#uc04--consultar-status-do-pedido)
- [UC05 – Receber Lembretes](#uc05--receber-lembretes)
- [UC06 – Manter Cadastro de Clientes](#uc06--manter-cadastro-de-clientes)
- [UC07 – Chat Interno](#uc07--chat-interno)
- [UC08 – Registrar Retirada](#uc08--registrar-retirada)
- [UC09 – Registrar Entrega](#uc09--registrar-entrega)
- [UC10 – Atualizar Status da Reserva](#uc10--atualizar-status-da-reserva)
- [UC11 – Manter Reserva](#uc11--manter-reserva)
- [UC12 – Buscar Brinquedos](#uc12--buscar-brinquedos)
- [UC13 – Verificar Disponibilidade](#uc13--verificar-disponibilidade)
- [UC14 – Enviar Orçamento via WhatsApp](#uc14--enviar-orçamento-via-whatsapp)
- [UC15 – Manter Brinquedos](#uc15--manter-brinquedos)
- [UC16 – Manter Manutenção](#uc16--manter-manutenção)
- [UC17 – Visualizar Calendário](#uc17--visualizar-calendário)
- [UC18 – Registrar Pagamentos e Despesas](#uc18--registrar-pagamentos-e-despesas)
- [UC19 – Gerar Relatórios Financeiros](#uc19--gerar-relatórios-financeiros)
- [UC20 – Gerar Relatórios de Locações](#uc20--gerar-relatórios-de-locações)
- [UC21 – Gerenciar Usuários e Permissões](#uc21--gerenciar-usuários-e-permissões)
- [UC22 – Backup Automático do Banco de Dados](#uc22--backup-automático-do-banco-de-dados)
- [UC23 – Logs de Acesso e Alterações](#uc23--logs-de-acesso-e-alterações)

---

## UC01 – Visualizar Brinquedos Disponíveis

**Objetivo**  
Permitir que o ator visualize os brinquedos disponíveis para locação.

**Requisitos**  
RF004

**Atores**  
Cliente Final

**Condição de Entrada**  
O ator acessou o sistema.

### Fluxo Principal
1. O ator seleciona a opção **“Visualizar Brinquedos Disponíveis”**.
2. O sistema consulta os brinquedos com status disponível.
3. O sistema exibe nome, categoria, descrição, imagens e valor.
4. O ator visualiza os brinquedos.

### Fluxos Alternativos
- **A1 – Filtrar brinquedos**
  1. O ator aplica filtros por categoria ou preço.
  2. O sistema atualiza a lista.

### Fluxos de Exceção
- **E1 – Nenhum brinquedo disponível**
  - O sistema exibe mensagem informativa.

---

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

---

## UC03 – Receber Notificações

**Objetivo**  
Notificar o cliente sobre eventos da reserva.

**Requisitos**  
RF010

**Atores**  
Cliente Final

### Fluxo Principal
1. O sistema identifica alteração na reserva.
2. O sistema envia notificação ao cliente.

### Fluxos Alternativos
- **A1 – Envio via WhatsApp**
  - O sistema utiliza integração externa.

### Fluxos de Exceção
- **E1 – Falha no envio**
  - O sistema registra erro.

---

## UC04 – Consultar Status do Pedido

**Objetivo**  
Permitir que o cliente acompanhe o status da reserva.

**Requisitos**  
RF013

**Atores**  
Cliente Final

### Fluxo Principal
1. O ator acessa **“Meus Pedidos”**.
2. Seleciona uma reserva.
3. O sistema exibe o status atual.

### Fluxos Alternativos
- **A1 – Filtrar por status**

### Fluxos de Exceção
- **E1 – Pedido não encontrado**

---

## UC05 – Receber Lembretes

**Objetivo**  
Enviar lembretes automáticos de entrega e retirada.

**Requisitos**  
RF017

**Atores**  
Cliente Final

### Fluxo Principal
1. O sistema identifica eventos próximos.
2. O sistema envia lembrete ao cliente.

### Fluxos Alternativos
- **A1 – Lembrete antecipado configurável**

### Fluxos de Exceção
- **E1 – Contato inválido**

---

## UC06 – Manter Cadastro de Clientes

**Objetivo**  
Cadastrar, editar, excluir e consultar clientes.

**Requisitos**  
RF002

**Atores**  
Funcionário de Atendimento

### Fluxo Principal
1. O ator acessa **“Clientes”**.
2. O sistema exibe formulário.
3. O ator preenche os dados de nome do cliente, data de nascimento, endereco, e-mail e telefone.
4. O sistema valida e salva.
5. O sistema confirma a operação.

### Fluxos Alternativos
- **A1 – Editar cliente**
- **A2 – Excluir cliente**

### Fluxos de Exceção
- **E1 – Campos obrigatórios não preenchidos**

---

## UC07 – Chat Interno

**Objetivo**  
Permitir comunicação entre cliente e funcionário.

**Requisitos**  
RF006

**Atores**  
Cliente Final, Funcionário de Atendimento

### Fluxo Principal
1. O ator acessa o chat.
2. Seleciona o destinatário.
3. Envia mensagem.
4. O sistema registra a conversa.

### Fluxos Alternativos
- **A1 – Enviar anexo**

### Fluxos de Exceção
- **E1 – Destinatário offline**

---

## UC08 – Registrar Retirada

**Objetivo**  
Registrar a retirada do brinquedo.

**Requisitos**  
RF007

**Atores**  
Equipe Logística

### Fluxo Principal
1. O ator localiza a reserva.
2. Registra data e horário da retirada.
3. O sistema atualiza o status.

### Fluxos Alternativos
- **A1 – Retirada parcial**

### Fluxos de Exceção
- **E1 – Reserva inexistente**

---

## UC09 – Registrar Entrega

**Objetivo**  
Registrar a entrega do brinquedo.

**Requisitos**  
RF007

**Atores**  
Equipe Logística

### Fluxo Principal
1. O ator localiza a reserva.
2. Registra a entrega.
3. O sistema atualiza o status.

### Fluxos Alternativos
- **A1 – Entrega parcial**

### Fluxos de Exceção
- **E1 – Reserva não localizada**

---

## UC10 – Atualizar Status da Reserva

**Objetivo**  
Atualizar o status da reserva.

**Requisitos**  
RF005, RF007

**Atores**  
Sistema

### Fluxo Principal
1. O sistema identifica evento.
2. Atualiza o status da reserva.

### Fluxos Alternativos
- **A1 – Atualização manual**

### Fluxos de Exceção
- **E1 – Status inválido**

---

## UC11 – Manter Reserva

**Objetivo**  
Criar, alterar ou cancelar reservas.

**Requisitos**  
RF003, RF005

**Atores**  
Funcionário de Atendimento

### Fluxo Principal
1. O ator acessa **“Reservas”**.
2. Busca brinquedos.
3. Verifica disponibilidade.
4. Informa o brinquedo, descreve o evento, informa o local do evento, 
a data do pedido, data de inicio da locação e data de fim da locação.
5. Registra a reserva.

### Fluxos Alternativos
- **A1 – Cancelar reserva**

### Fluxos de Exceção
- **E1 – Data inválida**

---

## UC12 – Buscar Brinquedos

**Objetivo**  
Buscar brinquedos por nome ou código.

**Requisitos**  
RF019

**Atores**  
Funcionário de Atendimento

### Fluxo Principal
1. O ator acessa a pagina principal da aplicação.
2. O ator informa o critério na barra de pesquisa.
3. O sistema exibe resultados da busca.

### Fluxos Alternativos
- **A1 – Busca parcial**

### Fluxos de Exceção
- **E1 – Nenhum resultado encontrado**

---

## UC13 – Verificar Disponibilidade

**Objetivo**  
Verificar disponibilidade de brinquedos.

**Requisitos**  
RF003

**Atores**  
Sistema

### Fluxo Principal
1. O sistema cruza datas e reservas.
2. Retorna disponibilidade.

### Fluxos de Exceção
- **E1 – Conflito de agenda**

---

## UC14 – Enviar Orçamento via WhatsApp

**Objetivo**  
Enviar orçamento ao cliente.

**Requisitos**  
RF016

**Atores**  
Funcionário de Atendimento

### Fluxo Principal
1. O ator gera o orçamento.
2. O sistema envia via WhatsApp.

### Fluxos de Exceção
- **E1 – Falha na integração**

---

## UC15 – Manter Brinquedos

**Objetivo**  
Cadastrar, editar, excluir e consultar brinquedos.

**Requisitos**  
RF001

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator acessa **“Brinquedos”**.
2. Preenche os dados de nome do brinquedo, categoria, 
descrição, envia as imagens, valor, disponibilidade, condição.
3. O sistema valida e salva.

### Fluxos Alternativos
- **A1 – Editar brinquedo**
- **A2 – Excluir brinquedo**

### Fluxos de Exceção
- **E1 – Dados inválidos**

---

## UC16 – Manter Manutenção

**Objetivo**  
Registrar manutenções e limpezas.

**Requisitos**  
RF008

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator entra no menu de cadastro de manutenção dos equipamentos
2. Preenche as informações da manutenção informando o brinquedo, a empresa responsavel
o e-mail da empresa, o telefone da empresa, a ultima reserva do brinquedo, a descrição, 
o valor da manutencao, a data de inicio da manutencao, a data de fim da manutencao.
3. O ator clica em registrar manutenção.
2. O sistema salva os dados.

### Fluxos de Exceção
- **E1 – Brinquedo inexistente**

---

## UC17 – Visualizar Calendário

**Objetivo**  
Visualizar calendário de locações.

**Requisitos**  
RF011

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator acessa o calendário.
2. O sistema exibe os eventos.

### Fluxos de Exceção
- **E1 – Falha no carregamento**

---

## UC18 – Registrar Pagamentos e Despesas

**Objetivo**  
Controlar fluxo de caixa.

**Requisitos**  
RF014

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator registra pagamento ou despesa.
2. O sistema valida e salva.

### Fluxos de Exceção
- **E1 – Valor inválido**

---

## UC19 – Gerar Relatórios Financeiros

**Objetivo**  
Gerar relatórios financeiros.

**Requisitos**  
RF009, RF018

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator seleciona período.
2. O sistema gera o relatório.
3. O sistema permite exportação.

### Fluxos de Exceção
- **E1 – Dados insuficientes**

---

## UC20 – Gerar Relatórios de Locações

**Objetivo**  
Gerar relatórios de locações.

**Requisitos**  
RF009

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator seleciona filtros.
2. O sistema gera o relatório.

### Fluxos de Exceção
- **E1 – Nenhuma locação encontrada**

---

## UC21 – Gerenciar Usuários e Permissões

**Objetivo**  
Gerenciar acessos e permissões.

**Requisitos**  
RF012

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O ator cadastra usuário.
2. Define permissões.
3. O sistema salva.

### Fluxos de Exceção
- **E1 – Perfil inválido**

---

## UC22 – Backup Automático do Banco de Dados

**Objetivo**  
Garantir segurança dos dados.

**Requisitos**  
RF015

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O sistema executa backup automático.
2. Armazena com segurança.

### Fluxos de Exceção
- **E1 – Falha no backup**

---

## UC23 – Logs de Acesso e Alterações

**Objetivo**  
Registrar ações realizadas no sistema.

**Requisitos**  
RF020

**Atores**  
Administrador do Sistema

### Fluxo Principal
1. O sistema registra acessos e alterações.
2. O administrador consulta os logs.

### Fluxos de Exceção
- **E1 – Log indisponível**
