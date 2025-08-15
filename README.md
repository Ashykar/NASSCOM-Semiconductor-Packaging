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














