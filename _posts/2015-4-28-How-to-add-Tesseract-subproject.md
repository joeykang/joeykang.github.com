---
layout: post
title: How to import Tesseract API as sub project of the existing project
---
#### 1. Drag Tesseract OCR iOS.xcodeproj into the existing project,

#### 2. [Targets - Build Phases - Target Dependencies]
Add TesseratOCR

#### 3. [Targets - Build Phases - Link Binary With Libraries]
Add TesseratOCR.framework, CoreImage.framework, libstdc++.6.0.9.dylib

#### 4. [Targets - Build Setttings - Other Linker Flags]
Add link flag - ‘-ObjC’ and ‘-lstdc++’

#### 5. Add ‘tessdata’(training data file) to the exist project as folder reference.
