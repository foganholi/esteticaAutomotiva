# Estética Automotiva - Backend

Projeto desenvolvido para Projeto Academico na criação de um sistema para uma **estética automotiva**.  responsável por gerenciar as operações principais como cadastro de clientes, agendamentos e autenticação de usuários com confirmação por e-mail. 
## 🔧 Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **Spring Web**
- **Spring Security**
- **MySQL**
- **JavaMailSender (Spring Email)**
- **Flyway** *(opcional, para versionamento do banco)*
- **Maven** ou **Gradle**

## 🛠 Funcionalidades Implementadas

- ✅ CRUD de Clientes
- ✅ CRUD de Agendamentos
- ✅ Relacionamento entre clientes e agendamentos
- ✅ Sistema de autenticação e login
- ✅ Confirmação de conta via e-mail
- ✅ Proteção de rotas com Spring Security
- 📅 Organização por datas e horários de agendamento
- 📂 Estrutura limpa e modular (controller, service, repository, model)

## ✉️ Confirmação por E-mail

Ao realizar o cadastro, o usuário receberá um e-mail com um link de verificação. Somente após a confirmação o login será liberado.

Tecnologia utilizada:
- `JavaMailSender`
- Token único de verificação com expiração
- Reenvio de e-mail em caso de expiração

## ⚙️ Como Executar

## ⚙️ Como Executar
1. Clone:
   ```bash
   git clone https://github.com/foganholi/esteticaAutomotiva.git

2. Configure o `application.properties`:
   ```properties
  spring.application.name=esteticaAutomotiva

spring.datasource.url=jdbc:mysql://localhost:3306/auto_estetica
spring.datasource.username=root
spring.datasource.password=SEU_PASSWORD_AQUI

# JWT secret (corrige para JWT)
secret=${JWT_SECRET:12345678}

frontend.url=${FRONTEND_URL:http://localhost:3000}
backend.url=${BACKEND_URL:http://localhost:8080}

app.verify.url=${backend.url}/auth/confirmar-email?token=
front.trocarSenhaURL=${frontend.url}/recuperar-senha?token=

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=SEU_EMAIL
spring.mail.password=SEU_APP_PASSWORD
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

   ```

Suba o MySQL local com o schema auto_estetica.
Rodar:
./mvnw spring-boot:run
ou pela sua IDE.
🔗 Conexão com o Frontend
O backend expõe APIs REST consumidas pelo frontend (separado) para login, cadastro, agenda e perfil.

📜 Licença
Projeto de uso pessoal/colaborativo. Sugestões e melhorias são bem-vindas.

