# Swapchain



## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[NRSurfaceDataBase](Classes/struct_n_r_surface_data_base.md)**  |
| struct | **[NRSurfaceDataDisplayRecord](Classes/struct_n_r_surface_data_display_record.md)**  |

## Types

|                | Name           |
| -------------- | -------------- |
| typedef struct [NRSurfaceDataBase](Classes/struct_n_r_surface_data_base.md) | **[NRSurfaceDataBase](Files/nr__swapchain__enterprise_8h.md#typedef-nrsurfacedatabase)**  |
| typedef struct [NRSurfaceDataDisplayRecord](Classes/struct_n_r_surface_data_display_record.md) | **[NRSurfaceDataDisplayRecord](Files/nr__swapchain__enterprise_8h.md#typedef-nrsurfacedatadisplayrecord)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| | **[NR_ENUM](Files/nr__swapchain__enterprise_8h.md#function-nr-enum)**(NRSurfaceOperationType ) |
| NRResult | **[NRSwapchainGetBuffers](Files/nr__swapchain__enterprise_8h.md#function-nrswapchaingetbuffers)**(NRHandle rendering_handle, NRHandle swapchain_handle, uint32_t buffer_count, NRTextureID * out_buffers)<br>Gets the native buffers of the swap chain. The native buffers can be set outside instead of allocated inside the swap chain.  |
| NRResult | **[NRSwapchainWaitBuffer](Files/nr__swapchain__enterprise_8h.md#function-nrswapchainwaitbuffer)**(NRHandle rendering_handle, NRHandle swapchain_handle, uint32_t buffer_index, uint64_t time_out)<br>Waits for the swap chain's indexed native buffer to be free.  |
| NRResult | **[NRSwapchainReleaseBuffer](Files/nr__swapchain__enterprise_8h.md#function-nrswapchainreleasebuffer)**(NRHandle rendering_handle, NRHandle swapchain_handle, uint32_t buffer_index)<br>Releases the indexed native buffer.  |
| NRResult | **[NRSwapchainUpdateExternalSurface](Files/nr__swapchain__enterprise_8h.md#function-nrswapchainupdateexternalsurface)**(NRHandle rendering_handle, NRHandle swapchain_handle, int32_t transform_count, const NRTransform * transforms, const NRComponent * transform_components, uint64_t present_time, int32_t transform_index)<br>Matchs the pose index with the pose data as well as the timestamp of the pose and save the matching relationship.  |

## Types Documentation

### typedef NRSurfaceDataBase

```cpp
typedef struct NRSurfaceDataBase NRSurfaceDataBase;
```


### typedef NRSurfaceDataDisplayRecord

```cpp
typedef struct NRSurfaceDataDisplayRecord NRSurfaceDataDisplayRecord;
```



## Functions Documentation

### NR_ENUM

```cpp
NR_ENUM(
    NRSurfaceOperationType 
)
```


### NRSwapchainGetBuffers

```cpp
NRResult NRSwapchainGetBuffers(
    NRHandle rendering_handle,
    NRHandle swapchain_handle,
    uint32_t buffer_count,
    NRTextureID * out_buffers
)
```

Gets the native buffers of the swap chain. The native buffers can be set outside instead of allocated inside the swap chain. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **swapchain_handle** The handle of swap chian object. 
  * **buffer_count** The count of buffer array. 
  * **out_buffers** The pinter of buffer array. 


**Return**: The result of operation. 

Only for openxr 


### NRSwapchainWaitBuffer

```cpp
NRResult NRSwapchainWaitBuffer(
    NRHandle rendering_handle,
    NRHandle swapchain_handle,
    uint32_t buffer_index,
    uint64_t time_out
)
```

Waits for the swap chain's indexed native buffer to be free. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **swapchain_handle** The handle of swap chian object. 
  * **buffer_index** The index of the waited native buffer. 
  * **time_out** The time for the wait to last most, zero to last util rendering system free it. 


**Return**: The result of operation. 

Only for openxr 

The indexed native buffer maybe used by the rendering system, wait for the rendering system to release it.


### NRSwapchainReleaseBuffer

```cpp
NRResult NRSwapchainReleaseBuffer(
    NRHandle rendering_handle,
    NRHandle swapchain_handle,
    uint32_t buffer_index
)
```

Releases the indexed native buffer. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **swapchain_handle** The handle of swap chian object. 
  * **buffer_index** The index of native buffer. 


**Return**: The result of operation. 

Only for openxr 

After app rendering to this native buffer, release it and then the rendering system can use it.


### NRSwapchainUpdateExternalSurface

```cpp
NRResult NRSwapchainUpdateExternalSurface(
    NRHandle rendering_handle,
    NRHandle swapchain_handle,
    int32_t transform_count,
    const NRTransform * transforms,
    const NRComponent * transform_components,
    uint64_t present_time,
    int32_t transform_index
)
```

Matchs the pose index with the pose data as well as the timestamp of the pose and save the matching relationship. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **swapchain_handle** The handle of swap chian object. 
  * **layer_id** The unique id of the layer. 
  * **transform** The head pose data includes rotaion and translation. 
  * **present_time** The timestamp of the head pose. 
  * **transform_index** The index of the pose. This index is used to match the pose data. 


**Return**: The result of operation. 

This function is special for webxr. Webxr use this pose to render contents to a android surface and write the pose index into the contents. SDK will read the pose index from the android surface and get the pose data from the matching relationships to do reprojection.




