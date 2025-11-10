# 🛡️ Ransomware Educacional — Bootcamp Santander Cibersegurança 2025

> **Aviso legal e ético**  
> Este projeto foi desenvolvido **exclusivamente para fins educacionais** no **Bootcamp Santander - Cibersegurança 2025**.  
> Seu objetivo é demonstrar, em ambiente controlado, **como ransomwares operam** e, principalmente, **como proteger-se contra eles**.  
> **O uso não autorizado deste código é ilegal e antiético.** Execute-o apenas em **laboratórios isolados**, com **dados fictícios** e **consentimento explícito**.

---

## 📘 Sobre o projeto

Durante o bootcamp, foi proposto o desafio de criar um **ransomware educacional** — uma simulação de ataque controlado — com foco na **compreensão dos mecanismos de criptografia, impacto nos sistemas e contramedidas de defesa**.

O projeto é dividido em dois scripts:

- `ransoware.pyw` → simula o ataque (criptografa arquivos dentro de um diretório de teste).  
- `descriptografar.py` → permite restaurar os arquivos usando a chave gerada (para fins de laboratório).  

---

## 🧩 Estrutura e funcionamento

### 🔑 1. Geração da chave
O script cria uma chave de criptografia (`chave.key`) usando a biblioteca **cryptography (Fernet)**.  
Essa chave é essencial para descriptografar os arquivos posteriormente.

### 🗂️ 2. Descoberta de arquivos
Percorre recursivamente o diretório especificado (`test/` no exemplo) e lista todos os arquivos que **não** são a própria chave nem o código do ransomware.

### 🔒 3. Criptografia simulada
Cada arquivo encontrado é lido, criptografado com a chave e regravado — substituindo o conteúdo original.  
É uma demonstração **controlada**, sem propagação ou persistência.

### 💬 4. Mensagem de resgate
Cria um arquivo `LEIA ISSO.txt` simulando a típica mensagem de ransom.  
O texto é **puramente didático** e não deve ser usado fora do contexto educacional.

### 🔓 5. Descriptografia (recuperação)
Com o script `descriptografar.py`, é possível reverter o processo, usando a chave correta (`chave.key`) para restaurar os arquivos originais.

---

## 🧪 Demonstração segura — Ambiente recomendado

> ⚠️ **Execute somente em um ambiente isolado (sandbox ou máquina virtual).**

1. Crie uma pasta de testes, por exemplo `test/`, com arquivos de texto simples.  
2. Execute os scripts **sem conexão à internet** e **sem dados reais**.  

---

## 🔐 Defesa e mitigação — Como se proteger de ransomwares reais

### 🧱 1. Prevenção
- **Backups regulares** e **offline** (3-2-1: 3 cópias, 2 mídias, 1 offsite).  
- **Princípio do menor privilégio** — usuários comuns sem permissões administrativas.  
- **Segmentação de rede** — limitar propagação lateral.  
- **Atualizações frequentes** — corrigir vulnerabilidades exploráveis.  
- **Bloqueio de execução de scripts** não autorizados (Python, PowerShell, etc.).  
- **Antivírus e EDRs** com detecção comportamental ativa.  
- **Política de e-mail segura** — desativar macros e bloquear anexos executáveis.

### 🔍 2. Detecção
- Alertas para **modificação em massa de arquivos**.  
- Monitoramento de **criação de arquivos de resgate** ou chaves `.key`.  
- Uso de **Soluções EDR/FIM** (File Integrity Monitoring).  

### 🚨 3. Resposta a incidentes
1. **Isolar imediatamente** os sistemas afetados.  
2. **Coletar evidências** (logs, snapshots, dumps de memória).  
3. **Restaurar** sistemas a partir de backups limpos.  
4. **Trocar senhas** e revisar credenciais administrativas.  
5. **Relatar o incidente** conforme as políticas e leis locais (LGPD, etc.).  
6. **Fortalecer a segurança** — revisar e corrigir pontos explorados.
---

## 🚫 O que este projeto **não** cobre
- Persistência em sistemas.  
- Propagação em rede.  
- Ofuscação, empacotamento ou evasão de antivírus.  
- Mecanismos de comunicação com C2 (Command & Control).  
- Qualquer uso ofensivo, fraudulento ou ilegal.
---

## 🧑‍💻 Autor
**Cosme Ribeiro**  
Estudante de Desenvolvimento de Sistemas – SENAI Prof. Vicente Amato  
Bootcamp Santander – Cibersegurança 2025  
💻 Projeto educacional voltado à conscientização e defesa cibernética.

---

> “Conhecer o ataque é o primeiro passo para preveni-lo.”  
> — Bootcamp Santander Cibersegurança 2025

