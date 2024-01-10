
# Eclipse IDE

ABOUT

## Installation Guide

The installation guide depending on your operating system.

### Windows

A step-bystep guide is provided by the [Eclipse official webpage](https://www.eclipse.org/downloads/packages/installer "Install Eclipse on Windows"). Just download the Eclipse Installer and follow the wizard instructions.<br>

Once the installation is finished, you can find Eclipse among your applications.

### Linux (Ubuntu)

You can find the latest and stable version of Eclipse IDE directly from [Snapcraft](https://snapcraft.io/eclipse "Install Eclipse on Linux"). Install it by clicking on **Install** > **View in Desktop Store** > **Open Link** > **Ubuntu Software** > **Install**, or by using the command line `sudo snap install eclipse --classic`.<br>

Once the installation is finished, you can find Eclipse among your applications.

## Configuration Guide

### Download external resources automatically

Opening files which define DTD or XSD schemas, like in `pom.xml` and `persistence.xml`, requires those schemas to be downloaded and stored locally; for example, on Linux they are found in the `.lemminx` folder.<br>

If you find the error message `Downloading external resources is disabled` coming from these files, you can fix that by modifying Eclipse settings: **Window** > **Preferences** > **XML (Wild Web Developer)** > tick `Download external resources like referenced DTD, XSD` > **Apply** > **Apply and Close**.
