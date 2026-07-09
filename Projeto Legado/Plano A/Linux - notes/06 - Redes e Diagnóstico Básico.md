---
tags: [linux, redes, diagnostico]
---

# 06 - Redes e Diagnóstico Básico

- **Grau**: MR – Muito Recomendado
- **Objetivo**: saber verificar conexão, IP, DNS e identificar problemas comuns de rede.

[[00 - Roadmap Linux]]

---

## Assuntos

- `ip a`, `ip route` (interfaces de rede e rotas) – **MR**
- `ping`, `traceroute` ou `tracepath` – **MR**
- Ferramentas de rede do sistema (ex: `nmcli`, se usar NetworkManager) – **MR**
- Arquivo importante: `/etc/resolv.conf` – **MR**

---

## Check-list

- [ ] Sei checar se minha placa de rede tem IP (`ip a`)
- [ ] Sei ver a rota padrão do meu sistema (`ip route`)
- [ ] Sei testar conectividade básica com `ping`
- [ ] Sei diferenciar testes de ping para IP vs domínio (DNS envolvido)
- [ ] Sei onde olhar para ver qual servidor DNS está sendo usado (`/etc/resolv.conf` ou equivalente)

---

## Exercícios

**Exercício 1 – IP e gateway**

1. Sem usar interface gráfica, descubra:
   - Seu **IP interno** (na rede local)  
   - Seu **gateway padrão**  
2. Use comandos como `ip a` e `ip route`.  
3. Anote aqui:
   - Comandos usados  
   - O IP da sua máquina  
   - O IP do gateway.

**Exercício 2 – Testando conectividade e DNS**

1. Use `ping` para testar:
   - `ping 8.8.8.8`  
   - `ping google.com`  
2. Observe as diferenças:
   - Os dois funcionam?  
   - Se o ping para o IP funciona, mas para o domínio não, o que isso sugere?  
3. Anote aqui sua conclusão sobre o papel do **DNS** nesses testes.

---

## Resumo (para preencher depois de estudar)

- Passos que sigo quando não tenho internet:
  - 
- Ferramentas que mais ajudam no diagnóstico:
  - 
- Pontos que ainda geram dúvida:
  - 

