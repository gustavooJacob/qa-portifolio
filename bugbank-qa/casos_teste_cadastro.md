# Casos de Teste - Formulário de Cadastro Bug Bank

**Projeto:** Bug Bank - Sistema Bancário Digital  
**Módulo:** Cadastro de Conta  
**Data:** 23/07/2026  
**QA Senior:** Trabalho Prático de Testes

---

## CENÁRIOS DE SUCESSO

### CT-001: Cadastro Bem-Sucedido - Conta Com Saldo

**Cenário:** Registrar nova conta com saldo inicial de R$1.000,00

**Pré-condição:**
- Usuário está na página de cadastro do Bug Bank
- Formulário está limpo (nenhum campo preenchido)
- Checkbox "Criar conta com saldo" está visível

**Passos:**
1. Preencher campo "Email" com "usuario.teste@bugbank.com"
2. Preencher campo "Nome" com "João Silva"
3. Preencher campo "Senha" com "Senha@123"
4. Preencher campo "Confirmação senha" com "Senha@123"
5. Marcar checkbox "Criar conta com saldo"
6. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário é submetido com sucesso
- Sistema exibe número da conta criada (ex: "Conta criada: 123456")
- Saldo inicial da conta é R$1.000,00
- Usuário é redirecionado para página de login ou dashboard da conta

---

### CT-002: Cadastro Bem-Sucedido - Conta Sem Saldo

**Cenário:** Registrar nova conta com saldo inicial de R$0,00

**Pré-condição:**
- Usuário está na página de cadastro do Bug Bank
- Formulário está limpo
- Checkbox "Criar conta com saldo" está disponível

**Passos:**
1. Preencher campo "Email" com "usuario.novo@bugbank.com"
2. Preencher campo "Nome" com "Maria Santos"
3. Preencher campo "Senha" com "Segura@456"
4. Preencher campo "Confirmação senha" com "Segura@456"
5. Deixar checkbox "Criar conta com saldo" desmarcado
6. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário é submetido com sucesso
- Sistema exibe número da conta criada
- Saldo inicial da conta é R$0,00
- Usuário consegue fazer login com as credenciais fornecidas

---

### CT-003: Cadastro com Diferentes Domínios de Email

**Cenário:** Aceitar emails de diferentes provedores

**Pré-condição:**
- Usuário está na página de cadastro
- Domínios válidos: gmail.com, hotmail.com, empresa.com.br, etc

**Passos:**
1. Preencher campo "Email" com "teste@empresa.com.br"
2. Preencher campo "Nome" com "Carlos Souza"
3. Preencher campo "Senha" com "Abc123@xyz"
4. Preencher campo "Confirmação senha" com "Abc123@xyz"
5. Marcar checkbox "Criar conta com saldo"
6. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Cadastro é realizado com sucesso
- Número da conta é exibido
- Email é registrado corretamente no sistema

---

## CENÁRIOS COM CAMPOS OBRIGATÓRIOS VAZIOS

### CT-004: Email Obrigatório Vazio

**Cenário:** Tentar cadastrar sem preenchimento do email

**Pré-condição:**
- Usuário está na página de cadastro
- Campo email está vazio

**Passos:**
1. Deixar campo "Email" vazio
2. Preencher campo "Nome" com "Pedro Costa"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagem de erro: "Email é obrigatório" ou similar
- Campo "Email" é destacado como erro
- Usuário permanece na página de cadastro

---

### CT-005: Nome Obrigatório Vazio

**Cenário:** Tentar cadastrar sem preenchimento do nome

**Pré-condição:**
- Usuário está na página de cadastro
- Campo nome está vazio

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Deixar campo "Nome" vazio
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagem de erro: "Nome é obrigatório" ou similar
- Campo "Nome" é destacado com borda vermelha
- Usuário permanece na página de cadastro

---

### CT-006: Senha Obrigatória Vazia

**Cenário:** Tentar cadastrar sem preenchimento da senha

**Pré-condição:**
- Usuário está na página de cadastro
- Campo senha está vazio

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Ana Silva"
3. Deixar campo "Senha" vazio
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagem de erro: "Senha é obrigatória" ou similar
- Campo "Senha" é marcado como erro
- Usuário permanece na página

---

### CT-007: Confirmação de Senha Obrigatória Vazia

**Cenário:** Tentar cadastrar sem confirmação de senha

**Pré-condição:**
- Usuário está na página de cadastro
- Campo confirmação senha está vazio

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Roberto Alves"
3. Preencher campo "Senha" com "Teste@123"
4. Deixar campo "Confirmação senha" vazio
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagem de erro: "Confirmação de senha é obrigatória" ou similar
- Campo "Confirmação senha" é destacado
- Usuário permanece na página de cadastro

---

### CT-008: Todos os Campos Obrigatórios Vazios

**Cenário:** Tentar cadastrar com todos os campos vazios

**Pré-condição:**
- Usuário está na página de cadastro
- Todos os campos estão vazios

**Passos:**
1. Não preencher nenhum campo
2. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagens de erro para todos os campos obrigatórios
- Todos os campos vazios são destacados
- Usuário permanece na página

---

## CENÁRIOS DE VALIDAÇÃO DE SENHA

### CT-009: Senhas Diferentes - Não Coincidem

**Cenário:** Tentar cadastrar com senhas que não coincidem

**Pré-condição:**
- Usuário está na página de cadastro
- As senhas nos dois campos são diferentes

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Lucia Ferreira"
3. Preencher campo "Senha" com "Senha@123"
4. Preencher campo "Confirmação senha" com "Diferente@456"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe mensagem de erro: "As senhas não conferem" ou similar
- Campos de senha são destacados
- Usuário permanece na página para corrigir as senhas

---

### CT-010: Senhas Parcialmente Diferentes

**Cenário:** Senhas com apenas um caractere diferente

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Felipe Martins"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@124" (último dígito diferente)
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe erro: "As senhas não coincidem"
- Nenhuma conta é criada
- Usuário deve digitar as senhas novamente

---

### CT-011: Diferença de Case-Sensitive (Maiúscula/Minúscula)

**Cenário:** Senhas diferem apenas em maiúsculas/minúsculas

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Marcela Oliveira"
3. Preencher campo "Senha" com "teste@123"
4. Preencher campo "Confirmação senha" com "TESTE@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe erro: "As senhas não conferem" (senhas são case-sensitive)
- Usuário precisa corrigir as senhas

---

## CENÁRIOS DE BORDA - COMPRIMENTO DE CAMPOS

### CT-012: Senha Muito Curta

**Cenário:** Testar se há validação de comprimento mínimo de senha

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Gabriel Santos"
3. Preencher campo "Senha" com "Ab1" (3 caracteres)
4. Preencher campo "Confirmação senha" com "Ab1"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Se houver validação: exibir erro "Senha deve ter mínimo 8 caracteres"
- Se não houver validação: cadastro é aceito com sucesso
- Documentar o comportamento observado

---

### CT-013: Senha Muito Longa

**Cenário:** Testar limite máximo de caracteres da senha

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "Fernanda Lima"
3. Preencher campo "Senha" com 100 caracteres (Ex: A@1bBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBbBb)
4. Preencher campo "Confirmação senha" com os mesmos 100 caracteres
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Se houver limite: erro exibido "Máximo de caracteres excedido"
- Se não houver limite: cadastro é realizado com sucesso
- Documentar comportamento observado

---

### CT-014: Nome com Caracteres Especiais

**Cenário:** Aceitar nomes com acentos e caracteres especiais

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "José da Silva-Júnior"
3. Preencher campo "Senha" com "Segura@123"
4. Preencher campo "Confirmação senha" com "Segura@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Cadastro é realizado com sucesso
- Nome é armazenado corretamente com acentos e hífen
- Número da conta é exibido

---

### CT-015: Nome com Espaços em Branco Extras

**Cenário:** Testar como o sistema trata espaços extras no nome

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@bugbank.com"
2. Preencher campo "Nome" com "  João  Silva  " (espaços no início e fim)
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Cadastro é realizado com sucesso
- Sistema faz trim dos espaços e armazena "João Silva"
- Número da conta é exibido

---

## CENÁRIOS DE VALIDAÇÃO DE EMAIL

### CT-016: Email Inválido - Sem Arroba

**Cenário:** Tentar cadastrar com email sem símbolo @

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuariobugbank.com" (sem @)
2. Preencher campo "Nome" com "Daniela Costa"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe erro: "Email inválido" ou similar
- Campo email é destacado
- Usuário permanece na página

---

### CT-017: Email Inválido - Sem Domínio

**Cenário:** Email com @ mas sem domínio válido

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com "usuario@" (sem domínio)
2. Preencher campo "Nome" com "Tatiana Rocha"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe erro: "Email inválido" ou "Domínio de email inválido"
- Usuário permanece na página

---

### CT-018: Email Duplicado

**Cenário:** Tentar registrar com email já cadastrado

**Pré-condição:**
- Email "existente@bugbank.com" já está registrado no sistema

**Passos:**
1. Preencher campo "Email" com "existente@bugbank.com"
2. Preencher campo "Nome" com "Novo Usuario"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Formulário não é submetido
- Sistema exibe erro: "Email já cadastrado no sistema" ou similar
- Campo email é destacado
- Usuário é orientado a usar outro email ou fazer login

---

### CT-019: Email com Espaços em Branco

**Cenário:** Email com espaços no início ou fim

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Email" com " usuario@bugbank.com " (com espaços)
2. Preencher campo "Nome" com "Vanessa Alves"
3. Preencher campo "Senha" com "Teste@123"
4. Preencher campo "Confirmação senha" com "Teste@123"
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Cadastro é realizado com sucesso
- Sistema faz trim dos espaços: "usuario@bugbank.com"
- Número da conta é exibido

---

## CENÁRIOS DE CHECKBOX "CRIAR CONTA COM SALDO"

### CT-020: Alternar Checkbox Múltiplas Vezes

**Cenário:** Marcar e desmarcar o checkbox várias vezes

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher todos os campos corretamente
2. Marcar checkbox "Criar conta com saldo"
3. Desmarcar checkbox
4. Marcar checkbox novamente
5. Clicar no botão "Cadastrar"

**Resultado Esperado:**
- Checkbox final estar marcado
- Cadastro realizado com saldo de R$1.000,00
- Número da conta exibido corretamente

---

### CT-021: Verificar Saldo Imediatamente Após Cadastro

**Cenário:** Confirmar saldo correto após criar conta

**Pré-condição:**
- Usuário realizou cadastro com sucesso

**Passos:**
1. Após receber número da conta, fazer login com as credenciais
2. Acessar dashboard ou extrato da conta
3. Verificar saldo inicial

**Resultado Esperado:**
- Se checkbox estava marcado: saldo = R$1.000,00
- Se checkbox estava desmarcado: saldo = R$0,00
- Saldo corresponde à escolha feita no cadastro

---

## CENÁRIOS DE FLUXO E NAVEGAÇÃO

### CT-022: Voltar ao Login Após Navegar em Cadastro

**Cenário:** Cancelar cadastro e retornar à página de login

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher alguns campos (ex: Email e Nome)
2. Clicar no link/botão "Voltar ao login"
3. Verificar se voltou para página de login

**Resultado Esperado:**
- Usuário é redirecionado para a página de login
- Dados preenchidos não são salvos
- Formulário de login está limpo e pronto para nova entrada

---

### CT-023: Validação em Tempo Real

**Cenário:** Verificar se há validação enquanto o usuário digita

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Clicar no campo "Email"
2. Digitar "usuario" sem @
3. Sair do campo (blur)
4. Observar se há mensagem de erro
5. Corrigir para "usuario@bugbank.com"
6. Observar se erro desaparece

**Resultado Esperado:**
- Sistema exibe/remove mensagens de erro em tempo real (se implementado)
- Ou apenas valida ao clicar em "Cadastrar"
- Documentar comportamento observado

---

## CENÁRIOS DE SEGURANÇA

### CT-024: Senha Não Visível por Padrão

**Cenário:** Validar que a senha é mascarada

**Pré-condição:**
- Usuário está na página de cadastro

**Passos:**
1. Preencher campo "Senha" com "Teste@123"
2. Observar o campo de senha
3. Verificar o campo "Confirmação senha"

**Resultado Esperado:**
- Ambos os campos de senha mostram pontos (•••) ou asteriscos (***) em vez do texto real
- Senha não é visível para pessoas observando a tela
- Ícone de "olho" (show/hide password) está disponível

---

### CT-025: Mostrar/Ocultar Senha

**Cenário:** Testar funcionalidade de toggle de visibilidade de senha

**Pré-condição:**
- Usuário preencheu campo de senha

**Passos:**
1. Preencher campo "Senha" com "Teste@123"
2. Clicar no ícone de "olho" para mostrar a senha
3. Verificar se a senha fica visível
4. Clicar novamente para ocultar
5. Verificar se volta a ser mascarada

**Resultado Esperado:**
- Ao clicar no ícone, a senha fica visível (texto claro)
- Ao clicar novamente, é mascarada novamente
- Ícone muda de aparência (ex: "olho aberto" para "olho fechado")

---

## CENÁRIOS DE INTEGRAÇÃO DE DADOS

### CT-026: Dados Armazenados em Local Storage

**Cenário:** Verificar se dados são mantidos após refresh (se aplicável)

**Pré-condição:**
- Usuário preencheu formulário mas não enviou

**Passos:**
1. Preencher todos os campos do formulário
2. Fazer F5 ou refresh da página
3. Observar se os dados permanecem ou são limpos

**Resultado Esperado:**
- Dados devem ser limpos após refresh (não deve haver salvamento automático)
- Formulário aparece vazio
- Comportamento seguro: dados sensíveis não são salvos

---

### CT-027: Conta Criada é Verificável no Login

**Cenário:** Confirmar que conta criada pode fazer login imediatamente

**Pré-condição:**
- Usuário criou conta com sucesso

**Passos:**
1. Anotar Email e Senha utilizados no cadastro
2. Voltar à página de login
3. Preencher Email: "novo.usuario@bugbank.com"
4. Preencher Senha: "Senha@123"
5. Clicar em "Acessar"

**Resultado Esperado:**
- Login é realizado com sucesso
- Acesso à conta com dados corretos
- Dashboard da conta é exibido com o número correto

---

## CASOS DE TESTE PARA TRATAMENTO DE ERROS

### CT-028: Submissão do Formulário Duplicado (Double Click)

**Cenário:** Evitar cadastro duplicado por click duplo no botão

**Pré-condição:**
- Usuário preencheu todos os campos corretamente

**Passos:**
1. Preencher todos os campos
2. Fazer double-click no botão "Cadastrar" rapidamente
3. Observar o comportamento

**Resultado Esperado:**
- Apenas uma conta é criada
- Número de conta é exibido uma única vez
- Não há duplicação de registro
- Botão pode estar desabilitado durante submissão

---

### CT-029: Submissão com Conexão Lenta (Timeout)

**Cenário:** Testar comportamento em conexão lenta

**Pré-condição:**
- Usuário preencheu formulário
- Conexão de internet está lenta

**Passos:**
1. Preencher todos os campos
2. Simular conexão lenta (DevTools)
3. Clicar em "Cadastrar"
4. Aguardar resultado

**Resultado Esperado:**
- Mensagem de loading é exibida
- Após alguns segundos, resultado é apresentado
- Ou mensagem de timeout é exibida se demorar muito
- Usuário pode tentar novamente

---

### CT-030: Resposta do Servidor com Erro 500

**Cenário:** Tratar erros de servidor durante o cadastro

**Pré-condição:**
- Servidor está retornando erro 500

**Passos:**
1. Preencher todos os campos corretamente
2. Clicar em "Cadastrar"
3. Servidor retorna erro 500

**Resultado Esperado:**
- Sistema exibe mensagem: "Erro no servidor. Tente novamente."
- Usuário consegue tentar novamente
- Dados do formulário podem ser preservados para nova tentativa

---

## RESUMO DOS CENÁRIOS DE TESTE

| ID | Cenário | Tipo | Status |
|----|---------|------|--------|
| CT-001 | Cadastro com Saldo | Sucesso | Não Testado |
| CT-002 | Cadastro sem Saldo | Sucesso | Não Testado |
| CT-003 | Email Múltiplos Domínios | Sucesso | Não Testado |
| CT-004 | Email Vazio | Validação | Não Testado |
| CT-005 | Nome Vazio | Validação | Não Testado |
| CT-006 | Senha Vazia | Validação | Não Testado |
| CT-007 | Confirmação Senha Vazia | Validação | Não Testado |
| CT-008 | Todos os Campos Vazios | Validação | Não Testado |
| CT-009 | Senhas Diferentes | Validação | Não Testado |
| CT-010 | Senhas Parcialmente Diferentes | Validação | Não Testado |
| CT-011 | Case-Sensitive Diferente | Validação | Não Testado |
| CT-012 | Senha Muito Curta | Borda | Não Testado |
| CT-013 | Senha Muito Longa | Borda | Não Testado |
| CT-014 | Nome com Acentos | Borda | Não Testado |
| CT-015 | Nome com Espaços Extras | Borda | Não Testado |
| CT-016 | Email sem Arroba | Validação | Não Testado |
| CT-017 | Email sem Domínio | Validação | Não Testado |
| CT-018 | Email Duplicado | Validação | Não Testado |
| CT-019 | Email com Espaços | Borda | Não Testado |
| CT-020 | Toggle Checkbox | Funcionalidade | Não Testado |
| CT-021 | Verificar Saldo | Integração | Não Testado |
| CT-022 | Voltar ao Login | Navegação | Não Testado |
| CT-023 | Validação em Tempo Real | Funcionalidade | Não Testado |
| CT-024 | Senha Mascarada | Segurança | Não Testado |
| CT-025 | Show/Hide Senha | Funcionalidade | Não Testado |
| CT-026 | Local Storage | Integração | Não Testado |
| CT-027 | Login Pós-Cadastro | Integração | Não Testado |
| CT-028 | Double Click | Tratamento Erro | Não Testado |
| CT-029 | Conexão Lenta | Tratamento Erro | Não Testado |
| CT-030 | Erro Servidor 500 | Tratamento Erro | Não Testado |

---

## NOTAS IMPORTANTES

1. **Prioridade de Testes:** Os cenários CT-001, CT-002, CT-004 a CT-011, CT-016 a CT-018 devem ser executados com prioridade alta.

2. **Ambiente de Teste:** Todos os testes devem ser executados em um ambiente de desenvolvimento/QA com dados limpos.

3. **Documentação:** Cada teste executado deve ser documentado com screenshot (em caso de erro) e resultado observado.

4. **Browsers:** Testar em Chrome, Firefox e Safari para validar compatibilidade cross-browser.

5. **Responsividade:** Validar formulário em desktop (1920x1080) e mobile (375x667) para responsividade.

6. **Dados Persistência:** Bug Bank usa Local Storage, portanto, limpar dados entre rodadas de teste.

---

**Preparado por:** QA Senior  
**Data:** 23/07/2026  
**Versão:** 1.0
