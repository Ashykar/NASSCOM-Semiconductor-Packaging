# NASSCOM-Semiconductor-Packaging

This GitHub repository documents the [NASSCOM - Semiconductor Packaging - Fundamentals of Design and Testing 10-days Workshop](https://www.vlsisystemdesign.com/packaging/) offered by [VSD Corp. Pvt. Ltd.](https://www.vlsisystemdesign.com/about-us/) attended from 15-24 August, 2025.

https://github.com/Ashykar/NASSCOM-Semiconductor-Packaging/blob/main/README.md#55---applying-mold-compound-and-finalizing-the-package-model

??????Imtroduction????

## Table of Contents

| Module # | Topic(s) Covered | Status |
|----------|------------------|--------|
| [Module 1](#module-1-packaging-evolution-from-basics-to-3d-integration) | **Packaging Evolution: From Basics to 3D Integration**<br>1. [Introduction To Semiconductor Packaging And Industry Overview](#11---introduction-to-semiconductor-packaging-and-industry-overview-)<br>2. [Understanding Package Requirements And Foundational Package Types](#12---understanding-package-requirements-and-foundational-package-types)<br>3. [Evolving Package Architectures - From Single Chip To Multi-Chip Modules](#13---evolving-package-architectures---from-single-chip-to-multi-chip-modules)<br>4. [Interposers Re-distribution Layers And 2.5D/3D Packaging Approaches](#14---interposers-re-distribution-layers-and-25d3d-packaging-approaches)<br>5. [Comparative Analysis And Selecting The Right Packaging Solution](#15---comparative-analysis-and-selecting-the-right-packaging-solution) | <img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/9768417d-9351-4e4d-b293-5d0490a1225c" /> |
| [Module 2](#2---from-wafer-to-package-assembly-and-manufacturing-essentials) | **From Wafer to Package: Assembly and Manufacturing Essentials**<br>1. [Setting The Stage - Supply Chain And Facilities](#21---setting-the-stage---supply-chain-and-facilities)<br>2. [Wafer Pre-Preparation - Grinding And Dicing](#22---wafer-pre-preparation---grinding-and-dicing)<br>3. [Wire Bond Packaging – Die Attach To Molding](#23---wire-bond-packaging---die-attach-to-molding)<br>4. [Flip Chip Assembly – Bump Formation And Underfill](#24---flip-chip-assembly---bump-formation-and-underfill)<br>5. [Wafer Level Packaging And Conclusion](#25---wafer-level-packaging-and-conclusion) | <img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/9768417d-9351-4e4d-b293-5d0490a1225c" /> |
| [Module 3](#3---labs-thermal-simulation-of-semiconductor-packages-with-ansys-tools) | **Labs: Thermal Simulation of Semiconductor Packages with ANSYS**<br>1. [Introduction And Getting Started With ANSYS Electronics Desktop](#31---introduction-and-getting-started-with-ansys-electronics-desktop)<br>2. [Setting Up A Flip-Chip BGA Package](#32---setting-up-a-flip-chip-bga-package)<br>3. [Material Definitions And Thermal Power Sources](#33---material-definitions-and-thermal-power-sources)<br>4. [Meshing And Running The Thermal Analysis](#34---meshing-and-running-the-thermal-analysis)<br>5. [Viewing Results And Exploring Other Package Types](#35---viewing-results-and-exploring-other-package-types) | <img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/9768417d-9351-4e4d-b293-5d0490a1225c" /> |
| [Module 4](#4---ensuring-package-reliability-testing-and-performance-validation) | **Ensuring Package Reliability: Testing and Performance Validation**<br>1. [Introduction to Package Testing and Electrical Functionality Checks](#41---introduction-to-package-testing-and-electrical-functionality-checks)<br>2. [Reliability and Performance Testing of Semiconductor Packages](#42---reliability-and-performance-testing-of-semiconductor-packages) | <img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/9768417d-9351-4e4d-b293-5d0490a1225c" /> |
| [Module 5](#5---package-design-and-modeling-building-a-semiconductor-package-from-scratch) | **Package Design and Modeling: Building a Semiconductor Package from Scratch**<br>1. [Introduction to Package Cross - Section Modeling in ANSYS Electronics Desktop (AEDT)](#51---introduction-to-package-cross---section-modeling-in-ansys-electronics-desktop-aedt)<br>2. [Creating the Die and Substrate in AEDT](#52---creating-the-die-and-substrate-in-aedt)<br>3. [Adding Die Attach Material and Bond Pads](#53---adding-die-attach-material-and-bond-pads)<br>4. [Wire Bond Creation and Material Assignment](#54---wire-bond-creation-and-material-assignment)<br>5. [Applying Mold Compound and Finalizing the Package Model](#55---applying-mold-compound-and-finalizing-the-package-model) | <img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/9768417d-9351-4e4d-b293-5d0490a1225c" /> |
---
Adding Die Attach Material and Bond Pads
## Module 1. Packaging Evolution: From Basics to 3D Integration

??????Description????

### 1.1 - Introduction To Semiconductor Packaging And Industry Overview <br><br>

<img width="1894" height="1020" alt="image" src="https://github.com/user-attachments/assets/239ccd20-dd39-4a3c-8e89-6c8986ae6ced" /> <br><br>

A die, also known as an integrated circuit die or semiconductor die, is a small block of semiconducting material (typically silicon) on which a functional electronic circuit is fabricated. It represents the bare, unpackaged chip that contains the core components like transistors, diodes, resistors, and interconnects. Dies are produced in large batches on a silicon wafer during fabrication, then diced (cut) into individual units. 

A semiconductor foundry, often called a "fab" (short for fabrication plant), is a specialized manufacturing facility that produces integrated circuits and semiconductor chips based on designs provided by other companies. Foundries focus solely on the fabrication process and do not typically design the chips themselves. Foundries invest in advanced equipment and processes to manufacture at scale.

Semiconductor packaging is the process of enclosing a bare semiconductor die (or multiple dies) in a protective casing to create a functional, reliable component. Packaging also impacts the overall power efficiency, size, cost, and functionality of the final device.

It serves multiple purposes: 

* protecting the delicate die from mechanical damage, chemical corrosion, and environmental factors; 

* providing electrical interconnections to external circuits; and managing heat dissipation for optimal performance. 

* Semiconductor packages vary based on factors like pin count, size, mounting method (through-hole or surface-mount), and application needs . 

Semiconductor package, its key components and their roles in protecting and connecting the die :

* Die: The central semiconductor chip containing the integrated circuit. It’s the functional core where transistors and other components are fabricated on a silicon substrate. In the image, it’s shown as the dark rectangular block.

* Die Attach: The adhesive or material (often a conductive or non-conductive epoxy) used to mount the die securely onto the substrate. This ensures mechanical stability and proper heat transfer. In the image, it’s the layer between the die and substrate.

* Wire Bond: Thin wires (typically gold or copper) that electrically connect the die’s bond pads to the substrate’s traces. These wires allow signals and power to move between the die and the external circuit. In the image, they are the curved yellow lines extending from the die to the substrate.

* Molding Compound: A protective encapsulant (usually epoxy resin) that surrounds the die and wire bonds, shielding them from moisture, dust, and mechanical damage. In the image, it’s the gray material encasing the die and wire bonds.

* Substrate: The base layer (often made of ceramic, plastic, or a laminate like FR-4) that supports the die and provides electrical routing. It includes traces and contact points for external connections. In the image, it’s the green layer with metal contacts at the bottom.

* Trace: Conductive pathways (usually copper) on the substrate that route electrical signals from the wire bonds to the package’s external terminals (e.g., solder balls or pins). In the image, these are the thin lines within the substrate.

* Together, these components form a packaged semiconductor device, such as a DIP (Dual In-line Package), SOP (Small Outline Package), QFP (Quad Flat Package), BGA (Ball Grid Array), CSP (Chip Scale Package), QFN (Quad Flat No-leads), PGA (Pin Grid Array), WLP (Wafer-Level Package), 3D IC/Stacked Packages ,e.t.c ready for integration into electronic systems. <br><br>

<img width="1907" height="1060" alt="image" src="https://github.com/user-attachments/assets/4eadf233-d00f-42ff-a4ae-32d14c5ddfa1" />

Ref: SK Hynix Newsroom: Semiconductor Back-End Process Episode 1

Overview of the Semiconductor Supply Chain

The process involves multiple types of companies collaborating to produce a finished semiconductor product:

* IDM (Integrated Device Manufacturer): Companies like Intel, Samsung, Micron, Renesas, SK Hynix, TI, and ST Micro that design, manufacture, and test their own chips in-house.

* Fabless: Design-centric companies like Qualcomm, Nvidia, AMD, Apple, MediaTek, and others that focus on chip design but outsource manufacturing and testing to foundries and OSATs.

* Foundry: Specialized manufacturers (e.g., TSMC, GlobalFoundries) that produce wafers based on designs from fabless companies.

* OSAT (Outsourced Semiconductor Assembly and Test): Companies like ASE, Amkor, JCET, PTI, UTAC, and TSMC that handle packaging and testing. 


Stages of the Back-End Process


* Design: The initial stage where the semiconductor circuit is conceptualized and designed by fabless or IDM companies. This involves creating the blueprint for the integrated circuit.

* Wafer Process: Involves manufacturing the silicon wafers where multiple dies (individual chips) are fabricated. Conducted by foundries using advanced lithography and doping techniques.

* Package & Test: A critical stage where the bare dies are packaged and tested for functionality.


Sub-stages include:


* Wafer Test: Individual dies on the wafer are tested for defects to ensure they meet performance standards.

* Package: The tested dies are encapsulated in protective packages.

* Package Test: The packaged chips undergo final testing to verify reliability and performance under various conditions.

* Assembly: The final stage where the packaged chips are integrated into the final product (e.g., mounted on a PCB for devices like smartphones or computers). This step is often handled by OSATs or system         integrators.


### 1.2 - Understanding Package Requirements And Foundational Package Types


#### 1.2.1 - Package Requirements<br><br>

<img width="1917" height="948" alt="image" src="https://github.com/user-attachments/assets/c8c189e1-0fe7-4db0-85db-1de8bbac3479" /><br><br>

The package requirements revolve around selecting a design that matches the chip's functionality, provides adequate connectivity, manages heat, fits the physical space, ensures long-term reliability, and remains cost-effective. The choice of package type (e.g., BGA, QFN, DIP) depends on optimizing these factors for the intended application. The package requirements must ensure compatibility and efficient integration at each level , the chip (the die and its immediate packaging), the package (enclosing the chip with interconnects), and the board (the PCB where the package is mounted).


The key factors to consider when choosing the right semiconductor package, which directly inform the package requirements can be summarized as follows:

* Application (e.g., logic/memory/power): The package must be tailored to the specific function of the chip, such as logic (e.g., microprocessors), memory (e.g., DRAM), or power management. This influences the    package type (e.g., BGA for high-density logic, QFN for power ICs) and its design to support the chip's operational requirements.

* Pin Count (I/O pins): The package must accommodate the required number of input/output pins to connect the chip to the board. Higher pin counts (e.g., for complex CPUs) may necessitate packages like BGA or      QFP, ensuring sufficient electrical connectivity without compromising space.

* Thermal Dissipation: The package must effectively manage heat generated by the chip, especially for high-performance applications. This requires features like heat spreaders, thermal vias, or exposed pads       (e.g., in QFN packages) to transfer heat to the board or external cooling solutions.

* Form Factor: The package size and shape must align with the board's layout and the device's physical constraints. Compact packages like CSP or WLP are required for space-limited applications (e.g., smart        phones), while larger packages like DIP may suit prototyping or industrial uses.

* Reliability and Durability: The package must withstand environmental stresses (e.g., temperature fluctuations, humidity, mechanical shock) over its lifecycle. This involves using robust materials (e.g., epoxy   molding compounds) and designs that prevent delamination or wire bond failure.
  
* Cost: The package design must balance performance with manufacturing and material costs. Simpler packages (e.g., SOP) may be chosen for cost-sensitive applications, while advanced packages (e.g., 3D IC) may     be justified for high-value products despite higher costs.


#### 1.2.2 - Typical Package Structure <br><br>

<img width="1913" height="1060" alt="image" src="https://github.com/user-attachments/assets/1e709782-9d62-4cc1-9e10-b35631a4d11b" /><br><br>


The layered structure with three main levels and their interconnections:

* Mold Compound: The top layer, typically an epoxy resin, that encapsulates the die and protects it from environmental factors like moisture and mechanical stress.

* Die: The semiconductor chip containing the integrated circuit, positioned within the mold compound.

* Carrier: The substrate or base (e.g., leadframe, laminate, plastic, ceramic, organic RDL, silicon, glass) that supports the die and provides a platform for interconnections.

* Die-to-Carrier Interconnections: Connections between the die and carrier, which can be implemented using options like wirebond or bump/solder (e.g., flip-chip technology).

* Carrier to Board Interconnections: Links from the carrier to the system board (PCB), enabling the package to interface with the broader electronic system.

* System Board (PCB): The base layer where the package is mounted, providing electrical connectivity to other components.


Options for Materials and Interconnections

* Options for Carrier: Includes leadframe, laminate, plastic, ceramic, organic redistribution layer (RDL), silicon, or glass, chosen based on cost, thermal performance, and application needs.


Options for Interconnections:

* Wirebond: Thin wires (e.g., gold or copper) using curved connections connecting the die to the carrier, as shown in the detailed inset.

* Bump/Solder: Solder balls or bumps (e.g., in flip-chip or BGA packages) using direct vertical links, for direct die-to-carrier or carrier-to-board connections, also depicted in the inset with epoxy underfill    for stability and structural integrity.


Package Types

The variety of packages reflects different trade-offs in size, pin count, thermal management, and manufacturing complexity, catering to applications from simple transistors to advanced AI chips.

Through-hole Mounting:

* DIP (Dual In-line Package): Rectangular with two parallel rows of pins for through-hole mounting.

* TO (Transistor Outline): Cylindrical or flat packages for discrete components like transistors.

* PGA (Pin Grid Array): Square with an array of pins on the bottom for socketed connections.


Surface Mount Technology (SMT):

* QFN (Quad Flat No-leads): Flat package with exposed pads on the bottom for surface mounting.

* QFPP (Quad Flat Package): Similar to QFN but with extended leads on all four sides.

* CSP (Chip Scale Package): Ultra-compact, nearly the size of the die itself.

* PBGA (Plastic Ball Grid Array): Uses a plastic substrate with an array of solder balls.

* LGA (Land Grid Array): Flat contacts instead of balls, used in high-performance CPUs.

* PoP (Package on Package): Stacks packages vertically for memory and logic integration.

* MCM (Multi-Chip Module) - Intel Broadwell: Integrates multiple dies in one package for higher density.

* CoWoS (Chip on Wafer on Substrate) - Nvidia H100: Advanced 3D packaging with multiple chips on a silicon interposer, used in high-performance GPUs like the Nvidia H100.


### 1.3 - Evolving Package Architectures - From Single Chip To Multi-Chip Modules


#### 1.3.1 Anatomy of Semiconductor Packages<br><br>

<img width="1891" height="1060" alt="image" src="https://github.com/user-attachments/assets/e14c1f95-fd1f-4ac1-896f-d7bf639437be" /><br><br>

This anatomy showcases how package design evolves with technological demands, balancing cost, size, and performance. Semiconductor package structures, categorized by the type of substrate used: Leadframe, Laminate, and Advanced package substrates. 


Leadframe Packages

Leadframe packages use a metal frame (typically copper or alloy) as the substrate, with leads extending outward for electrical connections. 
Key examples include:

* DIP (Dual In-line Package): Features two parallel rows of pins, with a polymer overmold and gold wirebonds connecting the silicon die to the leadframe.
  
* QFN (Quad Flat No-leads): A flat package with exposed pads on the bottom, using gold wirebonds and a die pad for mounting.

* Leadframe-CSP (Chip Scale Package): A compact version with gold molding and wire connections, optimized for small form factors.

* Leadframe-QFP (Quad Flat Package): A square package with leads on all four sides, using gold wirebonds and a robust leadframe structure.


Laminate Packages

Laminate packages use a multilayer organic substrate (e.g., epoxy-based laminates) for higher density and performance. Key examples include:

* Wire Bond PBGA (Plastic Ball Grid Array): Features a mold compound encapsulating the die, with gold wirebonds connecting to a laminate substrate, and an array of solder balls for board attachment.

* Flip Chip PBGA: Uses flip-chip technology where the die is flipped and connected via solder bumps (with epoxy underfill) to the laminate substrate, improving performance and reducing size.

* LGA (Land Grid Array): A flat package with contact pads instead of balls, mounted directly onto the board.

* FC-CSP (Flip Chip Chip Scale Package): A compact flip-chip design with solder bumps on a laminate substrate, ideal for space-constrained applications.


Advanced Package Substrates

Advanced packages incorporate sophisticated substrates and 3D integration techniques for high-performance applications. They are categorized into 2D, 2.1D, 2.3D, and 2.5D configurations:

* 2D: Multiple dies (e.g., Die 1, Die 2) mounted side by side on an FCBGA (Flip Chip Ball Grid Array) substrate, connected via traditional methods.

* 2.1D: Similar to 2D but includes an organic interposer layer between the dies and FCBGA substrate for improved connectivity.

* 2.3D: Uses a silicon interposer to stack dies vertically, enhancing density and performance, mounted on an FCBGA substrate.

* 2.5D: An advanced example like CoWoS (Chip on Wafer on Substrate), featuring a silicon interposer with high-bandwidth memory (HBM), a system-on-chip (SoC), and hybrid bonding, all on a substrate. This is        exemplified by the Nvidia H100 GPU.

The advanced packaging technologies like CoWoS (Chip on Wafer on Substrate) or similar 2.5D/3D IC designs, as seen in products like the Nvidia H100. The use of an interposer allows for the integration of multiple heterogeneous dies (SoC and HBM) in a compact form factor, optimizing performance for data-intensive applications. The labeled components provide insight into its layered architecture.

* SoC (System on Chip): The top layer consists of one or more System on Chip dies. The SoC integrates various functions (e.g., CPU, GPU, memory controllers) onto a single chip, forming the core processing unit of the package.

* HBM (High-Bandwidth Memory): Adjacent to the SoC, this layer includes multiple HBM dies. HBM is a high-performance RAM technology that provides extremely fast data transfer rates, stacked vertically to maximize bandwidth and efficiency, often used in graphics cards and AI accelerators.

* Interposer: Positioned between the SoC/HBM layers and the substrate, the interposer is a silicon or organic layer with fine-pitch interconnects (e.g., through-silicon vias or TSVs). It facilitates high-density electrical connections between the SoC, HBM, and substrate, enabling efficient communication and reducing signal latency.

* Substrate: The base layer, typically a laminate or advanced organic material, connects the interposer to the system board (PCB). It provides mechanical support and routes electrical signals to external pins or balls (e.g., in a BGA package), ensuring integration with the broader electronic system.


### 1.4 - Interposers Re-distribution Layers And 2.5D/3D Packaging Approaches<br><br>

<img width="1898" height="1025" alt="image" src="https://github.com/user-attachments/assets/808cc61e-b573-46e3-b17e-964e473190a4" /><br><br>

#### 1.4.1 - Redistribution Layers (RDL)

RDL (Redistribution Layer) is a metal layer added on top of a die or wafer to reroute the I/O pads to new locations. This enables more flexible bump layouts, especially important for fan-out packages or wafer-level chip scale packaging (WLCSP).

#### 1.4.2 - Interposers

An interposer is a passive or active layer inserted between the die and the substrate, acting as an intermediate routing interface. It enables dense signal routing, power delivery, and die-to-die interconnect.

Types: Silicon, Organic, Glass

Functions: Routes signals between multiple dies (e.g., chiplets) - Provides thermal expansion management - Enables high bandwidth communication

Passive vs. Active Interposers

Passive: No logic, just routing and vias

Active: Includes power delivery, clocking, or even memory logic


#### 1.4.3 - 2.5D/3D Integration

2.5D: Multiple dies (e.g., CPU + HBM) placed side-by-side on a common interposer. Interposer provides connectivity, not the substrate directly. Popular in HPC and AI (e.g., AMD Instinct, NVIDIA GPUs with HBM).
3D: Dies are stacked vertically, interconnected through Through-Silicon Vias (TSVs). 3D NAND, HBM memory stacks, logic-on-logic stacking.

The nomenclature progresses from single-chip (e.g., COB) to advanced multi-chip configurations (2D to 3D), reflecting increasing complexity and performance. Advanced packages (2.5D, 3D) leverage interposers and TSVs to integrate diverse components like SoCs and HBM, enabling high-bandwidth applications (e.g., AI, GPUs). The transition from package substrate to PCB underscores the integration into complete electronic systems.

1. Semiconductors (Regular, SoC, Chiplets etc.):

* Single Chip: Refers to a package containing a single semiconductor die.

  Example: COB (Chip on Board), shown as a single LED die mounted directly on a substrate, often used in lighting applications.

* Multichip: Involves multiple dies or chiplets within a single package, categorized by interconnection methods:

  * Inorganic/Organic TSV-less Interposer: Uses through-silicon vias (TSVs) without an active interposer, relying on organic or inorganic materials.

  * Passive TSV Interposer: Incorporates passive TSVs in an interposer for vertical connections.

  * Active TSV Interposer: Features an active interposer with embedded circuitry for enhanced functionality.


2. Package Substrate (Carrier):

The intermediate layer that supports the semiconductor dies and facilitates connections. Package types are classified based on complexity and integration:

* PBGA (Plastic Ball Grid Array): A basic multi-chip package with solder balls.
  
* FcCSP (Flip Chip Chip Scale Package): Uses flip-chip technology for a compact, high-performance design.

* 2D: Multiple dies placed side by side on a single plane.

* 2.1D: Similar to 2D but with an interposer for improved connectivity.

* 2.3D: Incorporates a passive interposer with TSVs for vertical stacking.

* 2.5D: Uses an active interposer to integrate heterogeneous dies (e.g., SoC and HBM), as shown in the detailed inset with SoC, interposer, and substrate layers.

* 3D: Full 3D stacking of dies, maximizing density and performance.


Printed Circuit Board (PCB):

The base layer where the package is mounted, providing electrical and mechanical connectivity to the system.


### 1.5 - Comparative Analysis And Selecting The Right Packaging Solution

The following table provides a comparison of the various IC package types and their typical applications:<br><br>

<img width="1899" height="1046" alt="image" src="https://github.com/user-attachments/assets/7689b8b4-d4e5-4bbf-a9c8-74faf25c7c5d" /><br><br>

Selecting the right semiconductor packaging depends on multiple criteria across performance, reliability, form factor and cost.

***

## 2 - From Wafer to Package: Assembly and Manufacturing Essentials

????Package Manufacturing Introduction????

### 2.1 - Setting The Stage - Supply Chain And Facilities

#### 2.1.1 - Review of the supply chain

<img width="1909" height="1049" alt="image" src="https://github.com/user-attachments/assets/8b511ed7-a390-4fa1-9806-4f757653db56" /><br><br>

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

#### 2.1.2 - Introduction to a Package Manufacturing Unit (ATMP)

The section provides an overview of a semiconductor package manufacturing unit, focusing on the ATMP process (Assembly, Testing, Marking, and Packaging). This is a critical back-end stage in semiconductor production where fabricated dies are assembled into functional packages, tested for quality, marked for identification, and prepared for shipment.

<img width="1912" height="1057" alt="image" src="https://github.com/user-attachments/assets/4a488c2c-2819-4061-9f60-c33fba37583a" /><br><br>

Key Concepts

* Process: ATMP (Assembly, Testing, Marking, and Packaging): This encompasses the steps to transform bare dies into protected, testable, and ready-to-use chips. It includes die attachment (e.g., bonding),         encapsulation, electrical testing, reliability checks, marking (e.g., laser etching for traceability), and final packaging.

* Organization: OSAT (Outsourced Semiconductor Assembly and Test): Specialized companies like ASE, Amkor, or TATA that handle ATMP for fabless or IDM firms. The ATMP process can also be performed in-house by      integrated manufacturers such as Intel, TSMC, Micron, Samsung, or SK Hynix, allowing for greater control over quality and supply chain.

* Flexibility: The ATMP can be outsourced to OSATs or integrated internally, depending on the company's model and scale.

Example: Micron ATMP Facility in Sanand, Gujarat

The facility has a total area of 1.4 million square feet, with a clean room area (ISO class 1000/10000) of 500,000 square feet. This setup ensures contamination-free environments for sensitive processes.
Source cited: Forbes India.

Updated Status (as of August 2025): The Micron ATMP facility in Sanand is nearing completion, with cleanroom validation currently underway for Phase 1. Construction, including civil, mechanical, electrical, and plumbing work, is expected to be handed over by Tata Projects to Micron by December 2025. Partial operations are anticipated to begin in late 2025 (December) or early 2026, with full-scale production potentially by December 2026. The plant is designed for a capacity of approximately 101.6 million units per month, representing a significant investment of INR 22,500 crores. This aligns with India's push into semiconductor manufacturing.

This layout emphasizes separation of clean and non-clean areas to minimize contamination risks, with cleanrooms (e.g., ISO 6/7) central to sensitive processes. A typical floor plan for an ATMP facility, divided into functional zones to optimize workflow, safety, and efficiency and is presented with the following sections:

* Offices: Administrative areas for management, engineering, and quality control teams.

* Material Preparation and Storage: Dedicated space for preparing and storing raw materials like substrates, dies, bonding wires, and encapsulation compounds. This ensures materials are handled in controlled      conditions to prevent contamination.

* Processing Zone (Clean Room: ISO Class 6 & 7): The core production area, maintained at high cleanliness standards (ISO Class 6 and 7, which allow limited particles per cubic meter). Key processes here include:

* Die bonding: Attaching the die to the substrate.

* Wire or flip-chip bonding: Creating electrical connections (e.g., using thin wires or solder bumps).

* Encapsulation: Sealing the die with protective materials.

* Flip-chip processes and RDL (Redistribution Layer) formation: For advanced packages, redistributing connections for better integration.

Testing Area: Zone for post-assembly validation, including:

* Electrical tests: Checking functionality and performance.

* Burn-in tests: Stress-testing under elevated temperatures and voltages to identify early failures.

* Reliability chamber tests: Simulating real-world conditions (e.g., humidity, thermal cycling) to ensure durability.

Ware-house: Storage for finished packages, ready for shipping or further integration.

Utility and Maintenance Room: Houses support systems like power supplies, HVAC for cleanrooms, and maintenance equipment to keep the facility operational.

### 2.2 - Wafer Pre-Preparation - Grinding And Dicing<br><br>

<img width="1911" height="1040" alt="image" src="https://github.com/user-attachments/assets/abbfc4d1-76f0-4aa0-b842-a84be64a4b32" /><br><br>

#### 2.2.1 Activities Inside the Cleanroom Area

The section describes the key processes in the wafer preparation area within a semiconductor cleanroom (ISO Class 7), which is part of the back-end manufacturing in an ATMP (Assembly, Testing, Marking, and Packaging) facility. This area focuses on preparing fabricated silicon wafers for die separation and packaging. The cleanroom maintains strict particle control (ISO Class 7 allows up to 352,000 particles ≥0.5 μm per cubic meter) to prevent contamination that could ruin the delicate integrated circuits.

The process starts with incoming wafer handling and inspection, then proceeds to protective lamination. It flows downward to dicing, mounting, and grinding steps. This preparation is crucial before dies are assembled into packages, as it transforms a full wafer into individual, thinned dies ready for bonding and encapsulation. The overall process in the cleanroom prepares dies for downstream assembly, testing, and packaging in OSAT facilities.

Step-by-Step Breakdown

1. Incoming Wafer Carrier: A stack of wafers arrive in sealed carriers (e.g., FOUPs or cassettes) to protect them from contamination during transport.
   
2. Wafer Inspection: The wafer is visually and automatically inspected for defects, cracks, or contamination using tools like optical microscopes or automated scanners. This ensures only viable wafers proceed,     maximizing efficiency.

3. Wafer Front Tape Lamination: A protective tape is laminated onto the front (active) side of the wafer. This tape acts as a barrier to safeguard the circuit patterns and delicate structures from mechanical       damage, debris, or chemicals during subsequent aggressive processes like grinding and dicing. Without it, the front side could be scratched or contaminated, leading to die failure and reduced yield.

4. Two-Step Wafer Dicing (Laser Grooving + Blade Dicing): The wafer is cut into individual dies using a hybrid method: first, laser grooving creates precise shallow cuts, followed by mechanical blade dicing to     complete the separation. Modern wafers have thin, brittle layers and low-k dielectrics that are prone to chipping or cracking with traditional blade dicing alone. The two-step approach minimizes edge damage     laser grooving provides clean, narrow kerfs (cuts) without physical contact, while blade dicing ensures full separation. This is essential for high-density chips to maintain structural integrity and             electrical performance.

5. Tape Frame Mounting to Wafer Backside: The wafer's backside is mounted onto a dicing tape within a metal or plastic frame (ring frame). After initial preparation (e.g., lamination), this mounting provides       mechanical support and stability for the wafer during dicing and handling. It holds the dies in place post-dicing, preventing them from scattering, and facilitates easy transfer to pick-and-place tools for      assembly. Without this, thin wafers could warp or break, complicating automation and increasing defects.

6. Wafer Backside Grinding: The backside of the wafer is ground down using a spinning wheel and chuck table, with feeding direction and spindle. Wafers start thick (e.g., 775 μm) for stability during front-end     fabrication but must be thinned (to 50-200 μm) for compact packaging, better heat dissipation, and 3D stacking in advanced devices. Grinding removes excess silicon, but without prior front-side protection       (from lamination) or mounting, it could cause warping, cracking, or contamination.

   
### 2.3 - Wire Bond Packaging - Die Attach To Molding

The wire bond packaging process, a widely used technique in semiconductor packaging, focusing on the sequence from die attach to molding. This process is part of the back-end manufacturing in an ATMP (Assembly, Testing, Marking, and Packaging) facility and is conducted in a cleanroom environment. The below steps collectively transform a bare die into a robust, functional packaged IC, critical for downstream assembly onto PCBs and into final products. This process is common in cost-effective packages (e.g., QFN, SOP) and is suitable for a wide range of applications, from consumer electronics to automotive systems.<br><br>

<img width="1883" height="1051" alt="image" src="https://github.com/user-attachments/assets/9be46684-b4ca-49c9-b6d0-2fe2cfb2134d" /><br><br>

Wire Bond Packaging Process:

1. Die Attach: The silicon die, separated from the wafer, is attached to a substrate (e.g., leadframe or laminate) or a die pad using an adhesive material, such as epoxy. The die being placed onto a substrate      with a dispensing nozzle applying adhesive. This step provides mechanical stability and a thermal/electrical pathway between the die and the package. A secure attachment prevents movement during subsequent      processes (e.g., wire bonding, molding), ensures efficient heat dissipation, and, in some cases, establishes a ground connection if a conductive adhesive is used. Without proper die attach, the die could        shift, leading to misalignment or electrical failure.

2. Curing: The die-attached unit is subjected to a heating process to cure the epoxy, ensuring a strong and stable bond between the die and the substrate.

3. Wire Bonding (Starting with Free Air Ball): Wire bonding connects the die's bond pads to the substrate or leadframe using thin wires (typically gold, copper, or aluminum). The process begins with the            formation of a free air ball (FAB). A fine wire is fed through a capillary tool, and a high-voltage electric arc melts the wire tip to form a spherical FAB. The FAB is pressed onto the die's bond pad under      heat and ultrasonic energy, creating a metallurgical bond (e.g., ball bond). The capillary then moves to the substrate, forming a wedge bond or stitch bond, and the wire is cut, completing the connection.
   Wire bonding establishes electrical interconnections between the die and the external circuit, enabling signal and power transmission. Starting with a FAB ensures a strong, reliable initial bond due to its      uniform shape, which maximizes contact area and adhesion strength. This step is critical for packages like QFN, DIP, or PBGA, where high-density connections are needed without compromising signal integrity.

4. Molding: The assembled die, wire bonds, and substrate are encapsulated with a mold compound (e.g., epoxy resin) using a transfer molding machine. Molding protects the die and wire bonds from environmental       factors such as moisture, dust, mechanical stress, and thermal shock. It also provides structural integrity, preventing wire sweep or die damage during handling or operation. Without molding, the delicate       internal components would be vulnerable, reducing the package's reliability and lifespan.

5. Marking: It involves applying identification details to the molded package using techniques like laser etching, ink printing, or stamping. The information such as part numbers, manufacturer logos, batch         codes, or date codes is imprented on the top surface of the package after molding. Marking allows tracking of the IC through the supply chain, aiding in quality control, warranty claims, and recalls if          defects are identified. It provides critical information for assembly lines, customers, and end-users to distinguish between different IC types or versions. Manufacturer logos or codes enhance brand             recognition and authenticity. Without marking, it would be challenging to manage inventory or ensure the correct IC is used in specific applications, potentially leading to errors or counterfeit issues.

6. Singulation (Dicing Blade): Singulation separates individual packaged ICs from a panel or strip (e.g., a leadframe or substrate array) into standalone units. The sawing or punching machine cuts through the      molded panel along pre-defined scribe lines. These techniques are chosen based on package type (e.g., QFN, BGA) and material.
   
### 2.4 - Flip Chip Assembly - Bump Formation And Underfill<br><br>

<img width="1902" height="1054" alt="image" src="https://github.com/user-attachments/assets/e30d453c-b6a0-4775-b807-e12e6e085286" /><br><br>

The flip-chip packaging process, a sophisticated back-end semiconductor manufacturing technique within the ATMP (Assembly, Testing, Marking, and Packaging) workflow. Conducted in a cleanroom environment (e.g., ISO Class 6/7), this process transforms a silicon die into a fully packaged integrated circuit (IC) ready for integration. The below sequence reflects a comprehensive flip-chip process, typical in advanced packages like FC-BGA or 2.5D designs (e.g., Nvidia H100).

Flip-Chip Packaging Process

1. Bump Formation on Silicon: Solder bumps or copper pillars are created on the active side of the silicon die at the bond pad locations. This involves applying an under-bump metallurgy (UBM) layer followed by     solder deposition . Bumps provide electrical and mechanical connections when the die is flipped onto the substrate, enabling high pin counts and short signal paths for improved performance and reduced           inductance.

2. Chip Flip and Placement: The bumped die is inverted and precisely aligned with matching pads on the substrate (e.g., laminate or interposer). A pick-and-place machine positions the die, ensuring accurate        alignment before bonding. Flipping and placing the die face-down maximizes I/O density and thermal efficiency. Proper alignment prevents electrical shorts or open connections, critical for the subsequent        reflow process.

3. Flux Dispensing: A small amount of flux is dispensed using a dispensing tool onto the substrate pads or die bumps to remove oxides and improve solder wetting during reflow. Flux ensures a clean surface for      solder bonding, enhancing the strength and reliability of the connections by preventing oxidation and promoting uniform solder flow.

4. Solder Reflow: The assembly is heated in a reflow oven (e.g., 220-250°C) to melt the solder bumps, forming metallurgical bonds between the die and substrate. Reflow solidifies the electrical and mechanical      connections, locking the die to the substrate. This step is essential for establishing a robust interconnect network.

5. Flux Cleansing: Residual flux is removed using a cleaning agent (e.g., deionized water or solvent) to prevent corrosion or contamination. The cleaning station or rinse process eliminates flux residues that      could degrade long-term reliability by causing electrical leakage or chemical reactions, ensuring the package's durability.

6. Underfill Dispensing: Liquid epoxy underfill is applied along the die edges, flowing beneath via capillary action to fill the gap between the die and substrate. Underfill reinforces the structure,               compensating for thermal expansion mismatches and protecting bumps from mechanical stress or moisture ingress using a nozzle dispensing underfill.

7. Underfill Cure: The underfill is cured with heat (e.g., 100-150°C) in an oven to harden into a solid polymer. Curing stabilizes the underfill, securing the die and enhancing reliability by preventing            movement or degradation under operational conditions.

8. Molding: The entire assembly is encapsulated with a mold compound (e.g., epoxy resin) using a transfer molding machine to protect the die, bumps, and underfill. Molding shields the internal components from      environmental factors like humidity, dust, and mechanical shock, ensuring long-term functionality and robustness.

9. Marking: Identification details (e.g., part number, logo, batch code) are etched onto the molded package using laser marking or ink printing. Marking enables traceability, identification, and branding,          facilitating quality control and supply chain management.

10. Ball Mounting and Reflow on Substrate: Solder balls are placed on the substrate’s bottom pads (for BGA packages), and the assembly is heated in a reflow oven to bond the balls, completing the package-to-        board interface. Ball mounting and reflow create the external connections for surface-mounting the package onto a PCB, ensuring reliable electrical and mechanical attachment for final integration.

### 2.5 - Wafer Level Packaging And Conclusion

Wafer Level Packaging (WLP), a cutting-edge semiconductor packaging technique that encapsulates and interconnects dies at the wafer level before singulation. This process, part of the ATMP (Assembly, Testing, Marking, and Packaging) workflow, is conducted in a cleanroom environment (e.g., ISO Class 6/7) to maintain high yield and quality. This contrasts with traditional die-by-die packaging, offering a smaller form factor (close to the die size), better electrical performance, and cost efficiency for high-volume production.<br><br>

<img width="1920" height="1080" alt="M2_Lecture5" src="https://github.com/user-attachments/assets/d4aa3868-f1a0-437e-b6ff-441c2580b558" /><br><br>

Types of WLP

* Fan-in WLP (FI-WLP): Interconnects are confined within the die area, limiting I/O count but ideal for compact, low-pin-count devices.

* Fan-out WLP (FO-WLP): Extends interconnects beyond the die area onto the package, enabling higher I/O counts and supporting complex chips like CPUs or GPUs.

FO-WLP Process: Fan-out Wafer Level Packaging involves embedding known good dies into a reconstituted wafer, followed by redistribution and interconnection. FO-WLP allows for larger effective die areas and more I/O connections, accommodating advanced multi-chip designs and improving yield by using only tested dies.

1. Reconstitution Process: Individual dies (after wafer dicing) are placed face-up on a temporary carrier (e.g., glass or tape) with a gap between them. The carrier is then overmolded with an epoxy mold            compound to form a reconstituted wafer, embedding the dies. Reconstitution creates a uniform wafer-like structure from disparate dies, enabling wafer-level processing. This step is essential for FO-WLP to       expand the interconnect area and support high-density packaging.

2. RDL (Redistribution Layer) Preparation: A redistribution layer is fabricated on the reconstituted wafer to reroute the die’s bond pads to desired locations for external connections. This involves depositing     dielectric layers, patterning metal traces (e.g., copper), and via formation. RDL allows flexible pad placement, accommodating solder balls or other interconnects outside the original die footprint. It is       critical for fan-out designs, enhancing I/O density and electrical performance.

3. Solder Ball Attach: Solder balls are placed and reflowed onto the RDL pads to form the external connections (e.g., for BGA packages). Solder balls provide the mechanical and electrical interface for mounting    the package onto a PCB, ensuring reliable connectivity and supporting surface-mount technology.

4. Final Laser Marking: Identification details (e.g., part number, logo, batch code) are etched onto the package surface using a laser marking system after molding and ball attach. Marking enables traceability,    identification, and branding, crucial for quality control and supply chain management after the wafer-level processes are complete.

5. Singulation: The reconstituted wafer is diced into individual packages using a saw or laser along pre-defined scribe lines. Singulation separates the packaged dies into standalone units, allowing them to be     picked and placed onto PCBs or shipped. This final step completes the WLP process, transforming the wafer into marketable ICs.

***

## 3 - Labs: Thermal Simulation of Semiconductor Packages with ANSYS tools

### 3.1 - Introduction And Getting Started With ANSYS Electronics Desktop

ANSYS Electronics Desktop, a comprehensive simulation software suite widely used in the design and analysis of electronic systems, including semiconductor packaging, printed circuit boards (PCBs), antennas, and electromagnetic components. Developed by ANSYS, a leader in engineering simulation, this tool enables engineers to model complex electronic designs, predict behavior under various conditions, and refine them before physical prototyping.

### 3.2 - Setting Up A Flip-Chip BGA Package

We will be taking an already available FC-BGA package within the Icepak Toolkit for this simulation exercise.

Step 1 : Open AEDT and launch Icepak<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_1" src="https://github.com/user-attachments/assets/4192dc88-ca91-4304-af89-a323c3a8d32d" /><br><br>

The image highlights the following integrated tools within ANSYS Electronics Desktop:

Core Components

* HFSS (High-Frequency Structure Simulator): A 3D EM solver for high-frequency applications, such as antennas, filters, and RF circuits, analyzing signal integrity and electromagnetic interference (EMI).

* Maxwell: A 2D/3D solver for low-frequency electromagnetic fields, used for motors, transformers, and power electronics, focusing on magnetic and thermal effects.

* Q3D Extractor: A tool for extracting parasitic parameters (e.g., capacitance, inductance) from IC packages, interconnects, and PCBs, critical for signal integrity analysis.

* Icepak: A computational fluid dynamics (CFD) tool for thermal management, simulating heat dissipation in electronic assemblies.

* Circuit Simulator: Integrates with schematic tools to perform time-domain and frequency-domain analyses, linking EM models with circuit behavior.

Step 2.1 : Create a Flipchip BGA Package

Icepak -> Toolkit -> Geometry -> Packages -> Flipchip_BGA<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_2" src="https://github.com/user-attachments/assets/7790d44c-9de3-4bd2-ae21-c216dde688e2" /><br><br>

Step 2.2 : The Package Configuration window opens 

The dimensions and other aspects of the package, substrate, die, die underfill and the solder balls can be configured here.

Once configured, click OK to generate the package model.<br><br>

<img width="1023" height="560" alt="Lab1_FCBGA_ThermalSim_3 1" src="https://github.com/user-attachments/assets/914e36f6-9e22-4361-84c2-b58da394bf8d" /><br><br>

<img width="1010" height="548" alt="Lab1_FCBGA_ThermalSim_3 2" src="https://github.com/user-attachments/assets/0c5672c9-94de-4296-8fa7-9d8b5c3045c4" /><br><br>

<img width="1012" height="551" alt="Lab1_FCBGA_ThermalSim_3 3" src="https://github.com/user-attachments/assets/13ff5ba7-7e07-42cd-a60b-f26f73a531d5" /><br><br>

<img width="1007" height="552" alt="Lab1_FCBGA_ThermalSim_3 4" src="https://github.com/user-attachments/assets/87855867-a9bb-4b2f-97f2-953eb3268fc4" /><br><br>


Package generated in Icepak<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_4" src="https://github.com/user-attachments/assets/f0ad08ab-e9bf-4fff-9c3e-923390dd122a" /><br><br>

Step 3 : Explore the 3D Package Model Structure in Icepak

Ball group<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_5 1" src="https://github.com/user-attachments/assets/61bc81e7-87f6-404e-a794-644002b88a8f" /><br><br>

Substrate<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_5 2" src="https://github.com/user-attachments/assets/4000cf2d-aa92-4cfb-b932-d16ad0f3c6d7" /><br><br>

Die Underfill<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_5 3" src="https://github.com/user-attachments/assets/7eb9bc93-a808-4b92-a7ff-4f3b2a603446" /><br><br>

Die<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_5 4" src="https://github.com/user-attachments/assets/c3d5670c-b530-4c6f-a89a-5b6c23ed10c5" /><br><br>



### 3.3 - Material Definitions And Thermal Power Sources

Step 4 : Review and modify the material and definition types for the different components of the model.

Material Definitions<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_6" src="https://github.com/user-attachments/assets/b43d0b4e-29cc-4bac-8d17-bd0c7d49ad1f" /><br><br>

Step 5.1 : Add/ Assign Source Thermal Model for Die

In "Project Manager" sub-window, expand Thermal section and open the BGA1_die_source and configure the thermal condition as shown below:

Source Thermal Model for Die<br><br>

<img width="1920" height="1080" alt="Lab1_FCBGA_ThermalSim_6 1" src="https://github.com/user-attachments/assets/db6edeab-e95f-4d21-9895-2ea51949a30e" /><br><br>

Step 5.2 : Add/ Assign Source Thermal Model for Substrate

To add a thermal boundary condition for the substrate, right click on Flipchip_BGA1_substrate under Models -> Flipchip_BGA1_Group -> Solids and assign a Thermal Source.<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_6 2" src="https://github.com/user-attachments/assets/484be3af-ad14-4cd6-9cea-20ba1877f6ec" /><br><br>

Set the thermal condition on the substrate to Fixed Temperatue and the temperature as Ambient.<br><br>

<img width="1920" height="1025" alt="Lab1_FCBGA_ThermalSim_6 3" src="https://github.com/user-attachments/assets/e54c5ff7-11b9-412c-9cd8-22eb30f5fbd1" /><br><br>

Step 6 : Add Thermal monitors for the different components

To add a Thermal monitor to the substrate, right click on the Flipchip_BGA1_substrate under Models -> Flipchip_BGA1_Group -> Solids and then choose Assign Monitor -> Point...<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_6 4" src="https://github.com/user-attachments/assets/888be3f8-869e-410b-b80b-d876d64f5585" /><br><br>

In the sub-window that appears, select Temperature<br><br>

<img width="332" height="522" alt="Lab1_FCBGA_ThermalSim_6 5" src="https://github.com/user-attachments/assets/d732b8a9-105b-485c-a29e-85106257aa68" /><br><br>


Repeat the same to add thermal monitors for the die and the die-underfill.
.
Thermal monitors added<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_6 6" src="https://github.com/user-attachments/assets/819e777a-ffa2-4991-b2ea-70d8ca24c8b5" /><br><br>


### 3.4 - Meshing And Running The Thermal Analysis

Step 7.1 : Generate Mesh

Go to the Simulation tab and click on Generate Mesh<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_7" src="https://github.com/user-attachments/assets/3c260a8a-ca70-4cac-b59b-52fa6b37c430" /><br><br>

Save the project if prompted and wait for the mesh generation to get completed.

Take a note of any error(s) and warning(s) that are shown and ignore/ take steps to debug & fix the issue(s) as required.

Step 7.2 : Review Mesh Quality metrics

Once the mesh is generated, review the quality metrics of the generated mesh such as Face Alignment, Skewness and Volume.<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_7 1" src="https://github.com/user-attachments/assets/fd465888-7ae2-431f-a8a3-6ff2ae661d0a" /><br><br>

Mesh Quality - Face Alignment<br><br>

<img width="586" height="902" alt="Lab1_FCBGA_ThermalSim_7 2" src="https://github.com/user-attachments/assets/0e9f164b-8c3a-492f-b27c-f2ba22d93187" /><br><br>

Mesh Quality - Skewness<br><br>

<img width="585" height="906" alt="Lab1_FCBGA_ThermalSim_7 3" src="https://github.com/user-attachments/assets/7b6e0c34-fbfc-4673-bc07-91cb202537fa" /><br><br>

Mesh Quality - Volume<br><br>

<img width="583" height="902" alt="Lab1_FCBGA_ThermalSim_7 4" src="https://github.com/user-attachments/assets/b0ccf082-3a7e-4878-9ca7-b2447621fb4a" /><br><br>


Step 8 : Add Thermal Analysis

Under Project Manager, right click on Analysis and then, select Add Analysis Setup and configure the solver settings as required. (We will choose all default settings for our analysis)

Add Analysis Setup<br><br>

<img width="666" height="812" alt="Lab1_FCBGA_ThermalSim_7 5" src="https://github.com/user-attachments/assets/837c5d97-58f2-434a-8eb7-33cd24c8f8d3" /><br><br>

### 3.5 - Viewing Results And Exploring Other Package Types

Step 9 : Now, Validate the Simulation setup

Click on the Validate button in the top ribbon

Ensure all checks are validated successfully<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_8" src="https://github.com/user-attachments/assets/20104ea3-fb7e-4b4a-8941-8cccf6cbf9e8" /><br><br>

Step 10: Run the simulation and plot the temperature map

Click on Analyze All button in the top ribbon<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_9" src="https://github.com/user-attachments/assets/6519212a-e922-45e3-8efd-612f05f2d4a7" /> <br><br>

Wait for the simulation to get completed successfully. Take note of any warning(s) or errors that may need further debug or setup modification(s).

Once the simulation is completed, select the complete FC-BGA package in the 3D view by drawing a selection rectangle using the left-mouse button.

Right click and then select Plot Fields -> Temperature -> Temperature<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_10" src="https://github.com/user-attachments/assets/8cc3ccdf-4a3f-4e33-8bb1-851bcaca95f7" /><br><br>

Configure the different plot options:

Specify Name, Folder

Plot on Surface only

Surface Smoothing -> Enable Gaussian Smoothing

Field Plot Settings<br><br>

<img width="1903" height="1012" alt="Lab1_FCBGA_ThermalSim_10 1" src="https://github.com/user-attachments/assets/43967182-d3b9-40e8-b1a0-1ea02b0ee57b" /><br><br>

Field Plot - Top view<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_10 2" src="https://github.com/user-attachments/assets/70449d51-a063-442a-ae63-af368693da99" /><br><br>

Field Plot - Bottom view<br><br>

<img width="1920" height="1020" alt="Lab1_FCBGA_ThermalSim_10 3" src="https://github.com/user-attachments/assets/edc0a5e2-988d-494c-aa52-3e7f4a29f74f" /><br><br>

***

## 4 - Ensuring Package Reliability: Testing and Performance Validation

### 4.1 - Introduction to Package Testing and Electrical Functionality Checks

The process begins with Foundry activities, including Front end manufacturing (e.g., wafer creation) and Wafer probe test to check individual circuits. Next, Wafer sorting assesses wafer quality, followed by Package Manufacturing and OSAT (Outsourced Semiconductor Assembly and Test) for packaging and initial testing. Subsequently, Package Testing ensures packaged components function correctly, and System Level Tests (SLT) verify performance in real-world applications. Throughout these stages, Process development supports improvement, with diagnosis, failure analysis at the base to address issues and refine the process.


![M5_Lecture1](https://github.com/user-attachments/assets/df2d5487-3ddb-4704-962c-a917e7ae6990)


#### 4.1.1 - Foundry Testing Stages

1. Front End Manufacturing: This is the initial phase where silicon wafers are fabricated. It leads to fine tuning of the Process parameters to improve yield, reduce IDDQ/ leakage and improve speed/ performance.

2. Wafer Probe Test: After fabrication, individual circuits on the wafer are tested using probes to check for electrical performance and identify defective dies. Wafer is mounted on a probe station and a probe card with makes contact with the bond pads or bump pads of each die. An ATE can now send test patterns to mark the die as good or bad.

#### 4.1.2 - OSAT Testing Stages

OSAT refers to the outsourcing of assembly and testing to specialized firms. This stage includes final packaging adjustments and initial functional tests on the packaged chips. The Automatic Testing Equipment is used for precision testing to validate packaging integrity.

1. Wafer Sorting: Following the probe test, wafers are sorted based on test results. Functional dies are separated from defective ones, and the wafer may undergo visual or additional electrical inspections. Only functional dies proceed to packaging.

2. Package Manufacturing: This stage involves assembling the sorted dies into packages to protect them and enable connectivity. Processes include die attachment, wire bonding, and encapsulation. 

3. Package Testing: Packaged Testing phase in semiconductor manufacturing, divided into two main areas: the Processing Zone and the Testing Area, with a sequential testing process.
   

   ![M5_Lecture1 1](https://github.com/user-attachments/assets/7e9b813b-52d7-43ef-8677-9d55bf1a4a80)

   Processing Zone (Clean room: ISO class 6 & 7): This area handles initial packaging steps in a controlled environment. Key activities include die bonding, wire or flip-chip bonding, encapsulation, and RDL        (Redistribution Layer) formation. Inspection is integral to the manufacturing process to ensure quality. Packages are loaded onto a tray after singulation, as shown in the image with a tray of individual        packaged chips.

   Testing Area (Electrical, burn-in, and reliability chamber tests): This area focuses on validating the packaged chips. The process involves:
   
   AOST (Assembly Open and Short Test): Checks for open circuits and short circuits on the package board, using a package socket.


   ![M5_Lecture1 2](https://github.com/user-attachments/assets/e46c17ad-b761-4858-8e6f-1bb3023f1809)

   
   Burn-in Test: Elevated temperature and voltage and power cycling are applied to accelerate ageing to catch early-life reliability issues.
   
   Final Test: Conducts cold and hot tests to validate functional, parametric, reliability and validate the electrical performance of the packaged IC across temperature and voltage corners and ensure it meets      the datasheet specifications.

6. System Level Tests (SLT) : The final stage involves testing the chips within a complete system (e.g., a device or board) to ensure they perform as expected in real-world conditions.


### 4.2 - Reliability and Performance Testing of Semiconductor Packages


#### 4.2.1 Burn-in and Final Test


1. Burn-In Test

The Burn-in Test is a testing phase for package components under elevated (stressful) conditions, including temperature, voltage, and power cycling. The objective is to identify "Infant Mortality" failures before they reach customers. 


![M5_Lecture2](https://github.com/user-attachments/assets/fb90e245-8712-45b6-8558-c2dac72ac114)


Process: Parts are loaded from trays onto Burn-in Boards and then into ovens (via a Burn-in System) for testing. The system applies high voltage and temperature stress to accelerate failures.

Duration: The test is conducted long enough to capture the initial failure rate and slightly beyond where the failure rate curve flattens.

Defect Detection: It can detect defects like dielectric and metallization failures, as well as electromigration.

Trade-off: While it effectively removes unreliable components with a high probability of early failure, the total life span of components is shortened due to the stress.

The bath-tub graph illustrates the failure rate over time analogous to human life:

Infant Mortality: High initial failure rate (early "Infant Mortality" failures) that decreases rapidly.

Useful Life: A period of constant (random) failures with a low rate.

Wear Out: An increase in failure rate as components age.

The test targets the initial drop to eliminate weak components, as shown by the observed failure rate point.


2. Final Test (FT)
   

![M5_Lecture2 1](https://github.com/user-attachments/assets/f19ad80d-3be0-437b-b7c1-c7dc84862d08)


The Final Test is a temperature corner test to verify that packaged products meet specifications using an ATE (Electrical Testing Unit) with Handler for placing Devices Under Test (DUTs). ATE ensures precise testing across temperature extremes. The process involves loading the parts into a handler with temperature-controlled test fixtures (not ovens) during testing. They are electrically tested at elevated temperatures according to product specifications to confirm compliance. Finally the parts are subjected to low temperatures per product specifications and electrically tested.

4.2.2 Summary: ATE & Test Categories


![M5_Lecture2 2](https://github.com/user-attachments/assets/c629cee6-5ce7-4b27-8036-980691fa34ca)


## 5 - Package Design and Modeling: Building a Semiconductor Package from Scratch


This is a hands-on lab to design a semiconductor wire bond package from scratch using Ansys Electronics Desktop (AEDT).


### 5.1 - Introduction to Package Cross - Section Modeling in ANSYS Electronics Desktop (AEDT)

The main focus of this lab exercise is to build the virtual cross-section of a wire bond package, including die, substrate, bonding wires, and mold compound, rather than performing thermal simulation or analyses on a Pre loaded package. The complete process flow is once again shown below

Package Specifications:

<table>
  <tr>
    <td><strong>Component</strong></td>
    <td><strong>Properties</strong></td>
  </tr>
  <tr>
    <td>1. Die</td>
    <td>
      <ul>
        <li>Material : Silicon</li>
        <li>Dimensions : 3mm x 3mm</li>
        <li>Die Thickness : 200micron / 0.2mm</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>2. Substrate</td>
    <td>
      <ul>
        <li>Material : FR4</li>
        <li>Dimensions : 5mm x 5mm</li>
        <li>Thickness : 500micron / 0.5mm</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>3. Die Attach</td>
    <td>
      <ul>
        <li>Material : Modified Epoxy</li>
        <li>Dimensions : 3mm x 3mm</li>
        <li>Thickness : 100micron / 0.1mm</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>4. Die Bond Pads</td>
    <td>
      <ul>
        <li>Material : Copper</li>
        <li>Dimensions : 0.2mm x 0.2mm</li>
        <li>Thickness : 5micron / 0.005mm</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>5. Substrate Bond Pads</td>
    <td>
      <ul>
        <li>Material : Copper</li>
        <li>Dimensions : 0.2mm x 0.2mm</li>
        <li>Thickness : 10micron / 0.01mm</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>6. Bond Wire</td>
    <td>
      <ul>
        <li>Material : Gold wire</li>
        <li>Type: JEDEC 4-point</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>7. Mold Compound</td>
    <td>
      <ul>
        <li>Material : Epoxy</li>
        <li>Thickness : 1200micron / 1.2mm</li>
      </ul>
    </td>
  </tr>
</table>

![M6_Lecture1](https://github.com/user-attachments/assets/d4c3cb69-d5fa-437a-a135-183166b054b6)


#### Step 1 : Launch AEDT and select Q3D (or Icepak, Maxwell 3D)


<img width="1917" height="1015" alt="M6_Lecture2" src="https://github.com/user-attachments/assets/17958ff3-2b4c-4547-a495-789eaf5396e8" />


### 5.2 - Creating the Die and Substrate in AEDT

#### Step 2 : Define the working unit

Modeler -> Units...

Choose mm or um as the working unit for creating the model.<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 1" src="https://github.com/user-attachments/assets/93610cf2-13f8-4a6d-84bd-ae046a6da093" /><br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 2" src="https://github.com/user-attachments/assets/dda72335-f464-4186-8d3a-b10f30406671" /><br><br>

#### Step 3.1 : Create the Die Geometry

Select the rectangle tool from the ribbon or using the Menus (Draw -> Rectangle) to draw a rectangle

Now, double click on CreateRectangle Model -> Rectangle1 to open up its Properties Dialog box.

Specify the position with one corner at the origin (0, 0, 0) and the dimensions as 3mm x 3mm<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 3" src="https://github.com/user-attachments/assets/9692034d-07a3-4c78-853a-45003989c923" <br><br>

Select Model -> Rectangle1 and from the menu bar: Modeler -> Surface -> Thicken Sheet... and set the thickness to 200 microns (0.2mm)<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 4" src="https://github.com/user-attachments/assets/6636f95b-b303-4870-bf2f-8d88e48374d9" /><br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 5" src="https://github.com/user-attachments/assets/d2f969c2-e145-4cb3-be06-4a7197fe690c" /><br><br>

#### Step 3.2 : Assign Material Properties

Open up the Properties Dialog box either by double clicking on Model -> Rectangle1

Rename the geometry to Test Die

Choose Silicon as the material from the Material Library.><br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_2 6" src="https://github.com/user-attachments/assets/0dd50176-80f9-43d4-b606-0229694c1320" /><br><br>

#### Step 4.1 : Create the Substrate Geometry

Draw another rectangle for the substrate (5mm x 5mm) and position (-1, -1, 0) it such that the die is at the center.<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 7" src="https://github.com/user-attachments/assets/9fac4954-ffe5-4759-ac69-fe1ca6485f5b" /><br><br>

Set the thickness as -500 microns (-0.5mm). Note the negative sign so as to have the substrate lie beneath the die.<br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_2 8" src="https://github.com/user-attachments/assets/e2bfc752-7295-41ac-a95e-17cc0dc241bc" /><br><br>

Adjust the substrate position along Z-axis to account for the die attach thickness. Adjusted position: (-1, -1, -0.1)<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_2 9" src="https://github.com/user-attachments/assets/63bdd02e-1eb1-4cdb-a6b3-bc16a58fa219" /><br><br>


### 5.3 - Adding Die Attach Material and Bond Pads

#### Step 5 : Create the Die Attach Material

Draw a rectangle of the same size as that of the die (3mm x 3mm) and at the same co-ordinates (0, 0, 0).<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 1" src="https://github.com/user-attachments/assets/f62e092e-bbc6-4f22-b7c7-fce055c971f9" /><br><br>

Set the thickness to -100 microns (-0.1mm) as the Die Attach Material lies beneath the die and the substrate<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 2" src="https://github.com/user-attachments/assets/f7ffbede-f67c-4a74-a832-fd7ab89e1561" /><br><br>

Assign the material to Modified Eopxy<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 3" src="https://github.com/user-attachments/assets/943ed05c-95ef-4c63-82b7-4ff0870af28d" /><br><br>

NOTE: Assign different shades/ colours to adjacent components to easily discern in 3D view.<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 4" src="https://github.com/user-attachments/assets/e78026a6-3fd1-4fa0-96c2-2322690a77b2" /><br><br>

#### Step 6 : Create Bond pads on Die and Substrate

Draw a small rectangle and configure its size to to that of the die pad (0.2mm x 0.2mm). 

We will place the first Die Pad at the co-ordinates (0.2, 0.2, 0.2) so that it sits on top of the die and is at one of the edges.<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 5" src="https://github.com/user-attachments/assets/7c3c0eb0-bf45-4078-9429-face590d249e" /><br><br>

Set the thickness to 5 microns (0.005mm)<br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_3 6" src="https://github.com/user-attachments/assets/95437427-bd8d-47f8-b36c-b25f0bcf7504" /><br><br>

Similarly, draw a small rectangle and configure its size to to that of the substrate bond pad (0.2mm x 0.2mm).

We will place this Substrate Bind Pad at the co-ordinates (0.2, -0.7, -0.1) so that it sits aligned to the Die bond pad created in the previous step, and also on top of the substrate.<br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_3 7" src="https://github.com/user-attachments/assets/a0e2b4fd-964b-4536-a382-fa955bb58fca" /><br><br>

Set the substrate bond pad thickness to 10 microns (0.010mm)<br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_3 8" src="https://github.com/user-attachments/assets/cdbfe0d4-da85-4845-a17d-619380016eff" /><br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_3 9" src="https://github.com/user-attachments/assets/dffb6e4d-c55f-4b35-8fe7-4c71ad8619b3" /><br><br>

### 5.4 - Wire Bond Creation and Material Assignment

#### Step 7 : Create Bond Wires

Use the Bondwire tool under: Draw -> Bondwire

Connect the centre of the Die Bond pad to the centre of the Substrate Bond Pad. It might be easier to draw the wires from the Top view orientation.<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_4 1" src="https://github.com/user-attachments/assets/e9162281-403e-45b9-b9fd-d0abf35ecec9" /><br><br>

Select the Bondwire type as JEDEC 4-point<br><br>

<img width="1920" height="1020" alt="Lab2_Package modelling_4 2" src="https://github.com/user-attachments/assets/9483729e-02d4-4e4f-b363-b0d162400350" /><br><br>

Assign gold as the Bondwire material<br><br>

<img width="1903" height="1012" alt="Lab2_Package modelling_4 3" src="https://github.com/user-attachments/assets/8b28841c-20a5-4d2e-bee7-a7b2bb0c5aae" /><br><br>

Now, repeat the steps 6 and 7 to create and connect all the die and substrate bond pads using bondwires.

### 5.5 - Applying Mold Compound and Finalizing the Package Model
















