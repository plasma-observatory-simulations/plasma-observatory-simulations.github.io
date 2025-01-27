Vlasiator details
================================

Vlasiator [1]_ [2]_ is a 6D ion-kinetic hybrid-Vlasov model for the Earth's global magnetosphere. Vlasiator simulates the dynamics of plasma using a hybrid-Vlasov model, where protons are described by their distribution function f(r,v,t) in ordinary (r) and velocity (v) space, and electrons are a charge-neutralising fluid. This approach neglects electron kinetic effects but retains ion kinetics. The time-evolution of f(r,v,t) is given by Vlasov's equation, which is coupled self-consistently to Maxwell's equations giving the evolution of the electric and magnetic fields E and B. Maxwell's equations neglect the displacement current. The equations are closed by a generalised Ohm's law including the Hall term.

+------------------------+---------------------------------------------------------------------+
| Additional information | `Vlasiator <https://www.helsinki.fi/en/researchgroups/vlasiator>`_  |
|                        | group at Helsinki University                                        |
+------------------------+---------------------------------------------------------------------+
| WG Point of Contact    | Markku Alho                                                         |
+------------------------+---------------------------------------------------------------------+
| Current code version   | 5.3.1                                                               |
+------------------------+---------------------------------------------------------------------+
| code/repository        | `Zenodo <https://doi.org/10.5281/zenodo.3640593>`_,                 |
|                        | `GitHub <https://github.com/fmihpc/vlasiator>`_                     |
+------------------------+---------------------------------------------------------------------+
| Legal Code License     | `GPL-2.0 <https://www.gnu.org/licenses/old-licenses/gpl-2.0.html>`_ |
+------------------------+---------------------------------------------------------------------+
| Software code          | C++                                                                 |
| languages and tools    | `Analysator <https://github.com/fmihpc/analysator>`_ Python toolkit |
+------------------------+---------------------------------------------------------------------+

Use cases
---------

Vlasiator has been used to describe magnetic reconnection in global magnetospheric context, especially in the magnetotail [3]_ and the kinetic features of the tail reconnection processes [4]_ [5]_ and the global evolution of flux transfer events [6]_.

Data availability
-----------------

Available data to be listed (public/on-request/available via collaboration).

Data access subject to `Rules of the Road <https://www.helsinki.fi/en/researchgroups/vlasiator/rules-of-the-road>`_. Some data is available publicly.

Simulations-on-demand
---------------------

Global Vlasiator simulations take months to complete, and are not offered on an on-demand basis; larger collaborations can o fcourse be planned.

Small/local simulations can be set up and supported for external users on best-effort basis.

Numerical Methods
-----------------

Vlasiator propagates the distribution function forward in time with a conservative fifth-order accurate Semi-Lagrangian algorithm. This algorithm allows using long time steps even in the presence of strong magnetic fields, as the propagation in velocity space is not limited by the Courant-Friedrichs-Levy (CFL) condition. The field solver is a second-order accurate divergence-free upwind-constrained transport method.

Vlasiator has a parallel Cartesian mesh in ordinary space. In each spatial cell there is a 3-dimensional sparse velocity grid, modelling the in the full 6-dimensional distribution function. Empty velocity space cells are neither stored nor propagated, which in a typical case reduces the total number of phase space cells by a factor of at least 100 while impacting mass conservation to a relative level of no more than 10−6.

The ordinary space grid is implemented using the open source `DCCRG <https://github.com/fmihpc/dccrg>`_ grid library developed by the group. It is parallelized using MPI-based domain decomposition and OpenMP-based threading is used to further parallelise the work done by each process. The Vlasov solver is vectorised using AVX intrinsics. The load is balanced with the `Zoltan <http://www.cs.sandia.gov/zoltan/>`_ library using its recursive coordinate bisection partitioner. I/O is performed using our own parallel `VLSV <https://github.com/fmihpc/vlsv>`_ file format, which can be analyzed using VisIt or by using the Python-based `Analysator <https://github.com/fmihpc/analysator>` package.


References
----------

.. [1] Palmroth, M. et al. Vlasov methods in space physics and astrophysics. Living Rev Comput Astrophys (2018). `<https://doi.org/10.1007/s41115-018-0003-2>`_
.. [2] Ganse, U. et al. Enabling technology for global 3D + 3V hybrid-Vlasov simulations of near-Earth space. Phys. Plasmas (2023). `<https://doi.org/10.1063/5.0134387>`_
.. [3] Palmroth, M. et al. Magnetotail plasma eruptions driven by magnetic reconnection and kinetic instabilities. Nat. Geosci. (2023). `<https://doi.org/10.1038/s41561-023-01206-2>`_
.. [4] Cozzani, G. et al. Interplay of magnetic reconnection and current sheet kink instability in the Earth's magnetotail. Geophysical Research Letters (2025). `<https://doi.org/10.1029/2024GL111848>`_
.. [5] Zaitsev, I. et al. Ion‐mediated tearing and kink instabilities in the Earth's magnetosphere: Hybrid‐Vlasov simulations. Journal of Geophysical Research: Space Physics. (2025). `<https://doi.org/10.1029/2024JA032615>`_
.. [6] Pfau-Kempf, Y. et al. Global evolution of flux transfer events along the magnetopause from the dayside to the far tail. Ann. Geophys. Discuss. (preprint, 2024), `<https://doi.org/10.5194/angeo-2024-26>`_, in review.