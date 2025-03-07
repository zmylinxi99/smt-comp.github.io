+++
title = 'Parallel and Cloud Tracks'
date = 2024-05-07T10:09:02+01:00
draft = false
aliases = ['/parallel-and-cloud-tracks.html']
+++

## Parallel and Cloud Tracks

Like last year we are organising new, experimental, cloud and parallel tracks
for SMT-COMP. Similar tracks were organised in the SAT competition 2020
and the competition had a positive impact on the development of parallel
SAT solvers (see <https://satcompetition.github.io/2020/>).

### The Concept

The goal in both the cloud and the parallel tracks is to measure the
success of a solver in solving a single, hard instance. This will be done by
giving solvers instances one at a time, similar to the SMT-COMP single-query
track. The participating solvers will be scored based on the number of
instances that a solver solves within the per-instance wall-clock time limit
and the total run time, similar to the single-query track’s parallel score.

For these tracks we need to choose in total 400 benchmarks from the
single-query track logics, and we are specifically reaching out to you, the
community and especially the competitors, for suggesting suitable instances to
be included in the tracks. In addition we will try to identify instances that
are considered interesting. All instances should come from the smt-lib
benchmark library.

The solver submission rules follow those of the rest of the tracks. However,
on this track we do accept portfolio solvers, as defined in the rules, as
competitors. We encourage submission of non-portfolio solvers and reserve the
right to give special mentions to non-portfolio solvers in reporting the
results.

While the standard competition will be run in StarExec, the parallel and cloud
tracks will be run on Amazon Web Services. AWS has kindly agreed to sponsor
the participants in the testing phase.

### Cloud track

The Cloud Track evaluates the effectiveness of parallel SMT solvers to run in a
distributed manner. The solvers participating in this track will be executed
with a wall-clock time limit of 20 minutes running on 100 m4.4xlarge machines
in parallel. Each m4.4xlarge machine has 16 virtual CPUs and 64 GB memory.
Communication between the machines is possible using MPI and SSH.

Participants of this track are required to submit their solver via a GitHub
repository (which can be private). The repository should contain a docker file
that compiles the solver. As an example, scripts for account configuration and
instructions to run HordeSAT in the default configuration are available at
<https://github.com/aws-samples/aws-batch-comp-infrastructure-sample>.

### Parallel track

The solvers participating in this track will be executed with a wall-clock time
limit of 20 minutes, thus similar to the Single Query Track. Each solver will
be run on a single AWS machine of the type m4.16xlarge, which has 64 virtual
cores and 256GB of memory. More details about m4.16xlarge nodes can be found
[here](https://aws.amazon.com/about-aws/whats-new/2016/09/introducing-new-m4-instance-size-m4-16xlarge-and-new-region-availability-of-m4-instances/).

Similar to the Cloud Track, participants of this track are required to submit
their solver via a GitHub repository (which can be private). The repository
should contain a docker file that compiles the solver.
