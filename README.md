# LMS
Code implementing a simple Least Mean Squares adaptive filter

If we have two random processes x(n) and d(n), we can make some inference about d(n) if we know the statistics of the two processes.  In particular, we could design a [Wiener filter](https://en.wikipedia.org/wiki/Wiener_filter) if we knew the cross correlation between x and d.

In practice however these statistics are usually not known, and are time varying.  Another option is to use an adaptive filter.  The Least Mean Squares (LMS) filter [see here](https://en.wikipedia.org/wiki/Least_mean_squares_filter) is one of the simplest possible adaptive filters.

Example uses include tracking a time varying process, system identification, and channel identification.  These examples are given in test.py

Here is an example of using the LMS filter to track a brownian motion process.

![alt tag](https://raw.githubusercontent.com/RJTK/LMS/master/tracking.png)

Obviously, the filter can perform much better if the processes are Jointly WSS, or approximately so.