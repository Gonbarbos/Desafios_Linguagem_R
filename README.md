# Desafios_Linguagem_R
Algund desafios feitos na Linguagem R

# DESAFIO 3 ---------------------------------------------------------------

estoque <- c(12, 11, 28, 14, 12)
prod <- c("Notebook", "Smartphone", "Tablet", "Fone de ouvido", "Carregador")

names(estoque) <-  prod
print(estoque)

total_estoque <- sum(estoque)
print(total_estoque)

nome_total_estoque <-  c("total")
names(total_estoque) <- nome_total_estoque

print(estoque)
prod_reposicao <- estoque < 15
print(total_estoque)

prod_reposicao <- names(estoque[prod_reposicao])
print(prod_reposicao)

cat("Os produtos que precisam de reposição são: ", paste(prod_reposicao, collapse = ", " ))








# DESAFIO 4 ---------------------------------------------------------------

times <- c("Flamengo", "Fluminense", "Vasco", "Botafogo")
rodadas <- c("1º rod", "2º rod", "3º rod", "4º rod", "5º rod", "6º rod", "7º rod", "8º rod", "9º rod", "10º rod", "11º rod")

gols_flamengo <- c(1, 1, 1, 5, 2, 2, 5, 0, 1, 2, 5)
gols_fluminense <- c(0, 0, 1, 3, 0, 1, 1, 2, 0, 2, 3)
gols_vasco <- c(1, 0, 1, 2, 4, 1, 2, 1, 0, 0, 1)
gols_botafogo <- c(1, 2, 1, 1, 2, 2, 1, 0, 0, 1, 0)


gols_times <- c(gols_flamengo, gols_fluminense, gols_vasco, gols_botafogo)


matriz_gols <- matrix(gols_times, nrow = 4, byrow = TRUE)
rownames(matriz_gols) <- times
colnames(matriz_gols) <- rodadas
print(matriz_gols)

total_gols <- rowSums(matriz_gols)
matriz_gols <- cbind(matriz_gols, "Total" = total_gols)

total_mais_gols <- c(names(which.max(total_gols) ))
