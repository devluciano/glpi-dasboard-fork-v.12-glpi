# GLPI Dashboard Plugin (Fork para GLPI 12)

[![GLPI Version](https://img.shields.io/badge/GLPI-v12-blue.svg)](https://glpi-project.org/)
[![License: GPL v2+](https://img.shields.io/badge/License-GPL%20v2%2B-blue.svg)](COPYING.txt)

Este repositório é um **fork** do plugin **Dashboard** para GLPI, atualizado e adaptado para permitir a instalação e o pleno funcionamento na versão **GLPI 12**.

---

## 📌 Sobre o Fork

O plugin original de Dashboard foi amplamente utilizado nas versões anteriores do GLPI (0.9x, 9.x, 10.x). Com a evolução da arquitetura do GLPI na versão 12, foram necessárias adaptações na estrutura de hooks, verificação de compatibilidade, menus e carregamento de interfaces.

### Principais alterações neste fork:
- **Compatibilidade com GLPI 12**: Atualização dos pré-requisitos e validações de versão no `setup.php`.
- **Adaptação de Hooks e Menus**: Ajustes no registro de hooks (`plugin_dashboard_redefine_menus`) e permissões de perfil para a nova interface.
- **Correções de compatibilidade PHP/GLPI**: Tratamento de chamadas e tabelas para compatibilidade com o ecossistema moderno do GLPI.

---

## 🚀 Instalação

### 1. Clonar ou copiar os arquivos
Baixe ou clone este repositório para o diretório de plugins do seu servidor GLPI. A pasta do plugin deve se chamar obrigatoriamente `dashboard`:

```bash
cd /caminho/do/glpi/plugins
git clone https://github.com/devluciano/glpi-dasboard-fork-v.12-glpi.git dashboard
```

> **Atenção:** Certifique-se de que o diretório se chame `dashboard` (e não o nome padrão do repositório) para que o GLPI reconheça corretamente as rotas do plugin.

### 2. Permissões de arquivo
Ajuste as permissões para o usuário do seu servidor web (ex: `www-data` no Debian/Ubuntu ou `apache` no RHEL/CentOS):

```bash
chown -R www-data:www-data /caminho/do/glpi/plugins/dashboard
chmod -R 755 /caminho/do/glpi/plugins/dashboard
```

### 3. Ativar no GLPI
1. Acesse o GLPI com perfil de Administrador (`super-admin`).
2. Vá em **Configurar** > **Plugins** (ou *Setup > Plugins*).
3. Localize o plugin **Dashboard** (ou **ST-Dashboard**) na lista.
4. Clique em **Instalar** e, em seguida, em **Habilitar**.

### 4. Acessar o Dashboard
- Acesse através do menu lateral/superior em **Plugins** > **Dashboard** (ou através da aba customizada configurada para sua interface central).

---

## ⚙️ Pré-requisitos

- **GLPI**: Versão 12.x (ou superior)
- **PHP**: Compatível com os requisitos da sua versão do GLPI (PHP 8.1+)
- **Banco de Dados**: MariaDB / MySQL compatível com GLPI

---

## 👨‍💻 Autoria e Manutenção do Fork

Modificações e compatibilização para **GLPI 12** desenvolvidas por:
- **Luciano Silva** - *Dev FullStack*
- GitHub: [@devluciano](https://github.com/devluciano)

---

## 📄 Licença e Créditos

- Modificações para GLPI 12: **Luciano Silva - Dev FullStack**
- Baseado no trabalho original do plugin **GLPI Dashboard** desenvolvido pela comunidade GLPI / Stevenes Donato.
- Distribuído sob a licença **GPL v2+** (consulte o arquivo [COPYING.txt](COPYING.txt) para mais detalhes).
