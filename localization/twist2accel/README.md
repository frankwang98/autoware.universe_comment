# twist2accel

## Purpose

This package is responsible for estimating acceleration using the output of `ekf_localizer`. It uses lowpass filter to mitigate the noise. 加速度估计，用低通滤波去过滤噪声

## Inputs / Outputs

### Input

| Name          | Type                                             | Description           |
| ------------- | ------------------------------------------------ | --------------------- |
| `input/odom`  | `nav_msgs::msg::Odometry`                        | localization odometry |
| `input/twist` | `geometry_msgs::msg::TwistWithCovarianceStamped` | twist                 |

### Output

| Name           | Type                                             | Description            |
| -------------- | ------------------------------------------------ | ---------------------- |
| `output/accel` | `geometry_msgs::msg::AccelWithCovarianceStamped` | estimated acceleration |

## Parameters

{{ json_to_markdown("localization/twist2accel/schema/twist2accel.schema.json") }}

## Future work

Future work includes integrating acceleration into the EKF state.
