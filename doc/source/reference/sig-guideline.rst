=======================================================
Guidelines for OpenStack SIGs (Special Interest Groups)
=======================================================

Before we dive into more details, it is important to learn what a SIG is and
what the differences are to any other group. Please check
`Comparison of Official Group Structures`_ for more detail.

OpenStack SIGs (Special Interest Groups) are teams within the community where
we collaborate to bring unified discussions for all community members who
share a common interest. As examples, SIGs can be but are not limited to being
a first stage in the development of new projects, feature requests, standards
adoption, policy implementation, adjacent community work, and just general
discussion(s).

General governance of all SIGs are managed by Meta SIG. You can find Meta SIG
chairs in  `SIGs`_ or send mail in `OpenStack-discuss mailing-list`_ with
[meta-sig] tag on.

Finding a SIG
=============

There are now multiple SIGs formed. check all `SIGs`_  to find if any SIG
related to you.

Creating SIG
============

The one must-do thing for forming a SIG is to register the SIG under
`SIG Governance`_. And the rest are optional, you can consider any of them if
applied.

Before creating a SIG
---------------------

All actions here are optional, you can consider any actions if they applied.

Gathering opinions
~~~~~~~~~~~~~~~~~~

It's always nice to get more feedback, more hands, and attention at first step.

Name of SIG
~~~~~~~~~~~

Name can be a combination of ASCII letters, `-` and space.

.. note::
   The name of a SIG can be changed after it's created, For example, a SIG
   might consider changing its name when trying to target a wider range of
   goals.

Meaning of this SIG
~~~~~~~~~~~~~~~~~~~

Documenting down the very reason for this SIG will help others who have similar
interests to join this group. It's important to learn why we need to form a
SIG, where we need this SIG, and what's the goal and responsibility of this
SIG. Once a SIG is created, it's alway needed to review the SIG and check what
people in the group should be doing next. And review leads to plans, plan to
lead to actions, and the accomplishment of every action will bring SIG closer
to its mission. And like the name of SIG, the mission of SIG might also change
through time. It's essential to update the information around if you plan to
change the mission or name of SIG. Make sure all members aware of the process
and result so they might be able to join the discussion.

Select SIG chairs
~~~~~~~~~~~~~~~~~

Every SIG can appoint multiple SIG chairs, and it's encouraged to have more
than one chair so SIG can have a more flexible schedule.
A chair is encouraged as a moderator for the following works:

* Organize meeting agenda and host meetings
* Organize polling
* Coordinate with SIG members to generate a schedule for possible upcoming
  events (Summit, PTG, etc.) if needed.
* Moderate SIG tasks and help to find and encourage action takers for each
  task.
* Welcome new members to join the SIG.

.. note::
   It might not be a specific chair's responsibility to make sure the `how
   to join this SIG` guideline is completed, but chairs are encouraged to
   assist new members to join the SIG. The moderator role is not
   limited to chairs. Chairs can delegate to any trustworthy SIG members.

Set up SIG communications
-------------------------

`Set up SIG communications`_ will definitely help to have a place for all
members to join, share, and trigger discussions. Here are some general ways:

Mailing List
~~~~~~~~~~~~

Asynchronous communication between SIG members happens on the
`OpenStack-discuss mailing-list`_, prefixing the subject with[$signame-sig]
where$signame matches the SIG’s name. SIG work output can, of course, be posted
to other mailing-lists as needed to reach other groups.

IRC
~~~

IRC is the preferred method of communication as it aligns with historical and
current OpenStack community best practices for simple messaging, and is also
required for TC governed projects. It is understood that for some IRC does
not come with enough features by default and programming a bot to offer
additional features is beyond some; skill or patience to create/maintain. If
a SIG does decide to use an alternative to IRC, we ask that in keeping with
the Four Opens, in particular Open Community, that you do so by ensuring
meeting logs are stored/archived.

Slack
~~~~~

Free team accounts with Slack are not sufficient enough to meet
archiving/storage of logs alone. A great alternative is to connect
Slack with IRC and then follow the instructions for logging an IRC
channel. Check detail for `Slack+IRC connector`_. And
`docker image for Slack+IRC connector`_ is also available.


Due to SIG differences, each SIG might have its own way to communicate. It will
be nice if SIG can put detail information (like specific channel links and
guidelines for how to join) on document so anyone who plans to join the SIG
might know.


Process to create a SIG
-----------------------

This part introduces how to set up a SIG, and provides examples for reference.

.. note::
   This guideline will reuse part of `project creator guideline`_ so we don't
   need to rewrite everything again.

Register SIG
~~~~~~~~~~~~

First and the only must-do step, register this SIG to `SIG Governance`_.

You need to sign up SIG, SIG chairs and general link for more detail
information of this SIG in openstack/governance-sig for formal approval.
Here's an `example for register a SIG`_.

.. note::
     You might need to check if the information on SIG is still up to date.

.. note::
   All actions after the first step are optional, you can consider any actions
   if they applied.

IRC setup
~~~~~~~~~

If you're transforming from another structure (like a Working Group or Project
team) to SIG, you may keep using existing IRC channel. And if you plan to
create a new IRC channel, please reference for `IRC guideline`_.
If you're creating a new IRC channel, name rule of the channel should be
`openstack-${SIG_NAME}`. For example, the IRC channel for auto-scaling SIG
is `#openstack-auto-scaling`.
Here's an `example for adding status/meeting bot to channel`_.

.. note::
   Make sure you read through IRC guidelines before you start to create a new
   channel.

Meeting setup
~~~~~~~~~~~~~

You should consider to set up meeting schedule for SIG. SIG members can
decide the meeting schedule (frequency and location) and make sure there
will be moderator for each meeting. Here's an
`example for adding meeting schedule`_ to `meeting list`_. And
`example for adding meetbot to IRC channel`_.

.. note::
   Meeting location can be at SIG's IRC channel or other public places if
   more desired (Like K8s SIG uses Slack channel in K8s community for
   meeting). Make sure meeting location allows public access so everyone can
   join.

Repository
~~~~~~~~~~

SIG can have its own repository, however, under any circumstances, SIG can't
release a deliverable service by itself. If a SIG needs to release any
services, it should be maintained under any specific projects instead. You can
find some detail about this in `Comparison of Official Group Structures`_.
There's also a `guideline for project repository`_ for your reference.
The most different place is you should register repository under
`sigs-repos.yaml`_ for SIG instead. You also need to
`add Gerrit permission`_ and `ask Infra team to create core team`_ for
Gerrit. Here's an `example for register a repository under SIG`_ and
`example for setup config for repository`_.

Create StoryBoard
~~~~~~~~~~~~~~~~~

It's recommended to create StoryBoard to track tasks in SIG. Adding
`use_storyboard: true`  in `gerrit/projects.yaml`_ to automatically generate
a project in StoryBoard. It's allowed to track tasks for SIG in its own
way if another system seems to be a more reasonable place. But always consider
the situation when you got tasks from multiple projects to track. An
`example for add config in gerrit/projects`_ and generate
`their own storyboard`_.

Setup Zuul jobs
~~~~~~~~~~~~~~~

Setup Zuul jobs for SIG is not that much different than a project, please
reference `zuul guideline`_ for more detail.
One of most common job for SIGs is documentation test job. An example for how
you can `add your own documentation test job`_
(and a `following update for documentation job`_).

Initial document structure
~~~~~~~~~~~~~~~~~~~~~~~~~~

One of the most common functionalities of SIG is to provide documentation. Here
are a few things you can consider to document down:

* Use cases (user stories)

* what's xxx-SIG guideline: What's this SIG doing, what's the scope, goals,
  and SIG mission.

* How to join this SIG

  General information is always nice for a new member of SIG. Which might
  include:

  * Links to all resources for this SIG which may include StoryBoard,
    documents, repository, Gerrit, Communication channel information (like
    IRC, Slack, etc.).

  * How to contribute

  * Help needed list for SIG, or what's cycle goal for SIG.

* Concept guideline: Concept guideline for this special interest to
  explain when we need it, which services are considered a part of this, and
  what basic consideration should take place. An
  `example for concept guideline`_ for auto-scaling SIG.

* Specific guidelines, or white papers

Here's an example for `how to set up the Initial Sphinx structure`_ and
`its Zuul job`_.

.. note::
   For Initial documentation, it's hard to complete all documentation (to
   perfect stage) at once. We need to at least provide well `How to join
   this SIG` and `what's xxx-SIG guideline` so new join members always
   feel welcome.

Running a SIG
=============

We generally didn't provide much limits to SIGs because each SIG might need
totally different tools, and styles to achieve their mission. Here we try to
provide some guidelines for tasks you might find fit for your SIG.

Active meeting and channel
--------------------------

To have regular meetings and have people answering on channel helps people
to find this SIG. Share new update information in the channel also help SIG
members to get a better understanding of current status for tasks in SIG.

Expose SIG
----------

Special interest group (SIG) usually needs all hands from developers,
operators, and users. And in order to get attention, valid feedbacks, good
ideas, and action takers, get more attention on tasks that SIG is focused on
is always a good option.

Summit+PTG
----------

We encourage every SIG to join Summit and PTG if that's available option. You
can consider to have:

* PTG rooms for all technical discussion needs for SIG

* Feedback Forum session for all general feedbacks from community

* Next step or cycle plan discussion. Which might be a forum or PTG discussion.

* SIG Update. which might be better fit as a Summit session or a PTG topic
  (since people expect Forum to have discussions and action output from Forum,
  a general SIG update might not be a well fit).

* Answering call for presentation for each Summit is also encouraged.
  Here are some options for consideration:

  * Hands-on workshop for use case

  * General user story of this special interest

  * Community track sessions to share SIG builds experiences.

Template
--------

Provide and consistently update templates. SIG can consider generating
templates based on its interest (like feature request, bug report, use case
sharing, etc), so contributors don't need to rewrite everything on their own.
An `example for self-healing SIG provides a use case template`_.

Manage StoryBoard
-----------------

If SIG uses StoryBoard for tracking cross-project tasks or SIG tasks. Like
maintaining a project, SIG tasks should be consistently updated. Also,
(ideally) every SIG action should have its own tasks in StoryBoard so it will
be easier to track actions. SIG can also consider providing its own StoryBoard
for users to provide related bug reports or feature requests. This is useful
because we can have a single point to discuss, and create subtasks to track bug
fixes or feature implementation cross-project.

Gate jobs
---------

If SIG generates Zuul jobs by its own (like a cross-project gate job) or use
exists one (like documentation gate job), it's important to make sure the gate
job is up to date and stays green (unbroken). Also if you building a
cross-project job, consistently check the health and performance of that job is
important because cross-project functionality usually more complex to use.
And you don't want to slow down any projects because of the high failure rate
of a specific cross-project gate job. For example, it's possible to consider
building a cross-project gate job for self-healing use cases uses Mistral,
Vitrage, and Monasca. That means this job might be adopted in Mistral, Vitrage,
and Monasca. Any increase failure rate of that job will reflect upon all three
projects.

Health check
------------

It's encouraged to consistently provide health check of a SIG to make sure
everything is on track, good progress for each SIG task, and all current
resources are up to date. It's always friendly to announce chances (like
chances of meeting schedule, or documentation link) through any SIG channels.
Health check results can be sent out through ML so others might get more
up-to-date information.

Tag your SIG
------------
SIG can be tagged with different status and let people understand the SIG's
purpose and current state.
You can find all available status tag under
:doc:`SIG status </reference/sig-status>`.

SIG newsletter
--------------

It's encouraged to provide updates for all who might be interested in
learning. Through a mailing list, instant messaging channels, or anywhere
you think that helps. The reasons for doing so are both to attract new
members to join, and to make sure others know about the new changes. For
example, once your SIG creates nice documents that you believe will help
others, you can send a mailing list for it, and also mention it in IRC/Slack.

.. _Comparison of Official Group Structures: https://governance.openstack.org/tc/reference/comparison-of-official-group-structures.html
.. _SIGs: https://governance.openstack.org/sigs/
.. _SIG Governance: https://opendev.org/openstack/governance-sigs/src/branch/master/sigs.yaml
.. _Set up SIG communications: https://governance.openstack.org/sigs/#sig-communications
.. _OpenStack-discuss mailing-list: http://lists.openstack.org/cgi-bin/mailman/listinfo/openstack-discuss
.. _project creator guideline: https://docs.openstack.org/infra/manual/creators.html
.. _example for register a SIG: https://review.opendev.org/#/c/632252/
.. _IRC guideline: https://docs.openstack.org/infra/system-config/irc.html
.. _example for adding status/meeting bot to channel: https://review.opendev.org/#/c/656796
.. _example for adding meeting schedule: https://review.opendev.org/#/c/656810/
.. _meeting list: http://eavesdrop.openstack.org/
.. _example for adding meetbot to IRC channel: https://review.opendev.org/#/c/656796/1/hiera/common.yaml
.. _guideline for project repository: https://docs.openstack.org/infra/manual/creators.html#add-new-repository-to-the-governance-repository
.. _sigs-repos.yaml: https://opendev.org/openstack/governance/src/branch/master/reference/sigs-repos.yaml
.. _example for register a repository under SIG: https://review.opendev.org/#/c/637126
.. _example for setup config for repository: https://review.opendev.org/#/c/637125/
.. _add Gerrit permission: https://docs.openstack.org/infra/manual/creators.html#add-gerrit-permissions
.. _ask Infra team to create core team: https://docs.openstack.org/infra/manual/creators.html#update-the-gerrit-group-members
.. _gerrit/projects.yaml: https://github.com/openstack/project-config/blob/master/gerrit/projects.yaml
.. _example for add config in gerrit/projects: https://review.opendev.org/#/c/637125/7/gerrit/projects.yaml
.. _their own storyboard: https://storyboard.openstack.org/#!/project/openstack/auto-scaling-sig
.. _zuul guideline: https://docs.openstack.org/infra/manual/creators.html#add-project-to-zuul
.. _example for concept guideline: https://docs.openstack.org/auto-scaling-sig/latest/theory-of-auto-scaling.html
.. _how to set up the Initial Sphinx structure: https://review.opendev.org/#/c/656423/
.. _its Zuul job: https://review.opendev.org/#/c/659955
.. _example for self-healing SIG provides a use case template: https://opendev.org/openstack/self-healing-sig/src/branch/master/use-cases/template.rst
.. _Slack+IRC connector: https://github.com/ekmartin/slack-irc
.. _docker image for Slack+IRC connector: https://github.com/mrhillsman/dockerize-slack-irc.
.. _add your own documentation test job: https://review.opendev.org/#/c/656423/
.. _following update for documentation job: https://review.opendev.org/#/c/659955/
