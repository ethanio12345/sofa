cmake_minimum_required(VERSION 3.12)
project(SofaBaseCollision)

set(HEADER_FILES
    BaseContactMapper.h
    BaseIntTool.h
    BaseProximityIntersection.h
    BruteForceDetection.h
    CapsuleIntTool.h
    CapsuleIntTool.inl
    CapsuleModel.h
    CapsuleModel.inl
    ContactListener.h
    Cube.h
    CubeModel.h
    CylinderModel.h
    CylinderModel.inl
    DefaultContactManager.h
    DefaultPipeline.h
    DiscreteIntersection.h
    Intersector.h
    IntrCapsuleOBB.h
    IntrCapsuleOBB.inl
    IntrOBBOBB.h
    IntrOBBOBB.inl
    IntrSphereOBB.h
    IntrSphereOBB.inl
    IntrUtility3.h
    IntrUtility3.inl
    MinProximityIntersection.h
    NewProximityIntersection.h
    NewProximityIntersection.inl
    OBBIntTool.h
    OBBModel.h
    OBBModel.inl
    RigidCapsuleModel.h
    RigidCapsuleModel.inl
    Sphere.h
    SphereModel.h
    SphereModel.inl
    config.h
    initBaseCollision.h
)

set(SOURCE_FILES
    BaseContactMapper.cpp
    BaseIntTool.cpp
    BaseProximityIntersection.cpp
    BruteForceDetection.cpp
    CapsuleIntTool.cpp
    CapsuleModel.cpp
    ContactListener.cpp
    CubeModel.cpp
    CylinderModel.cpp
    DefaultContactManager.cpp
    DefaultPipeline.cpp
    DiscreteIntersection.cpp
    IntrCapsuleOBB.cpp
    IntrOBBOBB.cpp
    IntrSphereOBB.cpp
    IntrUtility3.cpp
    MinProximityIntersection.cpp
    NewProximityIntersection.cpp
    OBBIntTool.cpp
    OBBModel.cpp
    RigidCapsuleModel.cpp
    SphereModel.cpp
    initBaseCollision.cpp
)

add_library(${PROJECT_NAME} SHARED ${HEADER_FILES} ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} PUBLIC SofaCore SofaSimulationCommon)

sofa_add_targets_to_package(
    PACKAGE_NAME SofaBase
    TARGETS ${PROJECT_NAME} AUTO_SET_TARGET_PROPERTIES
    )
