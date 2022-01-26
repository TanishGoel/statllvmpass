# statllvmpass
An LLVM Pass that keeps track of all functions, basic blocks and instructions in a program.

The program should work although I couldn't exactly figure out how to exactly do the 2nd part of the assignment. To run the code, make a subdirectory, say, lib/transforms/llvmpass1 in the LLVM directory and write the following in the CMakeLists.txt file in lib/transforms:
<code>add_llvm_library(
  statllvmpass.cpp

  PLUGIN_TOOL
  opt
  )</code>
  <code>add_subdirectory(llvmpass1)</code>
  Compile the pass file with gmake to get so file.
  Compile the program you want to analyse with the command:
  <code>clang -c -emit-llvm program.c</code>
  and finally run, <code>opt -load statllvmpass.so program.bc >/dev/null</code>
  
