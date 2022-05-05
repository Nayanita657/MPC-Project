
# MPC Final Project
Nayanita Saha M21CS010 
Deepti Gupta M21CS005
Instructor: Dr. Suchetana Chakraborty (Assistant Professor, Department of Computer Science & Engineering @ Indian Institute of Technology, Jodhpur)




## Health Kit

Introducing an Android Application which will help us in measuring HeartRate , Respiration Rate, Blood Pressure and Oxygen Level using the camera of the phone.

This application uses the PPG signal obtained from the mobile camera solely by applying an image processing method to each frame to obtain the RGB intensities, each of which contains the PPG signal that will be processed to estimate the four vital signs.

The main goal of this project was to achieve good accuracy from the mobile camera when compared to commercial devices.

We used a sqlite local database for user privacy because critical information about the user, such as age, weight, height, and gender, must be entered to calculate blood pressure.



## Working Flow of this Application

The videos were captured at a sampling rate of 29.97 frames per second and an image pixel density of 1280 x 720 and the recording will be processed frame by frame to get the intensities of RBG colors on each frame.




## Heart Rate Measurement

Red and green intensities will be stored in an array that will be subjected to a Fast Fourier Transform; the highest peak on the resultant array, after ignoring the noise that will be present in the first few stored data, will contain the frequency of the heart rate on 1 second, and the heart beat will be estimated. (Fft)

## Respiration Rate Measurement

The Respiration rate is calculated in the same way as the Heart Rate, with the exception that a bandpass filter with a frequency range of 0.1Hz to 0.4Hz and a centre frequency of 0.2Hz must be applied to obtain the Respiration rate. (Fft2)

## Blood Pressure Measurement

Following the estimation of the heart rate, blood pressure can be calculated using some equations that will be mentioned in the references.
## Oxygen Saturation Measurement

The PPG signal must be converted into ac and dc signals for calculating the oxygen saturation. The Dc signal represents the average of the Red and Blue intensities across time, whereas the Ac signal is the Standard Deviation .


## How to run this application

1. Initial registration is done for the new user.

2. Once the user is registered User is redirected in the main page of the application.

3. Select Heart Rate and place the finger at the back of the Camera. The measurement will be shown for the Heart Rate.

4. Select Respiration Rate and place the finger at the back of the Camera. The measurement will be shown for the Respiration rRate.
 
5. Select Blood Pressure and place the finger at the back of the Camera. The measurement will be shown for the Blood Pressure. 

6. Select Oxygen saturation and place the finger at the back of the Camera. The measurement will be shown for the Oxygen Saturation.

7. Select Vital signs which will display the calculated the four values in a single display. 


## References

[1] Nastaran Hesam Shariati, Edmond Zahedi, “Comparison of selected parametric models for analysis of the photoplethysmographic signal”, 1st Conference on Computers, Communications, and Signal Processing, IEEE Malaysia Section, Kuala Lumpur, Malaysia, Nov. 2005, CDROM. 

[2] C.G. Scully, J. S. Lee, J. Meyer, A.M. Gorbach, D. GranquistFraser, Y. Mendelson, and K.H. Chon, “Physiological Parameter Monitoring from Optical Recordings With a Mobile Phone”, IEEE Transactions., Biomedical Engineering, vol. 59, no. 2, p.303-306, 2012

[3] E. Jonathan and L. Martin, “Investigating a smartphone imaging unit for photoplethysmography,” Physiological Meas., vol. 31, no. 11, p. N79, 2010.

[4] P. Pelegris, K. Banitsas, T. Orbach, and K. Marias, "A novel method to detect Heart Beat Rate using a mobile phone," Conf Proc IEEE Eng Eng Med Biol Soc, pp. 5488-5491, 2010.

[5] Mayur Lunawat, Aquibjaved Momin, Varun Nirantar, Abhishek Deshmukh “Heart Pulse Monitoring: The Smart Phone Way” International Journal of Engineering Research and Applications (IJERA) ISSN: 2248-9622 www.ijera.com Vol. 2, Issue 5, September- October 2012, pp.509-515 509 | P

[6] D. Laure “Heart Rate Measuring Using Mobile Phone’s Camera” Proceeding of the 12th conference of Open Innovations Association FRUCT and Seminar on e-Travel, 2012 

