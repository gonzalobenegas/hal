rootDir = ..
include ${rootDir}/include.mk
modObjDir = ${objDir}/identity

halIdentity_srcs = halIdentity.cpp
halIdentity_objs = ${halIdentity_srcs:%.cpp=${modObjDir}/%.o}
srcs = ${halIdentity_srcs}
objs = ${srcs:%.cpp=${modObjDir}/%.o}
depends = ${srcs:%.cpp=%.depend}
progs = ${binDir}/halIdentity

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

