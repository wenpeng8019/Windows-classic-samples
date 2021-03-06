RequestReplyNamedPipeClientWithWindowsTransportSecurityExample

Description
===========

This example shows a named pipe client that sends request-reply messages, with security provided by Windows SSPI transport security.  It also illustrates the client using security token properties to modify the allowed impersonation level from the default.

Security Note
=============

This sample is provided for educational purpose only to demonstrate how to use
Windows Web Services API. It is not intended to be used without modifications
in a production environment and it has not been tested in a production
environment. Microsoft assumes no liability for incidental or consequential
damages should the sample code be used for purposes other than as intended.

Prerequisites
=============

In order to run this sample on Windows XP, Windows Vista, Windows Server 2003
and Windows Server 2008, you may need to install a Windows Update that contains
the runtime DLL for Windows Web Services API. Please consult with the
documentation on MSDN for more information.

Building the Sample
===================

To build the RequestReplyNamedPipeClientWithWindowsTransportSecurityExample sample
  1. Open the solution RequestReplyNamedPipeClientWithWindowsTransportSecurityExample.sln in Visual Studio.
  2. Change the active solution platform to the desired platform in the
     Configuration Manager found on the Build menu.
  3. On the Build menu, click Build.

Reserving the HTTP URLs
=======================

In order to run server HTTP samples from non-elevated Visual Studio you
have to reserve some HTTP URLs first. Please run the following commands in an elevated CMD:
  1. netsh http add urlacl url=http://+:80/example user=%USERDOMAIN%\%USERNAME%
  2. netsh http add urlacl url=https://+:443/example user=%USERDOMAIN%\%USERNAME%
or if you are using elevated PowerShell:
  1. netsh http add urlacl url=http://+:80/example user=$env:USERDOMAIN\$env:USERNAME
  2. netsh http add urlacl url=https://+:443/example user=$env:USERDOMAIN\$env:USERNAME

To delete the reservations, please run in elevated CMD or PowerShell:
  1. netsh http delete urlacl url=http://+:80/example
  2. netsh http delete urlacl url=https://+:443/example

Running the Sample
==================

To run the RequestReplyNamedPipeClientWithWindowsTransportSecurityExample sample
  1. Run RequestReplyNamedPipeClientWithWindowsTransportSecurityExample by clicking Start Without Debugging on the Debug menu.

� Microsoft Corporation. All rights reserved.


