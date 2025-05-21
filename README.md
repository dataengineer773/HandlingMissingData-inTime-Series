We have missing values in time series data, In addition to the missing data strategies previously discussed, when we have time series data we can
use interpolation to fill in gaps caused by missing values, Alternatively, we can replace missing values with the last known value (i.e., forward-filling), We can also replace missing values with the latest known value (i.e., back-filling)
Interpolation is a technique for filling in gaps caused by missing values by, in effect, drawing a line or
curve between the known values bordering the gap and using that line or curve to predict reasonable
values. Interpolation can be particularly useful when the time intervals between are constant, the data is
not prone to noisy fluctuations, and the gaps caused by missing values are small. For example, in our
solution a gap of two missing values was bordered by 2.0 and 5.0. By fitting a line starting at 2.0 and
ending at 5.0, we can make reasonable guesses for the two missing values in between of 3.0 and 4.0.
If we believe the line between the two known points is nonlinear, we can use interpolate’s method to
specify the interpolation method, Finally, there might be cases when we have large gaps of missing values and do not want to interpolate
values across the entire gap. In these cases we can use limit to restrict the number of interpolated
values and limit_direction to set whether to interpolate values forward from at the last known value
before the gap or vice versa, Back-filling and forward-filling can be thought of as a form of naive interpolation, where we draw a flat
line from a known value and use it to fill in missing values. One (minor) advantage back- and forwardfilling have over interpolation is the lack of the need for known values on both sides of missing
value(s).
