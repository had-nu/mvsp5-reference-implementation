# mvsp5-reference-implementation

Este repositório contém um ambiente simulado inseguro para reproduzir as condições originais da aplicação de gestão de contratos de manutenção de veículos.  
**Atenção**: este repositório não é a implementação do MVSP5. Ele representa o estado inicial vulnerável sobre o qual o MVSP5 será aplicado como prova de conceito.

---

## Finalidade

- Simular a aplicação de contratos de manutenção desenvolvida originalmente com:
  - Arquitetura sobrecarregada (overengineered) em AWS.  
  - Rastreabilidade insípida (sem versionamento de infraestrutura).  
  - Falta de práticas de segurança no ciclo de vida (sem CI/CD seguro).  
  - Código e deploy feitos de forma manual ou terceirizada, sem controles formais.  

- Servir como baseline inseguro, evidenciando as lacunas identificadas pelo assessment OWASP SAMM, para que o MVSP5 possa demonstrar impacto ao introduzir segurança no CI/CD.

---

## O que esperar deste repositório

- **Aplicação em Go** (protótipo) imitando o sistema de contratos.  
- **Uso superficial de ferramentas**:
  - Versionamento, mas sem práticas de segurança no pipeline.  
  - Ferramentas de segurança configuradas apenas com regras genéricas, incapaz de detectar falhas críticas.  
- **Más práticas intencionais**, como:
  - Senhas de banco de dados hardcoded no código.  
  - Variáveis sensíveis expostas em arquivos de configuração.  
  - Ausência de RBAC/AuthZ.  
  - Falta de logs de auditoria.  
- Deploy manual e sem rastreabilidade (infraestrutura não descrita em IaC). 

---

## O que **não** é este repositório

- Não é a implementação do MVSP5.  
- Não é uma aplicação de produção.  
- Não é containerizada nem descrita em IaC. 

---

## Aviso

O código e configurações deste repositório são intencionalmente inseguros e não devem ser reutilizados em ambientes de produção.
