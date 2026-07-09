---
tags: [linux, filesystem, cli]
---

# 02 - Sistema de Arquivos e CLI Essencial

- **Grau**: CO – Conhecimento Obrigatório
- **Objetivo**: navegar e manipular arquivos com segurança usando o terminal.

[[00 - Roadmap Linux]]

---

## Assuntos

- **Hierarquia FHS** (`/`, `/home`, `/etc`, `/var`, `/usr`...) – **CO**
- Comandos básicos: `pwd`, `ls`, `cd`, `cp`, `mv`, `rm`, `mkdir`, `rmdir` – **CO**
- Visualização de arquivos: `cat`, `less`, `head`, `tail` – **CO**
- Globs (`*`, `?`) e caminhos **relativos/absolutos** – **MR**

---

## Check-list

- [ ] Sei a diferença entre **caminho absoluto** e **caminho relativo**
- [ ] Sei listar arquivos ocultos (`ls -a`) e com detalhes (`ls -lh`)
- [ ] Consigo criar, mover e apagar diretórios apenas com o terminal
- [ ] Sei usar `less` para ler arquivos grandes (logs/configs)
- [ ] Sei o propósito das principais pastas em `/` (/, /home, /etc, /var, /usr)

---

## Exercícios

**Exercício 1 – Laboratório de arquivos**

No seu diretório pessoal:

1. Crie uma estrutura de teste:
   - `~/lab_linux/{docs,bin,logs}`
2. Crie pelo menos 3 arquivos de texto dentro de `docs`.
3. Mova e copie esses arquivos entre `docs`, `bin` e `logs` usando **somente o terminal**.
4. Anote aqui quais comandos usou (exemplo: `mkdir -p`, `touch`, `cp`, `mv`, `rm` etc.).

**Exercício 2 – Lendo logs**

1. Abra um log do sistema com `less` (por exemplo: `/var/log/pacman.log`).  
2. Responda:
   - Qual foi o **último pacote** instalado/atualizado que aparece no log?
   - Qual comando você usaria para ver **somente as últimas 20 linhas** desse arquivo?
3. Escreva os comandos aqui e uma pequena explicação.

---

## Resumo (para preencher depois de estudar)

- Comandos que mais usei:
  - 
- Pastas do sistema que eu entendi melhor:
  - 
- Erros que cometi e como corrigi:
  - 

