# Sars-cov-2

def tour_vaccin(world,rzero,durée_infection,parallele,duree_vaccin):
    worldbis = np.copy(world)
    for i in range (0, len(world[:,0])):
        for j in range ( 0, len(world[0,:])):
            if world[i,j] == 1 and verif_voisins(worldbis,i,j):
                nb = 0 
                while nb < rzero and verif_voisins(worldbis,i,j):
                    x = i + (random.randint(-1,1))
                    y = j + (random.randint(-1,1))
                    if (x >= 0 and x <= len(world[:,0])-1) and (y>= 0 and y<= len(world[0,:])-1):
                        if worldbis[x,y] != None and worldbis[x,y]!= 1:
                            worldbis = infection_cellule(worldbis,x,y)
                            nb += 1
    return devaccin(desinfection(worldbis,durée_infection,parallele),duree_vaccin)




    def tour_boucle_vaccin(world,rzero,nbtour,freq_depla,duree_infection,parallele,duree_vaccin,freq_vaccin):
    worldbis = np.copy(world)
    parallelebis = np.copy(world)
    i = 0
    while i < nbtour:
        if i%freq_depla == 0:
            worldbis,parallelebis = deplacement(world,parallele)
        if i%freq_vaccin == 0:
            worldbis = vaccin(world)
        worldbis,parallelebis = tour_vaccin(world,rzero,duree_infection,parallele,durree_vaccin)
        print(world,parallele,"\n")
        i+= 1
    return worldbis
