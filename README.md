
# AnomalyDetectionCVPR2018-Pytorch  <!-- omit in toc -->

## Demo

### Off-line (with video loader)
Arguments:
* feature_extractor - path to the 3D model to use for feature extraction
* feature_method - which type of model to use for feature extraction (necessary in order to choose the correct pre-processing)
* ad_model - path to the trained anomaly detection model
* n_segments - the number of segments to chunk the video to (the original paper uses 32 segments)

```python video_demo.py --feature_extractor "path-to-pretrained-fe" --feature_method "fe-method" --ad_model "path-to-pretrained-ad-model" --n_segments "number-of-segments"```

The GUI lets you load a video and run the Anomaly Detection code (including feature extraction) and output a video with a graph of the Anomaly Detection prediction below.

**Note**: The feature extractor and the anomaly detection model must match. Make sure you are using the anomaly detector that was training with the corresponding features.

### On-line (via webcam)
Arguments:
* feature_extractor - path to the 3D model to use for feature extraction
* feature_method - which type of model to use for feature extraction (necessary in order to choose the correct pre-processing)
* ad_model - path to the trained anomaly detection model
* clip_length - the length of each video clip (in frames)

```python AD_live_prediction.py --feature_extractor "path-to-pretrained-fe" --feature_method "fe-method" --ad_model "path-to-pretrained-ad-model" --clip_length "number-of-frames"```

The GUI lets you load a video and run the Anomaly Detection code (including feature extraction) and output a video with a graph of the Anomaly Detection prediction below.

**Note**: The feature extractor and the anomaly detection model must match. Make sure you are using the anomaly detector that was training with the corresponding features.

*Contrbuted by Peter Overbury of Sussex Universty IISP Group

