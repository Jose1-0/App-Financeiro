# App-Financeiro

#### O objetivo desse projeto é puramente academico, com foco em aprender e implementar novos conhecimentos baseados em Java e posteriomente em Angular.

#### O projeto será um apolicativo que controlorá minhas finanças pessoais, de preferência que ele fiqaue hospedado em algum servidor na nivem, disponivel pemo maximo de tempo que meu bolso permitir.

# Linguagens:
- Java 21.
- Angular.
- Kafka
- Postgres SQL
- Mongo DB

 O README será atualizado conforme o projeto for atualizado, Lembrando que ele é para fins educativos e não em desempenho.

# app-financeiro-backend/
│
- ├── core/                      # Núcleo da aplicação (não depende de frameworks)
- │   ├── domain/                # Entidades e objetos de valor (ex: Conta, Transacao, Usuario)
- │   ├── usecases/              # Casos de uso (regras de negócio: criar conta, lançar transação, etc.)
- │   ├── gateways/              # Interfaces (contratos) para acessar recursos externos
- │   └── exceptions/            # Exceções de negócio
- │
- ├── infrastructure/            # Adaptações técnicas (depende do core, mas não o contrário)
- │   ├── database/              # Implementações dos repositórios (Postgres via JPA/Hibernate, por exemplo)
- │   ├── rest/                  # Controllers REST (Spring Boot / expostos para o front Angular)
- │   ├── security/              # Configuração de autenticação/autorização (OAuth2, JWT, Keycloak ou Azure AD)
- │   ├── kafka/                 # Produção e consumo de eventos (ex: notificação de transação)
- │   ├── config/                # Configurações do Spring Boot (Beans, CORS, cache, etc)
- │   └── featuretoggle/         # (opcional) Controle de feature flags
- │
- ├── application/               # Orquestração (services e mappers)
- │   ├── dto/                   # DTOs para entrada e saída (API)
- │   ├── mapper/                # Conversores entre domain ↔ dto
- │   └── service/               # Serviços de aplicação (chamam usecases, coordenam fluxos)
- │
- ├── tests/                     # Testes unitários e de integração
- │
- └── main/                      # Entry point (Spring Boot main class)
