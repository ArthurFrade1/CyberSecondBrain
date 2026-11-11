*Lighweight Directory Access Protocol* é um padrão para armazenamento e gerenciamento de arquivos em um banco de dados, com uma estrutura de dados de árvore, os recursos são organizados em níveis, facilitando as buscas e organização. Permite que as empresas armazenem logins, senhas, grupos e permissões de usuários em um único banco de dados central, evitando cadastros duplicados em vários sistemas.

Cada entrada possui um enderaço único chamado DN (*Distinguished Name*). Exemplos comuns:

- DC (*Domain component*): Componente de domínio (ex: `dc=empresa, dc=com`)
- OU (*Organizaqtional Unit*): Unidade organizacional ou setor (ex:  `ou=usuarios`, `ou=ti`)
- CN (*Common Name*): Nome comum do usuário ou objeto (ex: `cn=Ana silva`)

Portas e Segurança
- **Porta 389:** Porta padrão para tráfego LDAP (geralmente sem criptografia, a menos que utilize _StartTLS_).
- **Porta 636:** Porta para **LDAPS** (_LDAP Secure_), que roda sobre SSL/TLS.
- **Portas 3268 / 3269:** Utilizadas para o Catálogo Global do Microsoft Active Directory.