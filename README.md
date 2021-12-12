Why: https://news.ycombinator.com/edit?id=29531029

First, run the provisioning script to get Visual Studio.
Get something to drink, call your mom, etc. while it does its job.

Then, launch a developer powershell and follow along:


```
PS L:\src\hello> mkdir build


    Directory: L:\src\hello


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----       12/12/2021   6:59 PM                build


PS L:\src\hello> cd .\build
PS L:\src\hello\build> cmake -G Ninja ..
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 2.8.12 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- The C compiler identification is MSVC 19.29.30040.0
-- The CXX compiler identification is MSVC 19.29.30040.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: C:/Program Files (x86)/Microsoft Visual Studio/
2019/Community/VC/Tools/MSVC/14.29.30037/bin/Hostx86/x86/cl.exe - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: C:/Program Files (x86)/Microsoft Visual Studi
o/2019/Community/VC/Tools/MSVC/14.29.30037/bin/Hostx86/x86/cl.exe - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: L:/src/hello/build
PS L:\src\hello\build> ninja
[0/1] Re-running CMake...
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 2.8.12 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done
-- Generating done
-- Build files have been written to: L:/src/hello/build
[1/1] Linking CXX executable app.exe
PS L:\src\hello> echo build > .gitignore
PS L:\src\hello> git add .\main.cpp .\CMakeLists.txt
PS L:\src\hello> git commit -m "hello world!"
PS L:\src\hello> git remote add origin git@github.com:plq/hello-win32
PS L:\src\hello> git push --set-upstream origin master
```
