
# Enhancing Wearable Tap Water Audio Detection through Subclass Annotation in the HD-Epic Dataset

## Abstract
Wearable human activity recognition has been shown to benefit from the inclusion of acoustic data, as the sounds around a person often contain valuable context. However, due to privacy concerns, it is usually not ethically feasible to record and save microphone data from the device, since the audio could, for instance, also contain private conversations. Rather, the data should be processed locally, which in turn requires processing power and consumes energy on the wearable device. One special use case of contextual information that can be utilized to augment special tasks in human activity recognition is water flow detection, which can, e.g., be used to aid wearable hand washing detection. We created a new label called tap water for the recently released HD-Epic data set, creating 717 hand-labeled annotations of tap water flow, based on existing annotations of the water class. We analyzed the relation of tap water and water in the dataset and additionally trained and evaluated two lightweight classifiers to evaluate the newly added label class, showing that the new class can be learned more easily.

## Running the Code

Requirement for CNN training: Nvidia GPU with 8GB GDDR memory, Nvidia drivers installed.

1. Download the videos and hdf5 files from [HD-Epic](https://data.bris.ac.uk/data/dataset/3cqb5b81wk2dc2379fx1mrxh47):
  - You need the contents of Audio-HDF5, which need to be placed inside the empty folders at the root level of this repository.
  - If you want to check the annotations with the videos, place the videos in the "videos" folder.
  - A downloading tool like "jDownloader" can help at batch-downloading the relevant HD-Epic data.

2. Create and activate a new Python 3.11 virtual environment (e.g., with conda), run `pip install -r requirements.txt`
3. To generate all results, run all cells in epic-hd.ipynb
4. To generate additional plots run all cells in AdditionalPlots.ipynb

## Annotations
The newly created annotations are contained in [this file](/HD_EPIC_Sounds_annot.csv). The file also contains all [HD-Epic audio annotations](https://github.com/hd-epic/hd-epic-annotations/blob/main/audio-annotations/HD_EPIC_Sounds.csv), and shares its [license](https://creativecommons.org/licenses/by-nc/4.0/). 
"tap water" is added as a new class with class_id 44.

## Labeling the videos by yourself
If you want to follow the process of labeling, check out "Relabeling.ipynb".

## Cite as

```
citation available once paper is published
```
## License

### HD Epic, Annotations
HD-Epic, including the hdf5 files and video files and their annotations are copyright by the authors of HD-Epic and published under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/). This means that you must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use. You may not use the material for commercial purposes.

Our additional annotations are a derived work of the existing annotations, and we put them under the same license, the above terms apply.

### Code, Figures, Results of this Repository:
All code, notebooks, figures, and other artefacts of this repository, except for those belonging to HD-Epic itself, are under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en).
