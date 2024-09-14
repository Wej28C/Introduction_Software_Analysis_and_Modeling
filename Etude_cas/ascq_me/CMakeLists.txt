# Precise la version minimale pour assurer le bon fonctionnement de la génération de code
cmake_minimum_required(VERSION 3.0)

#Détaille le nom du projet et le cas échéant le langage associé
project(ascq_me CXX)


# Commande qui crée une variable locale
set (SRC src)
# Variable pour répertoire de tests
set (TEST tests)


# Commande qui donne le chemin vers un répertoire qui devrait aussi contenir un
# fichier CMakeList pour faire différentes choses ...
add_subdirectory(${SRC})

add_subdirectory(${TEST})

# Active dashboard
include(CTest)
