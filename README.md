The seismic line VB02 is part of the Valdivia Bank seismic survey in the southern Atlantic Ocean and it originates from the seismic cruise TN373. Valdivia Bank is a section of a larger conglomerate called Walvis ridge which sits outside the eastern shore of Namibia. The motivation of this study is to create seismic sections that can be used for geologic interpretation. In addition, this study is meant to articulate the preprocessing and processing steps for the seismic line VB02 and important findings from those steps. The presentation and the final report show different final PTSM images. After some criticism from the seismic processing presentation, I reprocessed the data and produced the processed SEGY PSTM seen in the report.

The seismic line VB02 is marine seismic data located in the UTM 31° S 3° E WGS 1984 projection system. It contains the FFIDs 1001 to 6945 and there were 96 channels in the streamer. Channel 1 was the closest channel to the source and the tail end of the streamer was channel 96. The group spacing was 6.25 m and the shot spacing was 25 m. This means the CMP spacing was 3.125 m. Each channel recorded for 8 seconds per shot with a sampling rate of 1 ms. There were two 45 in3 airguns that had a distance of 26.5 m behind the vessel. The near offset was 142 m between the source and the first channel, and the streamer length was 593.75 m, giving a far offset of 735.75 m. Lastly, the source and receiver depths were 3m and 4m, respectively

The final processing flow:
1. Load in data as SEGY full revision 1 prestack CMP time gathers
2. Inspect shot, receiver and cdp header values and locations as well as CDP model
3. Inspect for dead or noisy shots or channels
4. Static shift up 50 ms
5. Notch filter at .7 Hz
6. Time-variant band-limited noise suppression for frequencies between 0 and 20 Hz
7. Deghost with source at 3m depth, receivers at 4m depth and water velocity of 1500 m/s
8. Create first and updated velocity models via velocity analysis every 1000th CDP and every 50th CDP (in select areas)
9. Create a debubbling matching filter. Done by using the trace from stacking channel 1 common receiver gather with samples after 360 ms muted as the input wavelet and output
wavelet with samples before 82 ms and after 92 ms muted.
10. Filter the data with the matching filter
11. Amplitude compensation using spherical divergence as a function of time and velocity to
the power of 1 and 0, respectively
12. Water-bottom mute
13. Normal moveout, automatic stretch mute for stretching above 65% and stack
14. Finite difference post-stack migration using migration layer of 20 ms, CDP spacing of 3.125 m, migration spatial filter of 15 points, max dip of 30 ms/trace, and a max of 47659 traces to migrate
15. Notch filter at .7 Hz
16. Linear frequency domain signal enhancement using spatial and time windows of 100 traces and 100 ms. Low and high frequency limits were 0 Hz and 500 Hz.
