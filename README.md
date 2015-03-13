# Course Simulation Project -- Inverted Pendulum with Fuzzy Controller

In this project, a inverted pendulum system controled by a simple fuzzy controller is simulated in the Matlab environment. The main refereence is the book "*Fuzzy Control*" [1]. The main purpose is to evaluate effects of different parameters. There are three types of files: supported functions, simulation functions and simulation results.

# Supported Functions

1. Model of the inverted pendulum system `InvertedPendulum.m`: Calculate the current enviroment values based on values of previous time step;
2. Fourth order Runge Kutta method `ODE_RK.m`: Solve the ODE by using the fourth order Runge Kutta method. It is used in the `InvertedPendulum.m`;
3. Fuzzy Controller `FuzzyController.m`: Based on the user's settings and measured values to calculate the force which will transferred to the inverted pendulum system. It is only contains two inputs and one outputs. One input is the angle error. Another input is the angle speed error. The output is the force.

# Simulation Functions

1. `test_membershipfunction.m`: Plot the membership functions based on the user's settings. Example results are `e_membershipfunction.pdf`, `de_membershipfunction.pdf` and `F_membershipfunction.pdf`;
2. `test_InvertedPendulum_without_controller.m`: Test the model of the inverted pendulum. No control is performed. Example results are `without_control_1.pdf` and `without_control_2.pdf`;
3. `test_InvertedPendulum_with_fuzzy_controller.m`: Simulate the fuzzy control process of the inverted pendulum. Example results are `force_**.pdf` and `angleandposition_**.pdf`.

# Simulation Results

There are some example simulation results in the folder `Simulation_Results`. These example all follows the section "2.4 Simple Desgin Example: The Inverted Pendulum" of [1].

## Reference

[1] K. M. Passion and S. Yurkovich, *Fuzzy Cntrol*. Menlo Park, CA: Addison-Wesley, 1998.