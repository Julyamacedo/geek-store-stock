1. Produto
id_produto — SERIAL PRIMARY KEY
nome — VARCHAR(100)
franquia_anime — VARCHAR(100)
preco_venda — NUMERIC(10,2)
quantidade_estoque — INTEGER

2. Usuário
id_usuario — SERIAL PRIMARY KEY
nome — VARCHAR(100)
email — VARCHAR(100) 
senha — CHAR(8)

3. Pedidos
id_pedido — SERIAL PRIMARY KEY
situacao_pedido — ENUM(situação)
quantidade — INTEGER
data_pedido — TIMESTAMP
id_produto — INTEGER FOREIGN KEY
id_usuario — INTEGER FOREIGN KEY

Relacionamentos
Produto — Pedidos (1:N): um produto pode ter vários pedidos registradas ao longo do tempo.
Usuário — Pedidos (1:N): um usuário pode registrar vários pedidos , e cada pedido fica associada a um usuário.
