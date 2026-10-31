bash

```bash
# ==========================================
# PENTEST WEB - GOBUSTER
# ALVO: <ip_alvo>
# FERRAMENTA: Gobuster v3.8.2
# ==========================================

# 1. Verificar versão do Gobuster
gobuster version


# 2. Enumerar diretórios e arquivos
gobuster dir \
-u http://<ip_alvo>/ \
-w /usr/share/dirb/wordlists/common.txt


# ==========================================
# 3. RESULTADOS ENCONTRADOS
# ==========================================

# 403 - Acesso proibido
# .hta
# .htaccess
# .htpasswd
# cgi-bin/
# server-status

# 301 - Redirecionamento
# passwords/

# 200 - Acesso permitido
# index.html
# robots.txt


# ==========================================
# 4. ACESSAR O DIRETÓRIO PASSWORDS
# ==========================================

# IMPORTANTE:
# Após identificar o caminho /passwords/,
# ACESSE O LINK NO NAVEGADOR.
#
# Clique em:
# http://<ip_alvo>/passwords/
#
# Verifique o conteúdo disponível no diretório
# para procurar a flag do desafio.


# ==========================================
# 5. CONCLUSÃO
# ==========================================

# O Gobuster identificou o diretório /passwords/.
# Esse diretório deve ser acessado e analisado
# para verificar se contém a flag do desafio.
#
# A identificação do diretório não confirma,
# por si só, que a flag está presente.
#
# ==========================================
```
