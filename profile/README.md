*Because sharing open hardware projects should be like sharing open software projects*
# About the Distributed OSHW Framework (DOF)

**The DOF (Distributed OSHW Framework)** is a methodology for documenting and sharing Open Source Hardware (OSHW); an approach to model the "source" of an OSHW project, developed by [Mach 30](http://mach30.org/).

---

## Using the DOF unlocks OSHW's potential

Open source software (OSS) development benefits from several key practices and infrastructures that, without a framework like the DOF, are largely missing or fragmented in OSHW development. The DOF can impact OSHW projects by offering solutions to problems impacting collaboration, documentation standards, modularity, and portability.

### Improves collaboration for project maintainers and contributors

Standardized structure and documentation practices, achieved by modeling hardware projects with YAML, make it easy to see and review changes between versions (diffability). This lowers the barrier for new contributors to participate, and allows project maintainers to easily review and incorporate community contributions.

### Achieves greater documentation standards
Software development leverages README files, changelogs, and structured documentation that are versioned alongside the code. In contrast, hardware projects are often plagued by fragmented documentation, updated haphazardly, making it difficult to track design decisions and changes across versions and dependencies between related projects. By treating projects as source code, it becomes possible to use these standards and versioning tools in hardware projects. 

### Empowers reuse and modularity

The DOF addresses the need for reuse and modularity in hardware development. For example, in a 3D printer project, a subcomponent such as an extruder can be maintained in a standalone repository. Since the same extruder might be used across different 3D printer projects (for example, D3D-Pro and D3D-Universal), treating the extruder as its own “package” means you can manage it independently. Other projects can then easily “import” the extruder repo as a dependency, much like package management in software development. Note that managing subcomponents in their own standalone repositories is optional.

### Maintains portability

Although the reference implementation tooling uses git, npm, and gradle, the methodology is tool-agnostic as to allow for migration to other version control, package management, and build tools.

*Our approach was driven by feedback from the community. See our [user stories & community feedback](https://mach30.github.io/oshw-pm-user-stories)*.

---

Watch [J Simmons](https://thejsimmons.com/) talk **Fire, Smoke and Open Source Hardware** at [SCALE 2023](https://www.socallinuxexpo.org/scale/20x/presentations/fire-smoke-and-open-source-hardware):

[![J Simmons talk Fire, Smoke and Open Source Hardware](https://img.youtube.com/vi/qIMT--XEZiM/hqdefault.jpg)](https://www.youtube.com/watch?v=qIMT--XEZiM)

Dr. Simmons discusses the Mach 30's Shepard Test Stand as a case study demonstrating that open source software practices can be applied to aerospace hardware, detailing the project's successes, lessons learned, and need for future work, such as the creation of the DOF and related projects.

---

## Projects in Development
To advance the adoption and effectiveness of the DOF, we are actively developing and maintaining several complementary projects, each addressing a key aspect of DOF documentation, modeling, and tool support.
- [Mach 30 Distributed OSHW Framework Workspace (Kasm Image)](https://github.com/Mach30/kasm-dof-workspace) - This Kasm workspace is set up with all DOF tooling. Use of the workspace recommended for Mach 30 volunteers and contributors, as it ensures a consistent, reproducible developer environment. 
- [DOF Repository](https://github.com/Mach30/dof): The legacy implementation and reference for the Distributed OSHW Framework (DOF) methodology itself. This repository documents the principles, workflows, and best practices for DOF, serving both as a historical artifact and a foundation for ongoing tool and process development.
- [yaml-datastore](https://github.com/Mach30/yaml-datastore): Tool for managing distributed YAML content. Developed to meet the needs of m30ml, which requires handling of data spread across multiple YAML files and directories.
- [m30ml](https://github.com/Mach30/m30ml): A  lightweight YAML-based MBSE modeling language, loosely inspired by SysML v2, but intended for filesystem use. To support complex projects, m30ml relies on modular data management across multiple YAML files and directories, an approach made possible by the development of yaml-datastore.
- [m30pm](https://github.com/Mach30/m30pm): Minimum viable tooling to support defining and executing the next generation of the methodology (to be defined using a domain specific LinkML schema). CRUDs schemas and data described in m30ml.
- [linkml schema](https://github.com/Mach30/linkml-schema): Fork of linkml schema to make it compatible with npm.

---

## Ready to build the future of OSHW?
Contribute ideas, code, and feedback.  [**Join the Discussion on GitHub**](https://github.com/Mach30/dof/issues)

---

## Frequently Asked Questions

**Q: What is the value of OSHWA certification and how does the DOF support it?**  

A: OSHWA (Open Source Hardware Association) certification helps the community identify hardware projects that meet the widely accepted definition of open source hardware. The DOF methodology was developed to align with this [definition](https://oshwa.org/resources/open-source-hardware-definition/) and support the [requirements of the OSHW community](https://mach30.github.io/oshw-pm-user-stories/).

**Q: Is the DOF a tool?**  

A: No, the DOF is a methodology you can use with any tools or platforms. Like [Docs-as-Code](https://www.writethedocs.org/guide/docs-as-code/) is a methodology, one could consider the DOF as Docs-as-Models-as-Code; the framework treats documentation as a model, managed just like source code.  
- **Docs-as-Models:** Your docs are a structured, machine-queryable model of your hardware.
- **Models-as-Code:** These models live in your repository, versioned, reviewable, and forkable like any codebase.

**Q: I'm interested in using the DOF for my hardware project, how do I get started?**

A: The DOF is still in development, as we are currently working on completing the tooling. However you can look at an example projects in legacy DOF to get an idea (see next question). 

**Q: Are there example projects available?**

A: Yes, there are a couple of example projects using the legacy tooling: 

- [D3D 3D Printer](https://github.com/AlexandriaLittle/d3d-pro) Models a 3D printer design by contributor Alexandra Little for the Open Source Ecology D3D project which renders to https://alexandrialittle.github.io/d3d-pro/.

- [Sealion Mission Architecture](https://github.com/odu-cga-cubesat/sealion-mission-architecture) Ground station & flight software architecture for the joint CubeSat mission between Old Dominion University & Coast Guard Academy. Includes commentary on where the legacy tooling needs to be improved. 

**Q: Are there any active communities or forums to discuss DOF devlopment?**

A: Yes: 
- [Discord](#) (Coming Soon)
- [**GitHub Issues**](https://github.com/Mach30/dof/issues)
