# Alicante illustrative IFC4 sample

Verified (fetched URL): source dataset **3D Laser Scanning Data: Public Square in Murcia and Engineering Laboratory at the University of Alicante**, v1 (2024), by Adrian Riquelme, Roberto Tomas, Miguel Cano González and José Luis Pastor Navarro, University of Alicante. DOI: https://doi.org/10.5281/zenodo.11518223 . Source record: https://zenodo.org/records/11518223 . The fetched record declares **CC-BY-4.0**, https://creativecommons.org/licenses/by/4.0/ . Retained metadata: source-record.json.

Verified (local run): source.json records the exact LAS download URL, byte size, SHA-256 and source MD5. The LAS stays local and is excluded from Git.

Verified (local run): changes comprise LAS-to-point-cloud conversion, mean-coordinate translation, 2 cm voxel reduction, RANSAC plane fitting, largest connected patch selection, convex-hull extrusion and IFC4 export. The retained plane block comes from output/scan2bim-tls-merge-20261108/merge_bim.py. The geometry exporter comes from output/sample-pack-20261109/export.py. run.py adapts those existing stages to this single LAS input. No registration occurs with one scan.

Inferred: native Z supports illustrative wall/slab classification. Convex hulls can bridge disconnected surfaces and gaps. The 0.1 m extrusion thickness is illustrative and unmeasured. Neither element semantics nor extents have independent confirmation.

Verified (local export): all opening/occlusion labels remain **unknown: occlusion or opening not independently supported**. No IfcOpeningElement is exported.

Verified (local run): validation.json records IFC4 reopening, element counts and nonempty tessellation for each exported element. QA.html lists fitted-plane RMS residuals. These residuals measure agreement with fitted planes only.

Inferred: independent survey checks, dimensional accuracy, station-pair validation, boundaries and building semantics remain unproven. This is an illustrative sample. No client-ready accuracy claim or creator endorsement is made.

Verified (local reproduction command): `venv/bin/python run.py` from this directory uses the retained local LAS. The dependency versions appear in requirements.txt. Fetch only the source.json URL to reproduce the input; the entire record bundle is unnecessary.
