---
tags: [linux, arch, pacman, aur]
---

# 05 - Gerenciamento de Pacotes no Arch

- **Grau**: CO – Conhecimento Obrigatório
- **Objetivo**: instalar, remover e atualizar pacotes no Arch com segurança.

[[00 - Roadmap Linux]]

---

## Assuntos

- `pacman`: instalar, remover, procurar, atualizar – **CO**
- O que é **AUR** e helpers (ex: `yay`, `paru`) – **MR**
- Leitura básica de `/etc/pacman.conf` – **MR**

---

## Check-list

- [ ] Sei instalar/remover pacotes com `pacman -S` e `pacman -R`
- [ ] Sei atualizar o sistema (`pacman -Syu`) e entendo os riscos de forçar updates
- [ ] Sei pesquisar pacotes com `pacman -Ss` (remoto) e `pacman -Qs` (local)
- [ ] Sei o fluxo básico de instalação via AUR (se eu usar helper)
- [ ] Sei onde fica e para que serve `/etc/pacman.conf`

---

## Exercícios

**Exercício 1 – Ciclo instalar/usar/remover**

1. Escolha um pacote que você ainda não tem instalado (ex: algum editor de texto, player de música ou ferramenta de linha de comando).  
2. Use `pacman -Ss` para encontrar esse pacote.  
3. Instale o pacote com `pacman -S`.  
4. Teste o programa rapidamente.  
5. Remova o pacote com `pacman -R` (ou `-Rs` se quiser remover dependências não usadas).  
6. Anote aqui:
   - Nome do pacote  
   - Comandos usados  
   - Alguma observação que achou importante.

**Exercício 2 – Lista de pacotes explicitamente instalados**

1. Gere uma lista dos pacotes **explicitamente instalados** e salve em um arquivo:  
   - Exemplo: `pacman -Qe > ~/pacotes.txt`
2. Anote aqui:
   - O comando exato que você usou  
   - Em que pasta salvou o arquivo  
   - Para que essa lista pode ser útil (por exemplo: backup de ambiente).

---

## Resumo (para preencher depois de estudar)

- Comandos de `pacman` que vou usar no dia a dia:
  - 
- Boas práticas que quero seguir ao atualizar o sistema:
  - 
- O que aprendi sobre AUR e helpers:
  - 

