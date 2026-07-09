---
tags: [linux, permissoes, usuarios, grupos]
---

# 03 - Permissões, Usuários e Grupos

- **Grau**: CO – Conhecimento Obrigatório
- **Objetivo**: entender por que “Permission denied” acontece e como lidar com isso.

[[00 - Roadmap Linux]]

---

## Assuntos

- Conceitos de **usuário**, **grupo**, **root** – **CO**
- Permissões `rwx` e notação octal (`chmod 754`) – **CO**
- Comandos: `id`, `whoami`, `sudo`, `chown`, `chmod`, `chgrp` – **CO**
- Arquivo `sudoers` (noções básicas, sem alterar muito) – **MR**

---

## Check-list

- [ ] Sei ler a saída de `ls -l` e interpretar algo como `-rwxr-x---`
- [ ] Sei quando devo usar `sudo` e quando **não** devo usar
- [ ] Sei mudar permissões de um arquivo de forma consciente com `chmod`
- [ ] Sei verificar quais grupos eu pertenço (`id`)
- [ ] Entendo o risco de alterar permissões em `/` e `/etc`

---

## Exercícios

**Exercício 1 – Arquivo secreto**

1. Crie um arquivo `segredo.txt` em `~/lab_linux/docs`.  
2. Ajuste as permissões para que ele seja acessível **apenas para você** (leitura + escrita).  
3. Anote aqui:
   - Comandos que usou (`touch`, `chmod`, etc.)
   - Qual ficou a permissão final (ex: `-rw-------` ou `600`).

**Exercício 2 – Analisando um binário do sistema**

1. Rode: `ls -l /bin/bash`  
2. Anote:
   - Quem é o dono do arquivo  
   - Quais são as permissões para **dono/grupo/outros**  
   - Por que isso faz sentido para um binário do sistema? (explique com suas palavras)

---

## Resumo (para preencher depois de estudar)

- O que eu aprendi sobre permissões:
  - 
- Principais comandos que vou usar no dia a dia:
  - 
- Situações onde devo ter cuidado especial:
  - 

