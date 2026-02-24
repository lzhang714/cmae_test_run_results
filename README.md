# cmae_test_run_results
Listing here some results from running the cmae calculation with wien2k. 

The exact command lines executed: 

init_lapw -sp -rkmax 9 -numk 5000  

init_so_lapw

runsp_lapw -so -p -ec 0.0000001 -cc 0.001 -i 100

save_lapw -d save_runsp_lapw_so

~/github/cmae/code/setup_cmae.py

runsp_lapw_fix_orb -so -orb -p -ec 0.000001 -cc 0.001 -i 100

save_lapw_fix_orb -d save_runsp_lapw_fix_orb
