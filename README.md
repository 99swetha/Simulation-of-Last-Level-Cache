# Simulation-of-Last-Level-Cache
- Designed and Simulated the Last Level Cache (LLC) for a processor that can be used with up to three other processors in a shared memory configuration.
- The design implements a write allocate policy, uses the MESI protocol for ensuring cache coherence and pseudo-LRU replacement policy.
- Built trace files for exhaustively testing LLC behavior and record statistics.


Project Description: Final Project Description.pdf
Project Report: ECE585_F22_MSD_Group10_Project_Report.pdf
Git Repository Link: https://github.com/swethac99/MSD_Group10

# MSD_Group10
*********List of files to be included for project***********

CacheTB.sv
CacheDesign.sv
ParameterDefinitions.sv
PLRU_Get.sv
PLRU_Update.sv
GetSnoopResult.sv
PutSnoopResult.sv
BusOperation.sv
MessageToCache.sv
CacheStructure.sv
TraceFile.txt


**********list of packages used in project**********

import ParameterDefinitions::*;
import CacheStructure::*;
import PLRU_Update::*;
import PLRU_Get::*;
import GetSnoopResult::*;
import PutSnoopResult::*;
import BusOperation::*;
import MessageToCache::*;



********Command line**********
vlog -work work CacheTB.sv
vsim -voptargs=+acc work.CacheTB +TRACEFILE=TraceFile.txt +MODE=NORMAL
vsim -voptargs=+acc work.CacheTB +TRACEFILE=TraceFile.txt +MODE=SILENT
vsim -voptargs=+acc work.CacheTB +TRACEFILE=TraceFile.txt +MODE=DEBUG
add wave -r \*
run -all

