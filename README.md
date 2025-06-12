🎮 SteamRoxa - Microserviço de Gerenciamento de Jogos
📌 Descrição
SteamRoxa é um microserviço desenvolvido com Spring Boot, cujo objetivo é gerenciar um catálogo de jogos digitais. Ele oferece uma API RESTful que permite cadastrar, consultar, atualizar e deletar jogos, além de aplicar filtros personalizados. Este projeto foi realizado como trabalho final da disciplina de Programação Orientada a Objetos.

🛠️ Tecnologias e Ferramentas
Java 17

Spring Boot

Spring Data JPA

Banco de Dados H2 (dev) / MySQL (prod)

Swagger / Springdoc OpenAPI

JUnit 5 & Mockito

JaCoCo (cobertura de testes)

Git & GitHub

🚀 Como Executar o Projeto
Pré-requisitos
Java 17+

Maven 3.8+

Docker (opcional)

Passos
Clone o repositório

bash
Copiar
Editar
git clone https://github.com/seu-usuario/steamroxa.git
cd steamroxa
Executar com H2 (perfil default)

bash
Copiar
Editar
./mvnw spring-boot:run
Executar com MySQL (produção)

Configure application-prod.properties

Execute:

bash
Copiar
Editar
./mvnw spring-boot:run -Dspring-boot.run.profiles=prod
Swagger

Acesse: http://localhost:8080/swagger-ui.html

🎯 Funcionalidades da API
Verbo	Endpoint	Ação
POST	/games	Cadastrar novo jogo
GET	/games	Listar todos os jogos
GET	/games/{id}	Buscar jogo por ID
PUT	/games/{id}	Atualizar dados de um jogo
DELETE	/games/{id}	Deletar jogo
GET	/games/filter?genre={gênero}	Filtrar por gênero de jogo

🧱 Entidade Principal: Game
java
Copiar
Editar
public class Game {
    private Long id;
    private String name;
    private String genre;
    private Double price;
    private String platform;
}
Validações com anotações como @NotNull, @Size e @Positive garantem integridade dos dados.

🧪 Testes
Cobertura com JUnit 5 + Mockito

Testes em:

GameService (mock de GameRepository)

GameController (usando MockMvc)

Cenários:

Criação e busca com sucesso

Entidade não encontrada

Dados inválidos

Cobertura mínima: 90%+ (JaCoCo)

🗂️ Estrutura de Pacotes
arduino
Copiar
Editar
projetoFinal.steamRoxa
├── controller
├── service
├── model
├── repository
├── config
Segue o padrão MVC, com injeção de dependência e boas práticas de POO.

👥 Equipe
Nome	Responsabilidades
Nicolas Magalhães	Camada de serviço, testes
Bruno Sutil	Controller, validações, documentação
[Vago]	[Atribuição futura]
[Vago]	[Atribuição futura]

