# Buffer Spec



## Functions

|                | Name           |
| -------------- | -------------- |
| | **[NR_ENUM](Files/nr__buffer__spec__enterprise_8h.md#function-nr-enum)**(NRExternalSurfaceFlags )<br>The flag of external surface flag. Flags supported by vrapi_CreateAndroidSurfaceSwapChain3.  |
| | **[NR_ENUM](Files/nr__buffer__spec__enterprise_8h.md#function-nr-enum)**(NRSurfaceHolderType ) |
| NRResult | **[NRBufferSpecSetExternalSurfaceFlag](Files/nr__buffer__spec__enterprise_8h.md#function-nrbufferspecsetexternalsurfaceflag)**(NRHandle rendering_handle, NRHandle spec_handle, uint32_t surface_flag)<br>Sets the flag of external surface.  |
| NRResult | **[NRBufferSpecSetExternalSurfaceHolder](Files/nr__buffer__spec__enterprise_8h.md#function-nrbufferspecsetexternalsurfaceholder)**(NRHandle rendering_handle, NRHandle spec_handle, NRSurfaceHolderType surface_holder_type)<br>Sets the holder of external surface.  |
| NRResult | **[NRBufferSpecSetUsageFlags](Files/nr__buffer__spec__enterprise_8h.md#function-nrbufferspecsetusageflags)**(NRHandle rendering_handle, NRHandle spec_handle, uint64_t usage_flags)<br>Sets the create flag of buffer spec object.  |


## Functions Documentation

### NR_ENUM

```cpp
NR_ENUM(
    NRExternalSurfaceFlags 
)
```

The flag of external surface flag. Flags supported by vrapi_CreateAndroidSurfaceSwapChain3. 

### NR_ENUM

```cpp
NR_ENUM(
    NRSurfaceHolderType 
)
```


### NRBufferSpecSetExternalSurfaceFlag

```cpp
NRResult NRBufferSpecSetExternalSurfaceFlag(
    NRHandle rendering_handle,
    NRHandle spec_handle,
    uint32_t surface_flag
)
```

Sets the flag of external surface. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **spec_handle** The handle of buffer specification object. 
  * **surface_flag** Bit composition of NRExternalSurfaceFlags enum. 


**Return**: The result of operation. 

only for android 


### NRBufferSpecSetExternalSurfaceHolder

```cpp
NRResult NRBufferSpecSetExternalSurfaceHolder(
    NRHandle rendering_handle,
    NRHandle spec_handle,
    NRSurfaceHolderType surface_holder_type
)
```

Sets the holder of external surface. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **spec_handle** The handle of buffer specification object. 
  * **surface_holder_type** The type of surface holder. 


**Return**: The result of operation. 

Only for android 


### NRBufferSpecSetUsageFlags

```cpp
NRResult NRBufferSpecSetUsageFlags(
    NRHandle rendering_handle,
    NRHandle spec_handle,
    uint64_t usage_flags
)
```

Sets the create flag of buffer spec object. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **spec_handle** The handle of buffer specification object. 
  * **usage_flags** Bit composition of flag NRSwapchainUsedFlags enum. 


**Return**: The result of operation. 

Only for openxr 




