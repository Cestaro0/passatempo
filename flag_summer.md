bash

```bash
# ==========================================
# PENTEST WEB - COMMAND INJECTION
# ALVO: <ip_alvo>
# SERVIÇO: HTTP / CGI
# ARQUIVO: tracertool.cgi
# ==========================================


# 1. IDENTIFICAR O ENDPOINT
# ------------------------------------------

http://<ip_alvo>/cgi-bin/tracertool.cgi


# 2. IDENTIFICAR O PARÂMETRO
# ------------------------------------------

# Parâmetro utilizado pela aplicação:
# target=8.8.8.8
#
# Foi investigada uma possível falha
# de Command Injection no tratamento
# das entradas fornecidas pelo usuário.


# 3. ACESSO SSH
# ------------------------------------------

# Usuário identificado: summer

ssh summer@IP_DO_ALVO

# Senha: winter


# 4. VISUALIZAÇÃO DE ARQUIVOS
# ------------------------------------------

# Foi relatado que o comando cat
# não funcionou como esperado.

# Alternativa utilizada para visualizar
# arquivos no ambiente:

vim flag
#procure o caminho da flag

# 5. VULNERABILIDADE INVESTIGADA
# ------------------------------------------

# Command Injection
#
# Componente: tracertool.cgi
# Parâmetro: target
#
# Possível impacto:
# Execução de comandos não autorizados
# e exposição de informações do servidor.


# 6. RECOMENDAÇÕES
# ------------------------------------------

# - Validar entradas recebidas.
# - Evitar comandos com parâmetros não confiáveis.
# - Aplicar o princípio do menor privilégio.
# - Restringir permissões de arquivos.
# - Monitorar requisições suspeitas.


# ==========================================
# CONCLUSÃO DO PENTEST
# ==========================================

# Foi investigada uma possível vulnerabilidade
# de Command Injection no endpoint tracertool.cgi.
#
# Também foi identificado um possível acesso
# remoto via SSH com o usuário summer.
#
# A vulnerabilidade precisa ser confirmada
# por evidências do ambiente.
#
# ==========================================
```

Resultado: documentação do teste de Command Injection, acesso SSH e análise de arquivos.
