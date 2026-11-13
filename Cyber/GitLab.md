Plataforma de [[DevOps]] para gerenciamento e automação de código. Permite versionamento de código, trabalho em equipe, integração com pipeline [[CI/CD]] entre outras funcionalidades para facilitar o processo de desenvolvimento.

### Funcionamento
Funciona de forma remota ou local. Funciona com base no pipeline configurado, a sequência de instruções a se fazer após um Commit, até eventualmente resultar no software disponibilizado no ambeinte de produção devidamente testado e buildado. 

O pipeline decide as ações a serem tomadas em cada etapa, mas o agente que realmente executa é o Runner.

### Abuso
Por ser uma plataforma que gerencia todo o clico de vida do código, também tem acesso a arquivos e informações sensíveis, além de altas permissões.

Algumas formas de exploração são:
- Exploração de segredos expostos, como chaves de API e senhas esquecidas
- Ataques de Supply Chain
- Execução de código arbitrário por meio dos Runners
- Vulnerabilidades do próprio GitLab
- Roubo de [[PATs]]