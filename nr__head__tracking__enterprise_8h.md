# Head Tracking



## Functions

|                | Name           |
| -------------- | -------------- |
| NRResult | **[NRHeadTrackingDeepRecenter](Files/nr__head__tracking__enterprise_8h.md#function-nrheadtrackingdeeprecenter)**(NRHandle perception_handle, NRHandle head_tracking_handle, uint32_t deep_value)<br>Recenter the head orientation with deep value.  |
| NRResult | **[NRHeadPoseGetBias](Files/nr__head__tracking__enterprise_8h.md#function-nrheadposegetbias)**(NRHandle perception_handle, NRHandle head_pose_handle, NRVector3f * out_acc_bias, NRVector3f * out_gyro_bias)<br>Get the bias of head pose.  |
| NRResult | **[NRHeadPoseGetVelocity](Files/nr__head__tracking__enterprise_8h.md#function-nrheadposegetvelocity)**(NRHandle perception_handle, NRHandle head_pose_handle, NRVector3f * out_velocity, NRVector3f * out_angular_velocity) |


## Functions Documentation

### NRHeadTrackingDeepRecenter

```cpp
NRResult NRHeadTrackingDeepRecenter(
    NRHandle perception_handle,
    NRHandle head_tracking_handle,
    uint32_t deep_value
)
```

Recenter the head orientation with deep value. 

**Parameters**: 

  * **perception_handle** The handle of perception object. 
  * **deep_value** The value of deep. 


**Return**: The result of operation. 

Note: The method should only be used in 3dof perception. In 6dof perception, no effect occurs.


### NRHeadPoseGetBias

```cpp
NRResult NRHeadPoseGetBias(
    NRHandle perception_handle,
    NRHandle head_pose_handle,
    NRVector3f * out_acc_bias,
    NRVector3f * out_gyro_bias
)
```

Get the bias of head pose. 

**Parameters**: 

  * **perception_handle** The handle of perception object. 
  * **head_pose_handle** The handle of head pose object. 
  * **out_acc_bias** The bias of accelerometer. 
  * **out_gyro_bias** The bias of gyroscope. 


**Return**: The result of method execution. 

### NRHeadPoseGetVelocity

```cpp
NRResult NRHeadPoseGetVelocity(
    NRHandle perception_handle,
    NRHandle head_pose_handle,
    NRVector3f * out_velocity,
    NRVector3f * out_angular_velocity
)
```




