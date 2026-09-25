Busca em largura para encontrar vertices de um grafo, o algoritmo percorre por todos os vizinhos em camadas partindo do vertice s, sua complexidade de tempo é O(V + E)



BFS(G, S)
    for cada vertice u pertencente a V[G] - {S}
    u.cor = branco
    u.pai = nil
    u.d = infinito
s.cor = cinza
s.d = 0
s.pai = nil
enfileirar(Q, s)
while Q != NIL
    u = desenfileirar(Q)
    for cada v = Adj[u]
        if v.cor = branco
            v.cor = cinza
            v.d = u.d +1
            v.pai = u
            enfileirar (Q,v)
    u.cor = preto


