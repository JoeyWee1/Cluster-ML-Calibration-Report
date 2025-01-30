# Cluster-ML-Calibration-Report
THE four Cluster spacecraft in Earth orbit each carry a
three-axis fluxgate magnetometer (FGM). Each axis has
a zero error (offset) which must be calibrated. The spacecraft
rotate about their X axes at 0.25 Hz, causing the spinning
Y and Z axes to exhibit signals at the rotation frequency if
the offset is not calibrated. These offsets are calibrated by
minimising the signal at the rotation frequency. [1] However,
as the X axis is non-rotating, it cannot be calibrated in this
manner. Instead, these offsets must be determined when the
spacecraft enters the solar wind for a few months each year.
Offsets in between these periods must be interpolated.

The Cluster satellites also collect telemetry about themselves.
By determining which underlying variables affect the
offset and how, the offsets could be derived from telemetry.
Since human input is presently required for the offset calculations,
this could simplify the FGM instrument calibration.
Relating the offsets to the telemetry would also allow for
better methods of estimating the X axis offsets than by linear
interpolation.

Because which variables influence the offset and how are
unknown, it is not possible to simply fit a function to this
data. However, with over 3000 orbits of data per satellite
since August 2000, the volume of labelled data might make it
suitable to use a supervised machine learning approach to find
trends in the offset-telemetry data. To test the applicability of
using these techniques for predicting the offsets, four types of
ML models will be trained and tested on the data: K-nearest
neighbours (KNN), support vector regression (SVR), feedforward
neural network (FNN), and long short term memory
(LSTM) models.
