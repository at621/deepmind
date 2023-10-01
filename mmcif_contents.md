### mmCIF (Macromolecular Crystallographic Information File)

The mmCIF (Macromolecular Crystallographic Information File) format is a standard used in structural biology to store information about the three-dimensional structures of large biological molecules like proteins and nucleic acids. mmCIF files are a specific implementation of the more general CIF (Crystallographic Information File) format and are designed to capture a broad range of details about the molecule, its geometry, and the methods used to determine its structure. Below are some types of information you might find in an mmCIF file:

**Structural Information**
1. Atomic Coordinates: The core data in an mmCIF file is the 3D coordinates of each atom in the molecule. This includes the x, y, and z coordinates, usually in angstroms.
2. Unit Cell Parameters: In the case of crystallographic structures, information about the unit cell of the crystal may be included.
3. Connectivity: Information about which atoms are bonded to which, as well as more complex connectivity issues like disulfide bridges.
4. B-factors: These are temperature factors that give an indication of the mobility of atoms in the structure.
5. Occupancy: In crystal structures, the same position in the unit cell might be occupied by different atoms at different times. The occupancy factor gives the fraction of time a particular atom occupies a given position.

**Metadata**
1. Experimental Data: Details about how the structure was determined, such as the type of experiment (e.g., X-ray crystallography, NMR spectroscopy), the resolution, etc.
2. Annotations: Information about the biological context of the molecule, its function, the species it comes from, etc.
3. Authors and Citations: Information about the scientists who determined the structure and where the data was published.
4. Software: The computational tools used to refine the structure may also be mentioned.

**Sequence Information**
1. Primary Sequence: The amino acid or nucleotide sequence of the macromolecule.
2. Secondary Structure: Elements like alpha-helices and beta-sheets may be annotated.

**Validation**
1. Quality Metrics: Various statistics and metrics that provide insights into the quality of the structure, such as R-factors for crystal structures.

In summary, mmCIF files can contain a wealth of information that ranges from the raw coordinates of atoms to various types of metadata that provide context and validation for the structural data. These files are commonly used for storing structures in databases like the Protein Data Bank (PDB), and they can be read and manipulated using various bioinformatics tools, some of which you could use via Python and libraries like Biopython.


| Table Name                       | Group          | Explanation                                               |
| -------------------------------- | -------------- | --------------------------------------------------------- |
| `_entry`                         | General        | Basic information about the entry itself.                 |
| `_audit_conform`                 | Audit          | Conformance information to data dictionaries or standards.|
| `_database_2`                    | Database       | External database references.                             |
| `_pdbx_database_status`          | Database       | Status of the entry in the database.                      |
| `_audit_author`                  | Audit          | Information about authors who contributed to the entry.    |
| `_citation`                      | Citation       | Bibliographic citations related to the entry.              |
| `_citation_author`               | Citation       | Authors of the citations.                                 |
| `_cell`                          | Crystallography| Unit cell parameters.                                     |
| `_symmetry`                      | Crystallography| Space group symmetry.                                     |
| `_entity`                        | Entity         | Describes distinct biological molecules in the entry.     |
| `_entity_name_com`               | Entity         | Common names for entities.                                |
| `_entity_poly`                   | Entity         | Information on polymeric entities.                        |
| `_entity_poly_seq`               | Entity         | Sequence of monomers in polymeric entities.               |
| `_entity_src_gen`                | Entity         | Source information for genetically produced entities.     |
| `_struct_ref`                    | Structure      | Reference to other structures that are identical/similar.  |
| `_struct_ref_seq`                | Structure      | Mapping between referenced and entry sequences.           |
| `_struct_ref_seq_dif`            | Structure      | Sequence differences with the referenced structure.       |
| `_chem_comp`                     | Chemistry      | Description of chemical components.                       |
| `_exptl`                         | Experiment     | Information about the experiment.                         |
| `_exptl_crystal`                 | Experiment     | Information about the crystal used.                       |
| `_exptl_crystal_grow`            | Experiment     | Information about crystal growth conditions.              |
| `_diffrn`                        | Diffraction    | Information about the diffraction experiment.              |
| `_diffrn_detector`               | Diffraction    | Details about the detector used.                          |
| `_diffrn_radiation`              | Diffraction    | Information about the radiation source.                    |
| `_diffrn_radiation_wavelength`   | Diffraction    | Information about the wavelength of the radiation.         |
| `_diffrn_source`                 | Diffraction    | Information about the radiation source.                    |
| `_reflns`                        | Refinement     | Summary information about reflection data.                |
| `_reflns_shell`                  | Refinement     | Shell-wise reflection data.                               |
| `_refine`                        | Refinement     | Summary information about refinement.                      |
| `_refine_hist`                   | Refinement     | History of refinement iterations.                         |
| `_refine_ls_restr`               | Refinement     | Refinement restraint details.                             |
| `_pdbx_xplor_file`               | Software       | XPLOR software file details.                              |
| `_struct`                        | Structure      | General information about the structure.                   |
| `_struct_keywords`               | Structure      | Keywords for the structure.                               |
| `_struct_asym`                   | Structure      | Asymmetrical units.                                       |
| `_struct_biol`                   | Structure      | Description of the biological assembly.                    |
| `_struct_conf`                   | Structure      | Secondary structure conformation details.                 |
| `_struct_conf_type`              | Structure      | Types of secondary structure elements.                    |
| `_struct_conn`                   | Structure      | Connectivity between residues or atoms.                    |
| `_struct_conn_type`              | Structure      | Types of connections.                                     |
| `_struct_mon_prot_cis`           | Structure      | Cis peptide residues.                                     |
| `_struct_sheet`                  | Structure      | Beta-sheet details.                                       |
| `_struct_sheet_order`            | Structure      | Ordering of strands in beta-sheets.                        |
| `_struct_sheet_range`            | Structure      | Ranges of residues forming beta-strands.                  |
| `_pdbx_struct_sheet_hbond`       | Structure      | Hydrogen bonds in beta-sheets.                            |
| `_struct_site`                   | Structure      | Binding or active sites.                                  |
| `_struct_site_gen`               | Structure      | Atoms that generate binding sites.                        |
| `_database_PDB_matrix`           | Transformation | Transformation matrices for PDB compatibility.            |
| `_atom_sites`                    | Atom           | General information about atom sites.                     |
| `_atom_type`                     | Atom           | Type of atoms in the structure.                           |
| `_atom_site`                     | Atom           | Cartesian coordinates of each atom.                       |
| `_pdbx_poly_seq_scheme`          | Annotation     | Polypeptide sequence mapping scheme.                      |
| `_pdbx_nonpoly_scheme`           | Annotation     | Non-polypeptide annotation scheme.                        |
| `_pdbx_struct_assembly`          | Assembly       | Information about macromolecular assemblies.              |
| `_pdbx_struct_assembly_gen`      | Assembly       | Generation details for assemblies.                        |
| `_pdbx_struct_oper_list`         | Assembly       | List of operations for generating assemblies.              |
| `_pdbx_struct_conn_angle`        | Annotation     | Angles between connections.                               |
| `_pdbx_audit_revision_history`   | Audit          | Revision history.                                         |
| `_pdbx_audit_revision_details`   | Audit          | Revision details.                                         |
| `_pdbx_audit_revision_group`     | Audit          | Revision groups.                                          |
| `_pdbx_audit_revision_category`  | Audit          | Categories revised.                                       |
| `_pdbx_audit_revision_item`      | Audit          | Specific items revised.                                   |
| `_software`                      | Software       | Software used for data collection or refinement.           |
| `_pdbx_validate_rmsd_angle`      | Validation     | RMSD validation for angles.                               |
| `_pdbx_validate_torsion`         | Validation     | Torsion angle validation.                                 |
| `_pdbx_validate_planes`          | Validation     | Validation of planarity.                                  |
| `_pdbx_entity_nonpoly`           | Entity         | Information on non-polymeric entities.                    |
