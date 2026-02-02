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
