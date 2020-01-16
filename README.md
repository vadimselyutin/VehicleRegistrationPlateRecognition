# VehicleRegistrationPlateRecognition
## Skoltech "Intro to Computer Vision" course final project
### CV pipeline
The goal of this project is to recognize symbols on a registration plate. 3 main steps could be highlighted:
- plate frame recognition,
- plate symbols detection,
- specific symbols (numbers and letters) recognition.

For the first step we've applied two approaches:
- find the biggest contour,
- find 4-corners closed contour.

To detect a frame and its symbols we use Canny edge detector on the normalized image, detect biggest contours and find their rectangular boundary. Finally, recognition of specific symbol is done via 3 methods:
- correlation comparison of symbol and template,
- HOG feature description and applying Linear Support Vector Classifier classifier,
- by applying Pytesseract to the normalized plate frame.
