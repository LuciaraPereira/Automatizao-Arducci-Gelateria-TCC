# Arquitetura prevista — proposta

Conforme tecnologias previstas no README: React.js e Java/Spring Boot, Spring Security/JWT e JPA/Hibernate. O SGBD permanece a definir. Integrações PIX e fiscais são futuras, sujeitas a decisão da equipe.

```mermaid
flowchart LR
 U[Cliente ou operador] --> F[Frontend React responsivo]
 F --> A[API REST Spring Boot]
 A --> P[Autenticação e permissões: Spring Security]
 A --> D[Serviços de pedidos, caixa, mesas e estoque]
 D --> R[Persistência JPA e Hibernate]
 R --> B[Banco relacional: SGBD a definir]
 D -. Integração futura .-> X[Provedor PIX e emissão fiscal]
```
