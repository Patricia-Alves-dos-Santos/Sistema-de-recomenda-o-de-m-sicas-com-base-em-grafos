🎵 Sistema de Recomendação Musical com Grafos
📌 Objetivo

Desenvolver a modelagem de dados em grafo para um serviço de streaming de músicas, representando usuários, músicas, artistas e gêneros como nós interconectados.

O modelo permite identificar padrões de escuta e possibilita futuras implementações de sistemas de recomendação.

🧠 Estrutura do Modelo

A modelagem foi desenvolvida utilizando abordagem orientada a grafos, onde cada entidade principal é representada como um nó distinto.

🔹 Nós (Nodes)

👤 User

user_id: Integer

name: String

🎵 Music

music_id: Integer

title: String

duration: Integer

🎤 Artist

artist_id: Integer

name: String

🎼 Genre

name: String

🔗 Relacionamentos

(User)-[:LISTENS_TO]->(Music)
Representa as músicas escutadas por cada usuário.

(Music)-[:PERFORMED_BY]->(Artist)
Indica qual artista interpreta determinada música.

(Music)-[:IN_GENRE]->(Genre)
Classifica a música dentro de um gênero específico.

🎯 Justificativa da Modelagem

A separação entre Music, Artist e Genre evita redundância de dados e permite consultas mais eficientes.

O relacionamento LISTENS_TO possibilita:

Identificar preferências de usuários

Detectar padrões de consumo

Implementar recomendações baseadas em gênero ou artista

Analisar similaridade entre usuários

Este modelo é escalável e pode ser expandido futuramente com:

Playlists

Seguidores de artistas

Avaliações

Sistema de recomendação colaborativa

📊 Estrutura Visual
(User)-[:LISTENS_TO]->(Music)
(Music)-[:PERFORMED_BY]->(Artist)
(Music)-[:IN_GENRE]->(Genre)
