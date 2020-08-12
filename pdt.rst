.. vim: ft=rst


##################
System Development
##################

.. _`pdt`:

************
plan do test
************

Inform
======

.. _`pdttradition`:

:Tradition:

`Waterfall`_ documents including
*requirement-design-implementation-verification*
are quite common.

But many alternative, more
`agile`_ methods
have surfaced, for a reason.

.. _`pdtevolution`:

:Evolution:

A general approach starts from the `evolutionary`_ *mutation-selection*.
Considering encapsulations, this leads to

- plan
- do
- test

until fit.

Development goes in cycles of varying size:

- all of them are ``pdt``
- the `waterfall`_
  *requirement-design-implementation-verification* is a ``pdt`` cycle of ``pdt`` cycles.
- usage is the ultimate test and brings *maintenance* cycles
- system alternatives eventually end the *life cycle*
  with *deprecation*, *obsolescence* and *death/extinction*

``pdt`` is general, including the *horizontal* `waterfall`_,
but following `cohesion`_, *vertical* cycles, i.e. by topic, are preferred.
``pdt`` is `agile`_.

Plan
====

.. _`pdtencapsulation`:

:Encapsulation: `pdtevolution`_

Creation (of a variable) and selection (of a value) in `evolution`_
corresponds to **trial-and-error**.

- All systems evolving, do so by trial and error.
- Every algorithm is trial-and-error.
  Good algorithms have less trials.

To save energy
evolution produces

- **encapsulations**

Information flow `is energy`_.
Within encapsulations information flow is more efficient,
which makes encapsulations more economic.

An encapsulation has *input-processing-output*.
`Information`_ flow between encapsulations (input, output) is minimal:

- the **interface** is minimal

There are two orthogonal encapsulation
`lattices`_ (topologies).

- *Unit* is used for the *physical* topology.

  - Departments and ultimately the developer are
    *organizational* or *processing* units.
    They are physical units.

  - Reality and mind are different *physical* units.

  - Different organizations are different *physical* units.

- *Node* is used for the *content* topology.

We concentrate on the content topology.

.. _`pdtdevelopment`:

:Development: `pdtevolution`_

With shorter and less Roman wording,
evolution consists of *make-test* steps.

- *creation-selection* = *make-test*

When we consider *physical* units, we have e.g.

- *make-test* in mind: plan
- *make-test* in reality: do

Compared to *trial-error*, ``trial=plan,do``.
``plan,do`` emphasizes the two *units* and the interface between them (``,``).

The *mind* needs to have a good *map* of reality,

- to create a plan that fits
- to minimize the interaction between these two physical units

The map of reality evolves with reality.
So there needs to be *feedback*.
The *feedback* is called *test* here.

Compared to *trial-error*: ``error=feedback=test``
*Test* is more neutral than *error*.
It is an obvious evolutionary step of the map,
to sync up with reality.

The syncing needs to happen often,
if the reality changes often.
The same for seldom.

.. _`pdtcontent`:

:Content: `pdtevolution`_

Development is mapped to *development documentation*

- to organize thoughts

- to communicate with others

- to decrease the dependence of a project
  from *processing* units.

- to stay consistent over time despite

  - swap of *processing* units
  - memory loss of *processing* units

Note, that there is also system documentation, which is not considered here.

In the content topology,
*plan-do-test* are all documentation texts,
i.e. words that link to concepts, that are either up or down:

- *up*: more general (less variables)
- *down*: more concrete (more variables)

*Content items* are elementary nodes.
They are grouped to *content files* or directories.
All of them are *content nodes*.

The *test* is the environment of the *do* and
gets constructed in parallel or before the *do*
to check the *do* against the *plan*.

- *plan* = uplinks
- *do* = downlinks
- *test* = uplinks

*plan-test* forms a brace around the *do*.

.. _`pdtcode`:

Code is regarded as documentation using a programming language.
There is no need to duplicate that with a human language.

- Human language descriptions have

  - plan: uplinks to the human context in which the system is to be integrated
  - do: downlink to what needs to be done to make the system useful
  - test: uplink to verify that what was done is well integrated

- Computer language descriptions (code) has its own ``pdt``'s with possibly many further layers

  - plan: uplink to the *do* of the human description arguing for a specific *do* on this node
  - do: downlink, e.g. via an interface, to more detailed implementation
  - test: uplink to the *do* of the human description using the *do* of this node, e.g. this interface

*Content nodes* are grouped

- *vertically* (more abstraction layers into one document)
- *horizontally* (by topic)

For a software project vertical groupings are

- `pdt` documents
- the code (possibly in more ``pdt`` groupings)

.. _`pdtcycle`:

:Cycle: `pdtevolution`_

*plan,do,test* is a **development cycle**.

*Cycle* instead of *loop* emphasizes that
*plan,do,test* needs to repeat in time.

To link the *content* nodes between *processing* units, an additional

- ``inform`` is a minimal non-technical document

Development in regular expressions is ``(inform plan do test )*`` or

#) `p'=(pdt)*`
#) `d'=(pdt)*`
#) `t'=(pdt)*`

- **i** - **inform**, initiate, inception, abstract, purpose
- **p** - **plan**, motivate, analyze, model, drive, optimize, qualify, why
- **d** - **do**, specify, describe, interface, commit
- **t** - **test**, verify, validate, inspect, review

If only one organizational unit is involved,

- the ``i`` is dropped.
  This is the case for more detailed nodes done by one developer: `(pdt)*`.

For mere information between organizational units

- the ``pdt`` is dropped

.. _`pdtmethod`:

:Method: `pdttradition`_

Development follows the content links:

- vertical links are coherent, while
- horizontally we might just have a listing of unrelated parts

It is natural to have a development,
where every cycle deals with the full vertical stack,
*unless* the vertical links are *costly*.

Change of *physical* unit is costly.
It is a change of *physical* unit, e.g.

- when something is physically executed
- when another developer or organization is involved

If switching physical unit is done just once,
the processing unit ensures success,
by simulating using its map of reality

- construct the map
- test the map
- use the map

Using the map consists of

- ``pdt`` cycles where each
- encompasses most of the vertical abstraction stack.

Traditional methods derive from the link cost.

- For software development by one or a few developers links are cheap.
  `Agile`_
  methods are preferred.

- You build a house using the `waterfall`_ method.

- For Software, if the organizational responsibilities do not reflect the content structure,
  e.g. interface design by a separate organization,
  then `waterfall`_ is better than agile.

Despite the name in `waterfall`_ each layer is stabilized separately, i.e. *horizontal* development.

.. _`pdtprocessing`:

:Processing: `pdtevolution`_

Ideally there is one developer per ``pdt`` cycle.

A developer (initial *processing* unit)
creates a topology on the content
in a `maximum cohesion`_ - `minimal coupling`_ way.

This can be mapped to further processing units (organizations or developers).
The resulting sacrifice in efficiency can be minimized,
if their interactions are

- minimal, but
- still in place to operate the *plan-do-test* cycles

The map between content nodes and processing units should
stabilize quickly and be kept stable
to reduce

  - information flow between old and new *processing* units
  - memory loss (as documentation is never perfect)
  - loss of methodical consistency
  - reorganization of communication channels

Organizational changes are more costly than content changes.

.. _`pdtuid`:

:UID: `pdtevolution`_

Easy addressability reduces repeated formulation and thus effort.

``pdt`` permeates down to the most detailed content,
which is an atomic *variable*.

Detailed content items are split into 3 separate items (``pdt``)
if there is an *m-n* relation between each two.

All content nodes have a ``UID`` to make them addressable.
Instead of repeating, one makes a link with the ``UID``
(`DRY`_).

The ``UID`` can be considered as a `DSL`_ word for the project domain.
It is like an `identifiers`_ (IDs) in a programming language.

.. _`pdtinfrastructure`:

:Infrastructure: `pdtevolution`_

New structure builds on existing longer-living infrastructure.

- Processing units need infrastructure (e.g. office, tools, communication channels, methods, pay, ...)
- Content needs infrastructure (processing units, format, repo, ...)

The content for the development

- of one system
- is in one `repo`_

Why:

- content encapsulation by `maximum cohesion`_
- organizational communication
- scope for UID

A distributed `VCS`_ is used.

Why: organizationally and technically

- more independent
- less coordination needed

The repo is accessible to all physical units linked by the system (developers, users).

Why: The Repo

- is the communication hub
- is an easily findable, single point of information on the system
- avoids construction of separate communication channels
- avoids repeated interactions on costly link,
  especially between users and developers.

.. _`pdtcontinuity`:

:Continuity: `pdtinfrastructure`_

Continuity is very important.
Every living species on earth is

- the tip of more than 3 billion years of *continuous* development
- an information channel through 3 billion years of changing environments

The end of a system does not mean the end of its parts.
What is part is just a question of perspective.
But in general,
for a system to get versatile (advanced),
one needs to keep up the continuity of development.

*Continuity* asks for a stable *infrastructure*.


Do
===

.. _`pdtrepo`:

:Repo: `pdtinfrastructure`_ `pdtencapsulation`_ `pdtcontent`_ `pdtuid`_

`git`_ is used as `VCS`_,
because it is distributed and popular.

A git branch must not contain old and new versions in parallel.
Git is for versioning.

Cooperation is done over the internet via a central git repository.
All branches are pushed to the central repo.

Github/Gitlab/Butbucket/SourceForge support **issues**.

- Issues are for feedback from the users.
- ``pdt`` documents are used for development cycles that need more planning.

*Project forking* dissipates effort.
Repo maintainers need to react timely

- on issues or
- on pull requests

to prevent *project forking*.

*Repo forking* is part of normal development.
Those without write access to the central repo,

- work on their own forks and
- contribute pull requests

The source tree tries to stay flat. Example entries:

- ``pdt``: for ``pdt`` enhancements cycle, each in an ``AAA`` subdir

- ``doc``: system documentation for API, libraries, GUI,...; tutorials

- ``c``: platform neutral code in in C or C++

- ``python``: python bindings

- ``test``: test scripts

The ``build`` tree is outside of the repo tree.

.. _`pdtdocumentation`:

:Development Documentation: `pdtcontent`_

We try to have

- all information as hyperlinked text
- documentation as python code (``.stpl``)
- support of many graphic DSLs
- convertibility to many other formats

*Documentation as code* allows to

- generate documentation from different sources
  (code, system documentation, development documentation)
- reuse or generate boilerplate text
- create graphics in line with text

``pdt`` cycle documentation:

- The repo has a top level folder for ``pdt``'s (optionally named ``pdt``)
- Every cycle gets an ``AAA`` folder below ``pdt``, e.g. ``011``.
  Usage of base36, .i.e ``0-9A-Z``, keeps the UID short.
  Depending on the project size the actual length can be less the 3.
- A normal cycle has 4 documents below ``AAA``: 

  - ``i.rest.stpl`` or ``0.rest.stpl``
  - ``p.rest.stpl`` or ``1.rest.stpl``
  - ``d.rest.stpl`` or ``2.rest.stpl``
  - ``t.rest.stpl`` or ``3.rest.stpl``

- Informational entries have only an ``i`` document (`pdttype`_).

.. note:: ipdt = 0123

   To have the files in order and since the sequence is so obvious

   - intead of ``ipdt`` one could use ``0123``

   for the file names.

Project-relevant content is in paragraphs with a
project-wide **unique** ID::

  .. _`xAAABB`:

with ``A,B`` base36 and ``x∈{i,p,d,t}``.

.. note:: rstdoc

  ``pdt`` is integrated in `rstdoc`_.
  See the sample project generated with ``rstdoc --ipdt tmpipdt``.

  A document could look like this:

  | ``.. _`i001`:``
  |
  | ``%globals().update(include('pdt.rst.tpl'``
  | ``%,Title="Development Process"``
  | ``%,Type="inform"``
  | ``%))``
  |
  | ``.. _`i001header`:``
  | ``%__i001_('header')``
  |
  | ``.. _`i001keywords`:``
  | ``%__i001('key words')``
  |
  | ``Item content.``

  In ``__i001()``, `001` is the fix AAA, and the function automatically numbers the ``BB`` part.
  There is no need to have 3 digit/letters.
  Reference to items between RST documents is done with ``|i001keywords|``.
  Reference targets are not generated to allow `rstdoc`_ to create ``.tags``
  that point to the ``.rest.stpl`` instead of the ``.rest``.

.. _`pdtinform`:

``i.rest.stpl`` contains

- ``pdt`` fields (`pdtfields`_)
- a short non-technical introduction to the context (problem, goal, purpose).

``A`` is a base36 letter (``0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ``)

.. _`pdtfields`:

pdt fields:

The necessary fields are 

- **PDT** - The ``AAA`` ``pdt`` number
- **Contact** - instead of *author*, as the authors are documented via git
- **Status** - see `pdtstatus`_
- **Type** - see `pdttype`_
- **Created** - as a hint to how old the ``pdt`` is.

.. _`pdtstatus`:

pdt status:

- **sandbox** - work in progress
- **draft** - initial state until discussed and/or implemented and tested
- **final** - consistent with the rest of the repo or agreed upon
- **replaced** - for a conflicting change a new ``pdt`` replaces a *final* one
- **deferred** - possibly because other things are prioritized
- **rejected** - after a discussion the majority decided not go that way
- **withdrawn** - the one who proposed the ``pdt`` changed his mind

.. _`pdttype`:

pdt type:

- **pdt** - Enhancement to the project
- **inform** - Informs about processes or workflows, or
  anything not having a ``pdt`` cycle

The *inform* type does not have a development phase.
There can be just one file.
After discussion it goes to *final* or another status.

.. _`pdtworkflow`:

:Workflow: `pdtprocessing`_ `pdtmethod`_

- First add an ``pdt/AAA`` directory to the ``develop`` branch,
  directly if with write access, else via pull request.
- Let peers and yourself review and change the ``pdt`` content in their local forks.
- Make pull requests until ``pdt`` status is ``final`` in the ``develop`` branch of the central repo.
- Add an ``AAA`` feature branch.
- Do development until stable.
- Merge ``develop`` into ``AAA`` regularly to stay up-to-date,
  and specifically before declaring that ``AAA`` is ready.
- When ``AAA`` is ready, the ``AAA`` branch is first merged to the ``develop`` branch.
- When ``develop`` is stable, i.e. tests pass,
  the ``develop`` branch is merged to the ``master`` branch.

Active ``pdt``'s are those where

- ``pdt/AAA`` exists in the ``develop`` branch *and*
- an ``AAA`` **git branch exist**

Done cycles have their branch deleted.
Whether merged or not, the ``pdt/AAA`` folder stays.

Non-dependent cycles can run in parallel.

.. _`pdtplan`:

:Plan: `pdtcontent`_ `pdtcycle`_

``plan`` items considers the current state:

- input from above
- experience
- examples
- simulations (separate ``pdt``'s)

``plan`` items create **alternatives** by

- abstraction (*analysis*) and
- combination (*synthesis*)
- analogy

``plan`` items motivate choice (why).

``plan`` items are testable.

Alternatives are (stepwise) reduced to 1 choice,
which is specified as ``do`` item.

::

  (why choice test)* = (plan do test)* = (pdt)*

The ultimate evolutionary *why* is to save energy,
i.e. one invests energy to save energy.

Why's:

- more useful (more global energy minimum)

- less effort, less cost, with same utility

- improve development efficiency itself

- in the middle of a context: produce consistency

These generic guidelines still keep many choices open.
Among them

- how to group ``p``, ``d`` and ``t`` items to minimize effort

- how to integrate products from other organizational units (*qualification*)

.. _`pdtdo`:

:Do: `pdtcontent`_ `pdtcycle`_

Normally for every ``do`` item there is a linked ``plan``.
``do`` items don't need a separate ``plan`` item,
if a **why**

- can be stated very shortly and
- is local to the ``do`` item

``do`` items are a commitment to do things as specified.

``do`` items only specify based on (information from) ``plan`` items.

``do`` items are as general as the constraints from the ``plan`` items allow

``do`` items are **interface** that crystalizes from the ``plan`` items

``do`` items are testable

.. _`pdttest`:

:Test: `pdtcontent`_ `pdtcycle`_

The **test** is the link back up.

- *test* items check against *plan* items
- *test* items are planned together with *plan* items
- *test* items are executed after the *do* items

Tests in lower layers are not specified.

*Verification* is a synonym of *testing*, the process of executing tests.
*Validations* of a product from another organizational unit
are the subset of tests dealing with that product.

**Test-Driven Development**:
Tests form the evolutionary environment for a solution.
One best thinks of test items when formulating *plan* items.
This way the ``do`` items already have a environment to test against.

To make the expensive **do** more likely a success,
one better tests early, in

- mind (**thinking**) or via
- via (software) **experiments**/**simulations**

As tests finalize a cycle, they are also responsible for **consistency**.
Test items link to ``plan`` and ``do`` items,
and state that their consistency has been checked.

Traceability: With separate files for ``inform``, ``plan``, ``do`` and ``test``,
the content items get marked as such.
This can be used to automatically check
that test items are linked to ``plan`` and ``do`` items.

The ultimate test is the **usefulness**,

- which leads to applications in the real world,
- which provides new test cases,
- leading to further improvements

A system is not **bug-free**, unless proven so by tests.
Due to the complexity tests will

- most likely **never** cover everything

See

- `test coverage`_

A system is still **usable** even if not bug-free.
Most applications of a system use only a limited amount of functionality.
Broad adoption increases usage coverage.

To reach a stable, i.e. usable, state, reserve at least
as much time for stabilization as for "development",
because every development step has more test steps.

With

- `test driven development`_
- `continuous integration`_

testing accompanies all development steps and can be considered part of development.


Test
====

This document is informative.
It does not need testing.
I just reused the ``inform-plan-do-test`` structuring for this document
to separate

- abstract motivation (``plan``) and
- more concrete guidelines (``do``) and
- because it fits to the topic

The test is given by the application of these guidelines.
It should produce *feedback* and adaptations in this document.

In actual applications of the ``ipdt`` scheme,
the test consists in checking that ``plan`` and ``do`` fit together.

In simple cases, i.e.
if the ``do`` does not add more detail, but has the same description as the ``plan``,
then this description

- can just have a ``todo`` flag
- that becomes a ``done`` flag
- at the ``test``

In such case ``ipdt`` files are not needed,
but the idea of ``plan-do-test`` is still there.
Such simple items can be collected under one ``pdt`` folder.

Note that *bugs* sometimes entail big changes that need planning,
and are not just *todo* items.


.. _`waterfall`: https://en.wikipedia.org/wiki/Waterfall_model
.. _`agile`: https://en.wikipedia.org/wiki/Agile_software_development
.. _`rstdoc`: https://rstdoc.readthedocs.io/en/latest/
.. _`evolutionary`: `evolution`_
.. _`is energy`: `evolution`_
.. _`evolution`: https://rolandpuntaier.blogspot.com/2019/01/evolution.html
.. _`Information`: http://rolandpuntaier.blogspot.com/2015/03/what-is-information.html
.. _`lattices`: http://rolandpuntaier.blogspot.com/2015/06/fca.html
.. _`maximum cohesion`: `cohesion`_
.. _`cohesion`: https://en.wikipedia.org/wiki/Cohesion_(computer_science)
.. _`minimal coupling`: https://en.wikipedia.org/wiki/Coupling_(computer_programming)
.. _`DRY`: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
.. _`DSL`: https://en.wikipedia.org/wiki/Domain-specific_language
.. _`identifiers`: https://en.wikipedia.org/wiki/Identifier_(computer_languages)
.. _`repo`: https://en.wikipedia.org/wiki/Repository_(version_control)
.. _`VCS`: https://en.wikipedia.org/wiki/Comparison_of_version-control_software
.. _`git`: https://en.wikipedia.org/wiki/Git
.. _`test coverage`: https://en.wikipedia.org/wiki/Code_coverage
.. _`test driven development`: https://en.wikipedia.org/wiki/Test-driven_development
.. _`continuous integration`: https://en.wikipedia.org/wiki/Continuous_integration
