This readme file contains the following information:

* Overview
* How to Compile Sample Applications
* Sample Applications
* Limitations

## Overview

CADP for C v8.13.0.000 supports Key Management using NAE protocol for communication with the Key Manager server. Currently, only the following managed objects are supported: Symmetric Key, Template, and Secret Data.

For API details, refer to the NAE Key Management API section in the CADP for C API Guide. To use NAE with CADP for C, you must set the NAE_IP, NAE_Port, Protocol, and CA_File parameters in the properties file.

**Important!** Additional parameters can be set for additional features. To use the NAE Key Management features, the Protocol parameter should be set to ssl.

For details on NAE parameters, refer to "Configuration" page in the CADP for C user guide.

## How to Compile Sample Applications

Included with the CADP for C v8.13.0.000 software are sample C/C++ files, the source code for sample applications that you can use to test your installation.

>*To compile the sample application on **Windows**:*

1. Navigate to `<installation_Directory>` i.e., C:\Program Files\CipherTrust\CADP_for_C\.

2. Copy "C" directory of sample applications (CipherTrust_Application_Protection\key_management\C) to `<installation_Directory>`.

3. Navigate to `<installation_Directory>\C\VC`

4. Open the `sample.sln` file in Visual Studio 2010.

5. Select a sample project and build it.

>*To compile the sample application on **Linux**:*

You can compile this with a C++ or C compiler such as gcc (3.2.x or greater). If you have an older gcc or another C compiler, you may need to obtain libstdc++.so.5 and possibly libgcc_s.so.

1. Navigate to `<installation_Directory>`. For example, consider that `<installation_Directory>` is /opt/CipherTrust/CADP_for_C/.

2. Copy "C" directory of sample applications (CipherTrust_Application_Protection/key_management/C) to the `<installation_Directory>`.

3. Navigate to `<installation_Directory>/C/`.

4. Run make command.
```
   [root@machine C]# make
```
5. Run a sample with valid arguments.
```
   [root@machine C]# ./NAEKeyManagement -h
```

## Sample Applications

Sample applications to demonstrate the use of NAE Key Management.

**NAE Key Management Sample Applications**

The NAE Key Management sample applications supplied with CADP for C are:

Application | Description
---|---
NAEVersionedKey.c | Demonstrates the use of versioned keys.
NAEKeyManagement.c | Performs key creation and export on Key Manager.

## Limitations

* ModifyAttribute operation supports limited attributes. Only the String and DateTime attributes are currently supported.
* Locate operation using wild cards and regular expressions is not supported.

---