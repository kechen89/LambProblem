F77=f77

#LINK=f77 -g 
#LINK=f77 -O3
LINK=f77 -xlibmopt -xtarget=ultra1/170 -xchip=ultra -fast -native -O4 -reduction -s -xarch=v8plusa -libmil -xO4 -I/opt/SUNWspro/SC4.0/include -L/opt/SUNWspro/SC4.0/lib

#FLAGS=-c -g -e
#FLAGS=-c -e -O3
FLAGS=-c -e -xlibmopt -xtarget=ultra1/170 -xchip=ultra -fast -native -O4 -reduction -s -xarch=v8plusa -libmil -xO4 -I/opt/SUNWspro/SC4.0/include -L/opt/SUNWspro/SC4.0/lib

OBJS= force_verticale.o

.f.o:
	$(F77) $(FLAGS) $*.f

default: force_verticale

force_verticale:$(OBJS)
	$(LINK) $(OBJS) -o xforce
	/bin/rm -f force_verticale.o *.trace

all: 
	/bin/rm -f *.o *.trace
	make force_verticale

clean: 
	/bin/rm -f *.o *.trace
