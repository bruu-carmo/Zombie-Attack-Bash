# 🧟‍♂️ Zombie Attack Bash Script

> ⚠️ **ATENÇÃO:** Este script cria múltiplos processos zumbis. NÃO execute fora de ambientes controlados!

## 💀 O que é isso?

Este repositório contém um script Bash que simula um **ataque zumbi** ou **bomba de fork**, gerando milhares de processos com o comando `yes` em background, esgotando rapidamente os recursos do sistema.

---

## 📜 Script

```bash
#!/bin/bash
# zombie_attack.sh
# ⚠️ CUIDADO: Cria processos zumbis de forma contínua.
# ⚔️ Uso apenas em máquinas de teste / ambientes isolados.

while true; do
   nohup yes > /dev/null 2>&1 &
done
```
# 🧠 Guia Visual — Zombie Attack Bash Script

Este guia foi criado para você visualizar rapidamente a estrutura e o uso do projeto.

---

## 📁 Estrutura de Arquivos

```
zombie-attack-bash/
├── README.md            # Documentação completa
├── zombie_attack.sh     # Script de ataque zumbi (fork bomb)
└── .gitignore           # Arquivos ignorados pelo Git
```

---

## 🧪 Demonstração Visual

- Cria processos com `yes` em loop infinito
- Executa com `nohup` para continuar em background
- Redireciona saída com `> /dev/null 2>&1` para não exibir nada

---

## ☠️ Visual do Processo (`htop`)

```
PID USER      COMMAND
2345 bruna     yes
2346 bruna     yes
2347 bruna     yes
...
```
---

## ✅ Checklist de Segurança

- [x] Executar apenas em máquina virtual
- [x] Monitorar consumo de CPU com `htop`
- [x] Usar `ulimit -u` para limitar número de processos
- [x] Encerrar com `pkill yes`

---

## 🎯 Propósito

Ensinar sobre limites de processos e falhas por fork bombs.
Ideal para fins didáticos em segurança ofensiva e análise de estabilidade de sistemas.
---

## ⚙️ Como usar

> **NÃO execute esse script em sua máquina pessoal, de trabalho ou em produção.**

1. Clone este repositório (ou copie o script).
2. Execute em uma máquina virtual, sandbox ou container isolado.
3. Observe o consumo de CPU e processos com `htop`, `top` ou `ps`.
---

## 🧪 Finalidade

Este script foi criado **para fins educacionais e experimentação em ambientes controlados**.  
Ideal para demonstrar:

- Consumo de recursos por fork bomb
- Como o sistema operacional gerencia processos em excesso
- Comportamento de limites de usuários (`ulimit`)

---

## 🛡️ Como parar

Caso você execute por engano:

```bash
pkill yes
pkill zombie_attack.sh
```

> Ou reinicie a máquina/sessão se estiver travando.

---

## ⚠️ Aviso Legal

Este conteúdo é **apenas para fins educacionais**.  
O autor **não se responsabiliza** por danos causados por uso indevido.

---

## 👤 Autora

**Bruna Carmo**  
🔗 [github.com/bruu-carmo](https://github.com/bruu-carmo)
