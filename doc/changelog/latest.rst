[latest]
========

Release Notes
-------------
TODO: Summarize the most important changes

Changelog
---------

Backwards incompatible changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- nothing yet

Added
^^^^^
- implemented the :class:`~tenpy.models.lattice.IrregularLattice`.
- extended user guide on lattices, :doc:`/intro/lattices`.

Changed
^^^^^^^
- :meth:`tenpy.models.lattice.Lattice.plot_basis` now allows to shade the unit cell and shift the origin of the plotted basis.
- Don't use `bc_shift` in :meth:`tenpy.models.lattice.Lattice.plot_couplings` any more - it lead to confusing figures.
  Instead, the new keyword `wrap=True` allows to directly connect all sites.
  This is done to avoid confusing in combination with :meth:`~tenpy.models.lattice.Lattice.plot_bc_identified`.

Fixed
^^^^^
- Wrong results of :meth:`tenpy.networks.mps.MPS.get_total_charge` with ``only_physical_legs=True``.
- :meth:`tenpy.models.lattice.Lattice.plot_bc_identified` had a sign error for the `bc_shift`.
- :meth:`~tenpy.models.lattie.Lattice.calc_H_MPO_from_bond` didn't work for charges with blocks > 1.
- TEBD: keep qtotal of the B tensors constant
