# OSCP Stroke Classifier
The OSCP Stroke Classifier is a web-based tool designed to assist healthcare professionals in classifying strokes based on patient data. This tool utilizes a user-friendly interface to input patient information and provides classification results to aid in diagnosis and treatment planning.

## Items
* Item 3: Visual field defect
* Item 4: Facial palsy (L / R / Both / None)
* Item 5: Arm motor function (L / R / Both / None)
* Item 6: Leg motor function (L / R / Both / None)
* Item 7: Ataxia (L / R / Both / None)
* Item 8: Sensory Loss
* Item 9: Aphasia
* Item 10: Dysarthria (important condition: item 10: dysarthria is ignored if item 4 or item 9 is present!)
* Item 11: Neglect

## Classification Categories
The classification is in a two-step process:
1. **First Step**: Highlights major stroke categories:
    - A. At least 2 of items 4, 5, 6 on the same side (L or R) AND/OR Item 8 (Item 8 condition: Ipsilateral sensory loss on at least two of the following: face, arm, leg (L / R / Both)
    - B. Item 3
    - C. Item 11 AND/OR item 9
    - D. Item 7 AND/OR item 10

2. **Second Step**: Further classifies into the classes:
    - TACI. A + B + C (not D)
    - PACI. two of A, B or C (not D) OR C alone OR exactly one of items 4, 5, 6, 8 (Item 8 condition: sensory loss restricted to only one of the following areas: face, arm or leg (L / R / Both)
    - LACI. A (not B, C, D) OR A + item 7 (on same side as A) (not B, C or item 10) OR item 10 + item 5 (exclusively no other items)
    - POCI. D OR B (not A or C)