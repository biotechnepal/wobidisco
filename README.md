Wobidisco
=========

This is the umbrella documentation/tooling project for:

- [Biokepi](https://github.com/hammerlab/biokepi): a library of composable
  “pieces of bioinformatics workflows” (a.k.a. *“nodes”*).
- [Ketrew](https://github.com/hammerlab/ketrew): a computational workflow
  manager on which Biokepi is based.
- [Coclobas](https://github.com/hammerlab/coclobas): Ketrew can interact with
  Torque/PBS, Platform LSF, YARN, and other HPC schedulers; Coclobas is another
  such scheduler, specialized in cloud/docker computing environments (Google
  Container Engine, AWS Batch, or “local” Docker).
- [Epidisco](https://github.com/hammerlab/epidisco): a Biokepi workflow used in
  production for a clinical trial; i.e. an actively maintained large workflow
  example.
- [Secotrec](https://github.com/hammerlab/secotrec): a deployment/administration
  tool for Ketrew/Coclobas setups.


Documentation
-------------

Individual projects have detailed documentation websites at
<http://hammerlab.org/docs>.

The following tutorials are available here:

- [Running](./doc/running-local.md) Epidisco (or any Biokepi workflow) using
  Ketrew/Coclobas in *local-docker* mode (i.e. using Coclobas to schedule docker
  containers on a single machine).
- [Creating](./doc/debug-workflow-node.md) a “debug” workflow node to
  experiment/troubleshoot commands within the same environment as the one of the
  workflow (Secotrec-based).
- [Generating](./doc/biokepi-input-scripts.md)
  JSON input descriptions for Biokepi workflows which use the
  `Biokepi_pipeline_edsl.Pipeline_library.Input` modules (Epidisco is one of
  them).


Testing The Examples
--------------------

We use `tools/check-examples.sh` (with the tool `tools/code-of-markdown/`) to
run the examples in the Markdown files
(incl. with [TravisCI](https://travis-ci.org/hammerlab/wobidisco)).
You can run it by simply:

    sh ./tools/check-examples.sh

if you are debugging, you may want to speed-up the script by not
checking/installing the dependencies every time.

    without_deps=true sh tools/check-examples.sh




