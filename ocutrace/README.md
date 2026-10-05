# OcuTrace

OcuTrace turns a phone video of the eyes into a nystagmus and saccade recording. It is a research prototype, not a medical device, and not for diagnosis.

Live page: https://mark-esparza.github.io/ocutrace/

## How it works

1. Record a clip with the phone camera or choose one you already have. The video is processed in the browser and never uploaded.
2. Tap the center of one iris, then a fixed point on the face (a small sticker on the nose bridge works best) so head movement cancels out.
3. Track the clip. OcuTrace charts horizontal and vertical eye position, marks fast events, and reports slow phase velocity, beat frequency, square wave jerks and tracking quality. The trace exports as CSV.

A Stimulus tab runs fixation, gaze holding, saccade, smooth pursuit and optokinetic tasks on a second screen, and a Guide tab explains how to record a clip that tracks well.

## Limits

* Degrees are estimated from iris size (11.7 mm iris, 12 mm eye radius) and are not calibrated against a lab tracker.
* Below about 240 fps, peak saccade speeds read low and brief saccades can be missed.
* Torsional nystagmus is not measured.
* Validated so far only on synthetic clips with known nystagmus, not on patients.

The whole tool is this one `index.html` file with no external dependencies.
