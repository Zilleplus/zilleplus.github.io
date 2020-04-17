# Nmpc-codegen 

github.com/kul-forbes/nmpc-codegen

## The PANOC algorithm
Researches at the ku-leuven created at algorithm to solve constraint non-linear optimization problems. The algorithm uses less memory then the typical algorithms that are used to solve non-linear optimal control problems. 

## nmpc-codegen libary
nmpc-codgen is a python/Matlab library that has the capability to generate control systems that use PANOC to solve the optimal control problem. The user provides the behavior of the system with its constraints. And nmpc-codegen will generate a complete controller in C90 code. This allows academic's to generate very fast controllers, without ever needing to know how to implement them at a low level. The tool uses the casadi library to do the backward differentiation. It allows simulatins by compiling the generated C code fully automatic via CMake en Gcc/clang/msvc/intelCompiler. Because the result is an highly optimized binary, this is faster then any other tool I could find. And obviously makes for some interesting papers.

An other researcher used this library to create DC converters, you can find her code here: github.com/kul-forbes/dc_dc_simulator (paper 3 and 4)

## Papers (not writting by me, but the libary they use is nmpc-codegen)
1) Small E., Sopasakis E., Fresk E., Patrinos P., Nikolakopoulos G., "Aerial navigation in obstructed environments with embedded nonlinear model predictive control", in Proc. of the 2019 18th European Control Conference, Napoli, Italy, Jun. 2019, pp. 3556-3563. 

2) Katriniok A., Sopasakis P., Schuurmans M., Patrinos P., "Nonlinear Model Predictive Control for Distributed Motion Planning in Road Intersections Using PANOC", in 2019 IEEE Conference on Decision and Control (CDC), Nice, France, Dec. 2019, pp. 5272-5278.

3) A. Lekić, 2017. Simulation of PWM DC-DC converters using eigenvalues and eigenvectors. Journal of Electrical Engineering, 68(1), pp.13-22.

4) A. Lekić, 2014, Automated DC-DC converters symbolic state-space model generation by the use of free software, In Proceedings of the 22nd Telecommunications Forum Telfor (TELFOR), 2014, pp. 995-998.
