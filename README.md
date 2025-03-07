# ROS 2 Driver Repository

Before using this repository, make sure to download and set up the YDLidar SDK:

### 1. Download and Install YDLidar SDK
```bash
git clone https://github.com/KarthikeshJG/YDLidar-SDK.git
cd YDLidar-SDK
mkdir build && cd build
cmake ..
make
sudo make install
```

This SDK is required for proper communication with the YDLidar.

## Prerequisites

Ensure you have the following installed:
- ROS 2 (Humble, Iron, or appropriate distribution)
- Colcon build tool
- Git

## Installation

### 1. Set Up Your ROS 2 Workspace
```bash
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
```

### 2. Clone the Required Repositories
```bash
git clone <your-repo-url>
git clone https://github.com/KarthikeshJG/ydlidar_ros2_driver.git
```

### 3. Build the Workspace
```bash
cd ~/ros2_ws
colcon build --symlink-install
```

### 4. Source the Workspace
```bash
source install/setup.bash
```

## Running the Driver

### Launch the YDLidar Driver
```bash
ros2 launch ydlidar_ros2_driver ydlidar_launch_view.py
```

This will start the YDLidar ROS 2 driver and allow you to visualize the LiDAR data.

## Additional Notes
- Ensure the LiDAR device is properly connected before launching.
- If running on a different ROS 2 distribution, modify the setup commands accordingly.
- Use `colcon build --symlink-install --event-handlers console_cohesion+` for better logging.

For any issues, check the respective repositories' documentation or raise an issue on GitHub.

