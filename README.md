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
*Please describe and justify the use of selected AI technologies.*
- [AI technology 1],
- [AI technology 2],
- etc... .

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
*Please describe the details about the user interface(i.e, how does the client 'see' the technical result, whether a separate user interface was developed, command line script was developed, was it validated as an experiment, can the results be seen in ERP or are they integrated into work process)*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Future Potential of the Technical Solution
*Please describe the potential areas for future use of the technical solution.*
- [Use case 1],
- [Use case 2],
- etc... .

### Lessons Learned
*Please describe the lessons learned (i.e. assessment whether the technological solution actually solved the initial challenge).*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

# Custom agreement with the AIRE team
*If you have a unique project or specific requirements that don't fit neatly into the Docker file or description template options, we welcome custom agreements with our AIRE team. This option allows flexibility in collaborating with us to ensure your project's needs are met effectively.*

*To explore this option, please contact our demonstration projects service manager via katre.eljas@taltech.ee with the subject line "Demonstration Project Custom Agreement Request - [Your Project Name]." In your email, briefly describe your project and your specific documentation or collaboration needs. Our team will promptly respond to initiate a conversation about tailoring a solution that aligns with your project goals.*
