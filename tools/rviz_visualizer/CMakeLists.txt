# Copyright (c) 2017, United States Government, as represented by the
# Administrator of the National Aeronautics and Space Administration.
# 
# All rights reserved.
# 
# The Astrobee platform is licensed under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with the
# License. You may obtain a copy of the License at
# 
#     http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
# License for the specific language governing permissions and limitations
# under the License.

project(rviz_visualizer)

catkin_package(
  CATKIN_DEPENDS roscpp visualization_msgs
)

create_tool_targets(DIR tools
  LIBS ${catkin_LIBRARIES} msg_conversions common config_reader
  INC ${catkin_INCLUDE_DIRS}
)

install_launch_files()