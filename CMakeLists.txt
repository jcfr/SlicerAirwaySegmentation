cmake_minimum_required(VERSION 2.8.9)

project(AirwaySegmentation)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/Slicer/SlicerAirwaySegmentation")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Pietro Nardelli (University College Cork), Andras Lasso (PerkLab, Queen's University)")
set(EXTENSION_DESCRIPTION "Automated airway segmentation in chest CT images")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/Slicer/SlicerAirwaySegmentation/master/AirwaySegmentation-ICON.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/Slicer/SlicerAirwaySegmentation/master/Screenshot01.jpg")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(AirwaySegmentationCLI)
add_subdirectory(AirwaySegmentation)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
