# Perception



## Functions

|                | Name           |
| -------------- | -------------- |
| | **[NR_ENUM](Files/nr__perception__enterprise_8h.md#function-nr-enum)**(NRCalibrationResult )<br>The Calibration result.  |
| NRResult | **[NRImuCalibrationStart](Files/nr__perception__enterprise_8h.md#function-nrimucalibrationstart)**(NRHandle perception_handle, float delta_degree, float last_time) |
| NRResult | **[NRImuCalibrationPhaseStart](Files/nr__perception__enterprise_8h.md#function-nrimucalibrationphasestart)**(NRHandle perception_handle, float base_degree) |
| NRResult | **[NRImuCalibrationPhaseQueryRate](Files/nr__perception__enterprise_8h.md#function-nrimucalibrationphasequeryrate)**(NRHandle perception_handle, int32_t * out_rate) |
| NRResult | **[NRImuCalibrationQueryPitch](Files/nr__perception__enterprise_8h.md#function-nrimucalibrationquerypitch)**(NRHandle perception_handle, float * out_pitch_degree) |
| NRResult | **[NRImuCalibrationStop](Files/nr__perception__enterprise_8h.md#function-nrimucalibrationstop)**(NRHandle perception_handle, NRCalibrationResult calibration_result) |


## Functions Documentation

### NR_ENUM

```cpp
NR_ENUM(
    NRCalibrationResult 
)
```

The Calibration result. 

### NRImuCalibrationStart

```cpp
NRResult NRImuCalibrationStart(
    NRHandle perception_handle,
    float delta_degree,
    float last_time
)
```


### NRImuCalibrationPhaseStart

```cpp
NRResult NRImuCalibrationPhaseStart(
    NRHandle perception_handle,
    float base_degree
)
```


### NRImuCalibrationPhaseQueryRate

```cpp
NRResult NRImuCalibrationPhaseQueryRate(
    NRHandle perception_handle,
    int32_t * out_rate
)
```


### NRImuCalibrationQueryPitch

```cpp
NRResult NRImuCalibrationQueryPitch(
    NRHandle perception_handle,
    float * out_pitch_degree
)
```


### NRImuCalibrationStop

```cpp
NRResult NRImuCalibrationStop(
    NRHandle perception_handle,
    NRCalibrationResult calibration_result
)
```




