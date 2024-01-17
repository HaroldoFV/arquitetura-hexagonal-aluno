# Arquitetura hexagonal

Este é um projeto feito durante o curso de arquitetura hexagonal na FullCycle. 

## Descrição da Aplicação

Aplicação simples de cadastro de produtos feita em Golang usando ports, adpters da arquitetura hexagonal.

Também foi usado docker para o ambiente de desenvolvimento e o banco de dados sqlite.

Foi usado algumas bibliotecas como: negroni, mock, mux, cobra e testify.

## Subindo a Aplicação com Docker-Compose

Nosso ambiente é completamente baseado em Docker. Assim, levantá-lo é extremamente fácil com o docker-compose.

Os passos seguintes vão guiá-lo em como configurar e rodar o projeto:

1. Primeiro, você precisa clonar o repositório. Digite o seguinte comando no terminal:
2. git clone https://github.com/HaroldoFV/arquitetura-hexagonal-aluno.git
3. Navegue até a pasta recém-clonada com o comando:
4. cd hexagonal-aluno
5. docker-compose up -d
6. docker exec -it appproduct bash
7.  go run main.go http
8. Agora, a aplicação deve estar rodando e disponível na porta 9000 do seu host.


# Endpoinst:
## cadastro:

http://localhost:9000/product
{
    "name": "",
    "price": 0
}

## Habilitar/desabilitar produto: 

http://localhost:9000/product/{productId}/disable

http://localhost:9000/product/{productId}/enable

## Recuperar um produto:
http://localhost:9000/product/{productId}

