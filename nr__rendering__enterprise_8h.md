# Rendering



## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[NREGLGraphicContext](Classes/struct_n_r_e_g_l_graphic_context.md)**  |
| struct | **[NRD3DGraphicContext](Classes/struct_n_r_d3_d_graphic_context.md)**  |
| struct | **[NRGLXGraphicContext](Classes/struct_n_r_g_l_x_graphic_context.md)**  |
| struct | **[NRGraphicContext](Classes/struct_n_r_graphic_context.md)**  |

## Types

|                | Name           |
| -------------- | -------------- |
| typedef struct [NREGLGraphicContext](Classes/struct_n_r_e_g_l_graphic_context.md) | **[NREGLGraphicContext](Files/nr__rendering__enterprise_8h.md#typedef-nreglgraphiccontext)**  |
| typedef struct [NRD3DGraphicContext](Classes/struct_n_r_d3_d_graphic_context.md) | **[NRD3DGraphicContext](Files/nr__rendering__enterprise_8h.md#typedef-nrd3dgraphiccontext)**  |
| typedef struct [NRGLXGraphicContext](Classes/struct_n_r_g_l_x_graphic_context.md) | **[NRGLXGraphicContext](Files/nr__rendering__enterprise_8h.md#typedef-nrglxgraphiccontext)**  |
| typedef struct [NRGraphicContext](Classes/struct_n_r_graphic_context.md) | **[NRGraphicContext](Files/nr__rendering__enterprise_8h.md#typedef-nrgraphiccontext)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| | **[NR_ENUM](Files/nr__rendering__enterprise_8h.md#function-nr-enum)**(NRGraphicContextType ) |
| NRResult | **[NRRenderingInitSetGraphicContext](Files/nr__rendering__enterprise_8h.md#function-nrrenderinginitsetgraphiccontext)**(NRHandle rendering_handle, const [NRGraphicContext](Classes/struct_n_r_graphic_context.md) * graphic_context)<br>Set the graphic context before the rendering system is running.  |
| NRResult | **[NRRenderingBeginFrame](Files/nr__rendering__enterprise_8h.md#function-nrrenderingbeginframe)**(NRHandle rendering_handle)<br>Called just before the frame rendering.  |

## Types Documentation

### typedef NREGLGraphicContext

```cpp
typedef struct NREGLGraphicContext NREGLGraphicContext;
```


### typedef NRD3DGraphicContext

```cpp
typedef struct NRD3DGraphicContext NRD3DGraphicContext;
```


### typedef NRGLXGraphicContext

```cpp
typedef struct NRGLXGraphicContext NRGLXGraphicContext;
```


### typedef NRGraphicContext

```cpp
typedef struct NRGraphicContext NRGraphicContext;
```



## Functions Documentation

### NR_ENUM

```cpp
NR_ENUM(
    NRGraphicContextType 
)
```


### NRRenderingInitSetGraphicContext

```cpp
NRResult NRRenderingInitSetGraphicContext(
    NRHandle rendering_handle,
    const NRGraphicContext * graphic_context
)
```

Set the graphic context before the rendering system is running. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **graphic_context** The graphic context which app using to rendering. 


**Return**: The result of operation. 

Only for openxr 

Note: Only set once before the rendering system running. This function will be failed if set during rendeing system running period. App use this graphic context to do rendering jobs.


### NRRenderingBeginFrame

```cpp
NRResult NRRenderingBeginFrame(
    NRHandle rendering_handle
)
```

Called just before the frame rendering. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 


**Return**: The result of operation. 

Only for openxr 




