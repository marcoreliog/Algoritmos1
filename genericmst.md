//Algoritmo genérico para gerar uma arvore geradora minima. O conceito de uma AGM envolve percorrer o grafo para devolver uma arvore que conecte todos os vertices com o menor custo possível.
Dois pontos importantes:
A aresta de peso mínimo E do grafo pertence à alguma AGM criada. A prova se da ao fato de que se a aresta já está no grafo, isso é provado. Caso contrário, se adicionarmos a aresta ao grafo formaríamos um ciclo, assim, teríamos que remover outra aresta F, logo T2 = T1 - F + E, assim W(E) <= W(F), pois é tem peso mínimo. Mas T1 já era uma AGM, então T1 = T2, logo, T2 também é uma AGM que contém E

Se E for uma aresta de peso máximo, existe um AGM que não contém E. Se é não percente à AGM criada, pronto. Caso contrário, remova E de T, formando S e V-S. Adicione outra aresta F que fechava um ciclo no grafo original. Como E tinha peso máximo, E >= F, assim peso T1 >= T2, T1 era uma arvore geradora mínima, isso implica que T2 também é, logo existe uma AGM sem E



generic-mst(G,w)
A = 0 // subconjunto de alguma arvore geradora
While A não formar uma AGM 
    encontre uma aresta (u,v) que seja segura para A
    A = A união |(u,v)|
return A


