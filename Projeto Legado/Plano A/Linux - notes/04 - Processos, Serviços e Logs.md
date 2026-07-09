---
tags: [linux, processos, systemd, logs]
---

# 04 - Processos, Serviços e Logs

- **Grau**: CO – Conhecimento Obrigatório
- **Objetivo**: entender o que está rodando, como encerrar processos travados e lidar com serviços no Arch.

[[00 - Roadmap Linux]]

---

## Assuntos

- Conceito de **processo**, **PID**, **PPID**, **estado** – **CO**
- Comandos: `ps`, `top` ou `htop`, `kill`, `pkill` – **CO**
- `systemd` básico: `systemctl status/start/stop/enable` – **CO**
- Logs com `journalctl` – **MR**

---

## Check-list

- [ ] Sei listar processos meus e do sistema (`ps`, `top`/`htop`)
- [ ] Sei encontrar um processo específico pelo nome
- [ ] Sei encerrar um processo travado com segurança usando `kill`/`pkill`
- [ ] Sei verificar o status de um serviço usando `systemctl status`
- [ ] Sei ver os logs recentes do sistema com `journalctl -xe`

---

## Exercícios

**Exercício 1 – Matando um processo travado**

1. Abra um programa gráfico qualquer (por exemplo `firefox`).  
2. Use `ps`, `ps aux | grep`, ou `htop` para encontrar o **PID** desse processo.  
3. Encerre o processo via linha de comando (usando `kill` ou `pkill`).  
4. Anote aqui:
   - Comandos que usou para encontrar o PID  
   - Comando que usou para encerrar o processo  
   - Como verificou que ele realmente encerrou.

**Exercício 2 – Inspecionando serviços**

1. Use `systemctl` para checar o status de pelo menos **3 serviços importantes** no Arch (ex: `NetworkManager`, `sshd` ou `ssh`, `bluetooth`).  
2. Para cada serviço, anote:
   - Se está **ativo (running)** ou não  
   - Se está **habilitado** para iniciar com o sistema (`enabled`/`disabled`)  
3. Se quiser, use `journalctl -u <serviço>` para ver os logs mais recentes de um deles e anotar qualquer erro interessante.

---

## Resumo (para preencher depois de estudar)

- Como identificar o que está travando o sistema:
  - 
- Passo a passo que vou seguir quando algo travar:
  - 
- Serviços que descobri que são importantes no meu Arch:
  - 

