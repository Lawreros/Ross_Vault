# PHSR_v2

TODO:
- [ ] RR-interval preprocessing:
	- [ ] Investigate variance in transmission of data packets and the catch-up quick transmission. Specifically how to adjust the RR-intervals closer to "true time"
- [ ] ECG preprocessing:
	- [ ] Find list of simple preprocessing techniques
	- [ ] Replace recordings with NaNs when obvious errors/discrete shift is detected
	- [ ] Check for discrepancies between the iPhone timestamps and the polar strap timestamps
- [ ] Align ECG signal to RR-interval data
	- [ ] Add check for significant differences between sets of time stamps
	- [ ] Find good set of metrics for quantifying alignment
- [ ] Train/Test split class
	- [ ] write function out as class for future testing with other predictive models
- [ ] Affect analysis:
	- [ ] Add support for keeping unique affect labels (i.e. not just `problematic` vs `non-problematic`)
	- [ ] Add ability for multiple columns of affect flags

- [ ] Documentation:
	- [ ] Downloading and use of Xcode
	- [ ] Submission of new version of the iPhone app to the Apple Store for use with Testflight
	- [ ] PSHR_pipeline `README.md`

- [ ] iPhone:
	- [ ] Add check to the app which restarts ECG capture whenever it switches off while HR is still being collected (except by button press)
	- [x] Add sound effects for the disconnection of RR-interval collection
	- [x] Add sound effects for the disconnection of ECG collection
	- [x] Have sounds repeated for an extended amount of time

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


# RR-Interval
