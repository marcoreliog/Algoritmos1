// outro algoritmo para gerar uma MST - ARVORE GERADORA MINIMA, funciona de modo semelhante ao Dijkstra
- Mantemos uma lista vazia = visited, que armazenará vertices que já visitamos
- A = |{v,v,pi} : v pertence V -{r} - Q|
- selecionamos um vértice arbitrário para começar, por exemplo A, e adicionamos à visites. 
- depois analisamos os vértices adjacentes a A, como Prim é guloso, ele vai selecionar a aresta mais leve para visitar o próximo vértice, no caso, B. 
- agora, analisamos todos os vértices alcancaveis por A e B, selecionando um que é alcançavel pela aresta mais leve disponível, adicionando o vertice à visited. 
- Não selecionamos arestas que criariam um ciclo, pois os dois vertíces que resultam na aresta já estariam na lista visited, mesmo que o peso seja mínimo.



MST-Prim
    for cada u pertencente a V[G]
        u.chave = infinito
        u.pai = nil
    r.chave = 0
    Q = V[G]
    while Q != 0
        u = extract-min(Q)
        for cada v pertencente a G.Adj[U]
            if v pertence a Q e w(u,v) v.chave
                v.pai = u
                v.chave = w(u,v)