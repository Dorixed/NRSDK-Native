# Hmd



## Functions

|                | Name           |
| -------------- | -------------- |
| | **[NR_ENUM](Files/nr__hmd__enterprise_8h.md#function-nr-enum)**(NRChannelType )<br>channel type.  |
| NRResult | **[NRHMDGetComponentExtrinsic](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetcomponentextrinsic)**(NRHandle hmd_handle, NRComponent base_component, NRComponent target_component, NRMat4f * out_extrinsic)<br>Gets the transformation matrix from the base component pose to the target component pose. Or, Gets the position and rotation of the target component in the coordinate system of the base component. The following terms share the same spatial meaning: Term 1: the transformation from the base to the target. (aka target from base, base to target) Term 2: the position and rotation of the target in the coordinate system of the base. (aka target in base)  |
| NRResult | **[NRHMDGetComponentProjectionMatrix](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetcomponentprojectionmatrix)**(NRHandle hmd_handle, NRComponent display, NRMat4f * out_component_projection_matrix) |
| NRResult | **[NRHMDSetOverFillFactor](Files/nr__hmd__enterprise_8h.md#function-nrhmdsetoverfillfactor)**(NRHandle hmd_handle, float over_fill_x, float over_fill_y) |
| NRResult | **[NRHMDIsChannelEnabled](Files/nr__hmd__enterprise_8h.md#function-nrhmdischannelenabled)**(NRHandle hmd_handle, NRChannelType nr_channel_type, bool * out_is_enabled)<br>Query whether a sensor device is enabled.  |
| NRResult | **[NRHMDUpdateIPD](Files/nr__hmd__enterprise_8h.md#function-nrhmdupdateipd)**(NRHandle hmd_handle, float IPD)<br>Set specific IPD values and update related parameters.  |
| NRResult | **[NRHMDGetDisplayDistortionSize](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetdisplaydistortionsize)**(NRHandle hmd_handle, NRComponent display, NRSize2i * out_distortion_size)<br>Get the size of the distortion data.  |
| NRResult | **[NRHMDGetDisplayDistortionData](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetdisplaydistortiondata)**(NRHandle hmd_handle, NRComponent display, uint32_t data_size, float * out_distortion_data)<br>Get the distortion data of a single display.  |
| NRResult | **[NRHMDGetIMUAccelerometerBias](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetimuaccelerometerbias)**(NRHandle hmd_handle, NRVector3f * out_bias)<br>Get the offline bias data for the accelerometer.  |
| NRResult | **[NRHMDGetIMUGyroscopeBias](Files/nr__hmd__enterprise_8h.md#function-nrhmdgetimugyroscopebias)**(NRHandle hmd_handle, NRVector3f * out_bias)<br>Get the offline bias data for the gyroscope.  |


## Functions Documentation

### NR_ENUM

```cpp
NR_ENUM(
    NRChannelType 
)
```

channel type. 

### NRHMDGetComponentExtrinsic

```cpp
NRResult NRHMDGetComponentExtrinsic(
    NRHandle hmd_handle,
    NRComponent base_component,
    NRComponent target_component,
    NRMat4f * out_extrinsic
)
```

Gets the transformation matrix from the base component pose to the target component pose. Or, Gets the position and rotation of the target component in the coordinate system of the base component. The following terms share the same spatial meaning: Term 1: the transformation from the base to the target. (aka target from base, base to target) Term 2: the position and rotation of the target in the coordinate system of the base. (aka target in base) 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **base_component** The component type for the origin of the transformation. 
  * **target_component** The component type for the destination of the transformation. 
  * **out_extrinsic** Transformation matrix from origin component to the destination component. 


**Return**: The result of operation. 

Note: This function supports all kinds of component type including NR_COMPONENT_RGB_CAMERA.


### NRHMDGetComponentProjectionMatrix

```cpp
NRResult NRHMDGetComponentProjectionMatrix(
    NRHandle hmd_handle,
    NRComponent display,
    NRMat4f * out_component_projection_matrix
)
```


### NRHMDSetOverFillFactor

```cpp
NRResult NRHMDSetOverFillFactor(
    NRHandle hmd_handle,
    float over_fill_x,
    float over_fill_y
)
```


### NRHMDIsChannelEnabled

```cpp
NRResult NRHMDIsChannelEnabled(
    NRHandle hmd_handle,
    NRChannelType nr_channel_type,
    bool * out_is_enabled
)
```

Query whether a sensor device is enabled. 

**Parameters**: 

  * **hmd_handle** The Handle of HMD object. 
  * **nr_channel_type** The type of sensor channel. 
  * **out_is_enabled** The result of whether the sensor is enabled. 


**Return**: The result of operation. 

### NRHMDUpdateIPD

```cpp
NRResult NRHMDUpdateIPD(
    NRHandle hmd_handle,
    float IPD
)
```

Set specific IPD values and update related parameters. 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **IPD** The desired ipd value in meters. 


**Return**: The result of operation. 

Note: IPD should be specified in meters, in accord with extrinsic parameters. IPD values must be larger than zero, or nothing will happen.


### NRHMDGetDisplayDistortionSize

```cpp
NRResult NRHMDGetDisplayDistortionSize(
    NRHandle hmd_handle,
    NRComponent display,
    NRSize2i * out_distortion_size
)
```

Get the size of the distortion data. 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **display** NR_COMPONENT_DISPLAY_LEFT or NR_COMPONENT_DISPLAY_RIGHT. 
  * **out_distortion_size** The size of distortion data in NRSize2i. 


**Return**: The result of the operation. 

### NRHMDGetDisplayDistortionData

```cpp
NRResult NRHMDGetDisplayDistortionData(
    NRHandle hmd_handle,
    NRComponent display,
    uint32_t data_size,
    float * out_distortion_data
)
```

Get the distortion data of a single display. 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **display** NR_COMPONENT_DISPLAY_LEFT or NR_COMPONENT_DISPLAY_RIGHT. 
  * **data_size** The size of distortion data in uint32_t, which should be distortion_size.width * distortion_size.height * 4. 
  * **out_distortion_data** The distortion data in float array, where every four float values composes the data of one point, in the order pt_x, pt_y, dis_pt_x, dis_pt_y respectively. 


**Return**: The result of the operation. 

### NRHMDGetIMUAccelerometerBias

```cpp
NRResult NRHMDGetIMUAccelerometerBias(
    NRHandle hmd_handle,
    NRVector3f * out_bias
)
```

Get the offline bias data for the accelerometer. 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **out_bias** The output bias data for the accelerometer. 


**Return**: The result of operation. 

### NRHMDGetIMUGyroscopeBias

```cpp
NRResult NRHMDGetIMUGyroscopeBias(
    NRHandle hmd_handle,
    NRVector3f * out_bias
)
```

Get the offline bias data for the gyroscope. 

**Parameters**: 

  * **hmd_handle** The handle of HMD object. 
  * **out_bias** The output bias data for the gyroscope. 


**Return**: The result of operation. 



