TOP = ../..
AMREX_HOME       = ../../Submodules/amrex
AMREX_HYDRO_HOME = ../../Submodules/AMReX-Hydro

# Variables for the user to set ...
DIM                   = 3     # must be 3d for HIT
USE_MPI               = TRUE
USE_OMP               = FALSE
USE_CUDA              = FALSE
USE_TURBULENT_FORCING = TRUE
USE_FAST_FORCE        = FALSE
USE_VELOCITY          = FALSE

COMP	   = gcc
DEBUG	   = FALSE
PRECISION = DOUBLE

USE_HYPRE = FALSE
USE_METIS = FALSE
USE_XBLAS = FALSE
USE_SENSEI_INSITU = FALSE
#USE_ASSERTION=TRUE

EBASE     = amr

ifeq (${USE_XBLAS}, TRUE)
   XTRADEFS   += -DXBLAS
   XTRAINCLOC += $(HOME)/tmp/xblas-1.0.248/src
   XTRALIBLOC += $(HOME)/tmp/xblas-1.0.248/src
   XTRALIBS   += -lxblas
endif

ifeq (${USE_VELOCITY}, TRUE)
  #AMRVIS_DIR defines the directory in which we will find pAmrvis (e.g. DataServices, AmrData and FABUTIL)
  AMRVIS_DIR = $(AMREX_HOME)/Src/Extern/amrdata
endif

Blocs   := .

include ./Make.package
include $(TOP)/Exec/Make.IAMR
