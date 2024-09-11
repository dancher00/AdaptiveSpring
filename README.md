# AdaptiveSpring

This repo contains code and other supplementary materials for the paper **Optimizing energy consumption for legged robot in cyclic tasks by
adapting equilibrium position and stiffness of a parallel torsion spring** submitted to IEEE ROBIO 2024 Conference.

In this work, we propose a novel adaptive compliance mechanism that utilizes a torsion spring with a variable equilibrium position. This mechanism is designed to optimize energy consumption by adjusting the spring’s influence on the robot’s leg based on real-time load conditions. The adaptive mechanism has been integrated into the knee joint of a quadrupedal robot leg with three degrees of freedom, providing a dynamic response to changing terrains and tasks.

![Testing setup](https://github.com/dancher00/AdaptiveSpring/blob/main/stand.jpg)

File `energy.ipynb` consists general formulation of energy consumption of the knee motor of robotic leg with and without torsion spring, and equation for optimal equilibrium position.

`Simulation/Adaptive_spring_ws.zip` is ROS workspace with implementation of robotic leg with torsion spring parallel to knee joint in Gazebo simulator. 

Your can find our experimental results and it's analysis in `Simulation/results.zip` archive. Experimantal setup and methodology are described in our paper.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

Sumilation was tested on ROS Noetic Ubuntu 20.04 with Python 3.8.

### Installation

1. Download and unpack `Simulation/Adaptive_spring_ws.zip` archive with simulation workspace.
2. Source your ROS distro.
3. Build the workspace:
```sh
cd Adaptive_spring_ws
catkin_make
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

1. In first terminal:
```sh
cd Adaptive_spring_ws
source devel/setup.bash
roslaunch leg_utils controller.launch
```
2. In second terminal:
```sh
cd Adaptive_spring_ws
source devel/setup.bash
rosrun leg_controller start_control.py
```

After few seconds 'Saved' message will be printed, .csv file with knee torques, angles and hip position will be saved in the root of workspace.

To configure parameters of the spring:
```sh
cd Adaptive_spring_ws/src/standurdf_description/urdf
```
In file standurdf.gazebo you can edit knee_joint_torsional_spring plugin to change spring stiffness and twist angle.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Our previous paper on this robotic leg](https://arxiv.org/abs/2407.15622)
* [Plugin to add a torsional spring to your robot in Gazebo](https://github.com/aminsung/gazebo_joint_torsional_spring_plugin)


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
