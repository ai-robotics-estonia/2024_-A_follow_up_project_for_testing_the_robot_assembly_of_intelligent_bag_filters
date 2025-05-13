# [A follow-up project for testing the robot assembly of intelligent bag filters at the company Vado Filters OÜ]

## Summary
| Company Name | [Vado Filters OÜ](https://website.link) |
| :--- | :--- |
| Development Team Lead Name | [Martinš Sarkans, PhD](https://www.etis.ee/CV/Martins_Sarkans/eng/) |
| Development Team Lead E-mail | [martins.sarkans@taltech.ee](mailto:martins.sarkans@taltech.ee) |
| Duration of the Demonstration Project | 01.12.2024 - 30.04.2025 |
| Final Report | [Example_report.pdf](https://github.com/ai-robotics-estonia/_project_template_/files/13800685/IC-One-Page-Project-Status-Report-10673_PDF.pdf) |

# Description
## Objectives of the Demonstration Project

The aim of the demonstration project was to continue the development and testing of an intelligent robotic assembly workstation to produce bag filters at Vado Filters OÜ.
During the testing in the first demo project, it revealed bottlenecks in the compatibility between the existing filter frame and the robot workstation. It was concluded that automation of the workstation with the existing filter-frame solution was not feasible.

Thus, Vado Filters OÜ has invested in a new frame solution and has a new frame prototype that will enable robotic workplace assembly of filters and improve the quality of the final product.
The aim of this demo project was to develop and test the robotic installation of bag filter pockets in a new frame solution and the attachment of the frame and the filter material in such a way that the required quality (no leaks and all components intact) is guaranteed.

## Activities and Results of the Demonstration Project

Project activities and results:
1. The first step was to specify the technical task, map the assembly operations and describe them. This provided the necessary information for the development of an intelligent fixture for the product and for the selection of a collaborative robot.
2. In the second phase, work started on the development of ideas for fixing the frame and filter bags. This involved testing the suitability and performance of different technical solutions to achieve the expected quality and repeatability of the assembly.
3. The third phase included the development of an intelligent fixture concept for the installation of the top and bottom frames. This solution was also physically implemented to test the real assembly process and its performance.
4. In the fourth step, a virtual model of the workplace was created and simulated. For this purpose, the RoboDK software was used to check the robot's operating range and cycle duration.
5. In the last step, the assembly cell was tested with the product, data collection, data analysis and model verification were performed. This involved the use of AI tools such as machine vision to perform product identification on the workbench (supplying the coordinates of the product to the collaborative robot), pre-production quality control of the filter bag (location and presence of seams), and quality control of the final product assembly (presence of all filter bags in the assembly).

### Challenge

Now, the frame is assembled by hand from various parts (using profiles and corners). The filter pockets are manually mounted next to each other on the springboard, with the "pocket mouth" open to connect the pockets with a plastic joint.

The fitting of the plastic joint is carried out by manual installation using a manually operated pneumatic tool to close the lock of the plastic joint. The interconnected pockets are manually inserted into the U-profile of the filter frame and secured with plastic clips, which ensure that the material remains firmly in place and provides the required air density for the filter. The fastening clips are then manually inserted into the frame and fastened either by finger force or with a pneumatic tool.

During this demo project we tested the suitability of a new frame solution for the creation of a smart robot assembly workplace. The challenge in developing the technical solution is to attach non-shape-holding textiles to the solid frame and to close the frame in such a way that the quality of the final product is guaranteed. All the manual activities described above will be addressed by an automated smart and self-configuring Workstation (intelligent fixture solution).

Another technical challenge is the integration of AI technologies into the product assembly process to ensure product quality in the assembly process and in final product control. This will require ongoing modification of the assembly program based on data from the manufacturing process to find the right position for the assemblies and not break assemblies during assembly.

### Data Sources

For implementation of the project, research articles in this field were studied and analyzed. In addition, the following software solutions were used:
-	Cognex In-Sight Explorer and Basler Pylon software for machine vision testing and training
-	RoboDK simulation software for robot application testing, simulation and program generation
-	SolidWorks CAD software for intelligent fixture design and concept development
-	Python programming language for creation and generation of robot parametric programs in RoboDK

The following data was gathered during the project for the analysis and verification:
-	production data, process information (time for assembly of filters)
-	machine vision data (Picture data of the filters, filter elements, final product and their features) for training the model for product recognition, position detection and quality control
-	product position data for creation of the robot´s parametric programs

The algorithm for generating a program for robots and the principles for defining robot system positioning. Stages:
-	Identifying the product on the table
-	Determining the location of the product by the points of intersection
-	Importing the coordinates of the coordinates into the simulation environment.
-	Adjusting robot programs based on points
-	Program simulation, training and verification

For the Machine Vision training, the following data was gathered about the product: as the shape of the product on the table is quite well determined, it provides the basis for generating the robot program (corner of the product and pick-up point). By transferring the image program to the Cognex In-Sight Explorer system, the corresponding detection algorithms can be added, such as: Product presence check; Horizontal edge detection; Vertical edge detection; Edge intersection detection (basis for robot program zero coordinate). For the training, the dataset of product specific Pictures was used.

### AI Technologies

For each stage of the project, a detailed description has been documented, the necessary simulations have been carried out, test data have been collected (assembly data, measurement and product detection data, quality control data). The solutions have been tested and verified at different stages of the project. These are the following results:
-	physical testing for filter bag assembly process has been carried out on intelligent fixture, data collection about forces, technical solution suitability assessment.
-	generation of the cobot program in a simulation (RoboDK) environment, based on a script for generating the code, testing of the solution's functionality.
-	testing machine vision functionality, collection of data on the product, evaluation of the suitability of different detection algorithms, testing of the performance of machine vision solution on a real test set-up.
-	carried out a workplace planning in the simulation environment, created a new workstation layout, designed a cell for product positioning.

Product detection, position detection and sewing lines detection is based on image recognition and it checks the position of the product based on the edges and the location and pattern of the sewing lines on the contours of the filter bag. Based on AI technology and image recognition, it decides whether the product is correct, identifies the coordinates of the filter bag and sends the commands to a collaborative robot, which selects the appropriate program and positioning for the product.

Machine vision solution testing and validation.
At the filter bag assembly workplace, it is necessary to identify the type, location and coordinates of the product to provide the collaborative robot with the necessary parameters to generate and run the assembly program. In this case, the product is a filter bag (placed on a flat surface) of a fairly fixed shape before the handling by the cobot. The cobot picks the filter bag from the material buffer, and the position of the product is not always the same. Therefore, it is important to provide the robot controller with the coordinates of the position of the bag filter. The following software and hardware have been used as a solution to the problem: Cognex camera Cognex In-Sight 7905C (color camera, 5 MP), Cognex In-Sight Explorer software, Optics Fujinon HF12.5HA-1S (C-mount), Optics Moritex LMC-ML-M2516UR (C-mount), lighting (LED, flood light, background light).

Generating the robot program (RoboDK)
The robot program uses a script to create the target points, which helps to read in the coordinates of the position of the filter bag. This is a machine learning technique that helps speed up the programming of the robot system. This is when the pattern or shape of the filter bag changes. Then, generating a new program for the robot is several times faster than doing it manually.
It is important to use correct coordinate systems when generating waypoints and working trajectories: robot base (workobject UR20 Base), Tool TCP (workobject Tool), Workobject of the application (workobject MyWorkObject).

### Technological Results
*Please describe the results of testing and validating the technological solution.*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Technical Architecture
*Please describe the technical architecture (e.g, presented graphically, where the technical solution integration with the existing system can also be seen).*
- [Component 1],
- [Component 2], 
- etc... .

![backend-architecture](https://github.com/ai-robotics-estonia/_project_template_/assets/15941300/6d405b21-3454-4bd3-9de5-d4daad7ac5b7)


### User Interface 

As the development of a user interface was not the aim of this demo project, there is no separate user interface as such. The UI solutions are related to the specific tools that were used (RoboDK simulation environment and script, and Cognex In-Sight Explorer environment for machine vision). These environments were used to validate the performance of the robot workstation and to validate the quality control capability of the product.

### Future Potential of the Technical Solution

The data collected and the solutions developed can also be used to automate the production processes of other textile companies or to apply artificial intelligence. In particular, we see similarities in the processes of sewing companies, where soft and stretchy textile materials are combined with form-holding components.

### Lessons Learned

As it is a complex end product that does not hold a fixed shape, the technical solution was to find directions to position the different elements of the product as well as possible and make them hold their shape. An intelligent jig developed for this purpose made it possible to achieve a situation where the filter bags could be well positioned to obtain a high quality end product. The solution developed during this demo project helped to solve the initial challenge well.
In addition, the simulation tools used, the use of machine learning, the use of AI tools (during this project) helped to check the previous quality of the product, its location and the final quality of the product.
When manufacturing complex products, it is also important to physically test the performance of the solutions and build test equipment to do so. Simulations and the use of AI tools can add the necessary additional flexibility to the robot and the intelligent fixture for such products.
Generally, several iterations of both the simulation and the technical solution are required before a suitable and mutually satisfactory result is reached.
