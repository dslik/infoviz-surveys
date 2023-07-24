## Waterfall visualizations overview

Waterfall visualizations represent three dimensions of information as an image on a 2D plane, where one of the dimensions is time.

Axis are typically:

* x axis: time or frequency
* y axis: frequency or time
* z axis: signal intensity as grayscale or a colour spectrum

The x and y axis can be panned to move backwards and forward in time and in frequency space. Often the edge of the display is set to the current time, with the data scrolling to the side or down over time, resulting in the characteristic resemblance to a waterfall.

Zooming in or out allows a larger or smaller region of time and frequency to be displayed. Alternatively, the visible area

Different communities have different conventions regarding which axis should be used for which variable. For example, radio astronomy tends to put time on the x axis, while radio engineering tends to put frequency on the x axis, so that a traditional spectrum analyzer display can be shown above or below the waterfall display.

Adjusting the range of values displayed in the z axis, or changing the mapping between input values and displayed colours allow for certain features to be emphasized.

## Example 1

The below waterfall display is from the [SatNOGS - Satellite Network Open Ground Station](https://satnogs.org) project. It displays frequency on the x axis, time on the y axis, and signal intensity in dB as a colour gradient.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/9248596a-87f1-40db-9ed1-54f1c17803f5)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed on the side.

### Commentary

This is a clean and basic waterfall display. The selection of display colours allows both the noise level and the received signal to be clearly seen. Selection of colour gradients is a challenging process, and has extensive research for elevation maps. See [Good Colour Maps: How to Design Them. arXiv:1509.03700 [cs.GR] 2015](https://peterkovesi.com/projects/colourmaps/) for an introduction.

The lack of grid lines makes it difficult to easily identify what time or frequency a given feature is associated with. Finding a good colour for grid lines requires coordination with the colour choice for displaying intensity.

This waterfall display will act as a baseline for further discussion.

## Example 2

The below waterfall display is from the [SDR Data File Analyzer](https://www.sdr-radio.com/analyser). It displays frequency on the x axis, time on the y axis, and signal intensity in dBm as a grey scale gradient.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/f2e19d96-eeb2-4ee0-86a7-e3001e46d0ef)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed inside the waterfall display region.

### Commentary

Displaying information inside the waterfall display area obscures usable display area. I prefer this information being displayed outside the display region.

## Example 3

The below waterfall display is from [DF2MZ](http://df2mz.de/), who has custom software to generate waterfalls. It displays time on the x axis, frequency on the y axis, and signal intensity in dB as a colour gradient. A small legend is included in the lower left.

An instantaneous frequency-intensity chart aligned with the waterfall is included on the far right, corresponding to the "now" position in the waterfall display.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/16e7a8ea-c610-4438-9b65-952c1e8f5142)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed inside the waterfall display region.

### Commentary

The small intensity legend obscures far less information than in example 2, but I still prefer this to be placed outside of the waterfall display region.

Displaying the time grid lines using dashes, with the time values inside the waterfall display region is easily to read and saves space, especially with longer date-time strings. This works best when the size of the waterfall display region is large.
