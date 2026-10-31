bash

```bash
# ==========================================
# PENTEST FTP
# ALVO: <ip_alvo>
# PORTA: 21
# ==========================================

# 1. Identificar a porta e versão do serviço
nmap -sV -p 21 <ip_alvo>


# 2. Conectar ao servidor FTP
ftp <ip_alvo>


# 3. Testar login
# Usuário: admin
# Resultado: 530 Login incorrect

# Usuário: anonymous
# Resultado: 230 Login successful


# 4. Listar arquivos disponíveis
ls -la


# 5. Baixar o arquivo encontrado
get flag.txt


# 6. Encerrar conexão FTP
bye


# 7. Ler o arquivo no Kali Linux
cat flag.txt


# ==========================================
# RESULTADO DO PENTEST
# ==========================================
#
# Serviço: FTP
# Porta: 21
# Versão: vsFTPd 3.0.5
# Login anônimo: Permitido
# Arquivo encontrado: flag.txt
#
# VULNERABILIDADE:
# Acesso FTP anônimo habilitado.
#
# RISCO:
# Possível exposição de informações.
#
# RECOMENDAÇÃO:
# Desabilitar login anônimo quando desnecessário.
# Restringir permissões de acesso aos arquivos.
#
# ==========================================
```
