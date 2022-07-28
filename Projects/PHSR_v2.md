# PHSR_v2

TODO:
[] Update coding comparison to account for the new formatting
[] Include code to get alignment time "iPhone reads ???" for affect alignment
[] Incorporate RR-interval preprocessing
	- Add check for significant breaks in time stamps for data
	- 
[] Incorporate ECG preprocessing
	- Check for discrepancies between the iPhone timestamps and the polar strap timestamps
	- Add check for significant breaks in time stamps for data
	- Replace recordings with NaNs when obvious errors/discrete shift is detected
[] Align ECG signal to the RR-interval data
	- This should be done post-processing, as to minimize the issues with alignment
[] Go through collected recordings to get "approved" versions of data
	- Also have "corrected" files which cut out the discrete shifts
[X] Expand documentation on PSHR `README.md` for a better tutorial
	- Do I include snippets into what each function does?

[] Change functions to work with `inputParser` in order to have default values for different variables.


# Coding

#### Useful Links
https://learn.adafruit.com/build-a-bluetooth-app-using-swift-5?view=all

https://github.com/pareeknikhil/biofeedback/blob/master/Polar%20Device%20Data%20Stream/ECG/main.py

https://towardsdatascience.com/creating-a-data-stream-with-polar-device-a5c93c9ccc59

#### Things about writing bytearrays to the ecg characteristic
https://stackoverflow.com/questions/69977624/how-do-i-find-out-which-uuid-i-should-use-to-request-data-from-my-polar-h10-sens
https://stackoverflow.com/questions/35480804/corebluetooth-write-data-with-byte-array
https://learn.adafruit.com/build-a-bluetooth-app-using-swift-5/communication

#### Learning Swift:
[[Stanford University SwiftUI]]


#### Project Train of thought:
- So, thanks to the polarstrap github page with all of the information that was needed, things are actually working now. However, I need to check further


# ECG
### Notes from *ECG Signal Processing, Classification and Interpretation*:
- 1.8) "The normal duration of the QRS complex does not exceed 0.12 seconds. The voltage usually varies between 1.5 and 2.0 mV"
- 



# RR-Interval
