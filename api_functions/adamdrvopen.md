# ADAMDrvOpen
| Product | OS | CPU Type | Library version |Image version |
| --| -- | -- | -- | -- |
| APAX-6572 | Win32/WinCE | X86 | V2.02 | V2.04B698 |

Users can use this function to open APAX device. The function returns a handle that can be used to access the APAX device.

#### Syntax

```c
ADAMDrvOpen(
    LONG *handle
);

```

#### Parameters

|Name|	Direction|  	Description|
|--|--|--|
|handle|	Output	[out] |The driver handler.|

#### Return Values
If driver initialization succeeded, the return value is **0 (ERR_SUCCESS)**. If the function fails, the return value is **325 (ERR_INTERNAL_FAILED)**. To get extended error information, call **GetLastError** function.

#### Remarks
Use the **[ADAMDrvClose](adamdrvclose.md)** function to close the ADAM/APAX device.

#### Example
```c
LONG lDriverHandle = NULL; /* Driver handler */
if(ERR_SUCCESS != ADAMDrvOpen(&lDriverHandle))
    printf("Fail to open driver\n");
```
For more detailed information regarding this function, please see

> $(Default install directory)\APAX\Win32\CPlusPlus\APAX-PAC-Sample\APAX-5013.cpp

