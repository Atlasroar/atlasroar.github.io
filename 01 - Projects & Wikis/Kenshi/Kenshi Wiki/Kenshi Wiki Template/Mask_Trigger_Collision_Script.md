This page is part of the [](Building_making_tutorial.md), this data is mostly
redundant. The game actually does this automatically, every time the mod
is loaded to the game. So, you only need to do this IF you need some
other settings than default for the collision. This is the reason I do
not delete this page, as someone might need to change the flags, some
day.

NOTE NOTE NOTE This script only works with cube as the collision
starting primitive. If your exported xml says 'triangle' this will not
work. Unfortunately I could not find a vanilla collision script that was
made for triangles (or any other shape than a cube), so I do not know
what changes would need to be done to make the script work for non-cube
primitives.

## How to make a Mask Trigger Collision Script

1\) Crate a collision file normally for your mask trigger, move it to
your mod folder and then just edit with notepad++ or visual studio and
**copy the dimensions to a separate notepad**

2\) Replace the entirety of it with the code below.

3\) Replace "D:\Kenshi\mods\MyMod\buildings\FloorOneTrigger.xml" with
your mod's actual path and collision xml file name.

4\) Search for dimensions and replace the data on
<NxBoxShapeDesc dimensions="236.286682 236.286682 100.949497"/> with
your dimensions. If you have an off-center build, also replace the
global position with yours.

If you need to make an odd shaped mask, fe. a pyramid etc. export the
mesh as normal but create a collision box shape that encompasses the
building and export that as collision shape box. Opening that in an
editor (like notepad++ or visual studio) allows you to copy the
dimensions and global position. Do not adjust the collision shape in
this script.

``` abap

<NXUSTREAM2>
         <NxuPhysicsCollection id="D:\Kenshi\mods\MyMod\buildings\FloorOneTrigger.xml" nxuVersion="103" sdkVersion="284">
            <NxPhysicsSDKDesc id="SDK">
            <hwPageSize>65536</hwPageSize>
            <hwPageMax>256</hwPageMax>
            <hwConvexMax>2048</hwConvexMax>
        </NxPhysicsSDKDesc>
        <NxParameterDesc param="NX_PENALTY_FORCE" value="0.800000012"/>
        <NxParameterDesc param="NX_SKIN_WIDTH" value="0.100000001"/>
        <NxParameterDesc param="NX_DEFAULT_SLEEP_LIN_VEL_SQUARED" value="0.010000001"/>
        <NxParameterDesc param="NX_DEFAULT_SLEEP_ANG_VEL_SQUARED" value="0.010000001"/>
        <NxParameterDesc param="NX_BOUNCE_THRESHOLD" value="-200"/>
        <NxParameterDesc param="NX_DYN_FRICT_SCALING" value="1"/>
        <NxParameterDesc param="NX_STA_FRICT_SCALING" value="1"/>
        <NxParameterDesc param="NX_MAX_ANGULAR_VELOCITY" value="7"/>
        <NxParameterDesc param="NX_CONTINUOUS_CD" value="0"/>
        <NxParameterDesc param="NX_VISUALIZATION_SCALE" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_WORLD_AXES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_BODY_AXES" value="1"/>
        <NxParameterDesc param="NX_VISUALIZE_BODY_MASS_AXES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_BODY_LIN_VELOCITY" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_BODY_ANG_VELOCITY" value="0"/>
        <NxParameterDesc param="NX_DUMMY15" value="0"/>
        <NxParameterDesc param="NX_DUMMY16" value="0"/>
        <NxParameterDesc param="NX_DUMMY17" value="0"/>
        <NxParameterDesc param="NX_DUMMY18" value="0"/>
        <NxParameterDesc param="NX_DUMMY19" value="0"/>
        <NxParameterDesc param="NX_DUMMY20" value="0"/>
        <NxParameterDesc param="NX_DUMMY21" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_BODY_JOINT_GROUPS" value="0"/>
        <NxParameterDesc param="NX_DUMMY23" value="0"/>
        <NxParameterDesc param="NX_DUMMY24" value="0"/>
        <NxParameterDesc param="NX_DUMMY25" value="0"/>
        <NxParameterDesc param="NX_DUMMY26" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_JOINT_LOCAL_AXES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_JOINT_WORLD_AXES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_JOINT_LIMITS" value="0"/>
        <NxParameterDesc param="NX_DUMMY30" value="0"/>
        <NxParameterDesc param="NX_DUMMY31" value="0"/>
        <NxParameterDesc param="NX_DUMMY32" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CONTACT_POINT" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CONTACT_NORMAL" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CONTACT_ERROR" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CONTACT_FORCE" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_ACTOR_AXES" value="1"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_AABBS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_SHAPES" value="1"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_AXES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_COMPOUNDS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_VNORMALS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_FNORMALS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_EDGES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_SPHERES" value="0"/>
        <NxParameterDesc param="NX_DUMMY46" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_STATIC" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_DYNAMIC" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_FREE" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_CCD" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_COLLISION_SKELETONS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_EMITTERS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_POSITION" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_VELOCITY" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_KERNEL_RADIUS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_BOUNDS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_PACKETS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_MOTION_LIMIT" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_DYN_COLLISION" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_STC_COLLISION" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_MESH_PACKETS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_DRAINS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_MESH" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_COLLISIONS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_SELFCOLLISIONS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_WORKPACKETS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_SLEEP" value="0"/>
        <NxParameterDesc param="NX_ADAPTIVE_FORCE" value="1"/>
        <NxParameterDesc param="NX_COLL_VETO_JOINTED" value="1"/>
        <NxParameterDesc param="NX_TRIGGER_TRIGGER_CALLBACK" value="1"/>
        <NxParameterDesc param="NX_SELECT_HW_ALGO" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_ACTIVE_VERTICES" value="0"/>
        <NxParameterDesc param="NX_CCD_EPSILON" value="0.01"/>
        <NxParameterDesc param="NX_SOLVER_CONVERGENCE_THRESHOLD" value="0"/>
        <NxParameterDesc param="NX_BBOX_NOISE_LEVEL" value="0.001"/>
        <NxParameterDesc param="NX_IMPLICIT_SWEEP_CACHE_SIZE" value="5"/>
        <NxParameterDesc param="NX_DEFAULT_SLEEP_ENERGY" value="0.005"/>
        <NxParameterDesc param="NX_CONSTANT_FLUID_MAX_PACKETS" value="925"/>
        <NxParameterDesc param="NX_CONSTANT_FLUID_MAX_PARTICLES_PER_STEP" value="4096"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_TEARABLE_VERTICES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_TEARING" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_ATTACHMENT" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_MESH" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_COLLISIONS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_WORKPACKETS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_SLEEP" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_TEARABLE_VERTICES" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_TEARING" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_ATTACHMENT" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FLUID_PACKET_DATA" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_FORCE_FIELDS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_VALIDBOUNDS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_VALIDBOUNDS" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_SLEEP_VERTEX" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_SOFTBODY_SLEEP_VERTEX" value="0"/>
        <NxParameterDesc param="NX_ASYNCHRONOUS_MESH_CREATION" value="0"/>
        <NxParameterDesc param="NX_FORCE_FIELD_CUSTOM_KERNEL_EPSILON" value="0.001"/>
        <NxParameterDesc param="NX_IMPROVED_SPRING_SOLVER" value="1"/>
        <NxParameterDesc param="NX_FAST_MASSIVE_BP_VOLUME_DELETION" value="0"/>
        <NxParameterDesc param="NX_LEGACY_JOINT_DRIVE" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_HIERARCHY" value="0"/>
        <NxParameterDesc param="NX_VISUALIZE_CLOTH_HARD_STRETCHING_LIMITATION" value="0"/>
        <NxConvexMeshDesc id="ConvexMesh_0" userProperties="">
            <points></points>
            <triangles></triangles>
            <NxConvexFlags id="flags">
                <NX_CF_FLIPNORMALS>false</NX_CF_FLIPNORMALS>
                <NX_CF_16_BIT_INDICES>false</NX_CF_16_BIT_INDICES>
                <NX_CF_COMPUTE_CONVEX>false</NX_CF_COMPUTE_CONVEX>
                <NX_CF_INFLATE_CONVEX>false</NX_CF_INFLATE_CONVEX>
                <NX_CF_USE_UNCOMPRESSED_NORMALS>false</NX_CF_USE_UNCOMPRESSED_NORMALS>
            </NxConvexFlags>
            <cookedDataSize>892</cookedDataSize>
            <cookedData>
                4E5853014356584D030000000000000049434501434C484C00000000494345014356484C05000000080000000C0000000C000000060000001800000018000000
                40780042775295C14CFE5142EFE8FF41A038C542E4E45342977005C2FC38C542A3105542565113C251F495C1393A534202D7FE41585FC542C80B6B40A6E5FF41
                C25295C1B5108E404D5113C24DF495C15CB17E403E6E05C24860C542341E4F400700000000010200020304050604060703020703070605040105010000030600
                0605020104020407000013F601F60EF619F625F633F639F62EF6DAC2D5BF36961E42C8F0E241040000000000000000000000B9C6923BB09B84BBCEFE7F3FFDDD
                52C2C2FD2B40FDDD52420400000004000000080000000641DB3BAFE5D5BB23FD7FBFAA4F8340F88558C2AA4F83C004000000080000001000000061E37FBFA414
                F23C81A31CB5A20911C2BB9E02C2A2091142040000000C00000018000000B8FF7F3F6D46913A3CAF31BB59A2FFC10FF913C259A2FF4104000000100000002000
                0000D33C963AF6FF7FBF0E1F1DB4D39D95C1D473C5C2D39D9541040000001400000028000000D3959437EBFF7F3F9911C93A7662C5C216E995C17662C5420001
                020304050607030207060504010000030605020104070B00000000030501080A0B0905060B070804000201070A02030409060000000000000000000100030005
                0102010402030207030604050407050606079107960733F0840722F08D0F0AF03BF0B107A407B607AD0700000000000000000000000000000000020000000202
                020202020202020202021600000000020406080A0C0E101214160003000403040005030500020205020401030105010401024943450156414C45020000000800
                000024000000050000000504050405040504010203050600020405000103040700020607010205060700010406000304050702030406620000004F5043010100
                000003000000010000000180FF7FFF7FFF7FFF7F0080000000C000000000DEC9963874E49F3A4904623ADFE5893A32DFEA3A5020483A48424D01000000000200
                00006500000005650C0000000B000000000304060A0B0107080902054860C53770271EC0C6FD1F42709CE241BDA49042565113C251F495C1341E4F4040780042
                4860C542A3105542F988BC480398AB4EAE748F4BB8A6874BAE748F4B03ACFE4D5DFFCECDB8A6874B5DFFCECD0CBC8E4E77C5D2BF7AC31E4259EBE241
            </cookedData>
        </NxConvexMeshDesc>
        <NxSceneDesc id="Scene_0" userProperties="" hasMaxBounds="false" hasLimits="false" hasFilter="true">
            <filterBool>true</filterBool>
            <filterOp0>NX_FILTEROP_AND</filterOp0>
            <filterOp1>NX_FILTEROP_AND</filterOp1>
            <filterOp2>NX_FILTEROP_AND</filterOp2>
            <NxGroupsMask id="groupMask0" bits0="0" bits1="0" bits2="0" bits3="0"/>
            <NxGroupsMask id="groupMask1" bits0="0" bits1="0" bits2="0" bits3="0"/>
            <gravity>0 0 -981.000061035</gravity>
            <maxTimestep>0.016666668</maxTimestep>
            <maxIter>8</maxIter>
            <timeStepMethod>NX_TIMESTEP_FIXED</timeStepMethod>
            <maxBounds>0 0 0  FLT_MAX FLT_MAX FLT_MAX</maxBounds>
            <NxSceneLimits id="limits">
                <maxNbActors>0</maxNbActors>
                <maxNbBodies>0</maxNbBodies>
                <maxNbStaticShapes>0</maxNbStaticShapes>
                <maxNbDynamicShapes>0</maxNbDynamicShapes>
                <maxNbJoints>0</maxNbJoints>
            </NxSceneLimits>
            <simType>NX_SIMULATION_SW</simType>
            <groundPlane>false</groundPlane>
            <boundsPlanes>false</boundsPlanes>
            <NxSceneFlags id="flags">
                <NX_SF_DISABLE_SSE>false</NX_SF_DISABLE_SSE>
                <NX_SF_DISABLE_COLLISIONS>false</NX_SF_DISABLE_COLLISIONS>
                <NX_SF_SIMULATE_SEPARATE_THREAD>false</NX_SF_SIMULATE_SEPARATE_THREAD>
                <NX_SF_ENABLE_MULTITHREAD>false</NX_SF_ENABLE_MULTITHREAD>
                <NX_SF_ENABLE_ACTIVETRANSFORMS>false</NX_SF_ENABLE_ACTIVETRANSFORMS>
                <NX_SF_RESTRICTED_SCENE>false</NX_SF_RESTRICTED_SCENE>
                <NX_SF_DISABLE_SCENE_MUTEX>false</NX_SF_DISABLE_SCENE_MUTEX>
                <NX_SF_FORCE_CONE_FRICTION>false</NX_SF_FORCE_CONE_FRICTION>
                <NX_SF_SEQUENTIAL_PRIMARY>false</NX_SF_SEQUENTIAL_PRIMARY>
                <NX_SF_FLUID_PERFORMANCE_HINT>false</NX_SF_FLUID_PERFORMANCE_HINT>
            </NxSceneFlags>
            <internalThreadCount>0</internalThreadCount>
            <backgroundThreadCount>0</backgroundThreadCount>
            <threadMask>0</threadMask>
            <backgroundThreadMask>0</backgroundThreadMask>
            <simThreadStackSize>0</simThreadStackSize>
            <simThreadPriority>NX_TP_NORMAL</simThreadPriority>
            <simThreadMask>0</simThreadMask>
            <workerThreadStackSize>0</workerThreadStackSize>
            <workerThreadPriority>NX_TP_NORMAL</workerThreadPriority>
            <backgroundThreadPriority>NX_TP_NORMAL</backgroundThreadPriority>
            <upAxis>0</upAxis>
            <subdivisionLevel>5</subdivisionLevel>
            <staticStructure>NX_PRUNING_STATIC_AABB_TREE</staticStructure>
            <dynamicStructure>NX_PRUNING_NONE</dynamicStructure>
            <dynamicTreeRebuildRateHint>100</dynamicTreeRebuildRateHint>
            <bpType>NX_BP_TYPE_SAP_SINGLE</bpType>
            <nbGridCellsX>0</nbGridCellsX>
            <nbGridCellsY>0</nbGridCellsY>
            <solverBatchSize>32</solverBatchSize>
            <NxMaterialDesc id="Material_0" userProperties="" hasSpring="false" materialIndex="0">
                <dynamicFriction>0</dynamicFriction>
                <staticFriction>0</staticFriction>
                <restitution>0</restitution>
                <dynamicFrictionV>0</dynamicFrictionV>
                <staticFrictionV>0</staticFrictionV>
                <frictionCombineMode>NX_CM_AVERAGE</frictionCombineMode>
                <restitutionCombineMode>NX_CM_AVERAGE</restitutionCombineMode>
                <dirOfAnisotropy>0 0 0</dirOfAnisotropy>
                <NxMaterialFlag id="flags">
                    <NX_MF_ANISOTROPIC>false</NX_MF_ANISOTROPIC>
                    <NX_MF_DISABLE_FRICTION>false</NX_MF_DISABLE_FRICTION>
                    <NX_MF_DISABLE_STRONG_FRICTION>false</NX_MF_DISABLE_STRONG_FRICTION>
                </NxMaterialFlag>
            </NxMaterialDesc>
            <NxMaterialDesc id="Material_1" userProperties="" hasSpring="false" materialIndex="1">
                <dynamicFriction>0.300000012</dynamicFriction>
                <staticFriction>0.300000012</staticFriction>
                <restitution>0.5</restitution>
                <dynamicFrictionV>0</dynamicFrictionV>
                <staticFrictionV>0</staticFrictionV>
                <frictionCombineMode>NX_CM_AVERAGE</frictionCombineMode>
                <restitutionCombineMode>NX_CM_AVERAGE</restitutionCombineMode>
                <dirOfAnisotropy>1 0 0</dirOfAnisotropy>
                <NxMaterialFlag id="flags">
                    <NX_MF_ANISOTROPIC>false</NX_MF_ANISOTROPIC>
                    <NX_MF_DISABLE_FRICTION>false</NX_MF_DISABLE_FRICTION>
                    <NX_MF_DISABLE_STRONG_FRICTION>false</NX_MF_DISABLE_STRONG_FRICTION>
                </NxMaterialFlag>
            </NxMaterialDesc>
            <NxActorDesc id="Actor_0" userProperties="" hasBody="false" name="Cube.001">
                <globalPose>1.000000 0.000000 0.000000  0.000000 1.000000 0.000000  0.000000 0.000000 1.000000  0.000000 0.000000 0.000000</globalPose>
                <NxBoxShapeDesc dimensions="236.286682 236.286682 100.949497"/>

                <density>0</density>
                <NxActorFlag id="flags">
                    <NX_AF_DISABLE_COLLISION>false</NX_AF_DISABLE_COLLISION>
                    <NX_AF_DISABLE_RESPONSE>false</NX_AF_DISABLE_RESPONSE>
                    <NX_AF_LOCK_COM>false</NX_AF_LOCK_COM>
                    <NX_AF_FLUID_DISABLE_COLLISION>false</NX_AF_FLUID_DISABLE_COLLISION>
                    <NX_AF_CONTACT_MODIFICATION>false</NX_AF_CONTACT_MODIFICATION>
                    <NX_AF_FORCE_CONE_FRICTION>false</NX_AF_FORCE_CONE_FRICTION>
                    <NX_AF_USER_ACTOR_PAIR_FILTERING>false</NX_AF_USER_ACTOR_PAIR_FILTERING>
                </NxActorFlag>
                <group>0</group>
                <compartment></compartment>
                <NxConvexShapeDesc meshData="ConvexMesh_0">
                    <NxMeshShapeFlag id="meshFlags">
                        <NX_MESH_SMOOTH_SPHERE_COLLISIONS>false</NX_MESH_SMOOTH_SPHERE_COLLISIONS>
                        <NX_MESH_DOUBLE_SIDED>false</NX_MESH_DOUBLE_SIDED>
                    </NxMeshShapeFlag>
                    <NxShapeDesc userProperties="" name="Storm_Shack_INTERIOR_TRIGGER">
                        <localPose>1 0 0  0 1 0  0 0 1  0 0 0</localPose>
                        <NxShapeFlag id="shapeFlags">
                            <NX_TRIGGER_ON_ENTER>false</NX_TRIGGER_ON_ENTER>
                            <NX_TRIGGER_ON_LEAVE>false</NX_TRIGGER_ON_LEAVE>
                            <NX_TRIGGER_ON_STAY>false</NX_TRIGGER_ON_STAY>
                            <NX_SF_VISUALIZATION>true</NX_SF_VISUALIZATION>
                            <NX_SF_DISABLE_COLLISION>false</NX_SF_DISABLE_COLLISION>
                            <NX_SF_FEATURE_INDICES>false</NX_SF_FEATURE_INDICES>
                            <NX_SF_DISABLE_RAYCASTING>false</NX_SF_DISABLE_RAYCASTING>
                            <NX_SF_POINT_CONTACT_FORCE>true</NX_SF_POINT_CONTACT_FORCE>
                            <NX_SF_FLUID_DRAIN>false</NX_SF_FLUID_DRAIN>
                            <NX_SF_FLUID_DISABLE_COLLISION>false</NX_SF_FLUID_DISABLE_COLLISION>
                            <NX_SF_FLUID_TWOWAY>false</NX_SF_FLUID_TWOWAY>
                            <NX_SF_DISABLE_RESPONSE>false</NX_SF_DISABLE_RESPONSE>
                            <NX_SF_DYNAMIC_DYNAMIC_CCD>false</NX_SF_DYNAMIC_DYNAMIC_CCD>
                            <NX_SF_DISABLE_SCENE_QUERIES>false</NX_SF_DISABLE_SCENE_QUERIES>
                            <NX_SF_CLOTH_DRAIN>false</NX_SF_CLOTH_DRAIN>
                            <NX_SF_CLOTH_DISABLE_COLLISION>false</NX_SF_CLOTH_DISABLE_COLLISION>
                            <NX_SF_CLOTH_TWOWAY>true</NX_SF_CLOTH_TWOWAY>
                            <NX_SF_SOFTBODY_DRAIN>false</NX_SF_SOFTBODY_DRAIN>
                            <NX_SF_SOFTBODY_DISABLE_COLLISION>false</NX_SF_SOFTBODY_DISABLE_COLLISION>
                            <NX_SF_SOFTBODY_TWOWAY>true</NX_SF_SOFTBODY_TWOWAY>
                        </NxShapeFlag>
                        <group>0</group>
                        <materialIndex>1</materialIndex>
                        <CCDSkeleton></CCDSkeleton>
                        <shapeDensity>0</shapeDensity>
                        <shapeMass>190.227828979</shapeMass>
                        <skinWidth>0.100000001</skinWidth>
                        <NxGroupsMask id="groupsMask" bits0="1" bits1="0" bits2="1" bits3="0"/>
                        <NxShapeCompartmentType id="nonInteractingCompartmentTypes">
                            <NX_COMPARTMENT_SW_RIGIDBODY>false</NX_COMPARTMENT_SW_RIGIDBODY>
                            <NX_COMPARTMENT_HW_RIGIDBODY>false</NX_COMPARTMENT_HW_RIGIDBODY>
                            <NX_COMPARTMENT_SW_FLUID>false</NX_COMPARTMENT_SW_FLUID>
                            <NX_COMPARTMENT_HW_FLUID>false</NX_COMPARTMENT_HW_FLUID>
                            <NX_COMPARTMENT_SW_CLOTH>false</NX_COMPARTMENT_SW_CLOTH>
                            <NX_COMPARTMENT_HW_CLOTH>false</NX_COMPARTMENT_HW_CLOTH>
                            <NX_COMPARTMENT_SW_SOFTBODY>false</NX_COMPARTMENT_SW_SOFTBODY>
                            <NX_COMPARTMENT_HW_SOFTBODY>false</NX_COMPARTMENT_HW_SOFTBODY>
                        </NxShapeCompartmentType>
                    </NxShapeDesc>
                </NxConvexShapeDesc>
                <dominanceGroup>0</dominanceGroup>
                <contactReportFlags>0</contactReportFlags>
                <forceFieldMaterial>0</forceFieldMaterial>
            </NxActorDesc>
            <NxActorGroupPair group0="0" group1="0">
                <NxContactPairFlag id="flags">
                    <NX_IGNORE_PAIR>false</NX_IGNORE_PAIR>
                    <NX_NOTIFY_ON_START_TOUCH>true</NX_NOTIFY_ON_START_TOUCH>
                    <NX_NOTIFY_ON_END_TOUCH>true</NX_NOTIFY_ON_END_TOUCH>
                    <NX_NOTIFY_ON_TOUCH>true</NX_NOTIFY_ON_TOUCH>
                    <NX_NOTIFY_ON_IMPACT>false</NX_NOTIFY_ON_IMPACT>
                    <NX_NOTIFY_ON_ROLL>false</NX_NOTIFY_ON_ROLL>
                    <NX_NOTIFY_ON_SLIDE>false</NX_NOTIFY_ON_SLIDE>
                    <NX_NOTIFY_FORCES>false</NX_NOTIFY_FORCES>
                    <NX_NOTIFY_ON_START_TOUCH_FORCE_THRESHOLD>false</NX_NOTIFY_ON_START_TOUCH_FORCE_THRESHOLD>
                    <NX_NOTIFY_ON_END_TOUCH_FORCE_THRESHOLD>false</NX_NOTIFY_ON_END_TOUCH_FORCE_THRESHOLD>
                    <NX_NOTIFY_ON_TOUCH_FORCE_THRESHOLD>false</NX_NOTIFY_ON_TOUCH_FORCE_THRESHOLD>
                </NxContactPairFlag>
            </NxActorGroupPair>
        </NxSceneDesc>
    </NxuPhysicsCollection>
</NXUSTREAM2>
```

[Category:Modding](Category:Modding "wikilink")