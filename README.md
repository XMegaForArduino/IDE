# IDE

This repository contains downloadable files that are related to the Arduino
IDE (hardware manager etc.).

It is intended to make life easier for people who simply want to add this
extension to the IDE for the purpose of XMega processor development.

The packages contained here are snapshots of the 'HEAD' branch for the
project.  Whenever a major release is done, a new snapshot will be created,
and updates will be made to the JSON file (for the package manager).


SOME of the hardware supported by the XMegaForArduino project may not be
supported by the compilers and tools.  For example, the atxmega64d4 already
has support in avr-gcc, avr-binutils, and avr-libc.  However, the
atxmega32e5 is missing support in avr-binutils and avr-libc.  As a result,
if you attempt to build using the 'official' toolset, you will get errors
for those CPU types that are not fully supported.


At some point in the future I will include tool versions that support these
processors.  Until then, instructions for patching the existing tools can
be found in the 'patches' repository.


Additionally, the added files will reference a modified version of the
'avrdude.conf' file, to support the protocols used for the various
bootloaders.  Most of them duplicate the 'stk' protocols used by the Uno
('arduino') and the MEGA2560 ('wiring').  However, the actual CPU settings
associated with these protocols are typically NOT defined (or are incorrectly
defined in some cases) in the default 'avrdude.conf'.  Rather than forcing
you to patch it, the updated file is included in the prepared packages.


For additional information, see the 'Wiki' for this repository.

