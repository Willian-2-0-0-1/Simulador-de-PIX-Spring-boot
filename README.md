# Simulador-de-PIX-Spring-boot


CADASTRO

POST http://localhost:8080/api/pix/cadastro
Content-Type: application/json

{
    "nome": "João Silva",
    "email": "joao@exemplo.com",
    "senha": "123456",
    "chavePix": "1234-5",
    "banco": "Banco X",
    "saldo": 1000.00
}


LOGIN 


POST http://localhost:8080/api/pix/login
Content-Type: application/json

{
    "email": "joao@exemplo.com",
    "senha": "123456"
}


Transferencia 

POST http://localhost:8080/api/pix/transferir
Content-Type: application/json
Authorization: Bearer seu_token_jwt

{
    "chavePix": "1234-5",
    "valor": 100.00,
    "description": "Pagamento teste"
}

Consultar saldo

GET http://localhost:8080/api/pix/saldo
Authorization: Bearer seu_token_jwt

