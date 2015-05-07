# ADAMDrvClose
| Product | OS | CPU Type | Library version |Image version |
| --| -- | -- | -- | -- |
| APAX-6572 | Win32/WinCE | X86 | V2.02 | V2.04B698 |

Close the ADAM/APAX device by calling this function when operation is completed.

#### Syntax

```c
ADAMDrvClose (
    LONG *handle
);
```

#### Parameters

|Name|	Direction|  	Description|
|--|--|--|
|handle|	Input |[in] The driver handler.|

#### Return Values
If driver termination succeeded, the return value is **0 (ERR_SUCCESS)**. If the function fails, the return value is **325 (ERR_INTERNAL_FAILED)**. To get extended error information, call **GetLastError** function.


#### Example
```c
if(NULL != lDriverHandle) {
	ADAMDrvClose(&lDriverHandle);
	lDriverHandle = NULL;
}
```
For more detailed information regarding this function, please see

> $(Default install directory)\APAX\Win32\CPlusPlus\APAX-PAC-Sample\APAX-5013.cpp

