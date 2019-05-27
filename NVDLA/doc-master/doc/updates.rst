.. _updates:

Open NVDLA Repository Updates
*****************************

This document is a quick reference guide to changes in the NVDLA repository. Most recent updates are at the top of the document.  Detailed information can be obtained from the ``git`` list of commits. 

5/15/2018
=========

Release NVDLA Virtual platform on Amazon Web Services (AWS) FPGA which supports HW regression and SW tests. See :doc:`vp_fpga` section. Support "nv_small" configuration.

4/19/2018
=========

First release of NVDLA V2 -- the configurable NVDLA.  This release also includes
a new testbench which can be used to validate the design.  However,
the only tested configuration is the "nv_small" configuration. See
the :doc:`hw/v2/scalability` document for details on the nv_small 
design configuration parameters.  While the nv_small config passes many
tests, coverage isn't yet to tapeout quality levels.

12/1/2017
=========

Released a SystemC model of the NVDLA hardware, suitable for simulation and
verification.  This SystemC model lives in ``cmod/``, and information on
building it is in the :ref:`tree_build` section.

Additionally, this release contains experiemental support for building the
NVDLA RTL using Verilator; for more information on this, see the
:ref:`verilator_testbench` section.

11/21/2017
==========

A few updates in the nvdla hardware tree, most notably moving further
development on the non-configurable NVDLA implementation to its own stable
branch, ``nvdlav1``, and renaming the full-precision non-configurable
implementation to ``nv_full``.  The ``master`` branch, from now on, will
contain potentially-destabilizing ongoing effort for a configurable NVDLA. 
Note that the default branch has changed, and users may wish to modify which
upstream branch they are tracking.

This release includes bugfixes for Xilinx Vivado and Mentor Questa simulators.

11/1/2017
=========
First drop of RTL build system to be used for creating multiple NVDLA configurations.  The 
configurations themselves will be checked in as features become available.  All configuration
parameters to create a small config NVDLA with 64 MACs is expected before the end 2017.

10/24/2017
==========
Initial release of the NVDLA Kernel Mode Driver (KMD) for Linux.

10/18/2017
==========
The traceplayer testbench has been updated to split the memory model into two logically separate region. Support was added to the axi_slave and memory model for non-zero burst lengths which is used by the cvsram interface. Added cvsram form of sanity tests. Added sdp and pdp sanity tests. Added googlenet_conv2_3x3_int16 and cc_alexnet_conv5_relu5_int16_dtest_cvsram layer tests.

Changes to address issues #16, #23, #24 on the NVDLA GitHub site.

10/6/2017
=========
The large configuration RTL is updated to a 64-bit address bus on the DBBIF and RAMIF busses.  The previous design was 32-bit externally and 40-bit internally.  This reflects the final size for the large configuration.

Changes to address issues #6, #7, #9 on the NVDLA GitHub site.


9/25/2017
=========
Initial release of large configuration RTL, trace player testbench, synthesis scripts, performance model spreadsheet, and documentation.

