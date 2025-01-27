
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


Template model
^^^^^^^^^^^^^^

This is an example for adding pending descriptions.

.. toctree::
   Template details<models/template>
