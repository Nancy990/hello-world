
# AI Personal Trainer

An AI-powered exercise classification system that recognizes human exercises using joint angle data. Built using a Random Forest classifier and a Feedforward Neural Network (FNN), this project enables real-time exercise recognition with optimized deployment for low-resource environments.

## Dataset

- **Source**: [Kaggle - Exercise Detection Dataset](https://www.kaggle.com/datasets/mrigaankjaswal/exercise-detection-dataset)
- Includes joint angles such as `Shoulder_Angle`, `Elbow_Angle`, etc., with labels for different exercises and side information (`Left` or `Right`).

## Preprocessing

- Encoded labels into numeric format using `LabelEncoder`.
- Selected joint angle features to train classification models.

## Models

### Random Forest Classifier
- Classifies **5 exercises**:
  - Jumping Jacks
  - Pull Ups
  - Push Ups
  - Squats
  - Russian Twists
- Achieved **97% accuracy**.
- Model saved using `joblib` for inference.

### Feedforward Neural Network (FNN)
- Implemented with PyTorch.
- Achieved **53% accuracy**, requiring further tuning.
- Deployment tested with **TorchServe**.

## Model Optimization

- Performed **memory profiling**.
- Applied **Float32 quantization**:
  - Reduced model size by **83.34%**
  - Maintained **96%+ accuracy**
  - Ideal for **edge/low-resource deployment**

## Real-Time Pose Detection

- Integrated **MediaPipe** and **OpenCV** to capture live video feed.
- Extracted pose landmarks in real time.
- Converted landmark data into joint angles for live classification.
- Enables real-time exercise recognition and feedback via webcam.

## Deployment

- Tested API-based and edge-device deployment.
- Explored **TorchServe** for serving PyTorch-based FNN model.

## 📊 Performance Summary

| Component                | Description                               |
|--------------------------|-------------------------------------------|
| Accuracy (Random Forest) | 97%                                       |
| Quantization             | Float32 (83.34% size reduction)           |
| Real-time Inference      | (MediaPipe + OpenCV)                   |
| FNN Accuracy             | 53% (Baseline for future improvements)    |

## Tools & Libraries

- Python
- Scikit-learn
- Pandas / NumPy
- Joblib
- PyTorch
- TorchServe
- MediaPipe
- OpenCV
- Matplotlib

## Future Plans

- Improve FNN performance through hyperparameter tuning and more data.
- Add support for additional exercises and full-body routines.
- Build a web or mobile app interface.
- Implement real-time form correction and rep counting.

## Contact

For questions or collaboration, connect via [LinkedIn](https://www.linkedin.com/in/nancydianagudavalli/) or open an issue on GitHub.

---

follow for more real-world AI applications!

