# Clemsom University / Team Clemsom CyberTigers

## Hardware
For this competition, we will be using a Raspberry Pi cluster with N nodes. Raspberry Pi’s are being used
due to budget constraints. Since we will be competing from Clemson and not going to the UCSD or TACC
hotspots, we will set up a livestream of a digital watt meter that our power strip is plugged into to be sure
we do not go above the 250W limit. For internet access, we will be dedicating a single IP on Clemson’s
eduroam network for external internet access, and setting up the rest of the Pi’s in a Beowulf
configuration such that internet traffic is routed through the head node to each individual device

| Component | Price | # of items | Total cost | Item Link |
|-----------|-------|------------|------------|------------|
| Raspberry Pi 4 | $35 | 20 | $700 | [Link](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) |
| NETGEAR 24-Port Gigabit Ethernet Unmanaged Switch (JGS524) | $149.99 | 1 | $149.99 | [Link](https://www.amazon.com/dp/B0002CWPW2?ref=cm_sw_r_cso_cp_apin_dp_30JAGVDZDR1Z9E3ZJR0B&ref_=cm_sw_r_cso_cp_apin_dp_30JAGVDZDR1Z9E3ZJR0B&social_share=cm_sw_r_cso_cp_apin_dp_30JAGVDZDR1Z9E3ZJR0B&starsLeft=1&th=1) |
| **Overall Total** | | | **$849.99** | |


## Software
Our Raspberry Pi’s will be running the latest version of Raspbian, since group members have the most
experience using it on these devices. The Raspberry Pi release of Rocky Linux was also considered, but
because we are not as familiar with it, we are sticking with Raspbian for this competition.

We have not yet settled on specific management tools for our cluster, but intend to use them because this
system has a high node count. The challenge we are dealing with is finding one that supports PXE boot
with ARM. The provisioner we use for our Student Cluster Competition system is xCAT, which does not
support iPXE with ARM. Online research suggests that Warewulf provides this capability, but we have not
confirmed this ourselves on a testbed yet. We currently do not have an Ansible repo or other cluster
management system, but instead do all our setup in postscripts after provisioning.

Our software stack will be managed with Spack. Our primary OpenMPI version will 5.0.3, since it is the
latest version and Spack preferred. In case of issues, we are prepared to install other versions to suit our
needs via Spack. Our linear algebra library will be the Spack preferred version of OpenBLAS, 0.3.26. This
is also subject to change if this version has problems when building any of the applications

## Strategy
To make sure we do well in this competition, our main strategy will involve being as prepared as possible
going in. The hardware we will be using is already in our possession, and we will stand up our cluster as
soon as possible. We know all the benchmarks in advance of the competition, and will have them all
running and optimized on our cluster before the start of the competition. Come April 10th, all we will have
to do is run a script to produce the required results. In case anything goes wrong, all team members will
be trained and have experience with each benchmark so they can assist with debugging.

Being able to execute the benchmarks quickly will free up time for us to work on the mystery application.
To learn, build and run a new application on the fly, team members will have opportunities to build various
popular HPC applications on the Pi Cluster so they build the necessary skills

## Team Details
Ethan is a senior (CPE) interested in various realms of computer science, including HPC. He has interned
at Hawkes' Learning in 2023 as a development intern for AI solutions to streamline company data,
learning valuable research and programming skills in the process. He attended SC24 as an alternate for
the Student Cluster Competition team. He will be the team captain of the Single Board Cluster
Competition (SBCC) for the 2025 competition. He has applied to partake in a Creative Inquiry over the
summer at Clemson as well as the SULI program. Ethan plans on graduating in 2026 and will pursue a
Master's degree shortly after.

Yagiz, a freshman majoring in Computer Engineering, is interested in the general hardware aspect of
computing. Yagiz was previously involved in a creative inquiry, which can be described as “Clemson
University’s unique combination of undergraduate research, experiential learning and cross-disciplinary
interactions.”. He participated in this creative inquiry during his first semester of freshman year,
specializing in the education of circuits and electronics. In that creative inquiry, Yagiz learned how to
solder and identify certain parts of electronic components. He wants to explore various opportunities
regarding projects, creative inquiries, research, and internships that will help him learn more about his
desired field of practice and contribute to a team. Yagiz wants to stay involved in the hardware and
electronics field for his future endeavors as he hopes to pursue a career in hardware engineering.

Jacob is a sophomore (CS) with a double math major interested in scientific computing. Jacob has
previously interned with Cadence Design Systems, working on computational software for hardware
verification, and he's currently interning with CU-ICAR for machine learning. Jacob is also researching
machine learning algorithms, taking graduate coursework in algorithm design and analysis, and plans to
pursue at least an M.S. degree after graduation.

Tolga is a freshman majoring in Computer Engineering and is interested in embedded software. Tolga has
participated in 2 creative inquiries: XR/VR development and PLM Processes and CAD/CAE Tools with
Application to Vehicle Component Design, where he developed a wireless dashboard system for a robotic
vehicle. Tolga also developed a plugin for MPV player (popular video player) that dynamically alternates
subtitle languages based on the user's language proficiency and is integrated with Anki (SRS flashcard
tool). Tolga is also working on building a 4-bit computer from individual transistors.

Benjamin is a senior computer engineering major, and is a veteran cluster competitor. He has competed
in the IndySCC in 2022, and the in person SCC in 2023 and 2024. Additionally, he has done two
internships at Los Alamos National lab in networking and data storage. He also is the system
administrator of a research cluster used by Jon Calhoun’s FTHPC lab and several others. Benjamin has
also done HPC research and presented at a workshop at SC23. After graduation, he will do the
accelerated Masters program at Clemson, and hopefully work full time at Los Alamos after that. As a
senior member of the team, he is looking forward to mentoring new students on the team.

Lane is a senior Computer Engineering major with plans to graduate in 2026. This is his third semester
involved with Clemson’s High-Performance Cluster Computing Creative Inquiry course, where he is
serving as a mentor to new students. He is currently striving to pursue as many means as possible as to
determine the branch of his major that he’d like to pursue as a career, with this competition and summer
research opportunities as a few of such means.

Chloe Crozier is a senior computer science major with minors in Math and Economics. She has interned
with the Navy as an automation engineer and at Deloitte as a Cloud Engineer. Chloe has been part of Jon
Calhoun’s HPC Creative Inquiry for one year and is completing her Departmental Honor thesis on cluster
security. Through this course, she competed in the Student Cluster Competition at SC24. After
graduation, Chloe accepted a full-time offer at NVIDIA to work as a Solutions Architect.

Camren Khoury is a senior dual major in Computer Engineering and Electrical Engineering. He has
interned with Athena Consulting Group in reference with the Department of Defense as a cyber security
Intern. This is his first semester in the creative inquiry. His other projects include microcontroller based
solutions using microcontrollers and microcomputers such as Raspberry Pis, ESP32s, and STM32s. As a
career he hopes to go into embedded systems and/or hardware engineering
