License:

ARDrone Control .NET - An application for flying the Parrot AR drone in Windows.
Copyright (C) 2010 Thomas Endres, Stephen Hobley, Julien Vinel

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, see <http://www.gnu.org/licenses/>.

-----------------------------------------------------------------
ARDrone.Net library for the Parrot AR Drone
Stephen Hobley, Thomas Endres and Julien Vinel November 2010
-----------------------------------------------------------------
You must have the DirectX and Windows SDK installed in order to compile this solution file.

A few quick tips to get the app up and running:
- This is a Visual Studio 2010 project using .NET framework 4.0
- You need to download and install Windows SDK, a fresh copy of the DirectX SDK as well as an SDL installation
  - Get DirectX from http://msdn.microsoft.com/en-us/directx/aa937788.aspx
  - Get Windows SDK from http://msdn.microsoft.com/de-de/windows/aa904949.aspx
  - Get SDL from http://www.libsdl.org/download-1.2.php
- You need to change the directories for Windows SDK and DirectX SDK in the file "ARDroneProperties.props" to your own directories
    <WinSDKDir></WinSDKDir>
    <DXSDKDir></DXSDKDir>
	<SDLDir></SDLDir>
    Link to the main directories where you installed the libraries (no subdirectories needed)
  These should point to the respective folders on your harddrive.
- For the ARDrone JNI bridge project, you will also need to set properties in the properties.props file:
    <JDKDir></JDKDir>
  For this to work, you will need to download and install a JDK: http://www.oracle.com/technetwork/java/javase/downloads/index.html
  Afterwards, point the JDKDir to the location where you installed the JDK to.
- You need to disable the loader lock exception in Visual Studio (Debug -> Exceptions -> Managed Debugging assistents -> Disable the "Loader lock" checkbox)

Once you have completed these steps, the solution should compile.

For more information, visit our websites:
https://github.com/shtejv/ARDrone-Control-.NET
http://parrotsonjava.com
http://stephenhobley.com/blog

This software uses the following libraries:
- Parrot AR Drone SDK:		https://projects.ardrone.org/projects/show/ardrone-api

!!! IMPORTANT INFO for Windows XP users !!!

Please comment the line

"define USE_WINDOWS_CONDITION_VARIABLES"

in vp_os_signal_dep.h.
Otherwise, you will get a DLLNotFoundException when pressing the startup button.



