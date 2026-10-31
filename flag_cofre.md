bash
```bash
# ==========================================
# PENTEST - ZIP / SSH / COFRE SECRETO
# ALVO: <ip_alvo>
# PORTA SSH: 22222
# USUÁRIO: Summer
# ==========================================


# 1. VISUALIZAR O DIÁRIO DO MORTY
# ------------------------------------------

cat flag_zip/morty_diario.txt

# Informações encontradas:
#
# FLAG{Quebra de senha do arquivo ZIP}
#
# Pontuação: 20 pontos
#
# Dica encontrada no diário:
# 129865Fatec


# 2. ACESSAR O SERVIDOR VIA SSH
# ------------------------------------------

ssh Summer@<ip_alvo> -p 22222

# Realizar autenticação com a credencial
# disponibilizada pelo laboratório.


# 3. ACESSAR O DIRETÓRIO DO JERRY
# ------------------------------------------

cd /home/Jerry/

# Entrar no diretório do cofre:

cd RICKS_SAFE/


# 4. EXECUTAR O COFRE
# ------------------------------------------

./cofre 129865Fatec

# A senha encontrada no diário do Morty
# foi utilizada para abrir o cofre.


# 5. FLAG ENCONTRADA
# ------------------------------------------

# FLAG{Cofre Secreto Foi Quebrado}
#
# Pontuação: 20 pontos


# ==========================================
# 6. NOVA PISTA ENCONTRADA
# ==========================================

# Jerry deixou uma dica sobre sua senha.
#
# Regras informadas:
#
# 1. Um caractere maiúsculo.
# 2. Um dígito.
# 3. Uma palavra em inglês relacionada
#    ao nome de sua antiga banda.
#
# A dica sugere uma investigação adicional
# sobre a composição da senha.


# ==========================================
# FERRAMENTAS UTILIZADAS
# ==========================================

# CAT - Leitura do diário do Morty.
# SSH - Acesso remoto ao servidor.
# CD  - Navegação entre diretórios.
# COFRE - Programa utilizado no desafio.


# ==========================================
# CONCLUSÃO DO PENTEST
# ==========================================

# 1. Foi analisado o diário do Morty.
# 2. Foi identificada a senha 129865Fatec.
# 3. Foi realizado acesso SSH como Summer.
# 4. Foi acessado o diretório RICKS_SAFE.
# 5. A senha foi utilizada para executar o cofre.
# 6. A flag do desafio foi recuperada.
#
# RESULTADO:
# FLAG{Cofre Secreto Foi Quebrado}
#
# ==========================================
```
