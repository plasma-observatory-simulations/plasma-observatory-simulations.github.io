
Model descriptions
==================

Models overview
---------------

Vlasiator
^^^^^^^^^

Vlasiator is a 6D ion-kinetic hybrid-Vlasov model for the Earth's global magnetosphere. Vlasiator simulates the dynamics of plasma using a hybrid-Vlasov model, where protons are described by their distribution function f(r,v,t) in ordinary (r) and velocity (v) space, and electrons are a charge-neutralising fluid. This approach neglects electron kinetic effects but retains ion kinetics. The time-evolution of f(r,v,t) is given by Vlasov's equation, which is coupled self-consistently to Maxwell's equations giving the evolution of the electric and magnetic fields E and B. Maxwell's equations neglect the displacement current. The equations are closed by a generalised Ohm's law including the Hall term.

.. toctree::
   Vlasiator details<models/vlasiator>


HYPSI
^^^^^

HVM
^^^^

ViDA
^^^^

MAGE
^^^^

SWMF
^^^^

The Space Weather Modeling Framework (SWMF) is a software framework which models a wide range of temporal and spatial scales as well as the different physical processes governing the different heliophysics domains through a modular approach. The heart of the framework is the BATS-R-US versatile, high-performance, generalized magnetohydrodynamic code with adaptive mesh refinement that can be configured to solve the governing equations of ideal and resistive MHD, semi-relativistic, anisotropic, Hall, multispecies, and multi-fluid extended magnetofluid equations (XMHD) and non-neutral multifluid plasmas. The BATS-R-US is used to model several physics domains, and its high efficiency (faster than real time) is crucial for the success of the framework. Further descriptions of the SWMF modules can be found below.

.. toctree::
   SWMF details<models/swmf>

MENURA
^^^^^^

Amitis
^^^^^^

Hall-MHD
^^^^^^^^

CAMELIA
^^^^^^^

iPIC3D
^^^^^^

Athena++
^^^^^^^^

GPAT
^^^^

VPIC
^^^^

*muphyII* 
^^^^^^^^^^

The *muphyII* code is a simulation framework for collisionless plasma physics and targeted at space plasmas in particular. The *muphyII* code utilizes a hierarchy of models with different inherent scales to address the separation of scales problem typically encountered in these plasmas. It allows stand-alone use of models as well as a model-based dynamic and adaptive domain decomposition and resorts to novel techniques for energy conservation, careful treatment of inner-domain model boundaries for interface coupling, and robust time stepping algorithms.


.. toctree::
   muphyII details<models/muphyii>

PSC
^^^

Plasma Simulation Code (PSC) is a 3-dimensional fully electromagnetic particle-in-cell code for kinetic plasma simulations. It supports Nvidia GPUs and patch-based dynamic load balancing.

.. toctree::
   PSC details<models/psc>

Template model
^^^^^^^^^^^^^^

This is an example for adding pending descriptions.

.. toctree::
   Template details<models/template>
