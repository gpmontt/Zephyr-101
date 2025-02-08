.. zephyr:code-sample:: blinky
   :name: blinky

   Turn on and of LED0.

Overview
********

A simple sample how to configurate a custom code 
using a old :ref:`supported board <boards>` and

Building and Running
********************

This application can be built and executed on QEMU as follows:

.. zephyr-app-commands::
   :zephyr-app: samples/basic/blinky
   :host-os: unix
   :board: qemu_x86
   :goals: run
   :compact:

To build for another board, change "qemu_x86" above to that board's name.

