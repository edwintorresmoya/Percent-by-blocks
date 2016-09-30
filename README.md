# Percent-by-blocks
Retuns the percentage by blocks


percent.colmns = function(base, columnas = 1:ncol(base), filas = 1:nrow(base)){
    base2 = base
    for(j in columnas){
        suma.c = sum(base[,j])
        for(i in filas){
            base2[i,j] = base[i,j]*100/suma.c
        }
    }
    return(base2)
}
