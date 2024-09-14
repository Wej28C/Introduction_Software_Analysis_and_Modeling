
# Permet d'avoir accès à la macro CHECK_INCLUDE_FILE_CXX
include(CheckIncludeFileCXX)

# Vérifie si sstream est disponible
# la variable SSTREAM indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(sstream SSTREAM)

# Test de la valeur de SSTREAM
if(NOT SSTREAM)
  message("====> No <sstream> found")
endif()


# Vérifie si math.h est disponible
# La variable MATH_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(math.h MATH_H)

# Test de la valeur de MATH_H
if(NOT MATH_H)
  message("====> No <math.h> found")
endif()

# Vérifie si stdio.h est disponible
# La variable STDIO_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(stdio.h STDIO_H)

# Test de la valeur de STDIO_H
if(NOT STDIO_H)
  message("====> No <stdio.h> found")
endif()

# Vérifie si stdlib.h est disponible
# La variable STDLIB_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(stdlib.h STDLIB_H)

# Test de la valeur de STDLIB_H
if(NOT STDLIB_H)
  message("====> No <stdlib.h> found")
endif()

# Vérifie si time.h est disponible
# La variable TIME_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(time.h TIME_H)

# Test de la valeur de TIME_H
if(NOT TIME_H)
  message("====> No <time.h> found")
endif()

# Vérifie si ctype.h est disponible
# La variable CTYPE_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(ctype.h CTYPE_H)

# Test de la valeur de CTYPE_H
if(NOT CTYPE_H)
  message("====> No <ctype.h> found")
endif()

# Vérifie si string.h est disponible
# La variable STRING_H indique si oui ou non la recherche a été fructueuse 
CHECK_INCLUDE_FILE_CXX(string.h STRING_H)

# Test de la valeur de STRING_H
if(NOT STRING_H)
  message("====> No <string.h> found")
endif()

# Recherche d'un fichier inexistant
# Et affichage de l'échec
CHECK_INCLUDE_FILE_CXX(swiper SWIPER)
if(NOT SWIPER)
  message("====> No <swiper> found")
endif()

#liste des fichiers headers

set (HEADERS 
	*.h )

# Créez une bibliothèque à partir des fichiers headers 
add_library(AskmeLib ${HEADERS})

# pour qu'il soit ajouté à sources 
# target_include_directories(AskmeLib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})