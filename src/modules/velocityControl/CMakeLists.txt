# Copyright (C) 2008 RobotCub Consortium
# Author: Lorenzo Natale
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

SET(PROJECTNAME velocityControl)

PROJECT(${PROJECTNAME})

SET(folder_source main.cpp
                  velControlThread.cpp)

SET(folder_header velControlThread.h)

SOURCE_GROUP("Source Files" FILES ${folder_source})
SOURCE_GROUP("Header Files" FILES ${folder_header})

ADD_EXECUTABLE(${PROJECTNAME} ${folder_source} ${folder_header})

TARGET_LINK_LIBRARIES(${PROJECTNAME} ${YARP_LIBRARIES})

INSTALL(TARGETS ${PROJECTNAME} DESTINATION bin)



