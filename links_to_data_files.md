## Icon dataset (for training and evaluating icon classification): ##
We provide a dataset of 250K icon images downloaded from Google images to cover [391 different tag classes](https://github.com/cvzoya/visuallydata/blob/master/29kfiles/map_labels_tags.txt).
* [validation set](https://www.dropbox.com/s/5zrpvh4ryq9bw1f/icons_val.zip?dl=0) (4.5 GB uncompressed)
* [training set, split into 4 parts](https://www.dropbox.com/sh/3dva85zh00bezll/AACDbkQzE4izaISIT9yOXoc3a?dl=0) (each around 4.5-5.5 GB uncompressed, 21 GB total)

Note: these are the original downloaded image sets, uncurated (warning: data may be noisy)

## Parsed text (OCR from within infographics): ##
Computed using Google's Cloud Vision API for OCR: https://cloud.google.com/vision/
* [raw_ocr_output.pickle](https://www.dropbox.com/s/49wwv7xuqr43m9k/raw_ocr_output.pickle?dl=0) (2.2 GB) contains all the extracted text along with the bounding boxes of individual words
  * contains a dictionary that maps infographic filenames to the extracted text
  * the extracted text is a list, where the first element is the full text extraction (with coordinates) 
  * subsequent elements are individual words and their bounding box coordinates e.g., ('Road', ['(11,26)', '(55,26)', '(55,47)', '(11,47)'])
* [google_text_extraction_output.pckl](https://www.dropbox.com/s/emi1dar3yryytfc/google_text_extraction_output.pckl?dl=0) (220 MB) contains just a list of the extracted words per infographic
  * contains a dictionary that maps infographic filenames to a list of individual extracted words

See [plot_text_detections.ipynb](https://github.com/cvzoya/visuallydata/blob/master/plot_text_detections.ipynb) for examples of how to use these files.
