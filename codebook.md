# Course Project Code Book

## Variable list and descriptions
The names of the attributes are similar to the following:
* tbodyacc-mean-x 
* tbodyacc-mean-y 
* tbodyacc-mean-z 
* tbodyacc-std-x
* tbodyacc-std-y 
* tbodyacc-std-z 
* tgravityacc-mean-x 
* tgravityacc-mean-y

Variable Name | Description
--------------|-------------
subject | ID the subject who performed the activity for each window sample. Its range is from 1 to 30.
activity | Activity name

## Data Set Information:

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

## Attribute Information

For each record in the dataset it is provided:
 * Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
 * Triaxial Angular velocity from the gyroscope.
 * A 561-feature vector with time and frequency domain variables.
 * Its activity label.
 * An identifier of the subject who carried out the experiment.

## Dataset Structure

> str(data)

```'data.frame':	180 obs. of  68 variables:
 $ subject                  : int  1 1 1 1 1 1 3 3 3 3 ...
 $ activity                 : Factor w/ 6 levels "laying","sitting",..: 4 6 5 2 3 1 4 6 5 2 ...
 $ tbodyacc.mean.x          : num  0.277 0.255 0.289 0.261 0.279 ...
 $ tbodyacc.mean.y          : num  -0.01738 -0.02395 -0.00992 -0.00131 -0.01614 ...
 $ tbodyacc.mean.z          : num  -0.1111 -0.0973 -0.1076 -0.1045 -0.1106 ...
 $ tbodyacc.std.x           : num  -0.284 -0.355 0.03 -0.977 -0.996 ...
 $ tbodyacc.std.y           : num  0.11446 -0.00232 -0.03194 -0.92262 -0.97319 ...
 $ tbodyacc.std.z           : num  -0.26 -0.0195 -0.2304 -0.9396 -0.9798 ...
 $ tgravityacc.mean.x       : num  0.935 0.893 0.932 0.832 0.943 ...
 $ tgravityacc.mean.y       : num  -0.282 -0.362 -0.267 0.204 -0.273 ...
 $ tgravityacc.mean.z       : num  -0.0681 -0.0754 -0.0621 0.332 0.0135 ...
 $ tgravityacc.std.x        : num  -0.977 -0.956 -0.951 -0.968 -0.994 ...
 $ tgravityacc.std.y        : num  -0.971 -0.953 -0.937 -0.936 -0.981 ...
 $ tgravityacc.std.z        : num  -0.948 -0.912 -0.896 -0.949 -0.976 ...
 $ tbodyaccjerk.mean.x      : num  0.074 0.1014 0.0542 0.0775 0.0754 ...
 $ tbodyaccjerk.mean.y      : num  0.028272 0.019486 0.02965 -0.000619 0.007976 ...
 $ tbodyaccjerk.mean.z      : num  -0.00417 -0.04556 -0.01097 -0.00337 -0.00369 ...
 $ tbodyaccjerk.std.x       : num  -0.1136 -0.4468 -0.0123 -0.9864 -0.9946 ...
 $ tbodyaccjerk.std.y       : num  0.067 -0.378 -0.102 -0.981 -0.986 ...
 $ tbodyaccjerk.std.z       : num  -0.503 -0.707 -0.346 -0.988 -0.992 ...
 $ tbodygyro.mean.x         : num  -0.0418 0.0505 -0.0351 -0.0454 -0.024 ...
 $ tbodygyro.mean.y         : num  -0.0695 -0.1662 -0.0909 -0.0919 -0.0594 ...
 $ tbodygyro.mean.z         : num  0.0849 0.0584 0.0901 0.0629 0.0748 ...
 $ tbodygyro.std.x          : num  -0.474 -0.545 -0.458 -0.977 -0.987 ...
 $ tbodygyro.std.y          : num  -0.05461 0.00411 -0.12635 -0.96647 -0.98773 ...
 $ tbodygyro.std.z          : num  -0.344 -0.507 -0.125 -0.941 -0.981 ...
 $ tbodygyrojerk.mean.x     : num  -0.09 -0.1222 -0.074 -0.0937 -0.0996 ...
 $ tbodygyrojerk.mean.y     : num  -0.0398 -0.0421 -0.044 -0.0402 -0.0441 ...
 $ tbodygyrojerk.mean.z     : num  -0.0461 -0.0407 -0.027 -0.0467 -0.049 ...
 $ tbodygyrojerk.std.x      : num  -0.207 -0.615 -0.487 -0.992 -0.993 ...
 $ tbodygyrojerk.std.y      : num  -0.304 -0.602 -0.239 -0.99 -0.995 ...
 $ tbodygyrojerk.std.z      : num  -0.404 -0.606 -0.269 -0.988 -0.992 ...
 $ tbodyaccmag.mean         : num  -0.137 -0.1299 0.0272 -0.9485 -0.9843 ...
 $ tbodyaccmag.std          : num  -0.2197 -0.325 0.0199 -0.9271 -0.9819 ...
 $ tgravityaccmag.mean      : num  -0.137 -0.1299 0.0272 -0.9485 -0.9843 ...
 $ tgravityaccmag.std       : num  -0.2197 -0.325 0.0199 -0.9271 -0.9819 ...
 $ tbodyaccjerkmag.mean     : num  -0.1414 -0.4665 -0.0894 -0.9874 -0.9924 ...
 $ tbodyaccjerkmag.std      : num  -0.0745 -0.479 -0.0258 -0.9841 -0.9931 ...
 $ tbodygyromag.mean        : num  -0.161 -0.1267 -0.0757 -0.9309 -0.9765 ...
 $ tbodygyromag.std         : num  -0.187 -0.149 -0.226 -0.935 -0.979 ...
 $ tbodygyrojerkmag.mean    : num  -0.299 -0.595 -0.295 -0.992 -0.995 ...
 $ tbodygyrojerkmag.std     : num  -0.325 -0.649 -0.307 -0.988 -0.995 ...
 $ fbodyacc.mean.x          : num  -0.2028 -0.4043 0.0382 -0.9796 -0.9952 ...
 $ fbodyacc.mean.y          : num  0.08971 -0.19098 0.00155 -0.94408 -0.97707 ...
 $ fbodyacc.mean.z          : num  -0.332 -0.433 -0.226 -0.959 -0.985 ...
 $ fbodyacc.std.x           : num  -0.3191 -0.3374 0.0243 -0.9764 -0.996 ...
 $ fbodyacc.std.y           : num  0.056 0.0218 -0.113 -0.9173 -0.9723 ...
 $ fbodyacc.std.z           : num  -0.28 0.086 -0.298 -0.934 -0.978 ...
 $ fbodyaccjerk.mean.x      : num  -0.1705 -0.4799 -0.0277 -0.9866 -0.9946 ...
 $ fbodyaccjerk.mean.y      : num  -0.0352 -0.4134 -0.1287 -0.9816 -0.9854 ...
 $ fbodyaccjerk.mean.z      : num  -0.469 -0.685 -0.288 -0.986 -0.991 ...
 $ fbodyaccjerk.std.x       : num  -0.1336 -0.4619 -0.0863 -0.9875 -0.9951 ...
 $ fbodyaccjerk.std.y       : num  0.107 -0.382 -0.135 -0.983 -0.987 ...
 $ fbodyaccjerk.std.z       : num  -0.535 -0.726 -0.402 -0.988 -0.992 ...
 $ fbodygyro.mean.x         : num  -0.339 -0.493 -0.352 -0.976 -0.986 ...
 $ fbodygyro.mean.y         : num  -0.1031 -0.3195 -0.0557 -0.9758 -0.989 ...
 $ fbodygyro.mean.z         : num  -0.2559 -0.4536 -0.0319 -0.9513 -0.9808 ...
 $ fbodygyro.std.x          : num  -0.517 -0.566 -0.495 -0.978 -0.987 ...
 $ fbodygyro.std.y          : num  -0.0335 0.1515 -0.1814 -0.9623 -0.9871 ...
 $ fbodygyro.std.z          : num  -0.437 -0.572 -0.238 -0.944 -0.982 ...
 $ fbodyaccmag.mean         : num  -0.1286 -0.3524 0.0966 -0.9478 -0.9854 ...
 $ fbodyaccmag.std          : num  -0.398 -0.416 -0.187 -0.928 -0.982 ...
 $ fbodybodyaccjerkmag.mean : num  -0.0571 -0.4427 0.0262 -0.9853 -0.9925 ...
 $ fbodybodyaccjerkmag.std  : num  -0.103 -0.533 -0.104 -0.982 -0.993 ...
 $ fbodybodygyromag.mean    : num  -0.199 -0.326 -0.186 -0.958 -0.985 ...
 $ fbodybodygyromag.std     : num  -0.321 -0.183 -0.398 -0.932 -0.978 ...
 $ fbodybodygyrojerkmag.mean: num  -0.319 -0.635 -0.282 -0.99 -0.995 ...
 $ fbodybodygyrojerkmag.std : num  -0.382 -0.694 -0.392 -0.987 -0.995 ...
 ```
## Summary of variables

```subject                  activity  tbodyacc.mean.x  tbodyacc.mean.y    
 Min.   : 1.0   laying           :30   Min.   :0.2216   Min.   :-0.040514  
 1st Qu.: 8.0   sitting          :30   1st Qu.:0.2712   1st Qu.:-0.020022  
 Median :15.5   standing         :30   Median :0.2770   Median :-0.017262  
 Mean   :15.5   walking          :30   Mean   :0.2743   Mean   :-0.017876  
 3rd Qu.:23.0   walkingdownstairs:30   3rd Qu.:0.2800   3rd Qu.:-0.014936  
 Max.   :30.0   walkingupstairs  :30   Max.   :0.3015   Max.   :-0.001308  
 tbodyacc.mean.z    tbodyacc.std.x    tbodyacc.std.y     tbodyacc.std.z   
 Min.   :-0.15251   Min.   :-0.9961   Min.   :-0.99024   Min.   :-0.9877  
 1st Qu.:-0.11207   1st Qu.:-0.9799   1st Qu.:-0.94205   1st Qu.:-0.9498  
 Median :-0.10819   Median :-0.7526   Median :-0.50897   Median :-0.6518  
 Mean   :-0.10916   Mean   :-0.5577   Mean   :-0.46046   Mean   :-0.5756  
 3rd Qu.:-0.10443   3rd Qu.:-0.1984   3rd Qu.:-0.03077   3rd Qu.:-0.2306  
 Max.   :-0.07538   Max.   : 0.6269   Max.   : 0.61694   Max.   : 0.6090  
 tgravityacc.mean.x tgravityacc.mean.y tgravityacc.mean.z tgravityacc.std.x
 Min.   :-0.6800    Min.   :-0.47989   Min.   :-0.49509   Min.   :-0.9968  
 1st Qu.: 0.8376    1st Qu.:-0.23319   1st Qu.:-0.11726   1st Qu.:-0.9825  
 Median : 0.9208    Median :-0.12782   Median : 0.02384   Median :-0.9695  
 Mean   : 0.6975    Mean   :-0.01621   Mean   : 0.07413   Mean   :-0.9638  
 3rd Qu.: 0.9425    3rd Qu.: 0.08773   3rd Qu.: 0.14946   3rd Qu.:-0.9509  
 Max.   : 0.9745    Max.   : 0.95659   Max.   : 0.95787   Max.   :-0.8296  
 tgravityacc.std.y tgravityacc.std.z tbodyaccjerk.mean.x tbodyaccjerk.mean.y 
 Min.   :-0.9942   Min.   :-0.9910   Min.   :0.04269     Min.   :-0.0386872  
 1st Qu.:-0.9711   1st Qu.:-0.9605   1st Qu.:0.07396     1st Qu.: 0.0004664  
 Median :-0.9590   Median :-0.9450   Median :0.07640     Median : 0.0094698  
 Mean   :-0.9524   Mean   :-0.9364   Mean   :0.07947     Mean   : 0.0075652  
 3rd Qu.:-0.9370   3rd Qu.:-0.9180   3rd Qu.:0.08330     3rd Qu.: 0.0134008  
 Max.   :-0.6436   Max.   :-0.6102   Max.   :0.13019     Max.   : 0.0568186  
 tbodyaccjerk.mean.z tbodyaccjerk.std.x tbodyaccjerk.std.y tbodyaccjerk.std.z
 Min.   :-0.067458   Min.   :-0.9946    Min.   :-0.9895    Min.   :-0.99329  
 1st Qu.:-0.010601   1st Qu.:-0.9832    1st Qu.:-0.9724    1st Qu.:-0.98266  
 Median :-0.003861   Median :-0.8104    Median :-0.7756    Median :-0.88366  
 Mean   :-0.004953   Mean   :-0.5949    Mean   :-0.5654    Mean   :-0.73596  
 3rd Qu.: 0.001958   3rd Qu.:-0.2233    3rd Qu.:-0.1483    3rd Qu.:-0.51212  
 Max.   : 0.038053   Max.   : 0.5443    Max.   : 0.3553    Max.   : 0.03102  
 tbodygyro.mean.x   tbodygyro.mean.y   tbodygyro.mean.z   tbodygyro.std.x  
 Min.   :-0.20578   Min.   :-0.20421   Min.   :-0.07245   Min.   :-0.9943  
 1st Qu.:-0.04712   1st Qu.:-0.08955   1st Qu.: 0.07475   1st Qu.:-0.9735  
 Median :-0.02871   Median :-0.07318   Median : 0.08512   Median :-0.7890  
 Mean   :-0.03244   Mean   :-0.07426   Mean   : 0.08744   Mean   :-0.6916  
 3rd Qu.:-0.01676   3rd Qu.:-0.06113   3rd Qu.: 0.10177   3rd Qu.:-0.4414  
 Max.   : 0.19270   Max.   : 0.02747   Max.   : 0.17910   Max.   : 0.2677  
 tbodygyro.std.y   tbodygyro.std.z   tbodygyrojerk.mean.x tbodygyrojerk.mean.y
 Min.   :-0.9942   Min.   :-0.9855   Min.   :-0.15721     Min.   :-0.07681    
 1st Qu.:-0.9629   1st Qu.:-0.9609   1st Qu.:-0.10322     1st Qu.:-0.04552    
 Median :-0.8017   Median :-0.8010   Median :-0.09868     Median :-0.04112    
 Mean   :-0.6533   Mean   :-0.6164   Mean   :-0.09606     Mean   :-0.04269    
 3rd Qu.:-0.4196   3rd Qu.:-0.3106   3rd Qu.:-0.09110     3rd Qu.:-0.03842    
 Max.   : 0.4765   Max.   : 0.5649   Max.   :-0.02209     Max.   :-0.01320    
 tbodygyrojerk.mean.z tbodygyrojerk.std.x tbodygyrojerk.std.y tbodygyrojerk.std.z
 Min.   :-0.092500    Min.   :-0.9965     Min.   :-0.9971     Min.   :-0.9954    
 1st Qu.:-0.061725    1st Qu.:-0.9800     1st Qu.:-0.9832     1st Qu.:-0.9848    
 Median :-0.053430    Median :-0.8396     Median :-0.8942     Median :-0.8610    
 Mean   :-0.054802    Mean   :-0.7036     Mean   :-0.7636     Mean   :-0.7096    
 3rd Qu.:-0.048985    3rd Qu.:-0.4629     3rd Qu.:-0.5861     3rd Qu.:-0.4741    
 Max.   :-0.006941    Max.   : 0.1791     Max.   : 0.2959     Max.   : 0.1932    
 tbodyaccmag.mean  tbodyaccmag.std   tgravityaccmag.mean tgravityaccmag.std
 Min.   :-0.9865   Min.   :-0.9865   Min.   :-0.9865     Min.   :-0.9865   
 1st Qu.:-0.9573   1st Qu.:-0.9430   1st Qu.:-0.9573     1st Qu.:-0.9430   
 Median :-0.4829   Median :-0.6074   Median :-0.4829     Median :-0.6074   
 Mean   :-0.4973   Mean   :-0.5439   Mean   :-0.4973     Mean   :-0.5439   
 3rd Qu.:-0.0919   3rd Qu.:-0.2090   3rd Qu.:-0.0919     3rd Qu.:-0.2090   
 Max.   : 0.6446   Max.   : 0.4284   Max.   : 0.6446     Max.   : 0.4284   
 tbodyaccjerkmag.mean tbodyaccjerkmag.std tbodygyromag.mean tbodygyromag.std 
 Min.   :-0.9928      Min.   :-0.9946     Min.   :-0.9807   Min.   :-0.9814  
 1st Qu.:-0.9807      1st Qu.:-0.9765     1st Qu.:-0.9461   1st Qu.:-0.9476  
 Median :-0.8168      Median :-0.8014     Median :-0.6551   Median :-0.7420  
 Mean   :-0.6079      Mean   :-0.5842     Mean   :-0.5652   Mean   :-0.6304  
 3rd Qu.:-0.2456      3rd Qu.:-0.2173     3rd Qu.:-0.2159   3rd Qu.:-0.3602  
 Max.   : 0.4345      Max.   : 0.4506     Max.   : 0.4180   Max.   : 0.3000  
 tbodygyrojerkmag.mean tbodygyrojerkmag.std fbodyacc.mean.x   fbodyacc.mean.y   
 Min.   :-0.99732      Min.   :-0.9977      Min.   :-0.9952   Min.   :-0.98903  
 1st Qu.:-0.98515      1st Qu.:-0.9805      1st Qu.:-0.9787   1st Qu.:-0.95361  
 Median :-0.86479      Median :-0.8809      Median :-0.7691   Median :-0.59498  
 Mean   :-0.73637      Mean   :-0.7550      Mean   :-0.5758   Mean   :-0.48873  
 3rd Qu.:-0.51186      3rd Qu.:-0.5767      3rd Qu.:-0.2174   3rd Qu.:-0.06341  
 Max.   : 0.08758      Max.   : 0.2502      Max.   : 0.5370   Max.   : 0.52419  
 fbodyacc.mean.z   fbodyacc.std.x    fbodyacc.std.y     fbodyacc.std.z   
 Min.   :-0.9895   Min.   :-0.9966   Min.   :-0.99068   Min.   :-0.9872  
 1st Qu.:-0.9619   1st Qu.:-0.9820   1st Qu.:-0.94042   1st Qu.:-0.9459  
 Median :-0.7236   Median :-0.7470   Median :-0.51338   Median :-0.6441  
 Mean   :-0.6297   Mean   :-0.5522   Mean   :-0.48148   Mean   :-0.5824  
 3rd Qu.:-0.3183   3rd Qu.:-0.1966   3rd Qu.:-0.07913   3rd Qu.:-0.2655  
 Max.   : 0.2807   Max.   : 0.6585   Max.   : 0.56019   Max.   : 0.6871  
 fbodyaccjerk.mean.x fbodyaccjerk.mean.y fbodyaccjerk.mean.z fbodyaccjerk.std.x
 Min.   :-0.9946     Min.   :-0.9894     Min.   :-0.9920     Min.   :-0.9951   
 1st Qu.:-0.9828     1st Qu.:-0.9725     1st Qu.:-0.9796     1st Qu.:-0.9847   
 Median :-0.8126     Median :-0.7817     Median :-0.8707     Median :-0.8254   
 Mean   :-0.6139     Mean   :-0.5882     Mean   :-0.7144     Mean   :-0.6121   
 3rd Qu.:-0.2820     3rd Qu.:-0.1963     3rd Qu.:-0.4697     3rd Qu.:-0.2475   
 Max.   : 0.4743     Max.   : 0.2767     Max.   : 0.1578     Max.   : 0.4768   
 fbodyaccjerk.std.y fbodyaccjerk.std.z  fbodygyro.mean.x  fbodygyro.mean.y 
 Min.   :-0.9905    Min.   :-0.993108   Min.   :-0.9931   Min.   :-0.9940  
 1st Qu.:-0.9737    1st Qu.:-0.983747   1st Qu.:-0.9697   1st Qu.:-0.9700  
 Median :-0.7852    Median :-0.895121   Median :-0.7300   Median :-0.8141  
 Mean   :-0.5707    Mean   :-0.756489   Mean   :-0.6367   Mean   :-0.6767  
 3rd Qu.:-0.1685    3rd Qu.:-0.543787   3rd Qu.:-0.3387   3rd Qu.:-0.4458  
 Max.   : 0.3498    Max.   :-0.006236   Max.   : 0.4750   Max.   : 0.3288  
 fbodygyro.mean.z  fbodygyro.std.x   fbodygyro.std.y   fbodygyro.std.z  
 Min.   :-0.9860   Min.   :-0.9947   Min.   :-0.9944   Min.   :-0.9867  
 1st Qu.:-0.9624   1st Qu.:-0.9750   1st Qu.:-0.9602   1st Qu.:-0.9643  
 Median :-0.7909   Median :-0.8086   Median :-0.7964   Median :-0.8224  
 Mean   :-0.6044   Mean   :-0.7110   Mean   :-0.6454   Mean   :-0.6577  
 3rd Qu.:-0.2635   3rd Qu.:-0.4813   3rd Qu.:-0.4154   3rd Qu.:-0.3916  
 Max.   : 0.4924   Max.   : 0.1966   Max.   : 0.6462   Max.   : 0.5225  
 fbodyaccmag.mean  fbodyaccmag.std   fbodybodyaccjerkmag.mean fbodybodyaccjerkmag.std
 Min.   :-0.9868   Min.   :-0.9876   Min.   :-0.9940          Min.   :-0.9944        
 1st Qu.:-0.9560   1st Qu.:-0.9452   1st Qu.:-0.9770          1st Qu.:-0.9752        
 Median :-0.6703   Median :-0.6513   Median :-0.7940          Median :-0.8126        
 Mean   :-0.5365   Mean   :-0.6210   Mean   :-0.5756          Mean   :-0.5992        
 3rd Qu.:-0.1622   3rd Qu.:-0.3654   3rd Qu.:-0.1872          3rd Qu.:-0.2668        
 Max.   : 0.5866   Max.   : 0.1787   Max.   : 0.5384          Max.   : 0.3163        
 fbodybodygyromag.mean fbodybodygyromag.std fbodybodygyrojerkmag.mean
 Min.   :-0.9865       Min.   :-0.9815      Min.   :-0.9976          
 1st Qu.:-0.9616       1st Qu.:-0.9488      1st Qu.:-0.9813          
 Median :-0.7657       Median :-0.7727      Median :-0.8779          
 Mean   :-0.6671       Mean   :-0.6723      Mean   :-0.7564          
 3rd Qu.:-0.4087       3rd Qu.:-0.4277      3rd Qu.:-0.5831          
 Max.   : 0.2040       Max.   : 0.2367      Max.   : 0.1466          
 fbodybodygyrojerkmag.std
 Min.   :-0.9976         
 1st Qu.:-0.9802         
 Median :-0.8941         
 Mean   :-0.7715         
 3rd Qu.:-0.6081         
 Max.   : 0.2878
 ```
