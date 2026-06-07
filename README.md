# vollmed.api-alura

Este projeto consiste em uma API REST robusta para a **Vollmed**, uma clínica médica virtual que necessita de um sistema de gerenciamento eficiente de médicos e pacientes. 

A aplicação foi desenvolvida durante o curso de **Desenvolvimento de APIs Rest em Java com Spring Boot 3** da Alura, focando em boas práticas de programação, design de API e persistência de dados.

## 🚀 Tecnologias e Ferramentas

O projeto utiliza as seguintes tecnologias do ecossistema Java e Spring:

- **Java 17+**
- **Spring Boot 3**
- **Spring Data JPA**: Para persistência de dados e integração com o banco de dados.
- **Spring Web**: Para criação de endpoints REST.
- **Bean Validation**: Para validação de dados de entrada (DTOs).
- **Lombok**: Para redução de código boilerplate (Getters, Setters, Construtores).
- **Flyway Migrations**: Para controle de versionamento do esquema do banco de dados.
- **MySQL Driver**: Para conectividade com o banco de dados MySQL.
- **Spring Boot DevTools**: Para agilidade no ciclo de desenvolvimento.
- **Insomnia**: Utilizado como ferramenta de testes para as requisições HTTP.

## 🛠️ Funcionalidades

- Cadastro, listagem, atualização e exclusão (soft delete) de **Médicos**.
- Cadastro, listagem, atualização e exclusão (soft delete) de **Pacientes**.
- Paginação e ordenação de dados.
- Endereços embutidos (Embeddables) em ambas as entidades.

## ⚙️ Instalação e Execução

Siga os passos abaixo para configurar o projeto localmente:

1. **Pré-requisitos**:
   - Possuir o **Java JDK 17** ou superior instalado.
   - Possuir o **MySQL** instalado e em execução.

2. **Configuração do Banco de Dados**:
   - No seu MySQL, crie um database chamado `vollmed_api`:
     ```sql
     CREATE DATABASE vollmed_api;
     ```

3. **Configuração das Credenciais**:
   - No arquivo `api/src/main/resources/application.properties`, ajuste as propriedades de conexão com o seu usuário e senha do MySQL:
     ```properties
     spring.datasource.username=seu_usuario
     spring.datasource.password=sua_senha
     ```

4. **Execução**:
   - Navegue até a pasta `api` e execute o comando:
     ```bash
     ./mvnw spring-boot:run
     ```

## ⚠️ Observações Importantes

### Migrações (Flyway)
As migrations do Flyway são aplicadas automaticamente ao iniciar a aplicação. Entretanto, para garantir a integridade do banco de dados e evitar conflitos, **certifique-se de realizar manutenções ou alterações manuais de schema apenas quando o projeto não estiver sendo executado**.

## 📝 Licença

Este projeto foi desenvolvido para fins didáticos através da plataforma Alura.

---
*Desenvolvido com o conhecimento adquirido na formação Java com Spring Boot da Alura.*
