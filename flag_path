bash

```bash
# ==========================================
# PENTEST WEB - GOBUSTER
# ALVO: <ip_alvo>
# FERRAMENTA: Gobuster v3.8.2
# ==========================================

# 1. Verificar versão do Gobuster
gobuster version


# 2. Realizar enumeração de diretórios
gobuster dir \
-u http://<ip_alvo>/ \
-w /usr/share/dirb/wordlists/common.txt


# ==========================================
# RESULTADOS ENCONTRADOS
# ==========================================

# Acesso proibido (403)
# .hta
# .htaccess
# .htpasswd
# cgi-bin/
# server-status

# Redirecionamento (301)
# passwords/

# Acesso permitido (200)
# index.html
# robots.txt


# ==========================================
# ANÁLISE DOS RESULTADOS
# ==========================================

# 403 - Acesso proibido
# 301 - Redirecionamento
# 200 - Requisição realizada com sucesso


# ==========================================
# CONCLUSÃO
# ==========================================

# Foram identificados 8 caminhos no servidor web.
# O diretório /passwords/ merece análise adicional.
# Os arquivos index.html e robots.txt estão acessíveis.
#
# RECOMENDAÇÃO:
# Revisar permissões e restringir o acesso
# a diretórios e arquivos que contenham
# informações sensíveis.
#
# ==========================================
```
