cmake_minimum_required(VERSION 2.8.3)
project(custom_srvs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  custom_msgs
)

add_service_files(
   FILES
   akinator/AkinatorStart.srv
   akinator/AkinatorAnswer.srv
   akinator/AkinatorResult.srv
   launcher/StartCmd.srv
   launcher/StopCmd.srv
   tts/TTSCmd.srv
   stt/STTCmd.srv
   supervisor/AppCmdList.srv
   supervisor/RunCmd.srv
   supervisor/AppList.srv
   supervisor/GetApp.srv
   supervisor/StartApp.srv
   supervisor/StopApp.srv
   supervisor/StartService.srv
   supervisor/StopService.srv
   supervisor/SetProcessParam.srv
   process/SetParam.srv
)

generate_messages(
  DEPENDENCIES
  custom_msgs
)

catkin_package(
 	CATKIN_DEPENDS message_runtime custom_msgs
 )

include_directories(
  ${catkin_INCLUDE_DIRS}
)
