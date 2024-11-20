# Introduction

One of the major challenges in space exploration is the lack of suitable destinations for the people to travel to, within the constraints of modern technology. We will provide a solution to this challenge in the form of a space hotel, utilizing the capabilities of the SpaceX Starship heavy lift launch system. 

In addition to the micro gravity modules of the space hotel station, we will also include an artificial gravity segment that can simulate natural gravity up to Moon (0.166g) and Martian level (0.378g). This will allow a wider range of entertainment and research activities compared to the previous generation of space stations, such as Mir, ISS or Tiangong. Furthermore, this capability will allow generation of valuable life science data for the future interplanetary colonists.

# Station Design

The obvious station design to allow artificial gravity would be a full ring structure, potentially with multiple rings providing different levels of gravity. However, due to the limit on the number of Starship launches available, a partial ring is more feasible option.

Based on the results of artificial gravity trade-offs, a diameter of around 75m is needed to have a comfortable level of low gravity. The partial ring of the station rotates around the hub, and the hub’s main body stays stationary to allow spacecraft to dock more easily without having to match rotation speed. The structure of the station is maintained thanks to cables between the modules.

![space stations.png](https://cdn.dorahacks.io/static/files/18d528f093b7396cbed583642daa69be.png)

It is made up of a total of 17 modules of 4 types:
- **Central hub** This module has a central stationary part where the airlock is located. There is also a welcoming directly after the guests exit the airlock after arriving. There is a rotating collar where the two main arms/corridors of the station connect to the artificial gravity section.

![central_hun.png](https://cdn.dorahacks.io/static/files/18d52980c0641c86cc5dbf24a95b7156.png)

- **Multipurpose** This type of module is very versatile, and is primarily used to connect the hub to the partial ring sections. Multiple modules are stacked to create the diameter of the partial ring needed to achieve the target artificial gravity. This module can be packed with required equipment at launch and everything can be connected in orbit during assembly. The module is used in the arms of the station and packed with life support machines and supplies needed to run the station. The module has the largest continuous interior by default so it is also used as a multi purpose room in the partial ring for sports and other activities.

![mpm.png](https://cdn.dorahacks.io/static/files/18d529eaabb352d8825ab904693a2e91.png)

- **Sleeping quarters**. This module contains up to 6 double rooms

![stores.png](https://cdn.dorahacks.io/static/files/18d529dbff484c8905f572b48bb948f3.png)

- **T-section** This module links the sleeping quarters to the rest of the station. It has a kitchen and communal areas for eating and relaxing.

![t_cell.jpg](https://cdn.dorahacks.io/static/files/18d52b90eab556c6f6ebea64d94a0f4c.jpg)

# Specifications

*Summary*

|  **Station Diameter** | **Mass, dry**  | **Mass, wet** | **Capacity** | **Power budget** | 
| :------ | :------ | :------ |  :------ | :------ |
| 75 m |  850 tonnes | 1550 tonnes | 18 people | 171 kW |

*Table 1 - Space Hotel space station summary*

# Artificial Gravity Considerations
For a rotating structure, its artificial gravity level can be assumed as the centripetal acceleration at the rim of the structure. The formula will be:

*a=w<sup>2</sup> * r*

Here r is rotation radius in meters, and w is rotational rate in rad/s. (REF 36, p.9). Below is the map of relation between rotation radius and angular velocity for given centripetal acceleration/artificial gravity level:

![Screenshot 2024-08-21 at 7.52.43 PM.png](https://cdn.dorahacks.io/static/files/191775bea55be902474ff884b4aab65a.png)
[1, p. 43]

**why choice of 0.166g (Lunar gravity) and 0.378g (Martian gravity) are important as design points?**

When it comes to understanding the impact of fractional gravity on human is mostly unknown - any data points on this subject will massively improve our understanding of the required level for long-term survival of of human. 
 
Furthermore, the knowledge of long-term exposure to this level of gravity would be critical to understand the health impact on the population of any future Martian or Lunar surface colony, especially on the gestation and health of second-generation colonists. 

Station architecture also allows rotation at lower levels of artificial gravity, simulating environment for all other smaller bodies and minor planets in Solar System (like Ceres, Pluto, moons of giant planets and so on).

In addition to the main parameter of the artificial gravity magnitude, there are also a list of secondary effects for human inhabitants, listed below

- **Artificial gravity gradient**

This is the variation of artificial gravity level between the different parts of human body, measured at head and feet distance, expressed as *∆A_c=(r-h)/r*

Here r is the centrifugal radius and is h the distance between the feet and head of an astronaut. There is no reliably known limits for this value, but currently available body of research indicated that values of up to 15% are well-tolerated [4, p.5]

- **Coriolis force**

Any linear motion along the habitat will produce an extra acceleration different from natural gravity environment, defined as: A_cor=-2*(w×v)

Here w is angular velocity, v is velocity of the moving object, with the resulting acceleration defined as cross product of above values ([1, p. 38). Its magnitude is maximum when the moving object velocity vector is perpendicular to the rotation vector.

- **Cross-coupled acceleration**

Cross-coupled acceleration appears during any rotational motion during the induced centrifugation. Its formula is:  *A_cca=w×wx*

Here *w* represents the angular velocity of the rotational environment and *wx* is the angular velocity of the rotating object. The absolute value of cross coupled acceleration acting on a human crew member is the sum of said angular acceleration and the cross product of the above values. ([2, p.12).

- **Euler force acceleration during acceleration and deceleration**

This is a transient force due to spin-up and spin-down phases, defined as *A_euler=-dw/dt×R*

Here *-dw/dt*  is the angular acceleration/deceleration and R is the vector position of the point where acceleration is measured relative to the axis of rotation ([2, p.42). This acceleration increases in magnitude with greater distance from the center of rotation.

- **Summary of acceleration components in the rotating environment**

The total acceleration acting on the point object in rotating reference frame is

*A_total = A_c + A_cor + A_cca + A_euler*

Definition of comfort zone and dimensions for the rotational gravity takes into account the secondary effects/acceleration factors. The magnitude of these effects will vary depending on the scenario in question. Stationary observers in a uniformly rotating environment will only experience centripetal acceleration, while moving objects in the same environment may experience Coriolis and cross-coupled accelerations.

*Sensitivity thresholds and comfort zone identified*
Over the 60 years of space exploration history a number of studies were dedicated to establishing upper and lower limits of artificial gravity, Coriolis force and gravity gradient. Note that sensitivity by itself doesn't imply any negative impact on human performance. Vestibular apparatus adapts successfully to motion sickness both at Earth’s gravity level on marine and airborne vessels and in space during weightlessness conditions. To summarize the current understanding of human physiology in rotating environments, a chart shows all of the available parameters with the hypothesized "comfort zone" highlighted:

![ag.png](https://cdn.dorahacks.io/static/files/18d5c2025ce0d9ccc5c2b08420da8e0a.png)
[3, p. 7]

With respect to chart above for artificial gravity comfort zone, we get the following specification for the station parameters:

|  *Artificial gravity level** |  **Revolutions per minute** | **Artificial gravity gradient** |  **Tangential velocity** | **Rotational radius** | **Comments** |
| :------ | :------ | :------ | :------ | :------ |  :------ |
| 1.66 m/s^2 | 2.00  | 4.85% | 7.77 m/s  | 37.5 m | Moon gravity 
| 3.17 m/s^2 | 3.00  | 4.79% | 11.80 m/s  | 37.5 m | Martian gravity 

*Table 2 - Artificial gravity environment parameters*

Illustrated below is the station environment with respect to artificial gravity parameters chart:

![Artificial_gravity_our_station.png](https://cdn.dorahacks.io/static/files/191aa422f267644084446b342869cb76.png)

# Operations overview
Initial mission operations assume 17 launches at 50% load capacity + 2 launches at 100% for tug operations, allowing a margin of safety for each launch plus spare launches available for contingency scenarios. 

After station assembly additional cargo can be brought aboard, both consumables like food, water, oxygen, fuel etc and additional structural or functional components. A total of 7 launches at 100% Starship payload capacity (700 tonnes) will bring the necessary equipment and consumables onboard after station assembly, keeping the total number of launches at the limit of 24.

Among the possible orbits for space hotel station (LEO, SSO, MEO or GEO)
The optimal orbit , taking into the consideration all available parameters selected to be of 550 km altitude at 28.5 inclination (assuming Cape Canaveral launch site), minimizing radiation exposure, residual atmosphere drag and space debris risk, as illustrated in the charts below:

![chart_drag.png](https://cdn.dorahacks.io/static/files/18d57336d48226c4a8a1632403eabded.png)
[5, Fig. 8]

![chart_rad_debris.png](https://cdn.dorahacks.io/static/files/18d5736158b3176fb7d41ce4adcaf6f8.png)
[6, Fig. 3]

Orbit visualization

![3D view.png](https://cdn.dorahacks.io/static/files/18d5736e1ea61c5fe5614c24ccbb7d3e.png)

Ground track

![gmat_sim.png](https://cdn.dorahacks.io/static/files/18d57370ece6977b3934f214bd28a94f.png)

The choice of orbit and design allows interoperation with existing cargo and crewed spacecraft for resupply, guest rotation and emergency egress procedures without excessive modifications. To facilitate in-orbit assembly for proposed space hotel, additional robotic tug spacecraft with a robotic arm can be utilized, as illustrated below, with sufficient propellant to perform all assembly operations:

![tug_1.png](https://cdn.dorahacks.io/static/files/18d573e6872b0e15bf1c011442b9f136.png)

The space tug is designed to fit inside Starship fairing dimensions, illustrated below:

![space_tug.png](https://cdn.dorahacks.io/static/files/18d57ced652e4a1847b28434bcf93230.png)

It will have sufficient fuel load to perform all necessary assembly activities at the target orbit, assuming the following specifications:

|**Total mass** | **Fuel mass** | **Diameter** | **dV** | 
| :------ | :------ | :------ | :------ |
| 100.0 tonnes | 80.0 tonnes | 6m  | 5.1 km/s |

*Table 3 - Orbital Tug specs*

## Radiation Environment Considerations
There are multiple sources of radiation at LEO: constant background from (mostly protons) lower edge of Van Allen radiation belt, galactic particle rays as well as episodic events such as CMEs, solar flares and gamma-ray bursts. Each of them require different shielding strategies, but to simplify things, low-energy (<10 MeV) charged particles and gamma-rays are most efficiently stopped by heavy, dense metals, but higher-energy (>20 MeV) particles have to rely on lower density materials with higher proportion of hydrogen atoms (polyethylene, paraffin or water) due to induced secondary radiation. Radiation levels at 550 km altitude are significantly more elevated compared to ISS orbital altitude and will require additional shielding to allow the inhabitants to stay within the same annual limit.

## Station outer shell design
Preliminary calculations using NASA OLTARIS tool (tables 2-3) showed that 35g/cm^2 of water shielding is sufficient to reduce the total annual dose below the ISS-equivalent safety limit within 150 milliSieverts per year under most of the expected conditions.

|  **Data** |  **Daily dose** | **Annual dose** |  **Unit** | 
| :------ | :------ | :------ | :------ |
| Earth Orbit GCR | 0.09916  | 36.19 | mSv  |
| Trapped + albedo | 0.3004  | 109.7 | mSv  |
| ***Total*** | ***0.3996***  | ***146.6*** | ***mSv***  |

*Table 4 - AP9 solar cycle averaged + 2001 Solar Maximum*

|  **Data** |  **Daily dose** | **Annual dose** |  **Unit** | 
| :------ | :------ | :------ | :------ |
| Earth Orbit GCR | 0.1144  | 41.76 | mSv  |
| Trapped + albedo | 0.3004  | 109.7 | mSv  |
| ***Total*** | ***0.4148***  | ***151.4*** | ***mSv***  |

*Table 5 - AP9 solar cycle averaged + 2001 Solar Maximum*

Module structure is assumed to be composed of the 50 mm Al-alloy pressure hull augmented by inner shielding formed by 10 mm polyethylene and 10 mm of teflon with 350mm of spacing that can be filled with water, with teflon being chosen for the crew-facing wall to reduce flammability hazards. Total thickness of the module’s wall is  420 mm and area density is 51.7 g/cm^2.

![Module structure](https://cdn.dorahacks.io/static/files/1916d51754291cefd5258274041b9fc2.png)

Additional measures can include screening of crew and passengers-candidates for high-risk cancer markers in their genomes and personalizing their daily schedule with respect to the radiation exposure and adding radioprotective food into the astronaut’s diet.Individual radiation shielding can be also added to crew and passengers work suites, using solutions such as AstroRad by LM (illustrated).

![Astrorad vest](https://cdn.dorahacks.io/static/files/1916d5be82f02d474bfe2894b4e9f021.png)
[7]

# Assembly Operations and Cable Management
Building the station and installing the tension cables will require the tug to have a visual processing system for autonomous, or semi autonomous operation, and one or more robotic arms. 

The space industry is seeing more and more developments in edge computing that will allow this to happen. We are seeing the kind of computing that allows complex processing of data such as Visual Odometry, detection, and tracking of objects in space for Rendez-vous and Docking.

Robotic arms used to be a cause for concern due to their complexity and the difficult space environment, however in recent years many companies have unveiled their robotics heavy missions.

Clear space is planning on using a multi arm space tug for clearing large space debris. And MDA has unveiled their Skymaker suite of robot arms for commercial space.

![MDA Skymaker Arm](https://cdn.dorahacks.io/static/files/1917262bb296fb96ef829554bf69a05b.png)
[8]

Given that the technological development is well on its way, station building will make heavy use of robot arms and visual processing. 
The modules will have attachment points, and the cable will be laid out by the tug, and using the robot arms to attach itself, and another to install the cable, it will link all the modules in such a way as to maintain tension when the station is made to rotate

The tug uses a combination of Visual Odometry and machine learning to estimate its position, and that of the robot arm in 3D space in order to perform the attachment maneuvers. It is possible to use other visual cues such as markers to increase the reliability of the visual processing system.

![Attachment Point Close-Up](https://cdn.dorahacks.io/static/files/19172646c27b03ffddfa03b47468fb04.png)

## Assembly procedure - details

- Step 1 - Build the spine of the station

![Step 1 illustrated](https://cdn.dorahacks.io/static/files/1917266ede3c480101ade784a7cb9868.png)

- Step 2 - At each end, begin assembling the segments using the semi-autonomous tug

![Step 2 illustrated](https://cdn.dorahacks.io/static/files/191726c40a898cc5d3275684c9e834f7.png)

- Step 3 - Complete the main structure of the station in its static configuration

![Step 3 illustrated](https://cdn.dorahacks.io/static/files/191726d6dbab3a2f8b9ba30436387886.png)

- Step 4 - The tug uses its multipurpose robot arm with robust visual processing to link up the cables from one side to the other. Using the attachment points on each module.

![Step 4 illustrated](https://cdn.dorahacks.io/static/files/191726ee61ed3ab98176ffc49f280070.png)

- Step 5 - The station is complete and can be made to rotate while the cables maintain tension and structural integrity of the extremities of the station

![Step 5 illustrated](https://cdn.dorahacks.io/static/files/19172723f3030ba08c4e92a4d1e978b5.png)

# Airlock operations

All modules have the ability to open/close hatches between each module allowing for isolation of any module has a leak, or even for use as an airlock.

![Airlock A](https://cdn.dorahacks.io/static/files/191818f5fc64d610c177d734242956ac.png)

This can be done through central command for pre-planned outings or automatically during emergencies where a pressure leak is detected beyond a predetermined threshold.

![Airlock B](https://cdn.dorahacks.io/static/files/19181908c56596c4864b132478194c76.png)

There is also a dedicated airlock at the station entrance for visitors coming from spacecraft with different pressure from the station (Apollo 11 was pressurized at 0.3 atmosphere for example)

![Airlock C](https://cdn.dorahacks.io/static/files/191819199a2f51b579bf88449ad88cf0.png)

## Control operations
There are multiple aspects to control on the station:
- Attitude control (where the station is pointing)
- Orbital control (adjusting the trajectory of the station around the Earth)
- Station rotation (for gravity and stability)

### Attitude control

With the modular design of the station, small RCS thrusters and reaction wheels will be included in all the modules. They are small and inexpensive, but working as one, they will produce enough control authority to change the station’s attitude. They will all be controlled from a central location.  Since the station is continuously rotating there will need to be a smart control mechanism to ensure control of the station is maintained while not causing damage to the structure.

### Orbital control 
The following shows the results of calculations showing how much propellant would be used to do an orbit transfer from the lowest orbit acceptable back to the nominal orbit. This assumes the nominal orbit is at 550 km and the orbit decays to 500 km. In reality there will need to be further analysis to determine the exact values, however this calculator provides a good order of magnitude.  Below is the estimation for the single orbit-raising manoeuvre (two burns) using bi-propellant (UDMH+Nitrogen Tetroxide) engine.

| Station Mass, Dry | Station Mass, Wet  | Propellant Mass | deltaV, total | 
| :------ | :------ | :------ | :------ |
| 850 tonnes | 1550 tonnes | 13.00 tonnes  | 27.65 m/s | 

*Table 6 - deltaV cost for orbit maintenance*

### Station rotation
The rotation will be controlled with same reaction control thrusters as used for attitude control. Thanks to the lack of air resistance the station can keep spinning without additional power.When needed the thrusters can start applying reverse thrust to slow down the rotation.

### Power Generation
The station's skin will be covered in solar panels and the panels will be mounted on hinges such that they can flatten out and point at the sun perpendicularly. This will ensure maximum efficiency. The station will always be spinning with its axis pointing at the sun. This will ensure the panels are always able to generate power.  At chose orbital altitude eclipse duration will be very roughly estimated at 1/3 of total orbital period, so power system budget should be provisioned as such.

See table below

| **Solar panel efficiency, EOL** | **Solar Constant, W/m^2** | **Solar Panel Effective Area**  | **Total Station Area, m^2** | **Total Power** |
| :------ | :------ | :------ | :------ |  :------ |
| 15% | 1361  | 30 |  840 | 171 kW |

*Table 7 - power budget estimate*

### Water Management
Water can be fully recycled at the same way as it is done on ISS (98% is current efficiency estimate) using a distillation process, and fresh water will be brought up when needed on supply ships. Use  of water in radiation shielding presents additional reserve that can be used in emergency scenarios.

### Crew Managament 
One of the proposed augmentation to the environment is an AI assistant integrated into this space hotel could be a highly advanced and multi-functional system, designed to assist the crew and visitors with various tasks and ensure the smooth operation of the hotel and reduce their workload. Here's its detailed description:

#### Core Functions:

**1. Operational Assistance:**

- **System Monitoring:** Continuously monitors all space station systems (life support, power, communication, propulsion, etc.) and alerts the crew to any anomalies or required maintenance.

- **Resource Management:** Tracks the usage and availability of essential supplies such as food, water, and medical supplies, providing real-time updates and forecasts.

**2. Crew Support:**

- **Health Monitoring:** Interfaces with wearable health devices to monitor the physical condition of crew members, offering health tips and reminders for exercise or medication.

- **Task Scheduling:** Manages crew schedules, assigning tasks, and ensuring adherence to timelines.

**3. Communication:**

- **Internal Communication:** Facilitates communication between crew members through voice, text, and video messages.

- **External Communication:** Manages communication with Earth-based mission control and other spacecraft, ensuring data integrity and security.

**4. Safety:**

- **Emergency Response:** Provides guidance during emergencies, such as fire, hull breach, or medical emergencies, offering step-by-step instructions and coordinating responses.

### Interface:

### Wall-Mounted Terminals:

- **Design:** Sleek, touchscreen interfaces placed strategically throughout the space station for easy access.

- **Voice Interaction:** Equipped with high-quality microphones and speakers, allowing for hands-free interaction. Visitors and crew members can issue voice commands, and ASTRA will respond verbally.

- **Visual Display:** High-resolution screens capable of displaying text, graphics, and video. Interfaces can show system statuses, schematics, real-time data, and more.

- Accessibility: Terminals can be adjusted for height and angle, ensuring usability for all crew members.

### User Interaction:

- **Personalized Experience:** Recognizes individual crew members through voice and facial recognition, providing personalized assistance based on their roles and preferences.

- **Context-Aware Responses:** Understands the context of commands and queries, offering relevant information and suggestions. For example, if a crew member asks about the status of an experiment, ASTRA can provide a detailed report and anticipated outcomes.

- **Learning Capability:** Continuously learns from interactions and feedback, improving its assistance and adapting to the crew's evolving needs.

### Security and Privacy:

- **Secure Access:** Implements robust authentication methods, ensuring that only authorized personnel can access sensitive information or critical systems.

- **Data Encryption:** All communications and data are encrypted to protect against unauthorized access and cyber threats.

- **Privacy Settings:** Allows crew members to control the level of access and information ASTRA has, ensuring personal privacy and comfort.

### Maintenance and Updates:

- **Self-Maintenance:** Regularly performs self-diagnosis and updates, ensuring optimal performance and security.

- **Remote Support:** Can receive software updates and technical support from Earth-based mission control, addressing any issues promptly.
ASTRA serves as an indispensable partner to the space station crew, enhancing operational efficiency, safety, and overall mission success.

# Growing food in space

Growing food in space is essential for long-term missions but challenging due to resource constraints. Researchers have developed stretchy sensors that attach to plants, monitoring their growth by measuring electrical signals. These sensors, made from special polymers, provide data wirelessly, reducing the need for astronaut intervention. They were tested successfully on oat plants, demonstrating resistance to humidity and temperature. Future tests will include leafy greens and tomatoes. These advancements aim to optimize plant growth in space, ensuring astronauts have access to fresh food on extended missions​

Growing food in space has advanced significantly since NASA installed the Vegetable Production System, or "Veggie," on the ISS in 2014. [9] This system tests food cultivation in microgravity, where simple tasks like watering and harvesting become complex. Discoveries from space agriculture, such as LED lighting and controlled-release fertilizers, benefit Earth’s agriculture by improving efficiency and sustainability. NASA collaborates with various partners to develop these technologies, which are crucial for future space missions and have substantial applications for terrestrial farming. The psychological benefits of growing food in space for astronauts are also notable.

The nutritional value of plants grown in space is notably high, especially when it comes to microgreens. These tiny plants have been found to possess four to ten times the nutritional density of their mature counterparts. This makes them an excellent choice for space cultivation due to their small size and high nutrient content. For instance, microgreens like broccoli and kale offer concentrated nutrients and flavors, which are crucial for supplementing astronauts' diets on long missions where traditional food storage and nutrition can be challenging​

In December 2023, astronauts on the International Space Station (ISS) found a tomato that had been missing for eight months. The tomato was lost shortly after NASA astronaut Frank Rubio harvested it in March. Despite extensive searches, the tomato remained elusive until it was discovered by another crew in December. 

The tomato was part of NASA's space botany studies aimed at understanding how to grow fresh food in space for long-term missions. When found, the tomato was dehydrated and slightly squished but showed no signs of microbial or fungal growth. [10] This finding highlights the challenges and unexpected events that can occur during space agriculture experiments.

As for raising chickens in space, current research has not advanced to the point of attempting to raise live animals such as chickens. The primary focus remains on plants and small organisms due to the complexities of life support systems and the ethical considerations involved in animal husbandry in microgravity environments.

Astronauts aboard the International Space Station tasted space-grown chili peppers for the first time on October 29, 2021. The peppers, part of the Plant Habitat-04 experiment, were grown from July 12 in the Advanced Plant Habitat. [11] This hybrid variety, chosen for its vitamin C content and successful ground test results, required careful environmental control and pollination. The peppers added essential nutrients to the astronauts' diet, supporting long-duration space missions. This experiment marked a significant step in NASA's ongoing research to grow food in space.

### Food growth hydroponics bay
As described previously, the food can be grown on-premises, at the hotel. One of the modules will be used as a hydroponics facility, where all of the growth supporting mechanisms will be stored. Because we are limited by the shape of the module, which is cylindrical, the optimal use of space can be achieved with a structure described in the following image:

![Food farm module ](https://cdn.dorahacks.io/static/files/1918c342645711fd146406b49cfa39d0.png)

The growth structure is smaller in diameter than than the module and can rotate to emulate movement and to support gravity direction.

There are 11 farm beds, thus, the whole hydroponics structure will support 17 plants per farm bed (maximum distance between each plant is 0.5m) or a maximum of 187 plants. The maximum height per plant is 1.5m, which allows free movement of the crew in the center of the module.

The nutrients for the plants shall all be stored at the ends of the structure and pumps will be use to circulate the nutrients through the farm beds. Because the nutritional solution is mostly water, we can reuse some of the water and redirect it to the hotel’s cooling systems. Before doing that, the water needs to be filtered. The filters will have to be replaced regularly, depending on the number of the plants.

The power consumption for the hydroponics section is significant but not abnormally high, and can be calculated:

11 light stripes x 45W each = 450W
2 water pumps x 50 W = 100 W
1 motor x 40W = 40W
Total power usage 590W

To conserve power and to emulate the daylight, the lights can and will be turned on and off every 12 hours. Note that farm production is not set to be maximized and can be increased with additional lighting and longer illumination hours.

Having a large number of plants will affect the oxygen concentration in the hotel, considering that 300-400 plants are necessary to produce enough oxygen for one person, the above number of a maximum of 187 plants will produce half of that amount daily. On the opposite side, plants also absorb CO2, therefore this will affect the CO2 concentration too(numbers are unclear at this time).

#### Drinks and refreshments in space

The concept of alcohol in space has a storied past, involving notable instances such as Buzz Aldrin's communion on the moon and Russian cosmonauts drinking on the Mir space station.

NASA, however, does not include beer or other carbonated beverages in astronauts' diets due to the unique problems posed by microgravity. In the absence of gravity, the gas in carbonated drinks doesn't separate from the liquid, leading to "wet burps" as the gas and liquid mix in astronauts' stomachs.

Despite these challenges, experiments have been conducted to explore the feasibility of brewing beer in space. For instance, a University of Colorado graduate student, Kirsten Sterrett, with support from the brewing company Coors, sent a miniature brewing kit into orbit. [12] While the experiment succeeded in producing a small amount of beer, the resulting brew was compromised by the chemicals used in the analysis, rendering it undrinkable​.Overall, while brewing beer in space is technically possible, the unique challenges of microgravity, especially related to carbonation and digestion, make it impractical with current technology. The experiments so far have provided valuable insights but highlight the difficulties in creating a palatable space beer.

According to this research, we can conclude that growing most of the vegetables that are consumed regularly on Earth can be grown and used to prepare meals in space. The hydroponics area will be separated from the habitat ones to avoid any contamination and other unexpected issues. 

The space kitchen will be located near the dining area and the hydroponics area to allow faster and easier access to the vegetables. 

Based on the previous research and facts, we can assemble a menu for our guests to allow them a more enjoyable experience at the space hotel.

**Space hotel menu:**
1. Salads
- Lettuce Salad
- Tomato/Garden Salad
- Potato Salad

2. Main Courses
- Veggie Burger (Black Beans)
- Beef
- Quail Eggs (Omelette, Boiled Eggs, Veggie Burgers with Quail Eggs)

3. Dehydrated Foods
- Ration Packs/Dehydrated Food
- Dehydrated Omelet

4. Desserts
- Ice Cream
- Chocolates

5. Beverages
- Beer
- Orange Juice
- Apple Juice
- Liquor
- Wine

# Available activities

*Views of Outer Space*
The space hotel might still feature windows or observation areas, allowing guests to enjoy stunning views of outer space while swimming. The combination of artificial gravity and panoramic views would create a unique and memorable aquatic experience.

*Spacewalks*
A spacewalk in a space hotel would be an extraordinary and memorable experience, providing you with the opportunity to float freely in the microgravity environment outside the confines of the hotel. Here's how a spacewalk might look like for you:
- Preparation:
Before embarking on a spacewalk, you would undergo thorough training on how to use the space suit, safety protocols, and how to navigate in microgravity. The space suit is a crucial piece of equipment, providing life support, temperature regulation, and protection against the vacuum of space.
- Exiting the Space Hotel:
To begin the spacewalk, you would exit the space hotel through an airlock or designated entry/exit point. The transition from the interior of the hotel to the vastness of space would be a breathtaking experience. You'd be greeted by the awe-inspiring view of Earth below and the vastness of outer space.
- Microgravity Floating:
Once outside, you would experience the freedom of microgravity. Your movements would be characterised by graceful floating, and you would use handrails, handholds, or small thruster units attached to your spacesuit to navigate in the three-dimensional environment.
- View of Earth:
The view from the spacewalk would be spectacular. You'd see the curvature of the Earth, the thin blue atmosphere, and the darkness of space. The lack of atmospheric distortion would provide an incredibly clear and vivid panorama of our planet.
- Photography and Documentation:
Spacewalks are not only about the experience but also about documenting and capturing the moment. You might have tools or cameras attached to your spacesuit to take photographs, record videos, or participate in scientific observations.
- Hotel Exterior and Features:
As you navigate the exterior of the space hotel, you would see its unique design, solar panels, and other features that make it suitable for space habitation. Special viewing platforms or transparent sections might allow you to observe the interior of the hotel from the outside.

*Swimming In Space (Optional)*
Available space and capabilities may allow installation of sub-scale swimming pool, once all the procedures for water management and recyling are established. Water would behave in a familiar manner, and swimming strokes and techniques would closely resemble those used in terrestrial pools. Swimmers would experience buoyancy in a way similar to Earth, making swimming movements more intuitive and natural. The sensation of being in the water and the resistance offered by it would be comparable to what people experience in swimming pools on our home planet. While the swimming environment may be more familiar, safety measures would still be in place. Lifeguards, safety equipment, and clear guidelines for guests would ensure a secure and enjoyable swimming experience.

*AR/VR-augmented activities*
An augmented reality (AR) or virtual reality (VR) headset can significantly enhance your stay in a space hotel, providing immersive and interactive experiences. Here are several ways in which such a headset might improve your stay:

- Virtual Space Tours
Explore virtual tours of the space hotel or nearby celestial bodies. VR can overlay information about each area, providing historical facts, scientific details, and interesting anecdotes, making your exploration more educational and engaging. As both microgravity and partial gravity environments are available for the participants, multiple different environment types can be simulated (orbital and atmospheric flights, surface operations)

- Enhanced Views 
Use the AR headset to enhance the views of outer space. Pointing the headset towards the Earth or celestial objects could trigger informative overlays, such as constellations, satellite trajectories, or details about the planets visible at that moment.

- AR Space Fitness Classes:
Participate in augmented reality fitness classes tailored for the microgravity environment. The headset could guide you through exercises designed to keep you active and healthy during your stay.

- Augmented Reality Art Galleries:
Experience augmented reality art installations or galleries within the space hotel. Artists could create three-dimensional digital art that guests can appreciate through their AR headsets, adding a new dimension to the aesthetic atmosphere of the hotel.

- Language Translation and Cultural Insights:
If the space hotel attracts a diverse international clientele, AR headsets could provide real-time language translation and cultural insights. This feature ensures smooth communication and a more inclusive experience for guests from around the world.

*Space activities for kids and families*
In a space hotel, the unique microgravity environment and the futuristic setting provide opportunities for a variety of exciting and innovative games for both adults and children. Here are some games that you and your kids might enjoy:

- Art and Crafts in Microgravity
Encourage creativity by organizing art and crafts activities. Floating art supplies and creating three-dimensional art pieces in microgravity can be a unique and enjoyable experience for both kids and adults.

- Microgravity Soccer:
Set up a floating soccer ball and goals in a designated play area. Players can use handrails, walls, or even each other to navigate and score goals. The lack of gravity adds an interesting twist to traditional soccer.

- Space Bowling:
Set up a floating bowling alley with specially designed lightweight balls. Players can push the balls off a starting point, and the lack of gravity will allow them to gracefully float toward the pins, adding an element of unpredictability to the game.

- Asteroid Dodgeball:
Adapt the traditional dodgeball game by incorporating soft, lightweight balls. Players can float and dodge in three dimensions, making the game more challenging and dynamic.

- Microgravity Scavenger Hunt:
Create a list of items or clues for a scavenger hunt within the space hotel. Participants must navigate the microgravity environment to find hidden items or complete challenges. This can be a fun and engaging way to explore the space hotel.

- VR/AR Educational Experiences for Kids:
For families with children, VR/AR can offer educational content and interactive experiences. Engage in augmented reality games designed specifically for the microgravity environment. Play space-themed puzzles, challenges, or even multiplayer games with fellow guests, adding a social and recreational aspect to your stay. From space-themed storytelling to virtual space exploration games, the VR/AR headset can turn learning into a fun and engaging activity for kids.

**Space Activities Pros and Cons**
Within a range of possible activities for space hotels patrons, the major factors to consider are the costs and potential health risks. While microgravity-augmented VR and AR activities will be relatively easy to implement and even can be self-administered, any zero-gravity sports will require presence of additional crew members for safety and guidance. EVAs for customers are even more involved, with spacewalks require supervision and additional training. The risk of emergency situations is also higher for such an activity, therefore not everyone among passengers may qualify for it.

# Costs, schedule and business model considerations. 
It would be a reasonable assumption to allow for 1 module per month launch schedule for a total of 17 months of initial construction time and 24 months of total construction time with further 7 launches with consumables and commissioning activities combined together.

Total cost of International Space Station is estimated to be $150B with annual operational budget of $4B. [13]

Assuming near-term projection of space launch cost going down to $1000/kg when Starship becomes available (one order of magnitude below current market low) and station module construction cost roughly equal to launch cost (as often the case with existing space missions), we can estimate the entire mission cost to be $50M to build and $50M to launch, giving the total construction cost of $1.7B (17x100M). Additional 7 launches delivering consumables and other good would add up to another $700M to the total cost of $2.4B. If the same percentage of capital to operational expenses is taken as with ISS, then the expected annual cost will be around $64M/yr. At 25 years of operational lifetime, comparable to existing space stations, that would add to $1.6B of operational costs, for a total of lifetime cost of $4B.

While this is a very approximate cost estimate, the value is within the same order of magnitude as planned space stations from Axiom and Blue Origin,  in $3-10B range[14, 15]

Assuming gross profit of 3x of the total lifetime costs for a 33% profit margin, we arrive at $12B gross revenue required for successful commercial operations, translated into annual figure of $480M.

As the station has the capability for 18 people, at 12 revenue-generating passengers and 6 crew,with utilization factor of 10 months per year and and taking into account 17 months of initial construction cost and 6 months of commissioning (non-operational time), we can calculate the cost of monthly gross profit of 52M. For a single man-month we have $4.3M of gross profit required and for a single man-day of $144K.

That translates into weekly stay for a single person at $1M - within the realm of today's space industry capabilities

# Development risks
Most of the technology used for our space design do not require any additional scientific R&D, as existing solutions used on previous generations of space stations (ISS, Mir, Salyut, Skylab) can be utilized, scaled up as required.

As with every new engineering project, there will be a considerable amount of the engineering research and design work. With that in mind, a pathfinder/pilot projects can be used as such, for example a smaller scale space station, consisting only of central hub and only two habitat modules, with support for rotational artificial gravity as well - to understand challenges required for construction and operations, including assembly, docking and spin-up/spin-down procedures. 

Alternatively, reduced module dimensions can be used for pilot project construction, similar to the current ISS ones (4.2x8.4m), that would full allow almost entire of possible operations with the benefit of reducing size, mass and cost of the entire station.

# References
1. Kingston JC, Fong KJ. Artificial gravity as a multi-system countermeasure to the physiological effects of long duration space flight. Cranfield: 2007

2. Clément, G, Charles JB, Norsk P, Paloski WH. Artificial Gravity, version 6.0
(NASA Human Research Program, Human Health Countermeasures Element,
Evidence Report).Houston, Texas, USA: NASA Johnson Space Center. (2015
May 12).

3. Hall TW. Artificial Gravity in Theory and Practice (ICES-2016-194). 46th International Conference on Environmental Systems (ICES), Vienna, Austria, 10-14 July 2016.  Lubbock Texas, USA: Texas Tech University. (2016 July).

4. Hoegenauer E, Wagner K. Artificial gravity for long duration manned space
flight, Space Programs and Technologies Conference and Exhibit. AIAA SPACE, Forum 1994.

5. Jinyu Liu Li Gangqiang Z. H. Zhu Xingqun Zhan. Orbital Boost Characteristics of Spacecraft by Electrodynamic Tethers with Consideration of Electric-Magnetic-Dynamic Energy Coupling.  March 2020 Acta Astronautica Issue 171 (2020)

6. Ma, Fujian & Zhang, Xiaohong & Li, Xingxing & Cheng, Junlong & Guo, Fei & Hu, Jiahuan & Pan, Lin. (2020). Hybrid constellation design using a genetic algorithm for a LEO-based navigation augmentation system. GPS Solutions. 24. 10.1007/s10291-020-00977-0.

7. https://www.lockheedmartin.com/en-us/products/astrorad---what-you-wear-in-space-could-save-your-life.html (accessed Aug 29, 2024)

8. https://spaceq.ca/mda-space-unveils-skymaker/ ((accessed Aug 29, 2024)

9. https://www.nasa.gov/missions/station/veggie-plant-growth-system-activated-on-international-space-station/ (accessed Aug 31, 2024)

10. https://www.nasa.gov/missions/station/iss-research/nasa-lets-ketchup-on-international-space-station-tomato-research/ (accessed Aug 31, 2024)

11. https://www.nasa.gov/image-article/astronauts-have-first-taste-of-peppers-grown-space/  (accessed Aug 31, 2024)

12. https://www.drinkingcolorado.com/features/to_bodly_go_beer.php  (accessed Aug 31, 2024)

13. https://www.planetary.org/articles/20180220-bye-iss-hello-private-stations  (accessed Aug 31, 2024)

14. https://www.geekwire.com/2021/blue-origin-teams-sierra-space-boeing-others-orbital-reef-space-station-project/

15. https://www.bloomberg.com/news/articles/2022-01-31/nasa-vet-and-space-mogul-aim-to-build-97-cheaper-space-station