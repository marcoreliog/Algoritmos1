// A ideia do algoritmo de Kruskal utiliza uma estrutura de dados de conjuntos disjuntos para manter vários conjuntos disjuntos de elementos. Cada conjunto contém os vértices em uma aŕvore da floresta atual. FIND-SET retorna um elemento representativo do conjunto que contém u. Assim, podemos testar se dois vertices percentem a mesma arvore testando find_set(u) é igual a find_set(v). Para combinar arvores, kruskal chama o procedimento UNION. Kruskal escolhe a aresta de peso minimo e adiciona a arvore, e vai escolhendo todas as arestas em ordem crescente de peso que nao formam um ciclo até incluir todos os vértices à árvore, ou adicionar V - 1 arestas. Tempo de execução é O(E lg V)

MST-Kruskal
A = 0
for cada vertice V pertencente a G.V
    make-set(v)
ordene as arestas de G.E em ordem não decrescente de peso w
for cada aresta (u,v) pertencente a G.E, tomada em ordem não decrescente de peso
    if find-set(u) != find-set(v)
    union(u,v)

    