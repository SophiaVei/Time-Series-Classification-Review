# Temporal Algorithmic Synthesis: Unraveling the Complexity of Time Series Classification


The present repository is dedicated to Time Series Classification.
### Systematic evaluation on various datasets from the UCR archive.
  🔎 The datasets are organized based on:
   * Dimensions (univariate or multivarite)
      * Length (<300, >=300, >700)
         * Classes (<10, >=10, >=30)
     
   We conducted our experiments on various datasets for this part, but we include here 11, since based on the former categorization UCR contains this number of datasets.
   We use numerous datasets to evaluate 21 classifiers which we separate in 6 categories:
   1. Deep Learning:
      * Multi Layer Perceptron (MLP)
      * Convolutional Neural Network (CNN)
      * Fully Convolutional Network (FCN)
      * Multi-Channels Deep Convolutional Neural Networks (MCD-CNN)
   2. Dictionary - based:
      * Bag of SFA Symbols (BOSS)
      * Contractable Bag of SFA Symbols (cBOSS)
      * Individual Bag of SFA Symbols (iBOSS)
      * Temporal Dictionary Ensemble (TDE)
      * Individual Temporal Dictionary Ensemble (iTDE)
      * Word Extraction for Time Series Classification (WEASEL)
      * MUltivariate Symbolic Extension (MUSE)
   3. Distance - based:
      * Shape Dynamic Time Warping (shapeDTW)
      * K-Nearest Neighbors (using DTW) (KNN)
   4. Feature - based:
      * Canonical Time-series Characteristics (catch22)
      * Fresh Pipeline with RotatIoN forest (FreshPRINCE)
   5. Interval - based:
      * Supervised Time Series Forest (STSF)
      * Time Series Forest (TSF)
      * Canonical Interval Forest (CIF)
      * Diverse Representation Canonical Interval Forest (DrCIF)
   6. Convolutional - based:
      * ROCKET
      * Arsenal

  We are using aeon library while except for MCD-CNN which is only available on sktime.
  For the evaluation we create metrics such as F1, Accuracy, Precision, AUC scores (macro and micro) while we also calculate execution times and memory consumptions.
  We also create plots such as macro average ROC AUC curve per classifier, confusion matrices and ROC AUC curves for each class.
  We also introduce results with and without cross-validation. For cross-validation we use both k-fold and TimeSeriesSplit. We use k-fold only for comparison reasons with other papers,
  since we are opposite to its use for time series data, for temporal structure reasons. Therefore, we always suggest TimeSeriesSplit if you want to use cross-validation.

💡 This analysis is very useful if this is the case:
  1. You want to see results based on a very large amount of datasets.
  2. You want to see a very thorough review - first work comparing so many time series classification algorithms on these datasets.
  3. You want to see the comparison of the algorithms based on the types (image, sound, sensors, EEG, ECG etc), the length, the size, the number of classes etc on the datasets.
  4. You are interested in different metrics besides accuracy.
  5. You are interested in different visualisations that reflect the performance.
