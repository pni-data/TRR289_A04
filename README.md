# TRR289 A04

## ℹ️ Information
*This repository is the Github sibling of the corresponding [DataLad](https://www.datalad.org/) dataset, i.e. it **does not** contain the data itself.*
The GitHub sibling, nevertheless, provides insights into the general data structure (directory tree, filenames) and serves as a starting point to download, share and discuss the dataset.
 Data is in BIDS format and may include behavioral, questionnaire and derivative data, too.
Data is stored in a special S3 remote provided by [Coscine](https://coscine.rwth-aachen.de/) and can't be downloaded without the dataset specific secret token.
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.

See `dataset_description.json` for project related meta-data.

## ⬇️ How to download dataset

#### 1. Install it with DataLad based on the github handle
This does not download the actual data, only the gin-annex "skeleton".
```bash
datalad install -s git@github.com:pni-data/<dataset_name>.git <dataset_name>
```
#### 2. Set up the security token to access the actual data
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.
```bash
export AWS_ACCESS_KEY_ID="XXXXX-XXXX-XXXX-XXXX-XXXX"
export AWS_SECRET_ACCESS_KEY="XXXXXXXX"
```

#### 2. Change to the dataset directory and download the file(s) you want
You can selectively download what you need (e.g. derivatives only).
```bash
cd <dataset_name>
datalad get <path/to/file*>
```


See our [documentation](https://github.com/pni-data/.github/blob/master/profile/README.md) for more detail.

Comments added by the SFB289 Z03 project coordinators
====================================================================

General Comments
--------------------------------------------------------------------
ToDo:

description of the dataset,including link to the openly available SFB proposal/some publication
eg: This dataset was acquired by the team of the SFB289 XX project. It includes YY subjects and the common sequences within the SFB289 project, namely a high resolution T1w, resting state fMRI, 133 direction multi shell DWI, and 2 fieldmaps for the functional data (one reversed phase encoding direction, one Siemens deafult fieldmap sequnce) and one fieldmap for the DWI (reversed field encoding direction). An additional reference image of the resting state fMRI is included without multiband factor.

Questionnaires data are also acquired and can be found in the ... fodler.

The proposal can be found here: link

The BIDS conversion was done with heudiconv by the XX project coordinators and/or supported by the Z03 project coordinators.

Defacing
--------------------------------------------------------------------
Defacing was done by the Z03 cooridnator.
Pydeface was used on all anatomical images to ensure deindentification of subjects. The code
can be found at https://github.com/poldracklab/pydeface


Known Issues
--------------------------------------------------------------------
N/A ToDo

--------------------------------------------------------------------

## bids-validator@1.13.1
	[33m1: [WARN] Not all subjects contain the same files. Each subject should contain the same number of files with the same naming unless some files are known to be missing. (code: 38 - INCONSISTENT_SUBJECTS)[39m
		./sub-428arm3s6/anat/sub-428arm3s6_run-02_T1w.json
			This file is missing for subject sub-428arm3s6, but is present for at least one other subject.
			Evidence: Subject: sub-428arm3s6; Missing file: sub-428arm3s6_run-02_T1w.json
		./sub-428arm3s6/anat/sub-428arm3s6_run-02_T1w.nii.gz
			This file is missing for subject sub-428arm3s6, but is present for at least one other subject.
			Evidence: Subject: sub-428arm3s6; Missing file: sub-428arm3s6_run-02_T1w.nii.gz
		./sub-42bm62qpd/anat/sub-42bm62qpd_run-02_T1w.json
			This file is missing for subject sub-42bm62qpd, but is present for at least one other subject.
			Evidence: Subject: sub-42bm62qpd; Missing file: sub-42bm62qpd_run-02_T1w.json
		./sub-42bm62qpd/anat/sub-42bm62qpd_run-02_T1w.nii.gz
			This file is missing for subject sub-42bm62qpd, but is present for at least one other subject.
			Evidence: Subject: sub-42bm62qpd; Missing file: sub-42bm62qpd_run-02_T1w.nii.gz
		./sub-431qsjek9/anat/sub-431qsjek9_run-02_T1w.json
			This file is missing for subject sub-431qsjek9, but is present for at least one other subject.
			Evidence: Subject: sub-431qsjek9; Missing file: sub-431qsjek9_run-02_T1w.json
		./sub-431qsjek9/anat/sub-431qsjek9_run-02_T1w.nii.gz
			This file is missing for subject sub-431qsjek9, but is present for at least one other subject.
			Evidence: Subject: sub-431qsjek9; Missing file: sub-431qsjek9_run-02_T1w.nii.gz
		./sub-43a8y7cpx/anat/sub-43a8y7cpx_run-02_T1w.json
			This file is missing for subject sub-43a8y7cpx, but is present for at least one other subject.
			Evidence: Subject: sub-43a8y7cpx; Missing file: sub-43a8y7cpx_run-02_T1w.json
		./sub-43a8y7cpx/anat/sub-43a8y7cpx_run-02_T1w.nii.gz
			This file is missing for subject sub-43a8y7cpx, but is present for at least one other subject.
			Evidence: Subject: sub-43a8y7cpx; Missing file: sub-43a8y7cpx_run-02_T1w.nii.gz
		./sub-43babkt9m/anat/sub-43babkt9m_run-02_T1w.json
			This file is missing for subject sub-43babkt9m, but is present for at least one other subject.
			Evidence: Subject: sub-43babkt9m; Missing file: sub-43babkt9m_run-02_T1w.json
		./sub-43babkt9m/anat/sub-43babkt9m_run-02_T1w.nii.gz
			This file is missing for subject sub-43babkt9m, but is present for at least one other subject.
			Evidence: Subject: sub-43babkt9m; Missing file: sub-43babkt9m_run-02_T1w.nii.gz
		./sub-43babkt9m/sub-43babkt9m_scans.tsv
			This file is missing for subject sub-43babkt9m, but is present for at least one other subject.
			Evidence: Subject: sub-43babkt9m; Missing file: sub-43babkt9m_scans.tsv
		./sub-44hr2hb1k/anat/sub-44hr2hb1k_run-02_T1w.json
			This file is missing for subject sub-44hr2hb1k, but is present for at least one other subject.
			Evidence: Subject: sub-44hr2hb1k; Missing file: sub-44hr2hb1k_run-02_T1w.json
		./sub-44hr2hb1k/anat/sub-44hr2hb1k_run-02_T1w.nii.gz
			This file is missing for subject sub-44hr2hb1k, but is present for at least one other subject.
			Evidence: Subject: sub-44hr2hb1k; Missing file: sub-44hr2hb1k_run-02_T1w.nii.gz
		./sub-44y844aqw/anat/sub-44y844aqw_run-02_T1w.json
			This file is missing for subject sub-44y844aqw, but is present for at least one other subject.
			Evidence: Subject: sub-44y844aqw; Missing file: sub-44y844aqw_run-02_T1w.json
		./sub-44y844aqw/anat/sub-44y844aqw_run-02_T1w.nii.gz
			This file is missing for subject sub-44y844aqw, but is present for at least one other subject.
			Evidence: Subject: sub-44y844aqw; Missing file: sub-44y844aqw_run-02_T1w.nii.gz
		./sub-4549xg9p7/anat/sub-4549xg9p7_run-02_T1w.json
			This file is missing for subject sub-4549xg9p7, but is present for at least one other subject.
			Evidence: Subject: sub-4549xg9p7; Missing file: sub-4549xg9p7_run-02_T1w.json
		./sub-4549xg9p7/anat/sub-4549xg9p7_run-02_T1w.nii.gz
			This file is missing for subject sub-4549xg9p7, but is present for at least one other subject.
			Evidence: Subject: sub-4549xg9p7; Missing file: sub-4549xg9p7_run-02_T1w.nii.gz
		./sub-455nbvhdy/anat/sub-455nbvhdy_run-02_T1w.json
			This file is missing for subject sub-455nbvhdy, but is present for at least one other subject.
			Evidence: Subject: sub-455nbvhdy; Missing file: sub-455nbvhdy_run-02_T1w.json
		./sub-455nbvhdy/anat/sub-455nbvhdy_run-02_T1w.nii.gz
			This file is missing for subject sub-455nbvhdy, but is present for at least one other subject.
			Evidence: Subject: sub-455nbvhdy; Missing file: sub-455nbvhdy_run-02_T1w.nii.gz
		./sub-46mp9256e/anat/sub-46mp9256e_run-02_T1w.json
			This file is missing for subject sub-46mp9256e, but is present for at least one other subject.
			Evidence: Subject: sub-46mp9256e; Missing file: sub-46mp9256e_run-02_T1w.json
		./sub-46mp9256e/anat/sub-46mp9256e_run-02_T1w.nii.gz
			This file is missing for subject sub-46mp9256e, but is present for at least one other subject.
			Evidence: Subject: sub-46mp9256e; Missing file: sub-46mp9256e_run-02_T1w.nii.gz
		./sub-46snpj229/anat/sub-46snpj229_run-02_T1w.json
			This file is missing for subject sub-46snpj229, but is present for at least one other subject.
			Evidence: Subject: sub-46snpj229; Missing file: sub-46snpj229_run-02_T1w.json
		./sub-46snpj229/anat/sub-46snpj229_run-02_T1w.nii.gz
			This file is missing for subject sub-46snpj229, but is present for at least one other subject.
			Evidence: Subject: sub-46snpj229; Missing file: sub-46snpj229_run-02_T1w.nii.gz
		./sub-46wcy65da/anat/sub-46wcy65da_run-02_T1w.json
			This file is missing for subject sub-46wcy65da, but is present for at least one other subject.
			Evidence: Subject: sub-46wcy65da; Missing file: sub-46wcy65da_run-02_T1w.json
		./sub-46wcy65da/anat/sub-46wcy65da_run-02_T1w.nii.gz
			This file is missing for subject sub-46wcy65da, but is present for at least one other subject.
			Evidence: Subject: sub-46wcy65da; Missing file: sub-46wcy65da_run-02_T1w.nii.gz
		./sub-47th7erw4/anat/sub-47th7erw4_run-02_T1w.json
			This file is missing for subject sub-47th7erw4, but is present for at least one other subject.
			Evidence: Subject: sub-47th7erw4; Missing file: sub-47th7erw4_run-02_T1w.json
		./sub-47th7erw4/anat/sub-47th7erw4_run-02_T1w.nii.gz
			This file is missing for subject sub-47th7erw4, but is present for at least one other subject.
			Evidence: Subject: sub-47th7erw4; Missing file: sub-47th7erw4_run-02_T1w.nii.gz
		./sub-48mtu68kx/anat/sub-48mtu68kx_run-02_T1w.json
			This file is missing for subject sub-48mtu68kx, but is present for at least one other subject.
			Evidence: Subject: sub-48mtu68kx; Missing file: sub-48mtu68kx_run-02_T1w.json
		./sub-48mtu68kx/anat/sub-48mtu68kx_run-02_T1w.nii.gz
			This file is missing for subject sub-48mtu68kx, but is present for at least one other subject.
			Evidence: Subject: sub-48mtu68kx; Missing file: sub-48mtu68kx_run-02_T1w.nii.gz
		./sub-48mtu68kx/sub-48mtu68kx_scans.tsv
			This file is missing for subject sub-48mtu68kx, but is present for at least one other subject.
			Evidence: Subject: sub-48mtu68kx; Missing file: sub-48mtu68kx_scans.tsv
		./sub-48zdywz1p/anat/sub-48zdywz1p_run-02_T1w.json
			This file is missing for subject sub-48zdywz1p, but is present for at least one other subject.
			Evidence: Subject: sub-48zdywz1p; Missing file: sub-48zdywz1p_run-02_T1w.json
		./sub-48zdywz1p/anat/sub-48zdywz1p_run-02_T1w.nii.gz
			This file is missing for subject sub-48zdywz1p, but is present for at least one other subject.
			Evidence: Subject: sub-48zdywz1p; Missing file: sub-48zdywz1p_run-02_T1w.nii.gz
		./sub-49rg92h8h/anat/sub-49rg92h8h_run-02_T1w.json
			This file is missing for subject sub-49rg92h8h, but is present for at least one other subject.
			Evidence: Subject: sub-49rg92h8h; Missing file: sub-49rg92h8h_run-02_T1w.json
		./sub-49rg92h8h/anat/sub-49rg92h8h_run-02_T1w.nii.gz
			This file is missing for subject sub-49rg92h8h, but is present for at least one other subject.
			Evidence: Subject: sub-49rg92h8h; Missing file: sub-49rg92h8h_run-02_T1w.nii.gz
		./sub-4ag74gdvw/anat/sub-4ag74gdvw_run-02_T1w.json
			This file is missing for subject sub-4ag74gdvw, but is present for at least one other subject.
			Evidence: Subject: sub-4ag74gdvw; Missing file: sub-4ag74gdvw_run-02_T1w.json
		./sub-4ag74gdvw/anat/sub-4ag74gdvw_run-02_T1w.nii.gz
			This file is missing for subject sub-4ag74gdvw, but is present for at least one other subject.
			Evidence: Subject: sub-4ag74gdvw; Missing file: sub-4ag74gdvw_run-02_T1w.nii.gz
		./sub-4aq6cttgu/anat/sub-4aq6cttgu_run-02_T1w.json
			This file is missing for subject sub-4aq6cttgu, but is present for at least one other subject.
			Evidence: Subject: sub-4aq6cttgu; Missing file: sub-4aq6cttgu_run-02_T1w.json
		./sub-4aq6cttgu/anat/sub-4aq6cttgu_run-02_T1w.nii.gz
			This file is missing for subject sub-4aq6cttgu, but is present for at least one other subject.
			Evidence: Subject: sub-4aq6cttgu; Missing file: sub-4aq6cttgu_run-02_T1w.nii.gz
		./sub-4audn1f6q/anat/sub-4audn1f6q_run-02_T1w.json
			This file is missing for subject sub-4audn1f6q, but is present for at least one other subject.
			Evidence: Subject: sub-4audn1f6q; Missing file: sub-4audn1f6q_run-02_T1w.json
		./sub-4audn1f6q/anat/sub-4audn1f6q_run-02_T1w.nii.gz
			This file is missing for subject sub-4audn1f6q, but is present for at least one other subject.
			Evidence: Subject: sub-4audn1f6q; Missing file: sub-4audn1f6q_run-02_T1w.nii.gz
		./sub-4bc1pg5fw/anat/sub-4bc1pg5fw_run-02_T1w.json
			This file is missing for subject sub-4bc1pg5fw, but is present for at least one other subject.
			Evidence: Subject: sub-4bc1pg5fw; Missing file: sub-4bc1pg5fw_run-02_T1w.json
		./sub-4bc1pg5fw/anat/sub-4bc1pg5fw_run-02_T1w.nii.gz
			This file is missing for subject sub-4bc1pg5fw, but is present for at least one other subject.
			Evidence: Subject: sub-4bc1pg5fw; Missing file: sub-4bc1pg5fw_run-02_T1w.nii.gz
		./sub-4bj7vquyx/anat/sub-4bj7vquyx_run-02_T1w.json
			This file is missing for subject sub-4bj7vquyx, but is present for at least one other subject.
			Evidence: Subject: sub-4bj7vquyx; Missing file: sub-4bj7vquyx_run-02_T1w.json
		./sub-4bj7vquyx/anat/sub-4bj7vquyx_run-02_T1w.nii.gz
			This file is missing for subject sub-4bj7vquyx, but is present for at least one other subject.
			Evidence: Subject: sub-4bj7vquyx; Missing file: sub-4bj7vquyx_run-02_T1w.nii.gz
		./sub-4buj7y7qd/anat/sub-4buj7y7qd_run-02_T1w.json
			This file is missing for subject sub-4buj7y7qd, but is present for at least one other subject.
			Evidence: Subject: sub-4buj7y7qd; Missing file: sub-4buj7y7qd_run-02_T1w.json
		./sub-4buj7y7qd/anat/sub-4buj7y7qd_run-02_T1w.nii.gz
			This file is missing for subject sub-4buj7y7qd, but is present for at least one other subject.
			Evidence: Subject: sub-4buj7y7qd; Missing file: sub-4buj7y7qd_run-02_T1w.nii.gz
		./sub-4ccekpvgh/anat/sub-4ccekpvgh_run-02_T1w.json
			This file is missing for subject sub-4ccekpvgh, but is present for at least one other subject.
			Evidence: Subject: sub-4ccekpvgh; Missing file: sub-4ccekpvgh_run-02_T1w.json
		./sub-4ccekpvgh/anat/sub-4ccekpvgh_run-02_T1w.nii.gz
			This file is missing for subject sub-4ccekpvgh, but is present for at least one other subject.
			Evidence: Subject: sub-4ccekpvgh; Missing file: sub-4ccekpvgh_run-02_T1w.nii.gz
		./sub-4d35q46xd/anat/sub-4d35q46xd_run-02_T1w.json
			This file is missing for subject sub-4d35q46xd, but is present for at least one other subject.
			Evidence: Subject: sub-4d35q46xd; Missing file: sub-4d35q46xd_run-02_T1w.json
		./sub-4d35q46xd/anat/sub-4d35q46xd_run-02_T1w.nii.gz
			This file is missing for subject sub-4d35q46xd, but is present for at least one other subject.
			Evidence: Subject: sub-4d35q46xd; Missing file: sub-4d35q46xd_run-02_T1w.nii.gz
		./sub-4dawt6wce/anat/sub-4dawt6wce_run-02_T1w.json
			This file is missing for subject sub-4dawt6wce, but is present for at least one other subject.
			Evidence: Subject: sub-4dawt6wce; Missing file: sub-4dawt6wce_run-02_T1w.json
		./sub-4dawt6wce/anat/sub-4dawt6wce_run-02_T1w.nii.gz
			This file is missing for subject sub-4dawt6wce, but is present for at least one other subject.
			Evidence: Subject: sub-4dawt6wce; Missing file: sub-4dawt6wce_run-02_T1w.nii.gz
		./sub-4dhdu5xzg/anat/sub-4dhdu5xzg_run-02_T1w.json
			This file is missing for subject sub-4dhdu5xzg, but is present for at least one other subject.
			Evidence: Subject: sub-4dhdu5xzg; Missing file: sub-4dhdu5xzg_run-02_T1w.json
		./sub-4dhdu5xzg/anat/sub-4dhdu5xzg_run-02_T1w.nii.gz
			This file is missing for subject sub-4dhdu5xzg, but is present for at least one other subject.
			Evidence: Subject: sub-4dhdu5xzg; Missing file: sub-4dhdu5xzg_run-02_T1w.nii.gz
		./sub-4dqecum7p/anat/sub-4dqecum7p_run-02_T1w.json
			This file is missing for subject sub-4dqecum7p, but is present for at least one other subject.
			Evidence: Subject: sub-4dqecum7p; Missing file: sub-4dqecum7p_run-02_T1w.json
		./sub-4dqecum7p/anat/sub-4dqecum7p_run-02_T1w.nii.gz
			This file is missing for subject sub-4dqecum7p, but is present for at least one other subject.
			Evidence: Subject: sub-4dqecum7p; Missing file: sub-4dqecum7p_run-02_T1w.nii.gz
		./sub-4dqh9tzwb/anat/sub-4dqh9tzwb_run-02_T1w.json
			This file is missing for subject sub-4dqh9tzwb, but is present for at least one other subject.
			Evidence: Subject: sub-4dqh9tzwb; Missing file: sub-4dqh9tzwb_run-02_T1w.json
		./sub-4dqh9tzwb/anat/sub-4dqh9tzwb_run-02_T1w.nii.gz
			This file is missing for subject sub-4dqh9tzwb, but is present for at least one other subject.
			Evidence: Subject: sub-4dqh9tzwb; Missing file: sub-4dqh9tzwb_run-02_T1w.nii.gz
		./sub-4drq4crsw/anat/sub-4drq4crsw_run-02_T1w.json
			This file is missing for subject sub-4drq4crsw, but is present for at least one other subject.
			Evidence: Subject: sub-4drq4crsw; Missing file: sub-4drq4crsw_run-02_T1w.json
		./sub-4drq4crsw/anat/sub-4drq4crsw_run-02_T1w.nii.gz
			This file is missing for subject sub-4drq4crsw, but is present for at least one other subject.
			Evidence: Subject: sub-4drq4crsw; Missing file: sub-4drq4crsw_run-02_T1w.nii.gz
		./sub-4e2sr6mvz/anat/sub-4e2sr6mvz_run-02_T1w.json
			This file is missing for subject sub-4e2sr6mvz, but is present for at least one other subject.
			Evidence: Subject: sub-4e2sr6mvz; Missing file: sub-4e2sr6mvz_run-02_T1w.json
		./sub-4e2sr6mvz/anat/sub-4e2sr6mvz_run-02_T1w.nii.gz
			This file is missing for subject sub-4e2sr6mvz, but is present for at least one other subject.
			Evidence: Subject: sub-4e2sr6mvz; Missing file: sub-4e2sr6mvz_run-02_T1w.nii.gz
		./sub-4e4f6myu2/anat/sub-4e4f6myu2_run-02_T1w.json
			This file is missing for subject sub-4e4f6myu2, but is present for at least one other subject.
			Evidence: Subject: sub-4e4f6myu2; Missing file: sub-4e4f6myu2_run-02_T1w.json
		./sub-4e4f6myu2/anat/sub-4e4f6myu2_run-02_T1w.nii.gz
			This file is missing for subject sub-4e4f6myu2, but is present for at least one other subject.
			Evidence: Subject: sub-4e4f6myu2; Missing file: sub-4e4f6myu2_run-02_T1w.nii.gz
		./sub-4evtav4d1/anat/sub-4evtav4d1_run-02_T1w.json
			This file is missing for subject sub-4evtav4d1, but is present for at least one other subject.
			Evidence: Subject: sub-4evtav4d1; Missing file: sub-4evtav4d1_run-02_T1w.json
		./sub-4evtav4d1/anat/sub-4evtav4d1_run-02_T1w.nii.gz
			This file is missing for subject sub-4evtav4d1, but is present for at least one other subject.
			Evidence: Subject: sub-4evtav4d1; Missing file: sub-4evtav4d1_run-02_T1w.nii.gz
		./sub-4ey68n584/anat/sub-4ey68n584_run-02_T1w.json
			This file is missing for subject sub-4ey68n584, but is present for at least one other subject.
			Evidence: Subject: sub-4ey68n584; Missing file: sub-4ey68n584_run-02_T1w.json
		./sub-4ey68n584/anat/sub-4ey68n584_run-02_T1w.nii.gz
			This file is missing for subject sub-4ey68n584, but is present for at least one other subject.
			Evidence: Subject: sub-4ey68n584; Missing file: sub-4ey68n584_run-02_T1w.nii.gz
		./sub-4f2jw436a/anat/sub-4f2jw436a_run-02_T1w.json
			This file is missing for subject sub-4f2jw436a, but is present for at least one other subject.
			Evidence: Subject: sub-4f2jw436a; Missing file: sub-4f2jw436a_run-02_T1w.json
		./sub-4f2jw436a/anat/sub-4f2jw436a_run-02_T1w.nii.gz
			This file is missing for subject sub-4f2jw436a, but is present for at least one other subject.
			Evidence: Subject: sub-4f2jw436a; Missing file: sub-4f2jw436a_run-02_T1w.nii.gz
		./sub-4f2jw436a/sub-4f2jw436a_scans.tsv
			This file is missing for subject sub-4f2jw436a, but is present for at least one other subject.
			Evidence: Subject: sub-4f2jw436a; Missing file: sub-4f2jw436a_scans.tsv
		./sub-4fcqkgtu7/anat/sub-4fcqkgtu7_run-02_T1w.json
			This file is missing for subject sub-4fcqkgtu7, but is present for at least one other subject.
			Evidence: Subject: sub-4fcqkgtu7; Missing file: sub-4fcqkgtu7_run-02_T1w.json
		./sub-4fcqkgtu7/anat/sub-4fcqkgtu7_run-02_T1w.nii.gz
			This file is missing for subject sub-4fcqkgtu7, but is present for at least one other subject.
			Evidence: Subject: sub-4fcqkgtu7; Missing file: sub-4fcqkgtu7_run-02_T1w.nii.gz
		./sub-4fe1ae7gk/anat/sub-4fe1ae7gk_run-02_T1w.json
			This file is missing for subject sub-4fe1ae7gk, but is present for at least one other subject.
			Evidence: Subject: sub-4fe1ae7gk; Missing file: sub-4fe1ae7gk_run-02_T1w.json
		./sub-4fe1ae7gk/anat/sub-4fe1ae7gk_run-02_T1w.nii.gz
			This file is missing for subject sub-4fe1ae7gk, but is present for at least one other subject.
			Evidence: Subject: sub-4fe1ae7gk; Missing file: sub-4fe1ae7gk_run-02_T1w.nii.gz
		./sub-4g1cuet2j/anat/sub-4g1cuet2j_run-02_T1w.json
			This file is missing for subject sub-4g1cuet2j, but is present for at least one other subject.
			Evidence: Subject: sub-4g1cuet2j; Missing file: sub-4g1cuet2j_run-02_T1w.json
		./sub-4g1cuet2j/anat/sub-4g1cuet2j_run-02_T1w.nii.gz
			This file is missing for subject sub-4g1cuet2j, but is present for at least one other subject.
			Evidence: Subject: sub-4g1cuet2j; Missing file: sub-4g1cuet2j_run-02_T1w.nii.gz
		./sub-4gtgh1a16/anat/sub-4gtgh1a16_run-02_T1w.json
			This file is missing for subject sub-4gtgh1a16, but is present for at least one other subject.
			Evidence: Subject: sub-4gtgh1a16; Missing file: sub-4gtgh1a16_run-02_T1w.json
		./sub-4gtgh1a16/anat/sub-4gtgh1a16_run-02_T1w.nii.gz
			This file is missing for subject sub-4gtgh1a16, but is present for at least one other subject.
			Evidence: Subject: sub-4gtgh1a16; Missing file: sub-4gtgh1a16_run-02_T1w.nii.gz
		./sub-4h3393ygf/anat/sub-4h3393ygf_run-02_T1w.json
			This file is missing for subject sub-4h3393ygf, but is present for at least one other subject.
			Evidence: Subject: sub-4h3393ygf; Missing file: sub-4h3393ygf_run-02_T1w.json
		./sub-4h3393ygf/anat/sub-4h3393ygf_run-02_T1w.nii.gz
			This file is missing for subject sub-4h3393ygf, but is present for at least one other subject.
			Evidence: Subject: sub-4h3393ygf; Missing file: sub-4h3393ygf_run-02_T1w.nii.gz
		./sub-4h5j6wr9g/anat/sub-4h5j6wr9g_run-02_T1w.json
			This file is missing for subject sub-4h5j6wr9g, but is present for at least one other subject.
			Evidence: Subject: sub-4h5j6wr9g; Missing file: sub-4h5j6wr9g_run-02_T1w.json
		./sub-4h5j6wr9g/anat/sub-4h5j6wr9g_run-02_T1w.nii.gz
			This file is missing for subject sub-4h5j6wr9g, but is present for at least one other subject.
			Evidence: Subject: sub-4h5j6wr9g; Missing file: sub-4h5j6wr9g_run-02_T1w.nii.gz
		./sub-4hgjn157r/anat/sub-4hgjn157r_run-02_T1w.json
			This file is missing for subject sub-4hgjn157r, but is present for at least one other subject.
			Evidence: Subject: sub-4hgjn157r; Missing file: sub-4hgjn157r_run-02_T1w.json
		./sub-4hgjn157r/anat/sub-4hgjn157r_run-02_T1w.nii.gz
			This file is missing for subject sub-4hgjn157r, but is present for at least one other subject.
			Evidence: Subject: sub-4hgjn157r; Missing file: sub-4hgjn157r_run-02_T1w.nii.gz
		./sub-4jmjwrmue/anat/sub-4jmjwrmue_run-02_T1w.json
			This file is missing for subject sub-4jmjwrmue, but is present for at least one other subject.
			Evidence: Subject: sub-4jmjwrmue; Missing file: sub-4jmjwrmue_run-02_T1w.json
		./sub-4jmjwrmue/anat/sub-4jmjwrmue_run-02_T1w.nii.gz
			This file is missing for subject sub-4jmjwrmue, but is present for at least one other subject.
			Evidence: Subject: sub-4jmjwrmue; Missing file: sub-4jmjwrmue_run-02_T1w.nii.gz
		./sub-4kh6y9wkg/anat/sub-4kh6y9wkg_run-02_T1w.json
			This file is missing for subject sub-4kh6y9wkg, but is present for at least one other subject.
			Evidence: Subject: sub-4kh6y9wkg; Missing file: sub-4kh6y9wkg_run-02_T1w.json
		./sub-4kh6y9wkg/anat/sub-4kh6y9wkg_run-02_T1w.nii.gz
			This file is missing for subject sub-4kh6y9wkg, but is present for at least one other subject.
			Evidence: Subject: sub-4kh6y9wkg; Missing file: sub-4kh6y9wkg_run-02_T1w.nii.gz
		./sub-4mbkuar3a/anat/sub-4mbkuar3a_run-02_T1w.json
			This file is missing for subject sub-4mbkuar3a, but is present for at least one other subject.
			Evidence: Subject: sub-4mbkuar3a; Missing file: sub-4mbkuar3a_run-02_T1w.json
		./sub-4mbkuar3a/anat/sub-4mbkuar3a_run-02_T1w.nii.gz
			This file is missing for subject sub-4mbkuar3a, but is present for at least one other subject.
			Evidence: Subject: sub-4mbkuar3a; Missing file: sub-4mbkuar3a_run-02_T1w.nii.gz
		./sub-4n157v5zb/anat/sub-4n157v5zb_run-02_T1w.json
			This file is missing for subject sub-4n157v5zb, but is present for at least one other subject.
			Evidence: Subject: sub-4n157v5zb; Missing file: sub-4n157v5zb_run-02_T1w.json
		./sub-4n157v5zb/anat/sub-4n157v5zb_run-02_T1w.nii.gz
			This file is missing for subject sub-4n157v5zb, but is present for at least one other subject.
			Evidence: Subject: sub-4n157v5zb; Missing file: sub-4n157v5zb_run-02_T1w.nii.gz
		./sub-4n6p8akyq/anat/sub-4n6p8akyq_run-02_T1w.json
			This file is missing for subject sub-4n6p8akyq, but is present for at least one other subject.
			Evidence: Subject: sub-4n6p8akyq; Missing file: sub-4n6p8akyq_run-02_T1w.json
		./sub-4n6p8akyq/anat/sub-4n6p8akyq_run-02_T1w.nii.gz
			This file is missing for subject sub-4n6p8akyq, but is present for at least one other subject.
			Evidence: Subject: sub-4n6p8akyq; Missing file: sub-4n6p8akyq_run-02_T1w.nii.gz
		./sub-4n8kgakqg/anat/sub-4n8kgakqg_run-02_T1w.json
			This file is missing for subject sub-4n8kgakqg, but is present for at least one other subject.
			Evidence: Subject: sub-4n8kgakqg; Missing file: sub-4n8kgakqg_run-02_T1w.json
		./sub-4n8kgakqg/anat/sub-4n8kgakqg_run-02_T1w.nii.gz
			This file is missing for subject sub-4n8kgakqg, but is present for at least one other subject.
			Evidence: Subject: sub-4n8kgakqg; Missing file: sub-4n8kgakqg_run-02_T1w.nii.gz
		./sub-4nq2qmrch/anat/sub-4nq2qmrch_run-02_T1w.json
			This file is missing for subject sub-4nq2qmrch, but is present for at least one other subject.
			Evidence: Subject: sub-4nq2qmrch; Missing file: sub-4nq2qmrch_run-02_T1w.json
		./sub-4nq2qmrch/anat/sub-4nq2qmrch_run-02_T1w.nii.gz
			This file is missing for subject sub-4nq2qmrch, but is present for at least one other subject.
			Evidence: Subject: sub-4nq2qmrch; Missing file: sub-4nq2qmrch_run-02_T1w.nii.gz
		./sub-4p377pw7q/anat/sub-4p377pw7q_run-02_T1w.json
			This file is missing for subject sub-4p377pw7q, but is present for at least one other subject.
			Evidence: Subject: sub-4p377pw7q; Missing file: sub-4p377pw7q_run-02_T1w.json
		./sub-4p377pw7q/anat/sub-4p377pw7q_run-02_T1w.nii.gz
			This file is missing for subject sub-4p377pw7q, but is present for at least one other subject.
			Evidence: Subject: sub-4p377pw7q; Missing file: sub-4p377pw7q_run-02_T1w.nii.gz
		./sub-4ppezjksp/anat/sub-4ppezjksp_run-02_T1w.json
			This file is missing for subject sub-4ppezjksp, but is present for at least one other subject.
			Evidence: Subject: sub-4ppezjksp; Missing file: sub-4ppezjksp_run-02_T1w.json
		./sub-4ppezjksp/anat/sub-4ppezjksp_run-02_T1w.nii.gz
			This file is missing for subject sub-4ppezjksp, but is present for at least one other subject.
			Evidence: Subject: sub-4ppezjksp; Missing file: sub-4ppezjksp_run-02_T1w.nii.gz
		./sub-4ppezjksp/sub-4ppezjksp_scans.tsv
			This file is missing for subject sub-4ppezjksp, but is present for at least one other subject.
			Evidence: Subject: sub-4ppezjksp; Missing file: sub-4ppezjksp_scans.tsv
		./sub-4q88uysz8/anat/sub-4q88uysz8_run-02_T1w.json
			This file is missing for subject sub-4q88uysz8, but is present for at least one other subject.
			Evidence: Subject: sub-4q88uysz8; Missing file: sub-4q88uysz8_run-02_T1w.json
		./sub-4q88uysz8/anat/sub-4q88uysz8_run-02_T1w.nii.gz
			This file is missing for subject sub-4q88uysz8, but is present for at least one other subject.
			Evidence: Subject: sub-4q88uysz8; Missing file: sub-4q88uysz8_run-02_T1w.nii.gz
		./sub-4qcqy53pg/anat/sub-4qcqy53pg_run-02_T1w.json
			This file is missing for subject sub-4qcqy53pg, but is present for at least one other subject.
			Evidence: Subject: sub-4qcqy53pg; Missing file: sub-4qcqy53pg_run-02_T1w.json
		./sub-4qcqy53pg/anat/sub-4qcqy53pg_run-02_T1w.nii.gz
			This file is missing for subject sub-4qcqy53pg, but is present for at least one other subject.
			Evidence: Subject: sub-4qcqy53pg; Missing file: sub-4qcqy53pg_run-02_T1w.nii.gz
		./sub-4qgzsgaz4/anat/sub-4qgzsgaz4_run-02_T1w.json
			This file is missing for subject sub-4qgzsgaz4, but is present for at least one other subject.
			Evidence: Subject: sub-4qgzsgaz4; Missing file: sub-4qgzsgaz4_run-02_T1w.json
		./sub-4qgzsgaz4/anat/sub-4qgzsgaz4_run-02_T1w.nii.gz
			This file is missing for subject sub-4qgzsgaz4, but is present for at least one other subject.
			Evidence: Subject: sub-4qgzsgaz4; Missing file: sub-4qgzsgaz4_run-02_T1w.nii.gz
		./sub-4qrppb7ey/anat/sub-4qrppb7ey_run-02_T1w.json
			This file is missing for subject sub-4qrppb7ey, but is present for at least one other subject.
			Evidence: Subject: sub-4qrppb7ey; Missing file: sub-4qrppb7ey_run-02_T1w.json
		./sub-4qrppb7ey/anat/sub-4qrppb7ey_run-02_T1w.nii.gz
			This file is missing for subject sub-4qrppb7ey, but is present for at least one other subject.
			Evidence: Subject: sub-4qrppb7ey; Missing file: sub-4qrppb7ey_run-02_T1w.nii.gz
		./sub-4rfa33vua/anat/sub-4rfa33vua_run-02_T1w.json
			This file is missing for subject sub-4rfa33vua, but is present for at least one other subject.
			Evidence: Subject: sub-4rfa33vua; Missing file: sub-4rfa33vua_run-02_T1w.json
		./sub-4rfa33vua/anat/sub-4rfa33vua_run-02_T1w.nii.gz
			This file is missing for subject sub-4rfa33vua, but is present for at least one other subject.
			Evidence: Subject: sub-4rfa33vua; Missing file: sub-4rfa33vua_run-02_T1w.nii.gz
		./sub-4rs7828jg/anat/sub-4rs7828jg_run-02_T1w.json
			This file is missing for subject sub-4rs7828jg, but is present for at least one other subject.
			Evidence: Subject: sub-4rs7828jg; Missing file: sub-4rs7828jg_run-02_T1w.json
		./sub-4rs7828jg/anat/sub-4rs7828jg_run-02_T1w.nii.gz
			This file is missing for subject sub-4rs7828jg, but is present for at least one other subject.
			Evidence: Subject: sub-4rs7828jg; Missing file: sub-4rs7828jg_run-02_T1w.nii.gz
		./sub-4s7bzy28k/anat/sub-4s7bzy28k_run-02_T1w.json
			This file is missing for subject sub-4s7bzy28k, but is present for at least one other subject.
			Evidence: Subject: sub-4s7bzy28k; Missing file: sub-4s7bzy28k_run-02_T1w.json
		./sub-4s7bzy28k/anat/sub-4s7bzy28k_run-02_T1w.nii.gz
			This file is missing for subject sub-4s7bzy28k, but is present for at least one other subject.
			Evidence: Subject: sub-4s7bzy28k; Missing file: sub-4s7bzy28k_run-02_T1w.nii.gz
		./sub-4s7veymgm/anat/sub-4s7veymgm_run-02_T1w.json
			This file is missing for subject sub-4s7veymgm, but is present for at least one other subject.
			Evidence: Subject: sub-4s7veymgm; Missing file: sub-4s7veymgm_run-02_T1w.json
		./sub-4s7veymgm/anat/sub-4s7veymgm_run-02_T1w.nii.gz
			This file is missing for subject sub-4s7veymgm, but is present for at least one other subject.
			Evidence: Subject: sub-4s7veymgm; Missing file: sub-4s7veymgm_run-02_T1w.nii.gz
		./sub-4spq4wg48/anat/sub-4spq4wg48_run-02_T1w.json
			This file is missing for subject sub-4spq4wg48, but is present for at least one other subject.
			Evidence: Subject: sub-4spq4wg48; Missing file: sub-4spq4wg48_run-02_T1w.json
		./sub-4spq4wg48/anat/sub-4spq4wg48_run-02_T1w.nii.gz
			This file is missing for subject sub-4spq4wg48, but is present for at least one other subject.
			Evidence: Subject: sub-4spq4wg48; Missing file: sub-4spq4wg48_run-02_T1w.nii.gz
		./sub-4tenc3ujs/anat/sub-4tenc3ujs_run-02_T1w.json
			This file is missing for subject sub-4tenc3ujs, but is present for at least one other subject.
			Evidence: Subject: sub-4tenc3ujs; Missing file: sub-4tenc3ujs_run-02_T1w.json
		./sub-4tenc3ujs/anat/sub-4tenc3ujs_run-02_T1w.nii.gz
			This file is missing for subject sub-4tenc3ujs, but is present for at least one other subject.
			Evidence: Subject: sub-4tenc3ujs; Missing file: sub-4tenc3ujs_run-02_T1w.nii.gz
		./sub-4tzuvbnue/anat/sub-4tzuvbnue_run-02_T1w.json
			This file is missing for subject sub-4tzuvbnue, but is present for at least one other subject.
			Evidence: Subject: sub-4tzuvbnue; Missing file: sub-4tzuvbnue_run-02_T1w.json
		./sub-4tzuvbnue/anat/sub-4tzuvbnue_run-02_T1w.nii.gz
			This file is missing for subject sub-4tzuvbnue, but is present for at least one other subject.
			Evidence: Subject: sub-4tzuvbnue; Missing file: sub-4tzuvbnue_run-02_T1w.nii.gz
		./sub-4u1j1u1zd/anat/sub-4u1j1u1zd_run-02_T1w.json
			This file is missing for subject sub-4u1j1u1zd, but is present for at least one other subject.
			Evidence: Subject: sub-4u1j1u1zd; Missing file: sub-4u1j1u1zd_run-02_T1w.json
		./sub-4u1j1u1zd/anat/sub-4u1j1u1zd_run-02_T1w.nii.gz
			This file is missing for subject sub-4u1j1u1zd, but is present for at least one other subject.
			Evidence: Subject: sub-4u1j1u1zd; Missing file: sub-4u1j1u1zd_run-02_T1w.nii.gz
		./sub-4u4b55tqr/anat/sub-4u4b55tqr_run-02_T1w.json
			This file is missing for subject sub-4u4b55tqr, but is present for at least one other subject.
			Evidence: Subject: sub-4u4b55tqr; Missing file: sub-4u4b55tqr_run-02_T1w.json
		./sub-4u4b55tqr/anat/sub-4u4b55tqr_run-02_T1w.nii.gz
			This file is missing for subject sub-4u4b55tqr, but is present for at least one other subject.
			Evidence: Subject: sub-4u4b55tqr; Missing file: sub-4u4b55tqr_run-02_T1w.nii.gz
		./sub-4uctr7u3x/anat/sub-4uctr7u3x_run-02_T1w.json
			This file is missing for subject sub-4uctr7u3x, but is present for at least one other subject.
			Evidence: Subject: sub-4uctr7u3x; Missing file: sub-4uctr7u3x_run-02_T1w.json
		./sub-4uctr7u3x/anat/sub-4uctr7u3x_run-02_T1w.nii.gz
			This file is missing for subject sub-4uctr7u3x, but is present for at least one other subject.
			Evidence: Subject: sub-4uctr7u3x; Missing file: sub-4uctr7u3x_run-02_T1w.nii.gz
		./sub-4udt43e5n/anat/sub-4udt43e5n_run-02_T1w.json
			This file is missing for subject sub-4udt43e5n, but is present for at least one other subject.
			Evidence: Subject: sub-4udt43e5n; Missing file: sub-4udt43e5n_run-02_T1w.json
		./sub-4udt43e5n/anat/sub-4udt43e5n_run-02_T1w.nii.gz
			This file is missing for subject sub-4udt43e5n, but is present for at least one other subject.
			Evidence: Subject: sub-4udt43e5n; Missing file: sub-4udt43e5n_run-02_T1w.nii.gz
		./sub-4uvs4yf1s/anat/sub-4uvs4yf1s_run-02_T1w.json
			This file is missing for subject sub-4uvs4yf1s, but is present for at least one other subject.
			Evidence: Subject: sub-4uvs4yf1s; Missing file: sub-4uvs4yf1s_run-02_T1w.json
		./sub-4uvs4yf1s/anat/sub-4uvs4yf1s_run-02_T1w.nii.gz
			This file is missing for subject sub-4uvs4yf1s, but is present for at least one other subject.
			Evidence: Subject: sub-4uvs4yf1s; Missing file: sub-4uvs4yf1s_run-02_T1w.nii.gz
		./sub-4uxvxj3ej/anat/sub-4uxvxj3ej_run-02_T1w.json
			This file is missing for subject sub-4uxvxj3ej, but is present for at least one other subject.
			Evidence: Subject: sub-4uxvxj3ej; Missing file: sub-4uxvxj3ej_run-02_T1w.json
		./sub-4uxvxj3ej/anat/sub-4uxvxj3ej_run-02_T1w.nii.gz
			This file is missing for subject sub-4uxvxj3ej, but is present for at least one other subject.
			Evidence: Subject: sub-4uxvxj3ej; Missing file: sub-4uxvxj3ej_run-02_T1w.nii.gz
		./sub-4w7tvp77v/anat/sub-4w7tvp77v_run-02_T1w.json
			This file is missing for subject sub-4w7tvp77v, but is present for at least one other subject.
			Evidence: Subject: sub-4w7tvp77v; Missing file: sub-4w7tvp77v_run-02_T1w.json
		./sub-4w7tvp77v/anat/sub-4w7tvp77v_run-02_T1w.nii.gz
			This file is missing for subject sub-4w7tvp77v, but is present for at least one other subject.
			Evidence: Subject: sub-4w7tvp77v; Missing file: sub-4w7tvp77v_run-02_T1w.nii.gz
		./sub-4w7tvp77v/sub-4w7tvp77v_scans.tsv
			This file is missing for subject sub-4w7tvp77v, but is present for at least one other subject.
			Evidence: Subject: sub-4w7tvp77v; Missing file: sub-4w7tvp77v_scans.tsv
		./sub-4wnr4we99/anat/sub-4wnr4we99_run-02_T1w.json
			This file is missing for subject sub-4wnr4we99, but is present for at least one other subject.
			Evidence: Subject: sub-4wnr4we99; Missing file: sub-4wnr4we99_run-02_T1w.json
		./sub-4wnr4we99/anat/sub-4wnr4we99_run-02_T1w.nii.gz
			This file is missing for subject sub-4wnr4we99, but is present for at least one other subject.
			Evidence: Subject: sub-4wnr4we99; Missing file: sub-4wnr4we99_run-02_T1w.nii.gz
		./sub-4wqs2zdqm/anat/sub-4wqs2zdqm_run-02_T1w.json
			This file is missing for subject sub-4wqs2zdqm, but is present for at least one other subject.
			Evidence: Subject: sub-4wqs2zdqm; Missing file: sub-4wqs2zdqm_run-02_T1w.json
		./sub-4wqs2zdqm/anat/sub-4wqs2zdqm_run-02_T1w.nii.gz
			This file is missing for subject sub-4wqs2zdqm, but is present for at least one other subject.
			Evidence: Subject: sub-4wqs2zdqm; Missing file: sub-4wqs2zdqm_run-02_T1w.nii.gz
		./sub-4x1ftxk4u/anat/sub-4x1ftxk4u_run-02_T1w.json
			This file is missing for subject sub-4x1ftxk4u, but is present for at least one other subject.
			Evidence: Subject: sub-4x1ftxk4u; Missing file: sub-4x1ftxk4u_run-02_T1w.json
		./sub-4x1ftxk4u/anat/sub-4x1ftxk4u_run-02_T1w.nii.gz
			This file is missing for subject sub-4x1ftxk4u, but is present for at least one other subject.
			Evidence: Subject: sub-4x1ftxk4u; Missing file: sub-4x1ftxk4u_run-02_T1w.nii.gz
		./sub-4x764rxqd/anat/sub-4x764rxqd_run-02_T1w.json
			This file is missing for subject sub-4x764rxqd, but is present for at least one other subject.
			Evidence: Subject: sub-4x764rxqd; Missing file: sub-4x764rxqd_run-02_T1w.json
		./sub-4x764rxqd/anat/sub-4x764rxqd_run-02_T1w.nii.gz
			This file is missing for subject sub-4x764rxqd, but is present for at least one other subject.
			Evidence: Subject: sub-4x764rxqd; Missing file: sub-4x764rxqd_run-02_T1w.nii.gz
		./sub-4xf8cq2s8/anat/sub-4xf8cq2s8_run-02_T1w.json
			This file is missing for subject sub-4xf8cq2s8, but is present for at least one other subject.
			Evidence: Subject: sub-4xf8cq2s8; Missing file: sub-4xf8cq2s8_run-02_T1w.json
		./sub-4xf8cq2s8/anat/sub-4xf8cq2s8_run-02_T1w.nii.gz
			This file is missing for subject sub-4xf8cq2s8, but is present for at least one other subject.
			Evidence: Subject: sub-4xf8cq2s8; Missing file: sub-4xf8cq2s8_run-02_T1w.nii.gz
		./sub-4xwgfbkzr/anat/sub-4xwgfbkzr_run-02_T1w.json
			This file is missing for subject sub-4xwgfbkzr, but is present for at least one other subject.
			Evidence: Subject: sub-4xwgfbkzr; Missing file: sub-4xwgfbkzr_run-02_T1w.json
		./sub-4xwgfbkzr/anat/sub-4xwgfbkzr_run-02_T1w.nii.gz
			This file is missing for subject sub-4xwgfbkzr, but is present for at least one other subject.
			Evidence: Subject: sub-4xwgfbkzr; Missing file: sub-4xwgfbkzr_run-02_T1w.nii.gz
		./sub-4xwgfbkzr/sub-4xwgfbkzr_scans.tsv
			This file is missing for subject sub-4xwgfbkzr, but is present for at least one other subject.
			Evidence: Subject: sub-4xwgfbkzr; Missing file: sub-4xwgfbkzr_scans.tsv
		./sub-4xzqx31ku/anat/sub-4xzqx31ku_run-02_T1w.json
			This file is missing for subject sub-4xzqx31ku, but is present for at least one other subject.
			Evidence: Subject: sub-4xzqx31ku; Missing file: sub-4xzqx31ku_run-02_T1w.json
		./sub-4xzqx31ku/anat/sub-4xzqx31ku_run-02_T1w.nii.gz
			This file is missing for subject sub-4xzqx31ku, but is present for at least one other subject.
			Evidence: Subject: sub-4xzqx31ku; Missing file: sub-4xzqx31ku_run-02_T1w.nii.gz
		./sub-4ybcwhkrn/anat/sub-4ybcwhkrn_run-02_T1w.json
			This file is missing for subject sub-4ybcwhkrn, but is present for at least one other subject.
			Evidence: Subject: sub-4ybcwhkrn; Missing file: sub-4ybcwhkrn_run-02_T1w.json
		./sub-4ybcwhkrn/anat/sub-4ybcwhkrn_run-02_T1w.nii.gz
			This file is missing for subject sub-4ybcwhkrn, but is present for at least one other subject.
			Evidence: Subject: sub-4ybcwhkrn; Missing file: sub-4ybcwhkrn_run-02_T1w.nii.gz
		./sub-4zhcnnzry/anat/sub-4zhcnnzry_run-02_T1w.json
			This file is missing for subject sub-4zhcnnzry, but is present for at least one other subject.
			Evidence: Subject: sub-4zhcnnzry; Missing file: sub-4zhcnnzry_run-02_T1w.json
		./sub-4zhcnnzry/anat/sub-4zhcnnzry_run-02_T1w.nii.gz
			This file is missing for subject sub-4zhcnnzry, but is present for at least one other subject.
			Evidence: Subject: sub-4zhcnnzry; Missing file: sub-4zhcnnzry_run-02_T1w.nii.gz

[36m	Please visit https://neurostars.org/search?q=INCONSISTENT_SUBJECTS for existing conversations about this issue.[39m

        [34m[4mSummary:[24m[39m                  [34m[4mAvailable Tasks:[24m[39m                     [34m[4mAvailable Modalities:[39m[24m 
        1641 Files, 17.8GB        rest                                 MRI                   
        78 - Subjects             TODO: full task name for rest                              
        1 - Session                                                                          


[36m	If you have any questions, please post on https://neurostars.org/tags/bids.[39m
