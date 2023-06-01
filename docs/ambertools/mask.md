---
layout: default
title: Amber Masks 
parent: AmberTools
---

# Amber Masks

| Option                  | Example |
| :-----                  | :------ |
| :RESIDUE_NUMBER         | ':1-10', ':1,3,5', or '1-3,5,7-9' |
| :RESIDUE_NAME           | ':ALA', or ':ARG,ALA,ASP' |
| @ATOM_NUMBER            | '@12,17', '@54-85', or '@12,54-85,90' |
| @ATOM_NAME              | '@CA', or '@CA,C,O,N,H'|
| @%ATOM_TYPE_NAME        | '@%CT' |
| @ATOM_ELEMENT_NAME      | '@/N' |

# Selection by Distance Mask

Select atoms within 2.4 Å distance of atoms selected by ’:11-17’ (residues numbered 11 through 17).

```
:11-17<@2.4
```

# Amber Mask Examples

| Mask                       | Explanation |
| :----                      | :----       | |
| :ALA,TRP	                 | All alanine and tryptophan residues. |
| :5,10@CA CA	             | Carbon in residues 5 and 10. | 
| :*&!@H=	                 | All non-hydrogen atoms (equivalent to “!@H=”). |
| @CA,C,O,N,H	             | All (protein) backbone atoms. |
| !@CA,C,O,N,H	             | All non-backbone atoms (=sidechains for proteins only). | 
| :1-500@O&!(:WAT|:LYS,ARG)	 | All backbone oxygens in residues 1-500 but not in water, lysine or arginine residues. |
| (:11@CD<:5.5)&:Na+	     | Select all residues within 5.5 Ang. of atom CD from residue 11) AND those residues must be named Na+ |
