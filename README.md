
Geek Store 

### 1\. Produto

* id\_produto — SERIAL PRIMARY KEY  
* nome — VARCHAR(100)  
* franquia\_anime — VARCHAR(100)  
* preco\_venda — NUMERIC(10,2)  
* quantidade\_estoque — INTEGER

### 2\. Usuário

* id\_usuario — SERIAL PRIMARY KEY  
* nome — VARCHAR(100)  
* email — VARCHAR(100)   
* senha — CHAR(8)

### 3\. Pedidos

* id\_pedido — SERIAL PRIMARY KEY  
* situacao\_pedido — ENUM(situação)  
* quantidade — INTEGER  
* data\_pedido — TIMESTAMP  
* id\_produto — INTEGER FOREIGN KEY  
* id\_usuario — INTEGER FOREIGN KEY

## Relacionamentos

* Produto — Pedidos (1:N): um produto pode ter vários pedidos registradas ao longo do tempo.  
* Usuário — Pedidos (1:N): um usuário pode registrar vários pedidos , e cada pedido fica associada a um usuário.
<img width="1238" height="541" alt="image" src="https://github.com/user-attachments/assets/44d750d0-6fd7-45ac-83fb-7f6d23e71f5d" />
