FROM buildpack-deps:jessie
MAINTAINER Konstantin Molchanov <moigagoo@live.com>

RUN git clone git://github.com/nim-lang/Nim.git nim;\
    cd nim; git clone --depth 1 git://github.com/nim-lang/csources;\
    cd csources; sh build.sh;\
    cd ..; bin/nim c koch; ./koch boot -d:release;\
    ln -s `pwd`/bin/nim /bin/nim