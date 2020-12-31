# MAWILabProbing-Causality
Inspection of causal structures among features in probing dataset - source from MAWILab
  - from https://github.com/gubertoli/ProbingDataset
  - looking to PC Graph Algorithm for preliminary causal structure analysis
  - cannot find true causality unless no relevant unmeasured confounders
  -  A few things to note about feature importance changes when
introducing randomly generated columns into the data 
frame is that the feature importances from fake variables
that appear to be drastically lower are from ip_flags,
ip_dsfield, tcp_seq, tcp_flags_fin, tcp_flags_urg, 
and tcp_flags_push. These
attributes seem to indicate that flagging perhaps is 
what could be causing the label to result in 
normal or one of the probing attacks. Xmas sends
packets of with FIN, URG, and PUSH flags "lit up like 
a christmas tree" and other port scanning methods 
use flagging patterns.
