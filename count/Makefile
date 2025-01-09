rootDir = ..
include ${rootDir}/include.mk
modObjDir = ${objDir}/count

halCount_srcs = halCount.cpp
halCount_objs = ${halCount_srcs:%.cpp=${modObjDir}/%.o}
srcs = ${halCount_srcs}
objs = ${srcs:%.cpp=${modObjDir}/%.o}
depends = ${srcs:%.cpp=%.depend}
progs = ${binDir}/halCount

all: progs
libs:
progs: ${progs}

clean: 
	rm -f ${objs} ${progs} ${depends}

test:

include ${rootDir}/rules.mk

# don't fail on missing dependencies, they are first time the .o is generates
-include ${depends}


# Local Variables:
# mode: makefile-gmake
# End:

