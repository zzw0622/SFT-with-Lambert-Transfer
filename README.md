Overview
This project implements Sims-Flanagan Transcription (SFT) to optimize low-thrust inter-asteroid transfers. The goal is to refine Lambert transfer trajectories by discretizing them 
into impulse-like thrust segments while minimizing delta-v and ensuring trajectory feasibility.

Features
Computes an initial impulsive transfer using SPICE ephemerides and grid search
Simulates forward and backward trajectories under two-body dynamics
Uses MATLAB’s fmincon to iteratively adjust thrust inputs, maximizing final spacecraft mass
Approximates continuous low-thrust propulsion with discretized impulses
Ensures smooth transitions between forward and backward propagated paths
Plots optimized trajectories, thrust application points, and asteroid orbits

Workflow
Load SPICE kernels and define spacecraft and mission parameters
Solve Lambert’s problem to find baseline delta-v optimal trajectory
Estimate initial thrust direction based on Lambert solution
Perform forward and backward trajectory propagation
Apply thrust impulses at fixed intervals and optimize with fmincon to refine thrust allocation
Generate 3D plots of the trajectory, highlighting thrust applications
