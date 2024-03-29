# Sars-cov-2

def devaccin(world,parallele,duree_vaccin):
    for i in range(len(world[:,0])):
        for j in range(len(world[0,:])):
            if (world[i][j] == 2 and parallele[i][j] != duree_vacin):
                parallele[i][j] += 1
            elif(parallele[i][j] == duree_vacin):
                world[i][j] = 0
                parallele[i][j] = 0
    return world , parallele
