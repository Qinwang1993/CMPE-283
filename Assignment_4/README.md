# CMPE 283 Assignment 4  
Team Member: Qin Wang - 013986752    
             Chen Zhang - 014536496  

## Assignment 3:  
This assignment is to illustrate the difference in performance when using nested paging versus shadow paging, and to illustrate the different exit frequencies and types.  

## Question: 
### 1. For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched. 
### Answer:
We met and did this research together. The following steps were all discussed and completed by ourselves:
1. Test nested paging
  Boost nested VM
  Run test_assignment3.c in nested VM
  Paste result in assignment4_nested.txt
  Shut down nested VM
  ![image](https://github.com/Qinwang1993/CMPE-283/blob/master/Assignment_3/Modify%20the%20code%20at%20the%20end%20of%20the%20cpuid.c%20file%20.png)
2. Test shadow paging
  Remove kvm-intel module from your running kernel
  sudo rmmod kvm-intel
  Reload kvm-intel module with the parameter ept=0
  Sudo insmod /lib/modules/5.12.0+/kernel/arch/x86/kvm/kvm-intel.ko ept=0
3. Boost the same nested VM
4. Run test_assignment3.c in nested VM
5. Paste result in assignment4_shadow.txt
6. Shut down nested VM


### 2. Include a sample of your print of exit count output from dmesg from “with ept” and “without ept”.
### 3. What did you learn from the count of exits? Was the count what you expected? If not, why not?
### 4. What changed between the two runs (ept vs no-ept)?
