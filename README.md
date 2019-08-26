# utl-keep-variables-that-end-in-M1-M2-or-M3-macro-varlist
Keep variables that end in M1 M2 or M3 macro varlist
    Keep variables that end in M1 M2 or M3 macro varlist                                                       
                                                                                                               
    gihub                                                                                                      
    https://tinyurl.com/y3x3ku94                                                                               
    https://github.com/rogerjdeangelis/utl-keep-variables-that-end-in-M1-M2-or-M3-macro-varlist                
                                                                                                               
    macros                                                                                                     
    https://tinyurl.com/y9nfugth                                                                               
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                 
                                                                                                               
    github                                                                                                     
    https://tinyurl.com/y5w5lcl5                                                                               
    https://stackoverflow.com/questions/24636814/regular-expression-only-match-if-string-ends-with-target      
                                                                                                               
    *_                   _                                                                                     
    (_)_ __  _ __  _   _| |_                                                                                   
    | | '_ \| '_ \| | | | __|                                                                                  
    | | | | | |_) | |_| | |_                                                                                   
    |_|_| |_| .__/ \__,_|\__|                                                                                  
            |_|                                                                                                
    ;                                                                                                          
                                                                                                               
    data have;                                                                                                 
                                                                                                               
     array ms[5] xm1-xm5 (5*1);                                                                                
     array ns[5] zn1-zn5 (5*9);                                                                                
                                                                                                               
    run;quit;                                                                                                  
                                                                                                               
    Up to 40 obs WORK.HAVE total obs=1                                                                         
                                                                                                               
    Obs    XM1    XM2    XM3    XM4    XM5    ZN1    ZN2    ZN3    ZN4    ZN5                                  
                                                                                                               
     1      1      1      1      1      1      9      9      9      9      9                                   
                                                                                                               
    *            _               _                                                                             
      ___  _   _| |_ _ __  _   _| |_                                                                           
     / _ \| | | | __| '_ \| | | | __|                                                                          
    | (_) | |_| | |_| |_) | |_| | |_                                                                           
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                          
                    |_|                                                                                        
    ;                                                                                                          
                                                                                                               
    WORK.WANT total obs=1                                                                                      
                                                                                                               
      XM1    XM2    XM3                                                                                        
                                                                                                               
       1      1      1                                                                                         
                                                                                                               
    *                                                                                                          
     _ __  _ __ ___   ___ ___  ___ ___                                                                         
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                        
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                        
    | .__/|_|  \___/ \___\___||___/___/                                                                        
    |_|                                                                                                        
    ;                                                                                                          
                                                                                                               
    data want;                                                                                                 
      set have(keep=%varlist(have,prx=/M1$|M2$|M3$/));                                                         
    run;quit;                                                                                                  
                                                                                                               
                                                                                                               
