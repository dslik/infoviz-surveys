# Overview

Waterfall visualizations (more generally known as spectrograms) represent three dimensions of information as an image on a 2D plane, where one of the dimensions is time.

Axis are typically:

* x axis: time or frequency
* y axis: frequency or time
* z axis: signal intensity as grayscale or a colour spectrum

The x and y axis can be panned to move backwards and forward in time and in frequency space. Often the edge of the display is set to the current time, with the data scrolling to the side or down over time, resulting in the characteristic resemblance to a waterfall.

Zooming in or out allows a larger or smaller region of time and frequency to be displayed. Alternatively, the visible area

Different communities have different conventions regarding which axis should be used for which variable. For example, radio astronomy tends to put time on the x axis, while radio engineering tends to put frequency on the x axis, so that a traditional spectrum analyzer display can be shown above or below the waterfall display.

Adjusting the range of values displayed in the z axis, or changing the mapping between input values and displayed colours allow for certain features to be emphasized.

# Examples

## Example 1 - Baseline

The below waterfall display is from the [SatNOGS - Satellite Network Open Ground Station](https://satnogs.org) project. It displays frequency on the x axis, time on the y axis, and signal intensity in dB as a colour gradient.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/9248596a-87f1-40db-9ed1-54f1c17803f5)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed on the side.

### Commentary

This is a clean and basic waterfall display. The selection of display colours allows both the noise level and the received signal to be clearly seen. Selection of colour gradients is a challenging process, and has extensive research for elevation maps. See [Good Colour Maps: How to Design Them. arXiv:1509.03700 [cs.GR] 2015](https://peterkovesi.com/projects/colourmaps/) for an introduction.

The lack of grid lines makes it difficult to easily identify what time or frequency a given feature is associated with. Finding a good colour for grid lines requires coordination with the colour choice for displaying intensity.

This waterfall display will act as a baseline for further discussion.

## Example 2 - Legend in watefall region

The below waterfall display is a screenshot from the [SDR Data File Analyzer](https://www.sdr-radio.com/analyser) software. It displays frequency on the x axis, time on the y axis, and signal intensity in dBm as a grey scale gradient.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/f2e19d96-eeb2-4ee0-86a7-e3001e46d0ef)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed inside the waterfall display region.

### Commentary

Displaying information inside the waterfall display area obscures usable display area. I prefer this information being displayed outside the display region.

## Example 3 - Time on x axis

The below waterfall display is from [DF2MZ](http://df2mz.de/), who has custom software to generate waterfalls. It displays time on the x axis, frequency on the y axis, and signal intensity in dB as a colour gradient. A small legend is included in the lower left.

An instantaneous frequency-intensity chart aligned with the waterfall is included on the far right, corresponding to the "now" position in the waterfall display.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/16e7a8ea-c610-4438-9b65-952c1e8f5142)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed inside the waterfall display region.

### Commentary

The small intensity legend obscures far less information than in example 2, but I still prefer this to be placed outside of the waterfall display region.

Displaying the time grid lines using dashes, with the time values inside the waterfall display region is easily to read and saves space, especially with longer date-time strings. This works best when the size of the waterfall display region is large.

As contentious as the axis debate is, and as strange as it is to see the frequency chart turned on its side, I prefer this axis arrangement, as it allows the waterfall display to be be aligned with other time series, as seen here.

## Example 4 - Chart above waterfall region

The below waterfall display is from an unknown source. It displays time on the x axis, frequency on the y axis, and signal intensity in dB as a colour gradient. A correlated chart showing noise amplitude is shown above the waterfall display.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/e28e306b-7846-408b-af2c-bae991d7998c)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed to the right of the waterfall display region.

### Commentary

The creators of this waterfall missed an opportunity to align the noise amplitude chart with the waterfall display. Likewise, the indicators of conditions (weekend, lockdown, etc) could have been shown as a series of strip charts. This highlights important use cases for correlated data display.

## Example 5 - Instantaneous frequencies above waterfall region

The below waterfall display is a screenshot from the [SDR Console](https://www.sdr-radio.com/console) software, version 3. It displays frequency on the x axis, time on the y axis, and signal intensity (with no units displayed) as a colour gradient, with the upper and lower bounds mapped to the ends of the colour gradient being adjustable.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/c31edb0e-a9db-4a5b-bb6b-8a41a72b5c86)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed outside the waterfall display region on the far right.

### Commentary

This shows the more traditional instantaneous frequency intensity on top arrangement. It is also a good example of a "frequency region of interest" selection, shown in green highlighting on the far upper right. Having the region of interest being highlighted down the entire waterfall would be better, as it allows the entire region of interest to be easily visually identified.

A second region is shown overlayed on the x axis (frequency) at the bottom of the screen, which indicates which region is being recorded.

## Example 6 - Stacked waterfall displays

The below waterfall display is from an unknown source, and shows the frequency stability of the NIST WWV carrier over time, which can be used to measure various atmospheric conditions. It displays time on the x axis, frequency on the y axis, and signal intensity (with no units displayed) as a colour gradient.

What is unique about this waterfall is that multiple waterfalls, one for each day, are stacked. This permits easy identification of patterns that occur during the same or similar times each day.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/515dfa6c-4711-46dd-946e-dd331bc8f4bd)

Axis labels for time and frequency, as well as day, are indicated on the outside of the waterfall display region. No intensity legend is provided.

### Commentary

While this is another example of the versatility of having time on the x axis, it is a bit of an unusual case, as the stacked waterfall displays effectively have time on both the x axis and the y axis.

The below rotated version gives a rough feeling of how this would look if time was on the y axis:

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/efb295a2-187a-4c7a-be80-25e0a9dc1f7c)

As the number of days grows, it is easier to scroll down vs. sideways, so that is a plus for the first variant.

## Example 7 - Title block

The below waterfall display is a from a report by AJ4CO on [Cassiopeia A Scintillation](https://www.aj4co.org/Publications/Cassiopeia%20A%20Scintillation%20Observed%20by%20Radio%20Jove%20Participants,%20Typinski%20et%20al%20(SARAJ,%202014).pdf). It displays frequency on the y axis, time on the x axis, and signal intensity (with no units displayed) as a colour gradient.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/217c2237-750e-4846-a201-50f5e29572cb)

Axis labels for time and frequency, as well as the day in a header block, are indicated on the outside of the waterfall display region. No intensity legend is provided.

### Commentary

The importance of a title block that provides clear attribution and the ability to determine the source as part of the image is very important. A summary of key configurations used to capture the data is also helpful for interpretation.

## Example 8 - Labels

The below waterfall display is a from a second report by AJ4CO on [Sweepers](https://www.aj4co.org/Publications/Sweepers,%20Typinski%20(SARAJ,%202010).pdf). It displays time on the y axis, frequency on the x axis, and signal intensity (with no units displayed) as a colour gradient.

Two signals of interest are annotated using labels.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/3314cd30-689a-43dd-a463-3c13a0c9e7af)

Axis labels for time and frequency are indicated on the outside of the waterfall display region with arrow pointers. No intensity legend is provided.

### Commentary

The concept of labels allows well-identified features to be identified and annotated, with the risk of obscuring other waterfall data. This works well for linear or point structures.

## Example 9 - Regions of Importance

The below annotated waterfall display is a from a blog post by windytan showing a [dialup V.8 bis trasnaction](https://www.windytan.com/2012/11/the-sound-of-dialup-pictured.html). It displays frequency on the y axis, time on the x axis, and signal intensity (with no units displayed) as a colour gradient.

Annotations are shown as rectangular regions of interests, with callout lines to more information, resulting in a very professional and informative presentation..

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/61bdf175-f431-4153-98c4-e8d76b3de228)

Axis labels for time and frequency, as well as day, are indicated on the outside of the waterfall display region. No intensity legend is provided.

### Commentary

Adding the concept of Regions of Importance (ROI), along with a standard visual way of indicating, numbering and associating them with additional information, is very powerful and useful. This works well for any region in time and frequency.

The indication of transaction phases can be generalized into strip charts, with different colours indicating different transaction phases.

## Example 10 - Histogram in intensity legend

The below waterfall display is a from an unknown source (screenshot from [AARONIA RTSA](https://aaronia.com/en/products/software/rtsa-software). It displays time on the y axis, frequency on the x axis, and signal intensity in dBm as a colour gradient to the right.

The signal intensity legend includes a histogram of how many points on the waterfall are binned into each intensity bucket, as well as allowing adjustment of the mapping of values to colours in the gradient by adjusting the ends and shape of a curve (a common feature in graphics software like Photoshop).

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/9486665c-a050-420c-b773-5a8bf39e69e2)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed on the side.

### Commentary

Histograms (and PDFs) are underutilized in conjunction with waterfall displays. While AARONIA only does this for intensity, one option worth considering is to display a power histogram and PDF for both the X and Y axis.

## Example 11 - Wrapped waterfalls

The below waterfall display is a screenshot from [AARONIA RTSA]([https://aaronia.com/en/products/software/rtsa-software](https://aaronia.com/media/wysiwyg/RTSA_Suite/12_hr_spectrum_view_full.jpg)). It displays time on the y axis, frequency on the x axis, and signal intensity in dBm as a colour gradient to the right.

This displays multiple waterfalls on the same screen to fit a larger span on the screen at the same time, at the expensive of resolution.

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/8fdf6ce9-2aea-47fe-9064-88c0243279e9)

Axis labels for all three dimensions are provided, two aligned with the waterfall display, with intensity displayed on the side.

### Commentary

AARONIA claims that stacking waterfall displays is "patented", but I couldn't this taught in their public patent filings (WO/2017/121634, US10914771B2, WO/2022/106330, DE102020007046B3).

The basic concept of stacking waterfall displays has significant prior art:

1, Stacking a spectrum goes back to echelle spectrometer, originally developed in the 1890's:

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/08017f94-1c7c-49d7-9d83-470dddae78ec)

Source: https://rsaa.anu.edu.au/observatories/instruments/echelle-spectrograph

2. FlexRadio has been displaying multiple "slices" of a frequency range, allowing a waterfall to be wrapped this way since the mid 2000's:

![image](https://github.com/dslik/infoviz-surveys/assets/5757591/4100d8c2-5fb8-4c3d-89ad-7fc2e632c13d)

Source: https://k9xn.org/2014/08/28/flex-radio-systems-flex-6500/

# Conclusions

1. Waterfall displays should be provided as a self-contained image. Specifically, they should contain the following:
  - A solid region showing the waterfall data
  - The time axis, preferably in UTC, along either the X or Y axis, with days indicated as part of the timestamps, or in a header
  - The frequency axis, with units.
  - An intensity scale, with units
  - A title block, indicating the source, the time period for the waterfall, and key information about the captured data.
2. The waterfall display region should have a clear border.
3. I have a preference towards time on the x axis.
4. Use perceptually uniform colour maps, preferably CET-L20
5. Grid lines can help, but can also obscure/distort apparant data. Use with care.
6. Waterfall displays should be combined with other chart types (heat charts, strip charts, flags, etc) as part of a unified visual grammer.
7. Display of regions of importance should be standardized.
