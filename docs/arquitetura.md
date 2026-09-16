## O caminho de uma requisição
```mermaid
sequenceDiagram
    participant D as Servidor DNS
    participant N as Navegador do paciente
    participant S as Servidor da Clínica Vida+
    N->>D: clinicavidamais.com.br?
    D-->>N: 203.0.113.42
    N->>S: conexão TCP e TLS na porta 443
    N->>S: GET /consultas/agendar
    S-->>N: 200 OK, HTML da agenda
```

## Evidência do DNS

Server: 127.0.0.53
Address: 127.0.0.53#53

Non-authoritative answer:
Name: github.com
Address: 189.126.108.15

## Evidência do HTTP

| Método | Recurso | Código de Status | Tipo |
| :--- | :--- | :--- | :--- |
| GET | markdown.css | 200 | stylesheet |
| GET | katex.min.css | 200 | stylesheet |
| GET | index.js | 200 | script |
| GET | aaaba | 404 | document |


Existe a necessidade do HTTPS para garantia de maior segurança, os usuários poderão se cadastrar e colocar seus dados como CPF, dados bancários, cartões, telefone e etc. 
O sistema de segurança previne que isso não vaze para terceiros. Seguindo a Lei Geral de Proteção de Dados (LGPD) garante 
