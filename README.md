# Cadastro de Usuários - API Java Spring com Arquitetura de Microservices
Este projeto consiste em uma API desenvolvida em Java Spring, implementando o padrão de arquitetura de microservices para um sistema de cadastro de usuários. A aplicação é composta por dois microservices principais: User e Email.

# Microservice User
O microservice User é responsável por receber e armazenar os dados dos usuários, incluindo nome e email, em um banco de dados. Possui endpoint apenas para criação de usuários.

# Microservice Email
O microservice Email cuida do envio de emails de confirmação para os usuários cadastrados. Utilizando o RabbitMQ como broker de mensagens, ele recebe as informações dos usuários provenientes do microservice User e encaminha emails personalizados de confirmação. Cada email enviado contém uma mensagem customizada com o nome do usuário, informando que seu cadastro foi realizado com sucesso na API.

# Tecnologias Utilizadas
- Java Spring
- RabbitMQ: O RabbitMQ é empregado como broker de mensagens para a comunicação eficaz entre os microservices, garantindo uma integração perfeita e confiável.
- Banco de Dados
