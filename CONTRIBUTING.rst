Contributing to EddyMotionCorrection
====================================

Welcome to the EddyMotionCorrection repository! We’re excited you’re
here and want to contribute.

**Imposter’s syndrome disclaimer**\  [1]_: We want your help. No,
really.

There may be a little voice inside your head that is telling you that
you’re not ready to be an open-source contributor; that your skills
aren’t nearly good enough to contribute. What could you possibly offer a
project like this one?

We assure you - the little voice in your head is wrong. If you can write
code at all, you can contribute code to open-source. Contributing to
open-source projects is a fantastic way to advance one’s coding skills.
Writing perfect code isn’t the measure of a good developer (that would
disqualify all of us!); it’s trying to create something, making
mistakes, and learning from those mistakes. That’s how we all improve,
and we are happy to help others learn.

Being an open-source contributor doesn’t just mean writing code, either.
You can help out by writing documentation, tests, or even giving
feedback about the project (and yes - that includes giving feedback
about the contribution process). Some of these contributions may be the
most valuable to the project as a whole, because you’re coming to the
project with fresh eyes, so you can see the errors and assumptions that
seasoned contributors have glossed over.

Driving principles
------------------

*EddyMotionCorrection* is very much influenced and envisioned as a
translation of `fMRIPrep <http://fmriprep.org>`__ to diffusion MRI data.
That means *EddyMotionCorrection* shares with *fMRIPrep* (and more
generally, other *NIPreps* [NeuroImaging Preprocessing pipelines]) the
fundamental design principles:

1. The tool only and fully supports BIDS and BIDS-Derivatives for the
   input and output data.
2. The tool is packaged as a fully-compliant
   `BIDS-App <https://bids-apps.neuroimaging.io>`__, not just in its
   user interface, but also in the continuous integration, testing and
   delivery.
3. The tool is rigorously restricted to diffusion MRI preprocessing
   tasks, including (but not limited to): input/output metadata
   assessment, head-motion correction, eddy-currents-derived artifact
   correction, susceptibility-distortion correction, denoising, B1-bias
   field correction, session-drift correction, co-registration with
   anatomical data, spatial normalization to neuroimaging templates,
   gradient non-linearity correction, Gibbs unringing, etc. In other
   words, the tool does not deal with modeling, tractography or
   connectivity extraction.
4. The tool is **agnostic to subsequent analysis**, i.e., any software
   supporting BIDS-Derivatives for its inputs should be amenable perform
   tractography and to analyze data preprocessed with the tool.
5. The tool is thoroughly and transparently documented (including the
   generation of individual reports that can be used as scaffolds for
   understanding the underpinnings and design decisions of the tool).
6. The tool is community-driven, with a very open concept of
   contribution that is always credited with authorship offers when
   writing relevant papers.

Practical guide to submitting your contribution
-----------------------------------------------

These guidelines are designed to make it as easy as possible to get
involved. If you have any questions that aren’t discussed below, please
let us know by opening an
`issue <https://github.com/nipreps/EddyMotionCorrection/issues>`__!

Before you start, you’ll need to set up a free
`GitHub <https://github.com/>`__ account and sign in. Here are some
`instructions <https://help.github.com/articles/signing-up-for-a-new-github-account>`__.

Already know what you’re looking for in this guide? Jump to the
following sections:

-  `Joining the conversation <#joining-the-conversation>`__
-  `Contributing through Github <#contributing-through-github>`__
-  `Understanding issues <#understanding-issues>`__
-  `Making a change <#making-a-change>`__
-  `Structuring
   contributions <#EddyMotionCorrection-coding-style-guide>`__
-  `Licensing <#licensing>`__
-  `Recognizing contributors <#recognizing-contributions>`__

Joining the conversation
------------------------

*EddyMotionCorrection* is maintained by a growing group of enthusiastic
developers— and we’re excited to have you join! Most of our discussions
will take place on open
`issues <https://github.com/nipreps/EddyMotionCorrection/issues>`__.

We also encourage users to report any difficulties they encounter on
`NeuroStars <https://neurostars.org/tags/EddyMotionCorrection>`__, a
community platform for discussing neuroimaging.

We actively monitor both spaces and look forward to hearing from you in
either venue!

Contributing through GitHub
---------------------------

`git <https://git-scm.com/>`__ is a really useful tool for version
control. `GitHub <https://github.com/>`__ sits on top of git and
supports collaborative and distributed working.

If you’re not yet familiar with ``git``, there are lots of great
resources to help you *git* started! Some of our favorites include the
`git Handbook <https://guides.github.com/introduction/git-handbook/>`__
and the `Software Carpentry introduction to
git <http://swcarpentry.github.io/git-novice/>`__.

On GitHub, You’ll use
`Markdown <https://daringfireball.net/projects/markdown>`__ to chat in
issues and pull requests. You can think of Markdown as a few little
symbols around your text that will allow GitHub to render the text with
a little bit of formatting. For example, you could write words as bold
(``**bold**``), or in italics (``*italics*``), or as a
`link <https://www.youtube.com/watch?v=dQw4w9WgXcQ>`__
(``[link](https://youtu.be/dQw4w9WgXcQ)``) to another webpage.

GitHub has a really helpful page for getting started with `writing and
formatting Markdown on
GitHub <https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github>`__.

Understanding issues
--------------------

Every project on GitHub uses
`issues <https://github.com/nipreps/EddyMotionCorrection/issues>`__
slightly differently.

The following outlines how the *EddyMotionCorrection* developers think
about these tools.

-  **Issues** are individual pieces of work that need to be completed to
   move the project forward. A general guideline: if you find yourself
   tempted to write a great big issue that is difficult to be described
   as one unit of work, please consider splitting it into two or more
   issues.

   Issues are assigned `labels <#issue-labels>`__ which explain how they
   relate to the overall project’s goals and immediate next steps.

Issue Labels
~~~~~~~~~~~~

The current list of issue labels are
`here <https://github.com/nipreps/EddyMotionCorrection/labels>`__ and
include:

-  |Good first issue| *These issues contain a task that is amenable to
   new contributors because it doesn’t entail a steep learning curve.*

   If you feel that you can contribute to one of these issues, we
   especially encourage you to do so!

-  |Bug| *These issues point to problems in the project.*

   If you find new a bug, please give as much detail as possible in your
   issue, including steps to recreate the error. If you experience the
   same bug as one already listed, please add any additional information
   that you have as a comment.

-  |Enhancement| *These issues are asking for new features and
   improvements to be considered by the project.*

   Please try to make sure that your requested feature is distinct from
   any others that have already been requested or implemented. If you
   find one that’s similar but there are subtle differences, please
   reference the other request in your issue.

In order to define priorities and directions in the development roadmap,
we have two sets of special labels:

+-----------------------------------+------------------------------------------------------------------------------------------+
| Label                             | Description                                                                              |
+===================================+==========================================================================================+
| | |GitHub labels - impact: high|  | Estimation of the downstream impact the proposed feature/bugfix will have.               |
| | |GitHub labels - impact: medium||                                                                                          |
| | |GitHub labels - impact: low|   |                                                                                          |
+-----------------------------------+------------------------------------------------------------------------------------------+
| | |GitHub labels - effort: high|  | Estimation of effort required to implement the requested feature or fix the reported bug.|
| | |GitHub labels - effort: medium||                                                                                          |
| | |GitHub labels - effort: low|   |                                                                                          |
+-----------------------------------+------------------------------------------------------------------------------------------+

These labels help triage and set priorities to the development tasks.
For instance, one bug regression that has been reported to affect most
of the users after a release with an easy fix because it is a known old
problem that came back. Such an issue will typically be assigned the
following labels |GitHub labels - bug| |GitHub labels - impact: high| |GitHub labels - effort: low|, and
its priority will be maximal since addressing low-effort high-impact
deliver the maximum turnout without increasing the churn by much.

Of course, the implementation of long-term goaled lines may include the
scheduling of |GitHub labels - impact: medium| |GitHub labels - effort: high|. Finally, |GitHub labels - impact: low|
|GitHub labels - effort: high| issues are less likely to be addressed.

Making a change
---------------

We appreciate all contributions to *EddyMotionCorrection*, but those
accepted fastest will follow a workflow similar to the following:

1. | **Comment on an existing issue or open a new issue referencing your
     addition.**\  This allows other members of the *EddyMotionCorrection*
     development team to confirm that you aren’t overlapping with work
     that’s currently underway and that everyone is on the same page with
     the goal of the work you’re going to carry out. 
   | `This blog <https://www.igvita.com/2011/12/19/dont-push-your-pull-requests/>`__
     is a nice explanation of why putting this work in up front is so
     useful to everyone involved.

2. | `Fork <https://help.github.com/articles/fork-a-repo/>`__\  **the** \ `EddyMotionCorrection
     repository <https://github.com/nipreps/EddyMotionCorrection>`__\  **to
     your profile.**\  
   | This is now your own unique copy of *EddyMotionCorrection*. Changes here won’t effect anyone else’s work,
     so it’s a safe space to explore edits to the code!

3. | `Clone <https://help.github.com/articles/cloning-a-repository>`__\  **your
     forked EddyMotionCorrection repository to your machine/computer.**\  
   | While you can edit files `directly on github <https://help.github.com/articles/editing-files-in-your-repository>`__,
     sometimes the changes you want to make will be complex and you will
     want to use a `text editor <https://en.wikipedia.org/wiki/Text_editor>`__ that you have
     installed on your local machine/computer. (One great text editor is
     `vscode <https://code.visualstudio.com/>`__).
   |
   | In order to work on the code locally, you must clone your forked
     repository.
   |
   | To keep up with changes in the EddyMotionCorrection repository, add
     the `“upstream” EddyMotionCorrection repository as a
     remote <https://help.github.com/articles/configuring-a-remote-for-a-fork>`__
     to your locally cloned repository.
   |

   .. code-block:: bash

      git remote add upstream https://github.com/nipreps/EddyMotionCorrection.git
      
   | Make sure to `keep your fork up to
     date <https://help.github.com/articles/syncing-a-fork/>`__ with the
     upstream repository.
   |
   | For example, to update your master branch on your local cloned
     repository:
   |  

   .. code-block:: bash
      
      git fetch upstream git
      checkout master
      git merge upstream/master

4. **Create a**\ `new
   branch <https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/>`__\ **to
   develop and maintain the proposed code changes.**\  For example:
   ``Shell     git fetch upstream  # Always start with an updated upstream     git checkout -b fix/bug-1222 upstream/master``
   Please consider using appropriate branch names as those listed below,
   and mind that some of them are special (e.g., ``doc/`` and
   ``docs/``):

   -  ``fix/<some-identifier>``: for bugfixes
   -  ``enh/<feature-name>``: for new features
   -  ``doc/<some-identifier>``: for documentation improvements. You
      should name all your documentation branches with the prefix
      ``doc/`` or ``docs/`` as that will preempt triggering the full
      battery of continuous integration tests.

5. **Make the changes you’ve discussed, following
   the**\ `EddyMotionCorrection coding style
   guide <#EddyMotionCorrection-coding-style-guide>`__\ **.**\  Try to
   keep the changes focused: it is generally easy to review changes that
   address one feature or bug at a time. It can also be helpful to test
   your changes locally, using a `EddyMotionCorrection development
   environment <https://EddyMotionCorrection.readthedocs.io/en/latest/contributors.html>`__.
   Once you are satisfied with your local changes, `add/commit/push
   them <https://help.github.com/articles/adding-a-file-to-a-repository-using-the-command-line>`__
   to the branch on your forked repository.

6. **Submit a**\ `pull
   request <https://help.github.com/articles/creating-a-pull-request-from-a-fork>`__\ **.**\ 
   A member of the development team will review your changes to confirm
   that they can be merged into the main code base. Pull request titles
   should begin with a descriptive prefix (for example,
   ``ENH: Adding Gibbs unringing step``):

   -  ``ENH``: enhancements or new features
      (`example <https://github.com/poldracklab/fmriprep/pull/1508>`__)
   -  ``FIX``: bug fixes
      (`example <https://github.com/poldracklab/fmriprep/pull/1378>`__)
   -  ``TST``: new or updated tests
      (`example <https://github.com/poldracklab/fmriprep/pull/1098>`__)
   -  ``DOC``: new or updated documentation
      (`example <https://github.com/poldracklab/fmriprep/pull/1515>`__)
   -  ``STY``: style changes
      (`example <https://github.com/poldracklab/fmriprep/pull/675>`__)
   -  ``REF``: refactoring existing code
      (`example <https://github.com/poldracklab/fmriprep/pull/816>`__)
   -  ``CI``: updates to continous integration infrastructure
      (`example <https://github.com/poldracklab/fmriprep/pull/1048>`__)
   -  ``MAINT``: general maintenance
      (`example <https://github.com/poldracklab/fmriprep/pull/1239>`__)
   -  For works-in-progress, add the ``WIP`` tag in addition to the
      descriptive prefix. Pull-requests tagged with ``WIP:`` will not be
      merged until the tag is removed.

7. **Have your PR reviewed by the development team, and update your
   changes accordingly in your branch.**\  The reviewers will take
   special care in assisting you to address their comments, as well as
   dealing with conflicts and other tricky situations that could emerge
   from distributed development. And if you don’t make the requested
   changes, we might ask
   [@bedevere-bot](https://github.com/search?q=commenter%3Abedevere-bot+soft+cushions)
   to `poke you with soft
   cushions! <https://youtu.be/XnS49c9KZw8?t=1m7s>`__

EddyMotionCorrection coding style guide
---------------------------------------

Whenever possible, instances of Nipype ``Node``\ s and ``Workflow``\ s
should use the same names as the variables they are assigned to. This
makes it easier to relate the content of the working directory to the
code that generated it when debugging.

Workflow variables should end in ``_wf`` to indicate that they refer to
Workflows and not Nodes. For instance, a workflow whose base-name is
``myworkflow`` might be defined as follows:

.. code:: python

   from nipype.pipeline import engine as pe

   myworkflow_wf = pe.Workflow(name='myworkflow_wf')

If a workflow is generated by a function, the name of the function
should take the form ``init_<basename>_wf``:

.. code:: python

   def init_myworkflow_wf(name='myworkflow_wf):
       workflow = pe.Workflow(name=name)
       ...
       return workflow

   myworkflow_wf = init_workflow_wf(name='myworkflow_wf')

If multiple instances of the same workflow might be instantiated in the
same namespace, the workflow names and variables should include either a
numeric identifier or a one-word description, such as:

.. code:: python

   myworkflow0_wf = init_workflow_wf(name='myworkflow0_wf')
   myworkflow1_wf = init_workflow_wf(name='myworkflow1_wf')

   # or

   myworkflow_lh_wf = init_workflow_wf(name='myworkflow_lh_wf')
   myworkflow_rh_wf = init_workflow_wf(name='myworkflow_rh_wf')

Licensing
---------

*EddyMotionCorrection* is licensed under the Apache 2.0 license. By
contributing to *EddyMotionCorrection*, you acknowledge that any
contributions will be licensed under the same terms.

Recognizing contributions
-------------------------

We welcome and recognize all contributions from documentation to testing
to code development. You can see a list of current contributors in our
`zenodo
file <https://github.com/nipreps/EddyMotionCorrection/blob/master/.zenodo.json>`__.
If you are new to the project, don’t forget to add your name and
affiliation to the list of contributors there! Before every release, the
`zenodo
file <https://github.com/nipreps/EddyMotionCorrection/blob/master/.zenodo.json>`__
will be checked for new contributors, who will be invited again to add
their names to the file (just in case they missed the automated message
from our Welcome Bot). The `update
script <https://github.com/nipreps/EddyMotionCorrection/blob/master/.maintenance/update_zenodo.py>`__
will also sort creators and contributors by the relative size of their
contributions, as provided by the ``git-line-summary`` utility
distributed with the ``git-extras`` package. Last positions in both the
*creators* and *contributors* list will be reserved to the project
leaders. These special positions can be revised to add names by punctual
request and revised for removal and update of ordering in an scheduled
manner every two years. All the authors enlisted as *creators*
participate in the revision of modifications.

Creators
~~~~~~~~

Creators are contributors who *drive the project*. Examples of steering
activities that *drive the project* are: actively participating in the
follow-up meetings, helping in the design of the tool and definition of
the roadmap, providing resources (in the broad sense, including
funding), code-review, etc.

Contributors
~~~~~~~~~~~~

Contributors helped the project in any sense: writing code, writing
documentation, benchmarking modules of the tool, proposing new features,
helping improve the scientific rigor of implementations, giving out
support on the different communication channels
(`mattermost <https://mattermost.brainhack.org/brainhack/channels/EddyMotionCorrection>`__,
`NeuroStars <https://neurostars.org/tags/EddyMotionCorrection>`__,
`GitHub
issues <https://github.com/nipreps/EddyMotionCorrection/issues>`__,
etc.).

Publications
~~~~~~~~~~~~

Anyone listed as a *creator* or a *contributor* in the `zenodo
file <https://github.com/nipreps/EddyMotionCorrection/blob/master/.zenodo.json>`__
can start the submission process of a manuscript as first author. To
compose the author list, all the *creators* MUST be included (except for
those people who opt to drop-out) and all the *contributors* MUST be
invited to participate. First authorship(s) is (are) reserved for the
authors that originated and kept the initiative of submission and wrote
the manuscript. The ordering of the rest of the authors follows the
ordering criteria of the `zenodo
file <https://github.com/nipreps/EddyMotionCorrection/blob/master/.zenodo.json>`__,
with the difference that all the authors are pulled together in a unique
list (i.e., *creators* and *contributors* are treated equivalently).
*EddyMotionCorrection* and its community adheres to open science
principles, such that a pre-print should be posted on an adequate
archive service (e.g., `ArXiv <https://arxiv.org>`__ or
`BioRxiv <https://biorxiv.org>`__) prior publication.

Thank you!
----------

You’re awesome. :wave::smiley:

*— Based on contributing guidelines from
the*\ `STEMMRoleModels <https://github.com/KirstieJane/STEMMRoleModels>`__\ *project.*

.. [1]
   The imposter syndrome disclaimer was originally written by `Adrienne
   Lowe <https://github.com/adriennefriend>`__ for a `PyCon
   talk <https://www.youtube.com/watch?v=6Uj746j9Heo>`__, and was
   adapted based on its use in the README file for the `MetPy
   project <https://github.com/Unidata/MetPy>`__.

.. |Good first issue| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/good%20first%20issue
   :target: https://github.com/nipreps/EddyMotionCorrection/labels/good%20first%20issue
.. |Bug| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/bug
   :target: https://github.com/nipreps/EddyMotionCorrection/labels/bug
.. |Enhancement| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/enhancement
   :target: https://github.com/nipreps/EddyMotionCorrection/labels/enhancement
.. |GitHub labels - impact: high| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/impact%3A%20high
.. |GitHub labels - impact: medium| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/impact%3A%20medium
.. |GitHub labels - impact: low| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/impact%3A%20low
.. |GitHub labels - effort: high| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/effort%3A%20high
.. |GitHub labels - effort: medium| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/effort%3A%20medium
.. |GitHub labels - effort: low| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/effort%3A%20low
.. |GitHub labels - bug| image:: https://img.shields.io/github/labels/nipreps/EddyMotionCorrection/bug