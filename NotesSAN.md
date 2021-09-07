1.8.0 => Rome and Implementation

RFC630

# Instances

https://facilitiessolutionsdev.service-now.com/
egonzalez29@dxc.com

https://facilitiessolutionstra.service-now.com/
egonzalez29@dxc.com

put a u_ to fields and tables which are not part of the baseline


Backup all the update sets before doing the clone.

Scheduled the clone. 


# Apps to maintain
- FMA
  - Gamification (SPAIN)
  - Mobile (SPAIN)

- CIR (DXC Spain) Roberto and Camino
- IFA For Santander legal team. DXC Netherlands Mathais and Roland
- Service Connector (DXC Netherlands) Jacob it is used in multiple system
- Office Templater (Fru Portugal -> DXC Portugal -> Convivavo) is usd FMA, IFA


Quebec
1. Support instance Santander to request the request

2. Skip records

3. Upgrade each application following the guide they provide for the deployment
[Try to not modify workflow]

4. 

Normally 2 weeks of merging things in applications

2 weeks of testing in UAT




MAJOR RFC's (to take into account in the regression testing)
- Planning team (jerarquie of the team)
- My facilities page the auto favorite assignment
- Transfer


- Order process
- Portal


CIR
System application => All available application
Filter by Fruitionpartners

Update without demo data (only in DEV when installing new)

IFA
CIR (Corporative Incident response)
Service Conector


# UPGRADE NOTES

- Upgrades are determined by FMA needed SN version.

- ServiceNow mandates to do at least 1 upgrade per year. In this case skipping one version in the middle.

- Merging and take note of what needs to retest. All the sensitive files should be retested.


- Check the XML when no differences as the embedded records are not included in the differences. If the previous version comes from an upgrade no problem, but if the previous version comes from a custom update set it's needed to review it. This applies to ChoiceLists, Record producers, etc...

- The skipped errors, are files without previous version so cannot be compared. Can be directly marked as Reviewed



Go to Global Helper Controller after the upgrade



## IFA

Choicelist => set to Reviewed

sys_metadata_link => Theses are demo datea => Set to Reviewed

Variables item_opt => Review and Retained. In Santander they change the help text so they will be always there.

Revert all changes installed by update set


## FMA
3d per upgrade FMA without checking customizations (collisions)
3d to 7d depending on the collisions depends on how long it takes.
