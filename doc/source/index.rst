================
 OpenStack SIGs
================

The OpenStack SIGs (Special Interest Groups) are a form of
working group in OpenStack that is an emanation of the community
as a whole and is not directly tied to a specific governance body.

SIGs are a good match for an activity that centers around a topic
or practice that spans all the community (developers, operators,
end users...), by forming a guild of people with a shared interest.

.. sigtable::
      :datafile: ../../sigs.yaml

SIG communications
==================

Email
~~~~~

Asynchronous communication between SIG members happens on the
`openstack-discuss mailing-list`_, prefixing the subject with
``[$signame-sig]`` where ``$signame`` matches the SIG's name. SIG work
output can of course be posted to other mailing-lists as needed to
reach other groups.

Instant Messaging
~~~~~~~~~~~~~~~~~

IRC is the preferred method of communication as it aligns with
historical and `current OpenStack community best practices for simple
messaging <https://governance.openstack.org/tc/reference/irc.html>`_,
and is also `required for TC governed projects
<https://governance.openstack.org/tc/reference/new-projects-requirements.html>`_.

It is understood that for some IRC does not come with enough features by
default and programming a bot to offer additional features is beyond
some; skill or patience to create/maintain. If a SIG does decide to use
an alternative to IRC, we ask that in keeping with `the Four Opens
<https://governance.openstack.org/tc/reference/opens.html>`_, in
particular Open Community, that you do so by `ensuring meeting logs are
stored/archived
<https://docs.openstack.org/infra/system-config/irc.html#logging>`_.

Slack
-----

Free team accounts with Slack are not sufficient enough to meet
archiving/storage of logs alone. A great alternative is to connect
Slack with IRC and then follow the instructions for logging an IRC
channel. Refer to https://github.com/ekmartin/slack-irc for a
Slack+IRC connector; a docker image is also available at
https://github.com/mrhillsman/dockerize-slack-irc.

Process to create a SIG
=======================

To propose creation of a SIG, please propose a change to the
``sigs.yaml`` file in the ``openstack/governance-sigs`` repository.
That change will be reviewed by members of the Meta SIG. If you have
questions, please ask them on the `openstack-discuss mailing-list`_
with subject prefix ``[meta-sig]``.

.. _`openstack-discuss mailing-list`: http://lists.openstack.org/cgi-bin/mailman/listinfo/openstack-discuss

.. toctree::
   :maxdepth: 1

   reference/sig-status
