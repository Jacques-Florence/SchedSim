target_sources(mdp
	PRIVATE
	${CMAKE_CURRENT_SOURCE_DIR}/glpkImplementation.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/learningStrategy.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/linearProgramming.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/matrixLearning.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/noLearning.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/twoPhases.cpp
	PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}/learningStrategy.h
	${CMAKE_CURRENT_SOURCE_DIR}/solver.h
	${CMAKE_CURRENT_SOURCE_DIR}/lpImplementation.h
	)
add_subdirectory(reinforcementLearning)
install(FILES
	${CMAKE_CURRENT_SOURCE_DIR}/learningStrategy.h
	${CMAKE_CURRENT_SOURCE_DIR}/solver.h
	${CMAKE_CURRENT_SOURCE_DIR}/lpImplementation.h
	DESTINATION include/mdp/learning)
