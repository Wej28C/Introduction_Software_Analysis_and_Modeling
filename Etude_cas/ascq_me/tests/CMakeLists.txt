#Dans le répertoire de test

enable_testing()

file(GLOB CONFIG_FILES ${CMAKE_BINARY_DIR}/_configuration/*.config)



# Inclusion  des fichiers de configuration
#include_directories(${CONFIG_PATH})

# Création d'un test pour chaque configuration

foreach(config_file ${CONFIG_FILES})
    get_filename_component(CONFIG_NAME ${config_file} NAME)

    # Créez une cible de test personnalisée pour chaque configuration
   	 add_test(NAME ${CONFIG_NAME} COMMAND ascq_me _configuration/${config_file})
    	
endforeach()
