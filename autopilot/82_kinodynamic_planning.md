---
title: kinodynamic_motion_planning
categories: motion planning
tags: kinodynamic
date: 2023-02-04
---  

- [bench-mr](https://github.com/robot-motion/bench-mr)
- [chomp-multigrid](https://github.com/eric-heiden/chomp-multigrid/tree/4cd8abef27e51204a0cdd2b3ce411b88eee411c0)
https://github.com/sailist/Awesome-Paper-List-py/blob/master/pdfs/sync-bypy.py
## ref

- blog
    - [MOTION PLANNING](http://motion.cs.illinois.edu/RoboticSystems/PlanningWithDynamicsAndUncertainty.html)
- paper
    - [2022 db-A*: Discontinuity-bounded Search for Kinodynamic Mobile Robot Motion Planning](https://arxiv.org/abs/2203.11108)
    - [2017-A tutorial on newton methods for constrained trajectory optimization and relations to slam, gaussian process smoothing, optimal control, and probabilistic inference](https://argmin.lis.tu-berlin.de/papers/17-toussaint-Newton.pdf)
    - [2008-kpiece:Kinodynamic Motion Planning by Interior-Exterior Cell Exploration](https://ioan.sucan.ro/files/pubs/wafr2008.pdf)

    
- book
    - [Robotic Systems](https://motion.cs.illinois.edu/RoboticSystems/)
- library
    - * Search-based: ARA* (using SBPL http://www.sbpl.net/)
    - * Sampling-based: SST* (using OMPL https://ompl.kavrakilab.org/)
    - * Optimization-based: KOMO(K-Order Markov Optimization) (using RAI https://github.com/MarcToussaint/rai)
        - [doc](https://github.com/MarcToussaint/rai/wiki)
    - * [Hybrid: db-A*](https://github.com/IMRCLab/kinodynamic-motion-planning-benchmark)