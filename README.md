Thanks for sharing the commit and build log. Here's a quick summary and some guidance based on what you've posted:

🧾 Summary of the Change:

Commit: LICEX-11640: Remove check Id 14002 from Licensing NCC
Author: Gurusreekanth
Date: Wed Oct 15 10:18:47 2025 -0700
Files Changed:

serviceability_client/alerts/interface/alert_type_ids.proto
serviceability_client/serviceability/interface/analytics_data_transfer.proto


Change Type: 4 deletions


🛠️ Build System Notes:

The build system detected .proto file changes.
It also flagged that the change includes:

ntnx_add_library
ntnx_add_executable
ntnx_target_link_libraries
ntnx_add_subdirectory
.proto modifications
Potential changes in bigbang/*.yml




⚠️ Required Action:
Because of the nature of the changes, the system recommends:

"This change needs to be verified with Recursive Build. Or Refer DPRO-1727."

This means:

You should trigger a recursive build to ensure all dependencies and generated files (like .pb.h, .pb.cc) are correctly updated.
Alternatively, refer to DPRO-1727 for guidance on handling such changes.


✅ Suggested Next Steps:


Run Recursive Build:
If you're using a build tool like bigtop, run:
Shellbigtop build --recursiveShow more lines
or the equivalent command in your environment.


Verify Generated Files:
Ensure that the .proto changes correctly regenerate the corresponding .pb.h and .pb.cc files.


Check CMake Integration:
Confirm that the modified .proto files are still correctly referenced in your CMake setup via ntnx_add_library or similar macros.


Refer to DPRO-1727:
If you're unsure about the recursive build process or its implications, check the internal documentation or ticket DPRO-1727.



Would you like help drafting a checklist or automation script for recursive build verification?
Provide your feedback on BizChat
