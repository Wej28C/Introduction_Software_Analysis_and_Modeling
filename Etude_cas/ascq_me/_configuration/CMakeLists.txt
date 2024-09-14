#Dans le répertoire config 

file(GLOB CONFIG_FILES *.config)

# Copiez les fichiers de configuration vers un répertoire de sortie

foreach(config_file ${CONFIG_FILES})

    configure_file(${config_file} ${CMAKE_BINARY_DIR}/_configuration/${config_file} COPYONLY)
endforeach()

# Créez une variable pour stocker le chemin vers les fichiers de configuration
#set(CONFIG_PATH ${CMAKE_BINARY_DIR}/_configuration)