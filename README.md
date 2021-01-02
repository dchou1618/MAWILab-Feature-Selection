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
a christmas tree", which could explain why these flags appear to be the driving
features for causing an observation to be labeled as normal or 
not.
  - From running wireshark for packet capture in real-time, one can run `sudo nmap -sX [routerIP]`
  to test how a local router may respond to an xmas tree scan. -sX is the tag indicating xmas
  that will flip on the flags urg, fin and push.

Looking ahead, there can be more work done to improve the accuracy of predictions with
the random forest model fit to the data. Because there is much more normal data, one
can either do oversampling of minority classes or undersampling of majority classes to handle
the imbalance in classes.
