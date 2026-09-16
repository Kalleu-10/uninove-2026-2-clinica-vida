## O caminho de uma requisição
```mermaid

sequenceDiagram
participant N as Navegador
participant D as DNS
participant S as Servidor
N->>D: IP de clinicavidamais.com.br?
D-->>N: 203.0.113.42
N->>S: TCP/TLS (Porta 443)
N->>S: GET /consultas/agendar
S-->>N: 200 OK (HTML)

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
