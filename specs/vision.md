<h1>Visão do Produto</h1>
<h2>SGBF - Sistema Gerenciador de Brinquedos de Festa</h2>
<small>Versão 1.0</small>

---

## Historico de Versões

|    Data    |  Versão |          Descrição           |      Autor       |
| :--------: | :----: | :---------------------------: |  :--------------:|
| 28/03/2023 |  1.0   |     Criação do documento      | Daniel Lucas e Carlos Silvio |

# Introdução
--

## Proposito 

O propósito deste documento é definir e descrever de forma clara os objetivos, necessidades e funcionalidades de alto nível do sistema. Ele visa apresentar as expectativas dos stakeholders e usuários, e as razões que levam essas necessidades. O documento também define os requisitos funcionais e casos de uso, detalhando como o sistema atenderá às demandas do negócio de locação de brinquedos e organização de festas.

## Deinições e Abreviações

| Termo | Definição |
| :----: | :---------: |
| SGBF | Sistema Gerenciador de Brinquedos de Festa |

## Escopo do Produto

O **SGBF** sistema que tem como objetivo facilitar o controle de estoque, reservas e manutenção, centralizando informações e melhorando a gestão de empresas de locação de brinquedos para festas.

---

# Posicionamento

## Oportunidade de negócios

--

## Descrição dos benefícios e dos problemas resolvidos 

| Benefício | Problema Resolvido | Afetados |
| :--------: | :----------------: | :------: | 
| Redução de erros e retrabalho | Reservas duplicadas ou perdidas, erros de agendamento | --
| Controle eficiente do estoque e calendario | Dificuldade de controlar o estoque e o calendario de locações | --
| Aumento da eficiência operacional | Gestão manual ineficiente (planilhas e anotações soltas, etc) | --
| Centralização e maior segurança das informações | Informações descentralizadas e perda de dados importantes | --

---

# Descrição dos stakeholders e dos usuários

Essa seção descreve os stakeholders e usuarios do **SGBF**.

## Stakeholders

Segue abaixo a lista de stakeholders.

| Stakeholder | Descrição | Papel |
| :---------: | :-------: | :---: |
| Donos das Empresas | Proprietários das empresas de locação de brinquedos e festas que contratam e utilizam o sistema | Usuário administrador do sistema |
| Funcionários de Atendimento | Profissionais que realizam reservas, cadastros de clientes e interações comerciais | Usuário do sistema |
| Equipe de Logística | Profissionais responsaveis pelas entregas e retiradas dos brinquedos | Consultar/Atualizar status de entregas e retiradas |
| Clientes Finais | Pessoas que contratam o aluguel dos brinquedos para festas |  Usuário externo, realiza reservas e acompanha status |
| Equipe de Desenvolvimento | Profissionais responsáveis por desenvolver e manter o sistema | Desenvolvedores |

## Usuarios e Atores

Segue abaixo a tabela de usuarios e atores.

| Usuário | Descrição | Responsabilidades | Stakeholders Relacionados |
| :----:  | :-------: | :---------------: | :----------: |
| Dono da Empresa | Proprietário da empresa.| Gerenciar reservas, estoque, finanças, usuários e relatórios do sistema. | Equipe de Desenvolvimento |
| Funcionário de Atendimento   | Profissional responsável por realizar reservas e atender clientes. | Cadastrar clientes, efetuar reservas, emitir comprovantes, consultar histórico de locações. | Donos das Empresas, Clientes Finais |
| Equipe Logística | Responsáveis por entrega e retirada dos brinquedos. | Acessar agenda, registrar entregas e retiradas, atualizar status no sistema. | Donos das Empresas |
| Cliente Final | Usuário externo que aluga brinquedos para festas. | Consultar disponibilidade, solicitar reservas, receber notificações e informações. | Donos das Empresas, Funcionarios de Atendimento|
| Administrador do Sistema | Responsável pela administração técnica do sistema. | Gerenciar usuários e permissões, manter o funcionamento do sistema, realizar backups e atualizações. | Equipe de Desenvolvimento |

---

# Descrição do ambiente de uso

## Ambiente de uso

## Necessidades principais quanto ao ambiente

---

# Visão geral do produto

## Visão geral

## Características e funcionalidades de alto nível

1. O sistema deve garantir o cadastro completo de brinquedos e equipamentos, incluindo fotos e estado de conservação, historico de manutenção e disponibilidade.

2. O sistema deve permitir o cadastro de clientes, com informações de contato, historico de locações e preferências

3. O sistema deve permitir o agendamento e controle de reservas de brinquedos, exibindo disponibilidade em tempo real.

4. O sistema deve enviar notificações automáticas aos usuários acerca das confirmações alterações, cancelamentos, ou lembretes de entrega e retirada. 

5. O sistema deve permitir o acompanhamento da manutenção e limpeza dos brinquedos, registrando datas, técnicos responsáveis e observações.

6. O sistema deve permitir o controle financeiro basico, incluindo registros de pagamentos, despesas, e relatórios de faturamento.

7. O sistema deve garantir níveis de acesso diferenciados para usuários (administrador, atendente, logística, técnico e cliente).

8. O sistema deve permitir acesso via web e dispositivos móveis com design responsivo.

9. O sistema deve ter integração com whatsapp para facilitar a atualização das informações por parte principalmente da equipe logistica. Bem como atender melhor o cliente, enviando resumos dos orçamentos e pedidos feitos.

10. O sistema deve permitir a geração de relatórios e gráficos sobre locações, receitas, brinquedos mais alugados e manutenções realizadas. 


## Restrições

Algumas restrições que se aplicam ao SGBF são:

1. Segurança de dados: O sistema deve seguir boas práticas de segurança, mas estará sujeito a limitações das APIs e serviços de terceiros (como WhatsApp API ou serviços de autenticação externos).

2. Treinamento dos usuários: Considerando que os usuários possuem conhecimentos básicos de informática, a interface deverá ser simples e intuitiva. Recursos muito avançados podem precisar ser adiados ou simplificados.

3. Manutenção e suporte técnico: O suporte e as atualizações dependerão da equipe de desenvolvimento ou de contratos futuros, o que pode limitar a evolução contínua do sistema após a entrega inicial.

4. Restrições de interoperabilidade: O sistema deve ser capaz de interoperar entre suas versões web, mobile e desktop, mantendo a sincronia e a atualização constante dos dados.

5. Backup em nuvem: O sistema deve fazer backups periódicos (de acordo com a necessidade do negócio e considerando o volume de dados) em um sistema de núvem atrelado a base de dados do servidor pessoal do dono da empresa. 

6. Controle de permissões: O acesso, de diferentes formas, por diferentes perfis de usuário (admin, atendente, cliente, logistica, tecnicos).

7. Restrições regulatórias: Dados de pessoas físicas serão manipulados, o que ativa a LGPD (Lei Geral de Proteção de Dados).


