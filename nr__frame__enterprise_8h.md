# Frame



## Functions

|                | Name           |
| -------------- | -------------- |
| NRResult | **[NRFrameCompose](Files/nr__frame__enterprise_8h.md#function-nrframecompose)**(NRHandle rendering_handle, NRHandle frame_handle, NRComponent component, NRTextureID composed_color_buffer, bool async)<br>Composes all the frame buffers and output result into composed_color_buffer. SDK will composite all the frame buffers without do rerojection as well as distortion afterwards.  |


## Functions Documentation

### NRFrameCompose

```cpp
NRResult NRFrameCompose(
    NRHandle rendering_handle,
    NRHandle frame_handle,
    NRComponent component,
    NRTextureID composed_color_buffer,
    bool async
)
```

Composes all the frame buffers and output result into composed_color_buffer. SDK will composite all the frame buffers without do rerojection as well as distortion afterwards. 

**Parameters**: 

  * **rendering_handle** The handle of rendering object. 
  * **frame_handle** The handle of frame object. 
  * **component** The target component of the compose. 
  * **composed_color_buffer** The target buffer of compose result. 
  * **async** True to return without wait for gpu to finish while false to wait until gpu finish. 


**Return**: The result of operation. 

Call this function after setting the frame info like buffer viewport, pose, present time and fucus plane etc. Parameter frame_handle is invalid after calling this function, do not use it anymore.




