# Lost-and-Found-via-Yolov5
This is my preliminary video analysis. This code has a low recognition rate in multi-person scenarios and needs to be improved.

# Frame Extraction
In fact, video surveillance is more used to detect remnants in real scenes, and video streaming is based on pictures, so we need to design a detection algorithm for detecting remnants in pictures first.
At this time, because we detect a static image, the # YOLOv5 algorithm # is the most commonly used and effective in the field of target detection.
For static pictures, the standard for distinguishing remains and non-remains is to determine whether the distance between the identified person and the box corresponding to the object is maintained within a threshold value.

# Target Detection - distance threshold
If the distance between boxes is not maintained within a threshold value, it will be identified as non-left objects. If the distance between boxes is maintained within a threshold value, it will be identified as left objects. The discriminant process of its model is shown as follows.

# Target Detection - time threshold
If the distance is greater than the threshold value and remains in this state for a period of time(also can be seen as the number of frames), it can be considered that people and objects are separated and can be identified as left behind. That's the judgment condition.

# Areas for improvement
Multi-person scene recognition has not been realized, but if you want to achieve this, the basic idea should be the same, just need to put the central coordinates of each person in each frame picture into the list, and then the central coordinates of the identified dynamic objects and the list of traversal comparison, should be able to identify the missing items.


# References and websites
Here are some references and websites. I respect every author's work and learn a lot from their ideas.

[1] K. Lin, S. -C. Chen, C. -S. Chen, D. -T. Lin and Y. -P. Hung, "Abandoned Object Detection via Temporal Consistency Modeling and Back-Tracing Verification for Visual Surveillance," in IEEE Transactions on Information Forensics and Security, vol. 10, no. 7, pp. 1359-1370, July 2015, doi: 10.1109/TIFS.2015.2408263. 

[2] GitHub(2022)gamblerInCoding[Source code]. https://github.com/gamblerInCoding/LegacyItems/
