# Lane detection validation and limitations

This project uses OpenCV for lane detection. Before changing the algorithm, confirm the actual entry point and dependencies in the source code.

## Suggested reproducible evaluation

1. Choose a short, legally usable road video with clearly visible lane markings.
2. Record its resolution, frame rate, lighting, and camera placement.
3. Run the existing pipeline without modifying its thresholds.
4. Inspect representative frames for missed lanes, false detections, and unstable overlays.
5. Repeat with curves, shadows, worn markings, rain, and nighttime footage if supported.
6. Record the exact commit, OpenCV version, and settings used for each run.

## Quality checklist

- [ ] Both left and right markings are detected when visible.
- [ ] No lane line is invented when markings are absent.
- [ ] Overlay positions remain stable across adjacent frames.
- [ ] The program handles missing or unreadable video files gracefully.
- [ ] No private vehicle footage or personal information is committed.

## Known limitations to evaluate

Classical image-processing pipelines may be sensitive to illumination, occlusions, camera angle, faded road paint, and nonstandard road geometry. Any accuracy or real-time claims should be supported by measurements on a documented dataset.

**Safety:** This is an experimental computer-vision project, not a driver-assistance or autonomous-driving system. Do not use its output to control a vehicle.
