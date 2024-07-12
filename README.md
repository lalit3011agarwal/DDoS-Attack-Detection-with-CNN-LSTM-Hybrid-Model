# DDoS Attack Detection using Convolutional Neural Network-Long Short-Term Memory (CNN-LSTM)

## Dataset Exploration
- CIC-IDS2017 dataset used for DDoS attack detection
- Contains both benign and DDoS attack network traffic flows
- Friday subset used, including various DDoS attack types
- 66,237 network flows: 31,284 benign, 34,952 DDoS attack instances

## Preprocessing
- Removal of rows with missing values
- Replacement of infinite values with NaN
- Conversion of categorical labels to binary (0 for benign, 1 for DDoS)
- Dataset split into training (46,365 samples) and testing (19,871 samples) sets

## Feature Engineering
- Grouping of related features:
  - Packet Counts
  - Packet Lengths
  - Length Stats
  - Flow Features
  - IAT Features
- Data transformation into 2D grids for CNN processing
- Standard scaling applied to normalize numerical features

## Model Architecture
- CNN-LSTM hybrid model
- Convolutional layers for spatial feature extraction
- Max-pooling layer for dimensionality reduction
- LSTM layer to capture temporal dependencies
- Dropout layer to prevent overfitting
- Dense output layer with sigmoid activation

## Performance Metrics
- Accuracy: 99.93%
- F1 Score: 0.9993
- Precision: 0.9996
- Recall: 0.9990

## Challenges and Limitations
- Potential overfitting in deep learning models
- Limited dataset diversity compared to real-world scenarios
- Need for real-time deployment evaluation

## Potential Model Improvements
- Explore alternative regularization techniques (L1, L2)
- Investigate different feature engineering approaches
- Evaluate on more recent and diverse datasets
- Assess real-time performance and adaptability
- Incorporate additional data sources (network logs, system metrics)

## Future Directions
- Enhance model robustness and generalizability
- Explore transfer learning for adapting to new attack patterns
- Investigate interpretability and explainability of model decisions
- Develop ensemble methods combining multiple detection techniques
- Integration with existing network security infrastructure
