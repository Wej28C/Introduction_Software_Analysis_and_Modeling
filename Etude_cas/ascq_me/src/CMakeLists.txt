# Liste des fichiers source
set(SOURCES
	aa.cpp
	ascq_me_configuration.cpp
	ascq_me_display.cpp
	ascq_me.cpp
	cleavage.cpp
	complex.cpp
	digest.cpp
	error.cpp
	fft4g.cpp
	formula.cpp
	isodistrib.cpp
	modification_table.cpp
	modifications_for_digestion.cpp
	seqio.cpp
	tables.cpp
	util.cpp
)

# Inclure le répertoire "include" pour que les fichiers d'en-tête soient accessibles
include_directories(include)


add_executable(ascq_me ${SOURCES})


# Créez une bibliothèque à partir des fichiers source
add_library(AskmeLib ${SOURCES})