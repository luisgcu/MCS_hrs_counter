# Machine control Studio hours counter.
Simple function to count working time of  a Control Techniques  AC  drive  "unidrive M family" ( code runs on the on-board PLC).  Working time is stored in power down save parameter.

It can be loaded on the internal plc of  any model  starting with the C200/300, M200, M400, M70x.

**The function block**.

![](https://github.com/luisgcu/MCS_hrs_counter/blob/master/docs/FB1.jpg)

**How it works.**

The first to do is to enter desire time to count ( time can be  entered in seconds or minutes or hours), when  desired time is completed the output is active.  I.e if we want to count 5 minutes we assign 5 to mins_tocount, when the 5 minutes is completed the mins_cnt_completed is active or true.

**Input variables  description.**

**enbl_count**  : enables the function to start counting time.

**rst_count** : Reset all output variables.

**hrs_toCount** : if hours count needed  assigns this input  the qty of hour to count.

**mins_tocount** : if minutes  count needed  assigns this input  the qty of minutes to count .

**segs_toCount**: if seconds  count needed  assigns this input  the qty of seconds to count. 

**Output variables  description.**

**hrs_cnt_completed** :  this  output  is activated when enbl_count input had been active a total = hrs_toCount .

**segs_cnt_completed** : this  output  is activated when enbl_count input had been active a total = segs_tocount .

**mins_cnt_completed** : this  output  is activated when enbl_count input had been active a total = mins_tocount .

**working_seg** : show the elapsed working time in seconds.

**working_min** : show the elapsed working time in minutes.

**working_hrs** : show the elapsed working time in hours.

### Function block working  on a program.

![](https://github.com/luisgcu/MCS_hrs_counter/blob/master/docs/FB2.jpg)





