# 📄 ESCÓPIO DE PROJETO: SISTEMA INTERNO "CONTROLBIZ"

**Empresa:** ControlBiz Soluções Internas  
**Segmento:** A empresa presta serviços de consultoria financeira e precisa de um sistema interno para gerenciar seus clientes, contratos e tarefas.

## 1. O Problema (A Dor do Cliente)

A ControlBiz está crescendo e hoje controla tudo em planilhas do Excel. Isso está causando:

- **Dados duplicados:** Clientes aparecem duas vezes.
    
- **Perda de prazos:** Eles esquecem de renovar contratos.
    
- **Sem histórico:** Não sabem quais serviços já foram prestados para um cliente antigo.
    

Sua missão: Criar a primeira versão (MVP - Produto Mínimo Viável) do sistema deles.

## 2. Regras de Negócio (O que o sistema precisa fazer)

### Módulo 1: Cadastro de Clientes

- A empresa atende dois tipos de cliente: **Pessoa Física (PF)** e **Pessoa Jurídica (PJ)** .
    
- **PF:** Nome, CPF (único), Data de Nascimento, Telefone, Email.
    
- **PJ:** Razão Social, Nome Fantasia, CNPJ (único), Telefone, Email.
    
- **Regra:** Um cliente PF não pode ter o mesmo CPF de outro. Um cliente PJ não pode ter o mesmo CNPJ.
    
- **Regra:** Ao cadastrar, o sistema deve gerar automaticamente uma data de "cadastro" (hoje).
    

### Módulo 2: Contratos

- Um contrato pertence a um único cliente (PF ou PJ).
    
- **Dados do contrato:** Número do contrato (gerado automaticamente), Data de Início, Data de Fim, Valor Mensal, Status (Ativo, Inativo, Suspenso).
    
- **Regra:** Um cliente pode ter vários contratos, mas só pode ter um contrato "Ativo" por vez.
    
- **Regra:** Se a data de fim for menor que a data de hoje, o status deve ser automaticamente "Inativo".
    

### Módulo 3: Tarefas (To-Do Interno)

- Cada contrato gera tarefas recorrentes.
    
- **Dados da tarefa:** Descrição (ex: "Entregar relatório mensal"), Data de Vencimento, Responsável, Status (Pendente, Concluída).
    
- **Regra:** Ao criar um contrato, o sistema deve gerar automaticamente uma tarefa chamada "Reunião de alinhamento" com vencimento em 7 dias após o início do contrato.
    

## 3. O que você PRECISA entregar (Requisitos Técnicos)

1. **Linguagem:** Java (Vanilla, sem Spring ainda) ou JavaScript (Node.js ou puro).
    
2. **Armazenamento:** Para este nível, use listas em memória (`ArrayList` no Java, `arrays` no JS). Nada de banco de dados ainda.
    
3. **Interação:** Deve rodar no terminal (CRUD básico via console).
    
    - Menu: [1] Cadastrar Cliente, [2] Listar Clientes, [3] Criar Contrato, [4] Listar Contratos de um Cliente, [5] Ver Tarefas Pendentes, [0] Sair.
        
4. **Validações:** O sistema não pode quebrar (dar erro) se o usuário digitar uma letra onde deveria ser número ou um CPF já existente. Trate isso.
    

## 4. 🕳️ Armadilhas (Desafios escondidos)

- **Herança:** PF e PJ são tipos de Cliente. Como você vai modelar isso? (Dica: Classe abstrata ou interface?)
    
- **Data:** Como você vai comparar datas (para saber se o contrato venceu) sem usar bibliotecas externas? (Dica: `LocalDate` no Java).
    
- **Associação:** Como garantir que um contrato "pertence" a um cliente específico? O contrato deve ter uma referência ao objeto Cliente, não apenas uma String com o nome.
    
- **Estado:** Como você vai mudar o status do contrato automaticamente baseado na data?
    

## 5. 📈 Marcos de Evolução (Versões)

- **Versão 1 (Hoje):** Fazer apenas o cadastro de clientes (PF e PJ) funcionar com validação de CPF/CNPJ duplicado.
    
- **Versão 2 (Semana 1):** Adicionar o módulo de contratos e a regra de "apenas um ativo por cliente".
    
- **Versão 3 (Semana 2):** Adicionar o módulo de tarefas e a geração automática da tarefa de "reunião".
    
- **Versão 4 (Desafio Final):** Adicionar relatórios simples (ex: "Qual cliente tem a maior soma de valores de contratos?").