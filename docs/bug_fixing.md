# Repository Bug Fixes & Resolved Issues

This document tracks all bugs, syntax errors, and build issues resolved in [`SubhamC07/level01_ros_assignment`](http://github.com/SubhamC07/level01_ros_assignment).

---

## 1. Syntax Error in `testbed_description/CMakeLists.txt`

### **Issue**
Building the `testbed_description` package fails during the CMake configuration step due to a syntax error on the final line of `CMakeLists.txt`.

* **Error Message / Cause:** CMake syntax error caused by missing function invocation parentheses on `ament_package`.

### **Root Cause**
The macros/functions in CMake require parentheses even if no arguments are passed. The file ended with:
`ament_package`

### **Fix**
Updated the last line of `testbed_description/CMakeLists.txt` to properly invoke the `ament_package()` function: `ament_package` to `ament_package()`

