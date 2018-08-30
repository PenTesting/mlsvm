All: get_mat_info
CC 	 = g++ -L. 
CFLAGS 	 = -I.	
CPPFLAGS = -std=c++11 -O3 

include ${PETSC_DIR}/lib/petsc/conf/variables
include ${PETSC_DIR}/lib/petsc/conf/rules

get_mat_info: get_mat_info.o  chkopts
	-${CLINKER} -o get_mat_info get_mat_info.o ${PETSC_MAT_LIB}
	${RM} -f get_mat_info.o 

get_vec_info: get_vec_info.o  chkopts
	-${CLINKER} -o get_vec_info get_vec_info.o ${PETSC_VEC_LIB}
	${RM} -f get_vec_info.o 

getSubMatrix: ../preprocessor.o ../common_funcs.o getSubMatrix.o  chkopts
	-${CLINKER} -o getSubMatrix  ../common_funcs.o ../preprocessor.o getSubMatrix.o ${PETSC_MAT_LIB}
	${RM} -f getSubMatrix.o 

getSubVector: ../preprocessor.o ../common_funcs.o getSubVector.o  chkopts
	-${CLINKER} -o getSubVector  ../common_funcs.o ../preprocessor.o getSubVector.o ${PETSC_MAT_LIB} ${PETSC_VEC_LIB}
	${RM} -f getSubVector.o 
	