# Bug Bank - Portfólio de QA

## 📌 Sobre Este Repositório

Este repositório faz parte do meu **portfólio de QA Junior** e documenta meus estudos e prática em testes de software, com foco em **testes funcionais, validação de requisitos e garantia de qualidade** de aplicações web.

O projeto utiliza o **Bug Bank**, uma plataforma bancária digital intencional com bugs e falhas, criada especificamente para fins de prática em QA e testes.

---

## 🎯 Objetivo

Demonstrar minha capacidade de:

- ✅ **Análise de requisitos** - Compreender e documentar funcionalidades
- ✅ **Design de casos de teste** - Criar testes estruturados e abrangentes
- ✅ **Cobertura de testes** - Incluir cenários de sucesso, validação e casos extremos
- ✅ **Identificação de bugs** - Encontrar e documentar falhas
- ✅ **Documentação profissional** - Preparar relatórios claros e objetivos
- ✅ **Teste manual** - Validar funcionalidades no navegador
- ✅ **Boas práticas de QA** - Seguir padrões da indústria

---

## 📂 Estrutura do Projeto

```
bugbank-qa/
├── README.md                                    # Este arquivo
├── casos_teste_cadastro.md                     # Casos de teste em Markdown
└── Casos_Teste_Bug_Bank_Cadastro.pdf           # Casos de teste em PDF
```

---

## 🔍 Documentação Disponível

### **Casos de Teste - Formulário de Cadastro**

Documento abrangente com **30 casos de teste** para validar o formulário de registro (signup) do Bug Bank.

**Arquivo:** `Casos_Teste_Bug_Bank_Cadastro.pdf`

#### Categorias de Testes Inclusos:

| Categoria | Quantidade | Detalhes |
|-----------|-----------|----------|
| **Cenários de Sucesso** | 3 | Cadastro com/sem saldo, múltiplos domínios |
| **Campos Obrigatórios** | 5 | Validação de email, nome, senha vazios |
| **Validação de Senha** | 3 | Correspondência, case-sensitive, parcialmente diferentes |
| **Casos de Borda** | 4 | Comprimento, acentos, espaços em branco |
| **Validação de Email** | 4 | Formato inválido, duplicado, sem domínio |
| **Checkbox de Saldo** | 2 | Toggle múltiplo, verificação de saldo |
| **Fluxo e Navegação** | 2 | Cancelamento, validação em tempo real |
| **Segurança** | 2 | Mascaramento de senha, visibilidade |
| **Integração de Dados** | 2 | Local Storage, login pós-cadastro |
| **Tratamento de Erros** | 3 | Double-click, timeout, erro 500 |

---

## 📋 Formato dos Casos de Teste

Cada caso de teste segue a estrutura profissional:

```
Cenário: [Descrição do teste]
Pré-condição: [Estado inicial necessário]
Passos: [Ações numeradas do usuário]
Resultado Esperado: [Comportamento esperado do sistema]
```

**Exemplo:**

```
CT-001: Cadastro Bem-Sucedido - Conta Com Saldo

Cenário: Registrar nova conta com saldo inicial de R$1.000,00

Pré-condição:
- Usuário está na página de cadastro do Bug Bank
- Formulário está limpo (nenhum campo preenchido)
- Checkbox "Criar conta com saldo" está visível

Passos:
1. Preencher campo "Email" com "usuario.teste@bugbank.com"
2. Preencher campo "Nome" com "João Silva"
3. Preencher campo "Senha" com "Senha@123"
4. Preencher campo "Confirmação senha" com "Senha@123"
5. Marcar checkbox "Criar conta com saldo"
6. Clicar no botão "Cadastrar"

Resultado Esperado:
- Formulário é submetido com sucesso
- Sistema exibe número da conta criada (ex: "Conta criada: 123456")
- Saldo inicial da conta é R$1.000,00
- Usuário é redirecionado para página de login ou dashboard da conta
```

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

- **Bug Bank** - Aplicação alvo de testes
  - URL: https://bugbank.netlify.app
  - Requisitos: https://bugbank.netlify.app/requirements

- **Ferramentas de Teste:**
  - Navegador (Chrome/Firefox/Safari)
  - DevTools para análise
  - Local Storage inspection

- **Documentação:**
  - Markdown (.md)
  - PDF (ReportLab)
  - Git/GitHub para versionamento

---

## 📖 Campos Testados

### Formulário de Cadastro

| Campo | Tipo | Obrigatório | Validações |
|-------|------|------------|-----------|
| **Email** | Text | ✓ Sim | Formato válido, sem duplicatas |
| **Nome** | Text | ✓ Sim | Aceita acentos e caracteres especiais |
| **Senha** | Password | ✓ Sim | Deve ser mascarada, case-sensitive |
| **Confirmação de Senha** | Password | ✓ Sim | Deve coincidir com Senha |
| **Criar Conta com Saldo** | Checkbox | ✗ Não | R$1.000 quando marcado, R$0 quando não |

---

## ✅ Critérios de Teste

Os casos de teste cobrem:

- ✓ **Funcionalidade** - Testa o comportamento esperado
- ✓ **Validação** - Verifica regras de negócio e constraints
- ✓ **Segurança** - Avalia proteção de dados sensíveis
- ✓ **Usabilidade** - Valida experiência do usuário
- ✓ **Integração** - Confirma persistência de dados
- ✓ **Tratamento de Erros** - Verifica comportamento em falhas
- ✓ **Edge Cases** - Testa situações extremas e incomuns

---

## 🚀 Como Utilizar

### 1. Visualizar os Casos de Teste

**Opção A - Formato PDF (Recomendado)**
```
Abrir: Casos_Teste_Bug_Bank_Cadastro.pdf
```

**Opção B - Formato Markdown**
```
Abrir: casos_teste_cadastro.md
```

### 2. Executar os Testes

1. Acesse https://bugbank.netlify.app
2. Navegue até o formulário de cadastro
3. Execute os casos de teste na ordem de prioridade
4. Documente os resultados (Pass/Fail)
5. Capture screenshots de erros/comportamentos inesperados

### 3. Reportar Bugs

Para cada bug encontrado, documente:
- ID do caso de teste (CT-XXX)
- Passos para reproduzir
- Comportamento observado
- Comportamento esperado
- Screenshots/evidência
- Severidade (Alta/Média/Baixa)

---

## 📊 Prioridade de Testes

### 🔴 Alta Prioridade
Executar em primeiro lugar:
- CT-001, CT-002 (Cenários de sucesso)
- CT-004 a CT-011 (Validação de campos obrigatórios e senha)
- CT-016 a CT-018 (Validação de email)
- CT-024, CT-027 (Segurança e integração)

### 🟡 Média Prioridade
Executar em seguida:
- CT-003 (Múltiplos domínios)
- CT-012 a CT-015 (Casos de borda)
- CT-019 a CT-023 (Funcionalidade)
- CT-025, CT-028, CT-030 (Outras funcionalidades)

### 🟢 Baixa Prioridade
Executar conforme disponibilidade:
- CT-026 (Local Storage)
- CT-029 (Conexão lenta)

---

## 📝 Notas Importantes

1. **Ambiente Limpo** - Sempre iniciar testes com dados limpos
2. **Clear Cache** - Limpar Local Storage entre rodadas (F12 → Application)
3. **Cross-Browser** - Testar em Chrome, Firefox e Safari
4. **Responsividade** - Validar em desktop (1920x1080) e mobile (375x667)
5. **Documentação** - Registrar evidências de testes realizados
6. **Regression** - Após correções, executar testes de regressão

---

## 🎓 Aprendizados

Este projeto me permitiu praticar:

- Análise sistemática de requisitos
- Criação de casos de teste estruturados
- Identificação de casos extremos (edge cases)
- Documentação profissional de testes
- Compreensão de fluxos de negócio
- Validação de regras de negócio
- Testes de segurança básicos

---

## 📚 Referências

- **Bug Bank:** https://bugbank.netlify.app
- **Requisitos:** https://bugbank.netlify.app/requirements

---

## 👤 Autor

**Gustavo Jacob**  
QA Junior Portfolio  
Email: vanio.insight@gmail.com

---

## 📅 Histórico

| Versão | Data | Descrição |
|--------|------|-----------|
| 1.0 | 23/07/2026 | Criação inicial com 30 casos de teste para formulário de cadastro |

---

## 📄 Licença

Este repositório é parte do meu portfólio educacional de QA.

---

**Última atualização:** 23/07/2026
