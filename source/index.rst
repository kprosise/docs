FoundriesFactory_ Documentation
===============================

The FoundriesFactory™ SaaS platform puts you in full control to simplify and reduce time to market for Linux based IoT and Edge devices on your choice of hardware, with lowered costs and code that remains yours.

The platform provides a comprehensive tool set for building, testing, deploying,
and maintaining updatable, security focused IoT and Edge products.

Combined with the :term:`Linux microPlatform` (LmP) and utilizing open source software projects including U-Boot, OP-TEE, OE/Yocto Project, and Docker®,
The FoundriesFactory Platform brings together key features and functions for developing professional embedded devices.

.. tip::
   See a typo or notice something missing? We are grateful for any public contributions!
   Fork our `repo <https://github.com/foundriesio/docs>`_ and checkout the README for contribution guidelines.

Documentation Overview
----------------------

* Getting Started will guide you from :ref:`gs-signup` and creating your :term:`Factory`, to :ref:`gs-flash-device`,
  installing the CLI tool :term:`Fioctl` for interacting with your Factory, and the basics of building and deploying an App.

* :ref:`Tutorials <tutorials>` will familiarize you with the workflow you will need to get the most from your Factory.

* :ref:`User Guide <user-guide>` walks you through common tasks and settings for your Factory.

* Advanced use cases and technical details are in the :ref:`Reference Manual <ref-manual>`.

* For adding support for a machine not already supported by the FoundriesFactory platform,
  see the :ref:`ref-pg`.

.. toctree::
   :maxdepth: 2
   :caption: Getting started
   :name: sec-learn

   getting-started/signup/index
   getting-started/flash-device/index
   getting-started/register-device/index
   getting-started/install-fioctl/index
   getting-started/building-deploying-app/index

.. toctree::
   :maxdepth: 2
   :caption: Tutorials
   :name: sec-tutorials

   tutorials/index
   tutorials/getting-started-with-docker/getting-started-with-docker
   tutorials/creating-first-target/creating-first-target
   tutorials/deploying-first-app/deploying-first-app
   tutorials/configuring-and-sharing-volumes/configuring-and-sharing-volumes
   tutorials/compose-app/compose-app
   tutorials/customizing-the-platform/customizing-the-platform
   tutorials/working-with-tags/working-with-tags

.. toctree::
   :maxdepth: 2
   :glob:
   :caption: User Guide
   :name: sec-user-guide

   user-guide/index
   user-guide/flashing/flashing
   user-guide/fioctl/index
   user-guide/qemu/qemu
   user-guide/account-management/account-management
   user-guide/ip-protection/ip-protection
   user-guide/custom-ci/custom-ci
   user-guide/mirror-action/mirror-action
   user-guide/submodule/submodule
   reference-manual/remote-access/remote-access
   user-guide/foundriesio-rest-api/foundriesio-rest-api
   user-guide/containers-and-docker/index
   reference-manual/docker/private-registries
   user-guide/lmp-customization/index
   user-guide/lmp-auto-hostname/lmp-auto-hostname
   user-guide/lmp-device-auto-register/lmp-device-auto-register
   user-guide/custom-sota-client
   user-guide/offline-update/offline-update
   reference-manual/linux/linux-disk-encryption
   reference-manual/linux/factory-device-reset
   reference-manual/linux/linux-update
   reference-manual/security/secure-machines
   reference-manual/security/offline-keys
   reference-manual/security/factory-keys
   reference-manual/factory/sboms
   user-guide/waves/waves
   user-guide/device-gateway-pki/device-gateway-pki
   user-guide/rotating-cert
   user-guide/troubleshooting/troubleshooting

.. toctree::
   :maxdepth: 2
   :caption: Reference Manual
   :name: sec-manual

   reference-manual/index
   reference-manual/docker/docker
   reference-manual/factory/factory
   reference-manual/linux/linux
   reference-manual/ota/ota
   reference-manual/remote-access/remote-access
   reference-manual/security/security
   reference-manual/testing/testing

.. toctree::
   :maxdepth: 2
   :caption: Porting Guide
   :name: sec-porting-guide

   porting-guide/pg.rst

.. toctree::
   :caption: Glossary
   :name: sec-glossary

   glossary/index

.. toctree::
   :caption: Appendix
   :name: sec-appendix

   appendix/fioctl-command-reference/index

.. toctree::
   :caption: Release Notes
   :name: sec-release-notes

   v95 <https://github.com/foundriesio/docs/blob/main/release-notes/rn_v95.md>
   v94 <https://github.com/foundriesio/docs/blob/main/release-notes/rn_v94.md>
   v93 <https://github.com/foundriesio/docs/blob/main/release-notes/rn_v93.md>
   v92 <https://github.com/foundriesio/docs/blob/main/release-notes/rn_v92.md>

.. _FoundriesFactory: https://cta-eu1.hubspot.com/web-interactives/public/v1/track/click?encryptedPayload=AVxigLLK0Z66%2FNiNKYD21fVW3XrygFqp0o1etaHiD9RRRp2Q67fr5UptBRX2EeK27YBKm2AP3Quj3YsTFf4zR04TkEyHZ9HoZzR1PlolICwWI0wh8tx3uq0OhDVQ5mrQQPJLnluzDkxhbbz%2Fhkmjf6JbAvCy0CGNeEVjHgcDLbFVswhaQQ%3D%3D&portalId=26493592
