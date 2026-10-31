bash
```bash
# ==========================================
# PENTEST WEB - FLAG VIA HTTPS
# ALVO: <ip_alvo>
# PORTA: 9090
# ==========================================

# 1. Criar diretório para armazenar o resultado
mkdir -p flag_ssl


# 2. Acessar o servidor HTTPS e salvar a página
curl -k https://<ip_alvo>:9090 > flag_ssl/index.html


# 3. Procurar a palavra FLAG no conteúdo baixado
cat flag_ssl/index.html | grep 'FLAG'


# ==========================================
# CONCLUSÃO
# ==========================================

# Foi realizada uma requisição HTTPS na porta 9090.
# O conteúdo da página foi salvo localmente.
# Em seguida, foi realizada uma busca pela
# palavra FLAG no arquivo index.html.
#
# RESULTADO ESPERADO:
# Identificação da flag, caso esteja presente
# no conteúdo retornado pelo servidor.
#
# ==========================================
```
