# 🧪 Minitab 22.2.2.0 Deployment (64 bits) - Script Batch para Lansweeper

Este repositório contém um script `.bat` desenvolvido para automatizar a instalação silenciosa do **Minitab 22.2.2.0 (64 bits)** em ambientes Windows, utilizando **Lansweeper** como plataforma de deployment.

---

## 🎯 Objetivo

Automatizar a instalação do Minitab 22 com foco em:

- Padronização do diretório de instalação
- Logging centralizado detalhado
- Compatibilidade com múltiplos discos (S:\ ou C:\)
- Execução silenciosa sem interação do usuário
- Aplicação automatizada de aceite de licença

---

## ⚙️ Funcionalidades

- 🔍 Verificação do disco `S:\` para uso preferencial como diretório de instalação
- 📁 Cópia do instalador para `C:\Windows\Temp` com limpeza após execução
- 📋 Instalação com parâmetros avançados:
  - `/exelog`, `/exenoui`, `/qn`, `/l*v`, `APPDIR`
- 📝 Log da instalação (`Minitab_MSI.log`) e log geral (`deployments.log`)
- 📆 Sub-rotina de log com timestamp + nível de severidade (INFO/WARN/ERROR)

---

## 🚀 Comando de Instalação Usado

```batch
"C:\Windows\Temp\minitab22.2.2.0setup.x64.exe" /exelog "C:\Logs\Minitab22.log" /exenoui /exelang 1033 /qn ACCEPT_SOFTWARESUBSCRIPTIONAGREEMENT=1 APPDIR="C:\Program Files\Minitab 22" /l*v "C:\Logs\Minitab_MSI.log"
