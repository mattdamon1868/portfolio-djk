
#### Note: for projects and work experience everything is ordered from present to past


## Education
1) San Diego State Univerity
   - Master of Science, Mechanical Engineering, Emphasis robotics, control, autonomous systems
   - August 2021 -> May 2024
   
2) California state university, Chico
   - Bachelor of science (BS), Mecatronics, Robotics and Automation Engineering
   - August 2013 -> May 2018

## Work Experience
1) San Diego State University
   
   - Graduate Research Assistant III:
   At the DSIM Lab, I collaborated with a research team dedicated to pursuing novel control theory approaches for autonomous systems, particularly focusing on the development of smart autonomous mobile robots. My role involved contributing to cutting-edge projects that push the boundaries of autonomous system capabilities. I led the development of an adaptive control approach extremum seeking control (ESC) implemented in ROS2 for mobile robots motion. The robot has no knowledge of its environment but with the real-time continuous optimization method the robot is able to perturb it's motion towards the source(designated by the designer, i.e. acoustic signal). This project demonstrated the practical application of advanced control theories in real-world robotic systems. This project compared previous methods with our novel design showcasing its superiority in efficiently reaching some optimal point(position unknown). Our method changed the movement of the sensor atop the robot therefore giving the system a wider search portfolio to locate the optimum point. This innovative approach employed information from a sensor to locate the source of the sound, or light in a room showcasing the potential of ESC in improving . My contributions have been pivotal in advancing the lab's research and development in smart robotics and control systems.
   - Teaching Assistant:
   As a Teaching Assistant for System Modeling and Robotics Control at SDSU, I was responsible for grading and evaluating student assignments and exams, ensuring fair assessment and providing constructive feedback to promote student learning. I collaborated closely with the course instructor to develop teaching materials and exercises that aligned with the curriculum, thereby enhancing the overall learning experience. Additionally, I acted as a liaison between students and faculty, advocating for student needs and contributing to the continuous improvement of course content and delivery. Systems Modeling and Analysis (Spring '24): Assisted in teaching an introductory course on control systems, focusing on system-level lumped parameter modeling of dynamic systems using first principles. Helped students understand and predict the performance of engineered systems based on their dynamic response prediction, and implement feedback control to achieve closed-loop stability and specified system performance. Robot Modeling Control (Fall '23): I served as a TA for a Robotic Model Control course, which focused on the design and implementation of control systems for robotics. The curriculum explored both forward and inverse kinematics, dynamics, sensor integration, and actuator control. In my role, I supported students through hands-on labs and projects, guiding them in using tools like MATLAB and ROS to model, and simulate robotic behaviors.

2) Course Designer
   
   - As a freelance Course Designer for The Construct, I was responsible for optimizing and debugging ROS2 and Gazebo simulation environments to create an engaging and intuitive learning experience for students. This involved aligning the simulations with students’ learning curves, ensuring the environments were both challenging and approachable. By fine-tuning these platforms, I enabled students to explore robotics concepts while building confidence in their skills. One of my key contributions was designing and implementing an image recognition system for a simulated security robot. Using convolutional neural networks (CNNs), I developed a framework that allowed the robot to identify and classify various objects within a virtual environment. This project involved leveraging ROS2 for communication between the robot’s perception and decision-making systems and using Gazebo to create a realistic testing area for students. This hands-on setup not only demonstrated the synergy between computer vision and robotics but also provided a practical, scalable approach for students to experiment with deep learning in a robotics context. In addition, I engineered a framework that integrated computer vision techniques and neural networks, focusing on their real-world applications in robotic perception and decision-making. By guiding students through the process of designing, implementing, and testing CNNs in a robotics environment, the course enabled them to develop both theoretical understanding and practical skills. This blend of robotics and AI helps students gain a strong foundation for tackling challenges in autonomous systems and intelligent automation.
   - Skills: python, programming, computer vision, deep learning, ROS2
  
   
3) Field Engineer II
   
   - As a Field Engineer II at Honeywell Process Solutions in San Bruno from April 2019 to March 2022, I served as the principal technical expert on HVAC systems, with a focus on the integration and maintenance of commercial Fire Alarm, Security, and Access Control Systems. My role involved spearheading the troubleshooting and resolution of startup issues, where I employed advanced diagnostic skills to ensure optimal equipment performance and reliability. I was pivotal in developing and programming building management controls using Honeywell software, which significantly improved the operational efficiency of buildings. This involved not only designing solutions that met client needs but also implementing them effectively to achieve measurable enhancements in system performance. Additionally, I led instructional sessions for subcontractors on electrical and mechanical system installations, fostering a culture of knowledge sharing and collaboration. Mentoring junior field service representatives was another key aspect of my role. I provided guidance and training in technical skills, customer service, and troubleshooting techniques, ensuring that the team was well-equipped to handle complex challenges. This mentorship not only improved team performance but also contributed to the professional growth of the individuals I worked with. My tenure at Honeywell Process Solutions was marked by a commitment to excellence, continuous improvement, and a dedication to fostering a collaborative and knowledgeable work environment.
      
   <img align="left" width="200" height="250" src="./images/control_panel.png">
   
   <img align="right"  width="250" height="200" src="./images/honeywel-controller.png">
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />

## Projects

1) Thesis project

- My master's project involves experimenting with various control theories applied to robots and autonomous systems. Our lab was particularly interested in extremum seeking control (ESC), an adaptive control approach extensively researched to expand its theoretical foundations. However, our focus was primarily on implementing these methods on real robots and conducting simulations. 
The robot used for my project was a TurtleBot3 from Robotis. It is a nonholonomic robot, capable of moving forward along the x-axis and rotating around the z-axis (angular velocity). Its modular design allowed me to make custom adjustments, such as adding an extra servo motor for a rotating sensor. This sensor moves back and forth to estimate the location of a signal source; in our case, we used light and sound as scalar signals. 
Using this estimation, local exploration based on the servo's motion allows the calculation of the derivative of the signal, which perturbs the vehicle's movement toward the source. The signals can be based on derivatives of arbitrary order, using periodic or near-periodic signals. These signals enable the average derivative estimates to converge to the true derivatives of the cost functions, provided they are sufficiently smooth (m-times differentiable). 
The robot does not have prior knowledge of the exact source location; it only receives gradient estimates derived from the sensor data. These estimates help the vehicle move toward the source by approximating the true derivative of the signal. Convergence, in this context, means that the vehicle is able to approach within approximately 0.5 meters of the source. 
This project involved applying hardware, software, and mechanical engineering skills to achieve the final design. The project comprised three main components: theoretical research and analysis, environment simulation for testing the theory, and physical robot construction for real-world testing. 
For the research analysis, I reviewed numerous papers on the application of ESC theory to nonholonomic robots and replicated prior work in Python to deepen understanding. This process led to the implementation of the theory within a Gazebo simulation using ROS2. This setup allowed for testing and tuning system parameters to optimize performance within the robot's speed constraints and to validate the theory's effectiveness.
The ROS2 packages were organized into distinct nodes, including vehicle state and sensor frame state nodes, a cost function update node, a derivatives estimation or filter node, a command controller node, a velocity command node, and a sensor feedback node. This modular design facilitated easier collaboration and updates by other researchers.
After successfully implementing and verifying the theory within the simulation, I proceeded to the physical robot. Additional components were designed, including a top layer and a rotating arm attached to a servo motor to hold testing sensors. These parts were modeled using ONshape (similar to SolidWorks) and fabricated with a Bambu H2S 3D printer, allowing the rotating arm to be attached to the servo.
The robot is equipped with wheel motors, a Raspberry Pi 4 as the control unit, and sensors including a microphone (for sound level measurement in dBA) and a photoresistor (for light resistance measurement). The software architecture mirrors that of the simulation but was adapted to incorporate real acoustic and light sources, replacing virtual representations.
The software modules include vehicle state nodes, filter nodes, control nodes, vehicle velocity nodes, and sensor feedback nodes (for encoders, microphone, and photoresistor). Using the parameters tuned in simulation, we successfully demonstrated that the robot could converge to the source based on both light and sound detection in real-world testing.
- Skills: Git, python, c++, autonomous systems, adaptive control, optimization, robotics, ROS2, leadership

<img align="left" width="200" height="250" src="./images/light-source.png">

<img align="right" width="200" height="250" src="./images/rotating-frame.png">
<br />
<br />

[![Watch the video](https://github.com/mattdamon1868/portfolio-djk/blob/main/images/tb3_thmb.png)](https://www.youtube.com/watch?v=K2YwE-z4ytc)

<br />
<br />
<br />
<br />
<br />
<br />



2) Optimization Path Planning project:

   -  This project involved formulating an optimization problem to select and justify the use of an optimal control approach. Although it was initially designed for a second-order system, the focus was primarily on applying first-order techniques within optimal control theory. The methodology centered on optimizing path planning for autonomous robots by utilizing duality principles and the simplex method within a linear programming framework. 
The objective function was designed to incorporate factors such as energy consumption, weight, distance to the source, and obstacle probability, each assigned arbitrary weightings to evaluate the most efficient cost value. To clarify the project's purpose, no physical dynamics or implementation were included; instead, the goal was to deepen understanding of linear programming techniques. 
The original nonlinear problem was simplified into a linear form to enable analysis using methods covered in this course, mainly focusing on the simplex method and the duality principle. The simplex method facilitates progression from one vertex of the feasible region to another, ensuring each step approaches the optimal solution. The duality principle involves deriving a dual problem from the primal by forming the Lagrangian with multipliers, adding these to the objective function, and solving for primal and dual variables simultaneously.
The revised objective function seeks to minimize the cost function considering the dual variables, which are constrained to be nonnegative. Utilizing these two techniques, we obtained results that minimized the cost, with the primary aim of testing different methods rather than identifying the absolute optimal gain values, which was outside the scope of this project.
     $$J(x) = \alpha x_1 + \beta x_2 + \gamma x_3 + \delta x_4 $$
where we have \(x_1\) representing energy, \(x_2\) the weight of the robot, \(x_3\) the distance provided as a function for the primary path with the adjusted path including a penalty (gain) for each factor, and finally, \(x_4\) indicating the likelihood of an obstacle present in the robot's path. Using this equation, we can apply the simplex method with the Gurobi optimization library to systematically identify the optimal path within the feasible region defined by these constraints, ultimately progressing toward an optimal solution.
   -  Skills used for the project: Optimiztion, duality, python, gurobi optimizer library

3) Autonomous systems CNNs how bad weather affects the safety of autonomous driving

   - The research paper on improving detection and prediction of noisy environments using deep learning and computer vision. Autonomous vehicles use different types of sensors to interpret their environments there is a controversial debate about how many sensors are actually needed for the vehicle to safely transport passengers to there destinations without any need for human intervention. Level 5 autonomy is seemly more achievable but can it be done with minimal sensors which would reduce cost for each unit (vehicle) produced to be autonomous? I explored the current research being done on to analyze the challenges computer vision and camera have been if bad weather is encountered. We focus on camera sensor and the difficulties that can happen rendering the vehicle unsafe potentially for passengers. Convolutional neural networks are integrated with recurrent nueral networks (RNN) to classify the sort of adverse weather conditions present in the surroundings, and these deep neural networks are used to extract visual characteristics from video frames.  We analyzed three different designs that are currently being used to research computer vision and weather, using deeep neural networks with algorithms such as YOLO, GRAMME, ReViewNet. Each method performs different defuzzing of images and eliminates false edge detection to assis the vehicle and understanding how to help with ensuring it can see in front of itself. The research studied rain, snow, hail and fog along with a couple of weather environments from this we were able to determine that the snow and fog were very challenging for the camera to identify objects where the precision went down by more than 20% for each of the methods.  Even with all the others they average around 50% precision which is less than ideal for the autonoumous vehicle. when the images get obscured it makes it very hard for the algorithm to enable the vechile to react if it cannot perceive its environment properly. we also know that the learning algorithms are realiant on the data and all th reseraach we found was using differnet data sets which makes it hard to make a true comparison. The more data you have the better but ths can also
   - Skills: Research, technical writing, deep learning, computer vision, autonomous vehicles 

4) Undergrad project robot pet waste collector
- The pet waste collection robot was designed to autonomously navigate a customer's yard, identify pet waste, and efficiently collect and dispose of it. As a team of four seniors with limited experience in computer vision and autonomous navigation, this project presented significant challenges; however, it allowed us to develop our problem-solving skills and quickly acquire new technical knowledge. 
Our primary focus was on developing the pickup mechanism and the computer vision algorithm for waste identification. We engineered a novel pickup system utilizing a 3D-printed "spike" puck that effectively punctures the waste and deposits it into an onboard waste container. The computer vision component employed a convolutional neural network trained on approximately 10,000 images of pet waste, achieving an accuracy of around 89% in correct identification.
- Skills: teamwork, CAD, coding, python, CNN, computer vision, fabrication, electronics, debugging

<img align="right" width="200" height="250" src="./images/pet_robot.jpeg">
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />


### Publications

<a id="1">[1]</a> 
James-Kavanaugh D., McNamee P. (2025). 
Servos for Local Map Exploration Onboard Nonholonmic Vehicles for Extremum Seeking
published to the IEEE controls systems and transactions journal. 
IEEE Transactions and Control Systems.
   
**Abstract:**

*Extremum seeking control (ESC) often employs perturbation-based estimates of derivatives for some  sensor field or cost function. These estimates are generally obtained by simply multiplying the output of a single-unit sensor by some time-varying function. Previous work has focused on sinusoidal perturbations to generate derivative estimates with results for arbitrary order derivatives of scalar maps or higher order derivatives of multivariable maps.  This work extends the perturbations from sinusoidal to bounded periodic or almost periodic functions and considers multivariable maps. A necessary and sufficient condition is given for determining if time-varying functions exist for estimating arbitrary order derivatives of multivariable maps for any given bounded periodic or almost periodic dither signal. These results are then used in a source seeking controller for a nonholonomic vehicle with a sensor actuated by servo. The conducted simulation and real-world experiments demonstrate that by distributing the local map exploration to a servo, the nonholonomic vehicle was able to achieve a faster convergence to the source.*
