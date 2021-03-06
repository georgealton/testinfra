.. _modules:

Modules
=======

Testinfra modules are provided as `pytest fixtures`_, declare them as
arguments of your test function to make them available::

    def test_foo(Package, File, Command):
        [...]


Note that you can also :ref:`make modules`.

Command
~~~~~~~

.. autoclass:: testinfra.modules.Command(command, *args)
   :members: check_output, run_expect, run_test


LocalCommand
~~~~~~~~~~~~


.. autofunction:: testinfra.plugin.LocalCommand(command, *args)


TestinfraBackend
~~~~~~~~~~~~~~~~

.. autoclass:: testinfra.backend.base.BaseBackend()
   :members:


File
~~~~

.. autoclass:: testinfra.modules.File
   :members:
   :undoc-members:
   :exclude-members: as_fixture, get_module_class


User
~~~~

.. autoclass:: testinfra.modules.User
   :members:
   :undoc-members:


Group
~~~~~

.. autoclass:: testinfra.modules.Group
   :members:
   :undoc-members:


Interface
~~~~~~~~~

.. autoclass:: testinfra.modules.Interface
   :members:
   :undoc-members:
   :exclude-members: get_module_class


Package
~~~~~~~

.. autoclass:: testinfra.modules.Package
   :members:


Process
~~~~~~~

.. autoclass:: testinfra.modules.Process
   :members:

Service
~~~~~~~

.. autoclass:: testinfra.modules.Service
   :members:


Socket
~~~~~~

.. autoclass:: testinfra.modules.Socket
   :members:


SystemInfo
~~~~~~~~~~


.. autoclass:: testinfra.modules.SystemInfo
   :members:


Salt
~~~~


.. autoclass:: testinfra.modules.Salt(function, args=None)
   :members:

Ansible
~~~~~~~

.. autoclass:: testinfra.modules.Ansible(module_name, module_args=None, check=True)
   :members:


PuppetResource
~~~~~~~~~~~~~~


.. autoclass:: testinfra.modules.PuppetResource(type, name=None)
   :members:


Facter
~~~~~~


.. autoclass:: testinfra.modules.Facter(*facts)
   :members:

Sysctl
~~~~~~

.. autoclass:: testinfra.modules.Sysctl(name)
   :members:

.. _pytest fixtures: https://pytest.org/latest/fixture.html
