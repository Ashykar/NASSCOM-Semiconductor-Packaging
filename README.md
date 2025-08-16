# NASSCOM-Semiconductor-Packaging

This GitHub repository documents the NASSCOM - Semiconductor Packaging - Fundamentals of Design and Testing 10-days Workshop offered by VSD Corp. Pvt. Ltd. attended from 15-24 August, 2025.

??????Imtroduction????

Module 1. Packaging Evolution: From Basics to 3D Integration

??????Description????

1.1 - Introduction To Semiconductor Packaging And Industry Overview



<img width="1894" height="1020" alt="image" src="https://github.com/user-attachments/assets/239ccd20-dd39-4a3c-8e89-6c8986ae6ced" />


A die, also known as an integrated circuit die or semiconductor die, is a small block of semiconducting material (typically silicon) on which a functional electronic circuit is fabricated. It represents the bare, unpackaged chip that contains the core components like transistors, diodes, resistors, and interconnects. Dies are produced in large batches on a silicon wafer during fabrication, then diced (cut) into individual units. 


A semiconductor foundry, often called a "fab" (short for fabrication plant), is a specialized manufacturing facility that produces integrated circuits and semiconductor chips based on designs provided by other companies. Foundries focus solely on the fabrication process and do not typically design the chips themselves. Foundries invest in advanced equipment and processes to manufacture at scale.


Semiconductor packaging is the process of enclosing a bare semiconductor die (or multiple dies) in a protective casing to create a functional, reliable component. Packaging also impacts the overall power efficiency, size, cost, and functionality of the final device.


It serves multiple purposes: 

protecting the delicate die from mechanical damage, chemical corrosion, and environmental factors; 

providing electrical interconnections to external circuits; and managing heat dissipation for optimal performance. 

Semiconductor packages vary based on factors like pin count, size, mounting method (through-hole or surface-mount), and application needs . 



Semiconductor package, its key components and their roles in protecting and connecting the die :

Die: The central semiconductor chip containing the integrated circuit. It’s the functional core where transistors and other components are fabricated on a silicon substrate. In the image, it’s shown as the dark rectangular block.

Die Attach: The adhesive or material (often a conductive or non-conductive epoxy) used to mount the die securely onto the substrate. This ensures mechanical stability and proper heat transfer. In the image, it’s the layer between the die and substrate.

Wire Bond: Thin wires (typically gold or copper) that electrically connect the die’s bond pads to the substrate’s traces. These wires allow signals and power to move between the die and the external circuit. In the image, they are the curved yellow lines extending from the die to the substrate.

Molding Compound: A protective encapsulant (usually epoxy resin) that surrounds the die and wire bonds, shielding them from moisture, dust, and mechanical damage. In the image, it’s the gray material encasing the die and wire bonds.

Substrate: The base layer (often made of ceramic, plastic, or a laminate like FR-4) that supports the die and provides electrical routing. It includes traces and contact points for external connections. In the image, it’s the green layer with metal contacts at the bottom.

Trace: Conductive pathways (usually copper) on the substrate that route electrical signals from the wire bonds to the package’s external terminals (e.g., solder balls or pins). In the image, these are the thin lines within the substrate.

Together, these components form a packaged semiconductor device, such as a DIP (Dual In-line Package), SOP (Small Outline Package), QFP (Quad Flat Package), BGA (Ball Grid Array), CSP (Chip Scale Package), QFN (Quad Flat No-leads), PGA (Pin Grid Array), WLP (Wafer-Level Package), 3D IC/Stacked Packages ,e.t.c ready for integration into electronic systems. 


<img width="1907" height="1060" alt="image" src="https://github.com/user-attachments/assets/4eadf233-d00f-42ff-a4ae-32d14c5ddfa1" />

Ref: SK Hynix Newsroom: Semiconductor Back-End Process Episode 1


Overview of the Semiconductor Supply Chain

The process involves multiple types of companies collaborating to produce a finished semiconductor product:

IDM (Integrated Device Manufacturer): Companies like Intel, Samsung, Micron, Renesas, SK Hynix, TI, and ST Micro that design, manufacture, and test their own chips in-house.

Fabless: Design-centric companies like Qualcomm, Nvidia, AMD, Apple, MediaTek, and others that focus on chip design but outsource manufacturing and testing to foundries and OSATs.

Foundry: Specialized manufacturers (e.g., TSMC, GlobalFoundries) that produce wafers based on designs from fabless companies.

OSAT (Outsourced Semiconductor Assembly and Test): Companies like ASE, Amkor, JCET, PTI, UTAC, and TSMC that handle packaging and testing. 


Stages of the Back-End Process


Design: The initial stage where the semiconductor circuit is conceptualized and designed by fabless or IDM companies. This involves creating the blueprint for the integrated circuit.


Wafer Process: Involves manufacturing the silicon wafers where multiple dies (individual chips) are fabricated. Conducted by foundries using advanced lithography and doping techniques.


Package & Test: A critical stage where the bare dies are packaged and tested for functionality.


Sub-stages include:


Wafer Test: Individual dies on the wafer are tested for defects to ensure they meet performance standards.

Package: The tested dies are encapsulated in protective packages.

Package Test: The packaged chips undergo final testing to verify reliability and performance under various conditions.


Assembly: The final stage where the packaged chips are integrated into the final product (e.g., mounted on a PCB for devices like smartphones or computers). This step is often handled by OSATs or system integrators.



1.2 - Understanding Package Requirements And Foundational Package Types


1.2.1 - Package Requirements



<img width="1917" height="948" alt="image" src="https://github.com/user-attachments/assets/c8c189e1-0fe7-4db0-85db-1de8bbac3479" />


The package requirements revolve around selecting a design that matches the chip's functionality, provides adequate connectivity, manages heat, fits the physical space, ensures long-term reliability, and remains cost-effective. The choice of package type (e.g., BGA, QFN, DIP) depends on optimizing these factors for the intended application. The package requirements must ensure compatibility and efficient integration at each level , the chip (the die and its immediate packaging), the package (enclosing the chip with interconnects), and the board (the PCB where the package is mounted).


The key factors to consider when choosing the right semiconductor package, which directly inform the package requirements can be summarized as follows:

Application (e.g., logic/memory/power): The package must be tailored to the specific function of the chip, such as logic (e.g., microprocessors), memory (e.g., DRAM), or power management. This influences the package type (e.g., BGA for high-density logic, QFN for power ICs) and its design to support the chip's operational requirements.


Pin Count (I/O pins): The package must accommodate the required number of input/output pins to connect the chip to the board. Higher pin counts (e.g., for complex CPUs) may necessitate packages like BGA or QFP, ensuring sufficient electrical connectivity without compromising space.


Thermal Dissipation: The package must effectively manage heat generated by the chip, especially for high-performance applications. This requires features like heat spreaders, thermal vias, or exposed pads (e.g., in QFN packages) to transfer heat to the board or external cooling solutions.


Form Factor: The package size and shape must align with the board's layout and the device's physical constraints. Compact packages like CSP or WLP are required for space-limited applications (e.g., smartphones), while larger packages like DIP may suit prototyping or industrial uses.


Reliability and Durability: The package must withstand environmental stresses (e.g., temperature fluctuations, humidity, mechanical shock) over its lifecycle. This involves using robust materials (e.g., epoxy molding compounds) and designs that prevent delamination or wire bond failure.


Cost: The package design must balance performance with manufacturing and material costs. Simpler packages (e.g., SOP) may be chosen for cost-sensitive applications, while advanced packages (e.g., 3D IC) may be justified for high-value products despite higher costs.



1.2.2 - Typical Package Structure


<img width="1913" height="1060" alt="image" src="https://github.com/user-attachments/assets/1e709782-9d62-4cc1-9e10-b35631a4d11b" />


The layered structure with three main levels and their interconnections:

Mold Compound: The top layer, typically an epoxy resin, that encapsulates the die and protects it from environmental factors like moisture and mechanical stress.

Die: The semiconductor chip containing the integrated circuit, positioned within the mold compound.

Carrier: The substrate or base (e.g., leadframe, laminate, plastic, ceramic, organic RDL, silicon, glass) that supports the die and provides a platform for interconnections.

Die-to-Carrier Interconnections: Connections between the die and carrier, which can be implemented using options like wirebond or bump/solder (e.g., flip-chip technology).

Carrier to Board Interconnections: Links from the carrier to the system board (PCB), enabling the package to interface with the broader electronic system.

System Board (PCB): The base layer where the package is mounted, providing electrical connectivity to other components.



Options for Materials and Interconnections

Options for Carrier: Includes leadframe, laminate, plastic, ceramic, organic redistribution layer (RDL), silicon, or glass, chosen based on cost, thermal performance, and application needs.


Options for Interconnections:

Wirebond: Thin wires (e.g., gold or copper) using curved connections connecting the die to the carrier, as shown in the detailed inset.

Bump/Solder: Solder balls or bumps (e.g., in flip-chip or BGA packages) using direct vertical links, for direct die-to-carrier or carrier-to-board connections, also depicted in the inset with epoxy underfill for stability and structural integrity.



Package Types

The variety of packages reflects different trade-offs in size, pin count, thermal management, and manufacturing complexity, catering to applications from simple transistors to advanced AI chips.

Through-hole Mounting:

DIP (Dual In-line Package): Rectangular with two parallel rows of pins for through-hole mounting.

TO (Transistor Outline): Cylindrical or flat packages for discrete components like transistors.

PGA (Pin Grid Array): Square with an array of pins on the bottom for socketed connections.



Surface Mount Technology (SMT):

QFN (Quad Flat No-leads): Flat package with exposed pads on the bottom for surface mounting.

QFPP (Quad Flat Package): Similar to QFN but with extended leads on all four sides.

CSP (Chip Scale Package): Ultra-compact, nearly the size of the die itself.

PBGA (Plastic Ball Grid Array): Uses a plastic substrate with an array of solder balls.

LGA (Land Grid Array): Flat contacts instead of balls, used in high-performance CPUs.

PoP (Package on Package): Stacks packages vertically for memory and logic integration.

MCM (Multi-Chip Module) - Intel Broadwell: Integrates multiple dies in one package for higher density.

CoWoS (Chip on Wafer on Substrate) - Nvidia H100: Advanced 3D packaging with multiple chips on a silicon interposer, used in high-performance GPUs like the Nvidia H100.



1.3 - Evolving Package Architectures - From Single Chip To Multi-Chip Modules


1.3.1 Anatomy of Semiconductor Packages



<img width="1891" height="1060" alt="image" src="https://github.com/user-attachments/assets/e14c1f95-fd1f-4ac1-896f-d7bf639437be" />


This anatomy showcases how package design evolves with technological demands, balancing cost, size, and performance. Semiconductor package structures, categorized by the type of substrate used: Leadframe, Laminate, and Advanced package substrates. 


Leadframe Packages


Leadframe packages use a metal frame (typically copper or alloy) as the substrate, with leads extending outward for electrical connections. Key examples include:


DIP (Dual In-line Package): Features two parallel rows of pins, with a polymer overmold and gold wirebonds connecting the silicon die to the leadframe.

QFN (Quad Flat No-leads): A flat package with exposed pads on the bottom, using gold wirebonds and a die pad for mounting.

Leadframe-CSP (Chip Scale Package): A compact version with gold molding and wire connections, optimized for small form factors.

Leadframe-QFP (Quad Flat Package): A square package with leads on all four sides, using gold wirebonds and a robust leadframe structure.



Laminate Packages


Laminate packages use a multilayer organic substrate (e.g., epoxy-based laminates) for higher density and performance. Key examples include:


Wire Bond PBGA (Plastic Ball Grid Array): Features a mold compound encapsulating the die, with gold wirebonds connecting to a laminate substrate, and an array of solder balls for board attachment.

Flip Chip PBGA: Uses flip-chip technology where the die is flipped and connected via solder bumps (with epoxy underfill) to the laminate substrate, improving performance and reducing size.

LGA (Land Grid Array): A flat package with contact pads instead of balls, mounted directly onto the board.

FC-CSP (Flip Chip Chip Scale Package): A compact flip-chip design with solder bumps on a laminate substrate, ideal for space-constrained applications.



Advanced Package Substrates


Advanced packages incorporate sophisticated substrates and 3D integration techniques for high-performance applications. They are categorized into 2D, 2.1D, 2.3D, and 2.5D configurations:

2D: Multiple dies (e.g., Die 1, Die 2) mounted side by side on an FCBGA (Flip Chip Ball Grid Array) substrate, connected via traditional methods.

2.1D: Similar to 2D but includes an organic interposer layer between the dies and FCBGA substrate for improved connectivity.

2.3D: Uses a silicon interposer to stack dies vertically, enhancing density and performance, mounted on an FCBGA substrate.

2.5D: An advanced example like CoWoS (Chip on Wafer on Substrate), featuring a silicon interposer with high-bandwidth memory (HBM), a system-on-chip (SoC), and hybrid bonding, all on a substrate. This is exemplified by the Nvidia H100 GPU.


The advanced packaging technologies like CoWoS (Chip on Wafer on Substrate) or similar 2.5D/3D IC designs, as seen in products like the Nvidia H100. The use of an interposer allows for the integration of multiple heterogeneous dies (SoC and HBM) in a compact form factor, optimizing performance for data-intensive applications. The labeled components provide insight into its layered architecture.


SoC (System on Chip): The top layer consists of one or more System on Chip dies. The SoC integrates various functions (e.g., CPU, GPU, memory controllers) onto a single chip, forming the core processing unit of the package.

HBM (High-Bandwidth Memory): Adjacent to the SoC, this layer includes multiple HBM dies. HBM is a high-performance RAM technology that provides extremely fast data transfer rates, stacked vertically to maximize bandwidth and efficiency, often used in graphics cards and AI accelerators.

Interposer: Positioned between the SoC/HBM layers and the substrate, the interposer is a silicon or organic layer with fine-pitch interconnects (e.g., through-silicon vias or TSVs). It facilitates high-density electrical connections between the SoC, HBM, and substrate, enabling efficient communication and reducing signal latency.

Substrate: The base layer, typically a laminate or advanced organic material, connects the interposer to the system board (PCB). It provides mechanical support and routes electrical signals to external pins or balls (e.g., in a BGA package), ensuring integration with the broader electronic system.



1.4 - Interposers, RDLs And 2.5D/3D Packaging Approaches


<img width="1898" height="1025" alt="image" src="https://github.com/user-attachments/assets/808cc61e-b573-46e3-b17e-964e473190a4" />



1.4.1 - Redistribution Layers (RDL): RDL (Redistribution Layer) is a metal layer added on top of a die or wafer to reroute the I/O pads to new locations. This enables more flexible bump layouts, especially important for fan-out packages or wafer-level chip scale packaging (WLCSP).


1.4.2 - Interposers: An interposer is a passive or active layer inserted between the die and the substrate, acting as an intermediate routing interface. It enables dense signal routing, power delivery, and die-to-die interconnect.

Types: Silicon, Organic, Glass

Functions: - Routes signals between multiple dies (e.g., chiplets) - Provides thermal expansion management - Enables high bandwidth communication

Passive vs. Active Interposers:

Passive: No logic, just routing and vias

Active: Includes power delivery, clocking, or even memory logic



1.4.3 - 2.5D/3D Integration

2.5D: Multiple dies (e.g., CPU + HBM) placed side-by-side on a common interposer. Interposer provides connectivity, not the substrate directly. Popular in HPC and AI (e.g., AMD Instinct, NVIDIA GPUs with HBM).
3D: Dies are stacked vertically, interconnected through Through-Silicon Vias (TSVs). 3D NAND, HBM memory stacks, logic-on-logic stacking.

The nomenclature progresses from single-chip (e.g., COB) to advanced multi-chip configurations (2D to 3D), reflecting increasing complexity and performance. Advanced packages (2.5D, 3D) leverage interposers and TSVs to integrate diverse components like SoCs and HBM, enabling high-bandwidth applications (e.g., AI, GPUs). The transition from package substrate to PCB underscores the integration into complete electronic systems.

1. Semiconductors (Regular, SoC, Chiplets etc.):

Single Chip: Refers to a package containing a single semiconductor die.

Example: COB (Chip on Board), shown as a single LED die mounted directly on a substrate, often used in lighting applications.

Multichip: Involves multiple dies or chiplets within a single package, categorized by interconnection methods:

Inorganic/Organic TSV-less Interposer: Uses through-silicon vias (TSVs) without an active interposer, relying on organic or inorganic materials.

Passive TSV Interposer: Incorporates passive TSVs in an interposer for vertical connections.

Active TSV Interposer: Features an active interposer with embedded circuitry for enhanced functionality.



2. Package Substrate (Carrier):

The intermediate layer that supports the semiconductor dies and facilitates connections. Package types are classified based on complexity and integration:

PBGA (Plastic Ball Grid Array): A basic multi-chip package with solder balls.

fcCSP (Flip Chip Chip Scale Package): Uses flip-chip technology for a compact, high-performance design.

2D: Multiple dies placed side by side on a single plane.

2.1D: Similar to 2D but with an interposer for improved connectivity.

2.3D: Incorporates a passive interposer with TSVs for vertical stacking.

2.5D: Uses an active interposer to integrate heterogeneous dies (e.g., SoC and HBM), as shown in the detailed inset with SoC, interposer, and substrate layers.

3D: Full 3D stacking of dies, maximizing density and performance.



Printed Circuit Board (PCB):

The base layer where the package is mounted, providing electrical and mechanical connectivity to the system. 



1.5 - Comparative Analysis And Selecting The Right Packaging Solution



The following table provides a comparison of the various IC package types and their typical applications:


<img width="1899" height="1046" alt="image" src="https://github.com/user-attachments/assets/7689b8b4-d4e5-4bbf-a9c8-74faf25c7c5d" />



Selecting the right semiconductor packaging depends on multiple criteria across performance, reliability, form factor and cost.



2 - From Wafer to Package: Assembly and Manufacturing Essentials

????Package Manufacturing Introduction????

2.1 - Setting The Stage - Supply Chain And Facilities


2.1.1 - Review of the supply chain


<img width="1909" height="1049" alt="image" src="https://github.com/user-attachments/assets/8b511ed7-a390-4fa1-9806-4f757653db56" />


This section outlines the structured workflow of semiconductor manufacturing process from design to final product assembly, highlighting key stages and the materials/equipment involved at each step. The process reflects a collaborative supply chain involving design houses, foundries, OSATs (Outsourced Semiconductor Assembly and Test), and system integrators. Testing occurs at multiple points (after packaging, board assembly, and product assembly) to ensure quality and reliability. 

Supply Chain Stages

The process is divided into five main stages, each supported by specific inputs:

1. Design House: The design phase involves creating the integrated circuit layout (GDSII file) and developing test protocols using specialized software and foundry-provided design kits. The image shows a complex IC design layout.

Inputs: EDA tools (Electronic Design Automation), foundry PDKs (Process Design Kits).

Output: IC Design (GDSII) and Test Program.


2. Wafer Fabrication: Silicon wafers with a grid of fabricated dies, such as the Apple A15 chip undergo processes like deposition, etching, and doping in a cleanroom to create multiple ICs. 

Inputs: Silicon wafers, equipment, gases, chemicals, materials.

Output: Wafer with fabricated ICs.


3. Package Assembly and Test: Fabricated dies are diced from the wafer, packaged (e.g., with substrates and lids), and tested for functionality for the next stage.

Inputs: Substrates, tools, materials, chemicals, lids.

Output: Individual ICs assembled in a package and tested.


4. Board Assembly and Test: Packaged ICs are mounted onto a PCB, along with other components, and the board is tested for performance.

Inputs: PCBs (Printed Circuit Boards), tools, materials.

Output: Many packages assembled on a board and tested.


5. Product Assembly and Test: The tested PCB is integrated into the final product (e.g., a smartphone), which undergoes final assembly and testing.

Inputs: Components, tools.

Output: Final product.


2.1.2 - Introduction to a Package Manufacturing Unit (ATMP)

The section provides an overview of a semiconductor package manufacturing unit, focusing on the ATMP process (Assembly, Testing, Marking, and Packaging). This is a critical back-end stage in semiconductor production where fabricated dies are assembled into functional packages, tested for quality, marked for identification, and prepared for shipment.


<img width="1912" height="1057" alt="image" src="https://github.com/user-attachments/assets/4a488c2c-2819-4061-9f60-c33fba37583a" />


Key Concepts

Process: ATMP (Assembly, Testing, Marking, and Packaging): This encompasses the steps to transform bare dies into protected, testable, and ready-to-use chips. It includes die attachment (e.g., bonding), encapsulation, electrical testing, reliability checks, marking (e.g., laser etching for traceability), and final packaging.


Organization: OSAT (Outsourced Semiconductor Assembly and Test): Specialized companies like ASE, Amkor, or TATA that handle ATMP for fabless or IDM firms. The ATMP process can also be performed in-house by integrated manufacturers such as Intel, TSMC, Micron, Samsung, or SK Hynix, allowing for greater control over quality and supply chain.

Flexibility: The ATMP can be outsourced to OSATs or integrated internally, depending on the company's model and scale.

Example: Micron ATMP Facility in Sanand, Gujarat

The facility has a total area of 1.4 million square feet, with a clean room area (ISO class 1000/10000) of 500,000 square feet. This setup ensures contamination-free environments for sensitive processes.
Source cited: Forbes India.

Updated Status (as of August 2025): The Micron ATMP facility in Sanand is nearing completion, with cleanroom validation currently underway for Phase 1. Construction, including civil, mechanical, electrical, and plumbing work, is expected to be handed over by Tata Projects to Micron by December 2025. Partial operations are anticipated to begin in late 2025 (December) or early 2026, with full-scale production potentially by December 2026. The plant is designed for a capacity of approximately 101.6 million units per month, representing a significant investment of INR 22,500 crores. This aligns with India's push into semiconductor manufacturing.

This layout emphasizes separation of clean and non-clean areas to minimize contamination risks, with cleanrooms (e.g., ISO 6/7) central to sensitive processes. A typical floor plan for an ATMP facility, divided into functional zones to optimize workflow, safety, and efficiency and is presented with the following sections:

Offices: Administrative areas for management, engineering, and quality control teams.

Material Preparation and Storage: Dedicated space for preparing and storing raw materials like substrates, dies, bonding wires, and encapsulation compounds. This ensures materials are handled in controlled conditions to prevent contamination.

Processing Zone (Clean Room: ISO Class 6 & 7): The core production area, maintained at high cleanliness standards (ISO Class 6 and 7, which allow limited particles per cubic meter). Key processes here include:

Die bonding: Attaching the die to the substrate.

Wire or flip-chip bonding: Creating electrical connections (e.g., using thin wires or solder bumps).

Encapsulation: Sealing the die with protective materials.

Flip-chip processes and RDL (Redistribution Layer) formation: For advanced packages, redistributing connections for better integration.


Testing Area: Zone for post-assembly validation, including:

Electrical tests: Checking functionality and performance.

Burn-in tests: Stress-testing under elevated temperatures and voltages to identify early failures.

Reliability chamber tests: Simulating real-world conditions (e.g., humidity, thermal cycling) to ensure durability.


Ware-house: Storage for finished packages, ready for shipping or further integration.

Utility and Maintenance Room: Houses support systems like power supplies, HVAC for cleanrooms, and maintenance equipment to keep the facility operational.


2.2 - Wafer Pre-Preparation - Grinding And Dicing


<img width="1911" height="1040" alt="image" src="https://github.com/user-attachments/assets/abbfc4d1-76f0-4aa0-b842-a84be64a4b32" />


2.2.1 Activities Inside the Cleanroom Area

The section describes the key processes in the wafer preparation area within a semiconductor cleanroom (ISO Class 7), which is part of the back-end manufacturing in an ATMP (Assembly, Testing, Marking, and Packaging) facility. This area focuses on preparing fabricated silicon wafers for die separation and packaging. The cleanroom maintains strict particle control (ISO Class 7 allows up to 352,000 particles ≥0.5 μm per cubic meter) to prevent contamination that could ruin the delicate integrated circuits.

The process starts with incoming wafer handling and inspection, then proceeds to protective lamination. It flows downward to dicing, mounting, and grinding steps. This preparation is crucial before dies are assembled into packages, as it transforms a full wafer into individual, thinned dies ready for bonding and encapsulation. The overall process in the cleanroom prepares dies for downstream assembly, testing, and packaging in OSAT facilities.

Step-by-Step Breakdown

1. Incoming Wafer Carrier: A stack of wafers arrive in sealed carriers (e.g., FOUPs or cassettes) to protect them from contamination during transport.
   
2. Wafer Inspection: The wafer is visually and automatically inspected for defects, cracks, or contamination using tools like optical microscopes or automated scanners. This ensures only viable wafers proceed, maximizing efficiency.

3. Wafer Front Tape Lamination: A protective tape is laminated onto the front (active) side of the wafer. This tape acts as a barrier to safeguard the circuit patterns and delicate structures from mechanical damage, debris, or chemicals during subsequent aggressive processes like grinding and dicing. Without it, the front side could be scratched or contaminated, leading to die failure and reduced yield.

4. Two-Step Wafer Dicing (Laser Grooving + Blade Dicing): The wafer is cut into individual dies using a hybrid method: first, laser grooving creates precise shallow cuts, followed by mechanical blade dicing to complete the separation. Modern wafers have thin, brittle layers and low-k dielectrics that are prone to chipping or cracking with traditional blade dicing alone. The two-step approach minimizes edge damage laser grooving provides clean, narrow kerfs (cuts) without physical contact, while blade dicing ensures full separation. This is essential for high-density chips to maintain structural integrity and electrical performance.

5. Tape Frame Mounting to Wafer Backside: The wafer's backside is mounted onto a dicing tape within a metal or plastic frame (ring frame). After initial preparation (e.g., lamination), this mounting provides mechanical support and stability for the wafer during dicing and handling. It holds the dies in place post-dicing, preventing them from scattering, and facilitates easy transfer to pick-and-place tools for assembly. Without this, thin wafers could warp or break, complicating automation and increasing defects.

6. Wafer Backside Grinding: The backside of the wafer is ground down using a spinning wheel and chuck table, with feeding direction and spindle. Wafers start thick (e.g., 775 μm) for stability during front-end fabrication but must be thinned (to 50-200 μm) for compact packaging, better heat dissipation, and 3D stacking in advanced devices. Grinding removes excess silicon, but without prior front-side protection (from lamination) or mounting, it could cause warping, cracking, or contamination.

   

2.3 - Wire Bond Packaging - Die Attach To Molding


The wire bond packaging process, a widely used technique in semiconductor packaging, focusing on the sequence from die attach to molding. This process is part of the back-end manufacturing in an ATMP (Assembly, Testing, Marking, and Packaging) facility and is conducted in a cleanroom environment. The below steps collectively transform a bare die into a robust, functional packaged IC, critical for downstream assembly onto PCBs and into final products. This process is common in cost-effective packages (e.g., QFN, SOP) and is suitable for a wide range of applications, from consumer electronics to automotive systems.


<img width="1883" height="1051" alt="image" src="https://github.com/user-attachments/assets/9be46684-b4ca-49c9-b6d0-2fe2cfb2134d" />


Wire Bond Packaging Process:

1. Die Attach: The silicon die, separated from the wafer, is attached to a substrate (e.g., leadframe or laminate) or a die pad using an adhesive material, such as epoxy. The die being placed onto a substrate with a dispensing nozzle applying adhesive. This step provides mechanical stability and a thermal/electrical pathway between the die and the package. A secure attachment prevents movement during subsequent processes (e.g., wire bonding, molding), ensures efficient heat dissipation, and, in some cases, establishes a ground connection if a conductive adhesive is used. Without proper die attach, the die could shift, leading to misalignment or electrical failure.

2. Curing: The die-attached unit is subjected to a heating process to cure the epoxy, ensuring a strong and stable bond between the die and the substrate.

3. Wire Bonding (Starting with Free Air Ball): Wire bonding connects the die's bond pads to the substrate or leadframe using thin wires (typically gold, copper, or aluminum). The process begins with the formation of a free air ball (FAB). A fine wire is fed through a capillary tool, and a high-voltage electric arc melts the wire tip to form a spherical FAB. The FAB is pressed onto the die's bond pad under heat and ultrasonic energy, creating a metallurgical bond (e.g., ball bond). The capillary then moves to the substrate, forming a wedge bond or stitch bond, and the wire is cut, completing the connection.
Wire bonding establishes electrical interconnections between the die and the external circuit, enabling signal and power transmission. Starting with a FAB ensures a strong, reliable initial bond due to its uniform shape, which maximizes contact area and adhesion strength. This step is critical for packages like QFN, DIP, or PBGA, where high-density connections are needed without compromising signal integrity.

4. Molding: The assembled die, wire bonds, and substrate are encapsulated with a mold compound (e.g., epoxy resin) using a transfer molding machine. Molding protects the die and wire bonds from environmental factors such as moisture, dust, mechanical stress, and thermal shock. It also provides structural integrity, preventing wire sweep or die damage during handling or operation. Without molding, the delicate internal components would be vulnerable, reducing the package's reliability and lifespan.

5. Marking: It involves applying identification details to the molded package using techniques like laser etching, ink printing, or stamping. The information such as part numbers, manufacturer logos, batch codes, or date codes is imprented on the top surface of the package after molding. Marking allows tracking of the IC through the supply chain, aiding in quality control, warranty claims, and recalls if defects are identified. It provides critical information for assembly lines, customers, and end-users to distinguish between different IC types or versions. Manufacturer logos or codes enhance brand recognition and authenticity. Without marking, it would be challenging to manage inventory or ensure the correct IC is used in specific applications, potentially leading to errors or counterfeit issues.

6. Singulation (Dicing Blade): Singulation separates individual packaged ICs from a panel or strip (e.g., a leadframe or substrate array) into standalone units. The sawing or punching machine cuts through the molded panel along pre-defined scribe lines. These techniques are chosen based on package type (e.g., QFN, BGA) and material.
