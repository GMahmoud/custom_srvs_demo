cmake_minimum_required(VERSION 2.8.3)
project(custom_srvs)

find_package(catkin REQUIRED COMPONENTS message_generation custom_msgs)

add_service_files(FILES
                  akinator/AkinatorStart.srv
                  akinator/AkinatorAnswer.srv
                  akinator/AkinatorResult.srv
                  behaviours/BehaviourList.srv
                  behaviours/HeadBehaviourCmd.srv
                  behaviours/LedBehaviourCmd.srv
                  tts/TTSCmd.srv
                  stt/STTCmd.srv
                  supervisor/AppCmdList.srv
                  supervisor/RunCmd.srv
                  supervisor/AppList.srv
                  supervisor/ServiceList.srv
                  supervisor/ProcessList.srv
                  supervisor/GetApp.srv
                  supervisor/GetServices.srv
                  supervisor/GetProcesses.srv
                  supervisor/StartApp.srv
                  supervisor/StopApp.srv
                  supervisor/StartService.srv
                  supervisor/StopService.srv
                  supervisor/SetProcessParam.srv
                  process/SetParam.srv
                  control/HeadCmd.srv
                  console/Logger.srv
                  monitoring/SystemInfo.srv
                  state_machine/GetState.srv
                  state_machine/Transition.srv
                  socket/ConnectIO.srv
                  socket/StateIO.srv)

generate_messages(DEPENDENCIES custom_msgs)

catkin_package(CATKIN_DEPENDS message_runtime custom_msgs)

include_directories(${catkin_INCLUDE_DIRS})
