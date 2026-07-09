---
tags: [linux, shell, bash, automatizacao]
---

# 07 - Shell, Alias e Automatização Simples

- **Grau**: MR – Muito Recomendado (com partes OA – Opcional/Avançado)
- **Objetivo**: usar o shell a seu favor, criando atalhos e pequenos scripts.

[[00 - Roadmap Linux]]

---

## Assuntos

- Variáveis de ambiente, histórico, autocomplete – **MR**
- Aliases (`alias ll='ls -lh'`) – **MR**
- Scripts simples em bash (`.sh`, `chmod +x`) – **MR**
- Funções no shell, arquivos de configuração (`~/.bashrc`, `~/.zshrc`) – **OA**

---

## Check-list

- [ ] Sei criar um `alias` temporário no shell
- [ ] Sei tornar um `alias` permanente editando o arquivo de configuração do shell
- [ ] Sei criar um script simples com shebang (`#!/usr/bin/env bash`)
- [ ] Sei tornar um script executável com `chmod +x`
- [ ] Sei em qual arquivo (ex: `~/.bashrc` ou `~/.zshrc`) devo colocar minhas configurações

---

## Exercícios

**Exercício 1 – Alias produtivo**

1. Crie um `alias` que liste o diretório atual em formato longo, legível e mostrando arquivos ocultos, por exemplo:
   - `ls -lah`
2. Torne esse alias **permanente**, adicionando-o ao arquivo de configuração do seu shell (ex: `~/.bashrc` ou `~/.zshrc`).  
3. Anote aqui:
   - Nome do alias (ex: `ll`)  
   - Linha exata adicionada no arquivo  
   - Qual arquivo você editou.

**Exercício 2 – Script de backup das notas**

1. Crie um script chamado `backup_notas.sh` em alguma pasta (por exemplo `~/bin` ou `~/scripts`):  
   - O script deve comprimir sua pasta de notas Linux (`/home/dev/Obsidian/Projeto Legado/Plano A/Linux - notes` ou caminho equivalente)  
   - O nome do arquivo `.tar.gz` deve incluir um **timestamp** (ex: `backup_linux_2026-03-09_1200.tar.gz`)  
   - O arquivo deve ser salvo em `~/backups` (crie a pasta se não existir).
2. Dê permissão de execução ao script (`chmod +x backup_notas.sh`).  
3. Rode o script e confirme que o arquivo foi criado.  
4. Anote aqui:
   - Caminho completo do script  
   - Comando usado para executar  
   - Nome do arquivo de backup gerado.

---

## Resumo (para preencher depois de estudar)

- Aliases que mais vão me ajudar no dia a dia:
  - 
- Scripts que pretendo criar no futuro:
  - 
- Ideias de automatização para meu ambiente Arch:
  - 

