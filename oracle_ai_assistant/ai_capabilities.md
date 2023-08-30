```python
class AICapabilitiesModule:
    def __init__(self):
        self.tensorflow = TensorFlow()
        self.pytorch = PyTorch()

    def train_model(self, model):
        if model == "image_recognition":
            self.tensorflow.train_image_recognition_model()
        elif model == "sentiment_analysis":
            self.tensorflow.train_sentiment_analysis_model()
        elif model == "natural_language_understanding":
            self.pytorch.train_natural_language_understanding_model()
        else:
            raise ValueError("Invalid model type")

    def deploy_model(self, model):
        if model == "image_recognition":
            self.tensorflow.deploy_image_recognition_model()
        elif model == "sentiment_analysis":
            self.tensorflow.deploy_sentiment_analysis_model()
        elif model == "natural_language_understanding":
            self.pytorch.deploy_natural_language_understanding_model()
        else:
            raise ValueError("Invalid model type")

class TensorFlow:
    def train_image_recognition_model(self):
        # Code for training image recognition model using TensorFlow
        pass

    def train_sentiment_analysis_model(self):
        # Code for training sentiment analysis model using TensorFlow
        pass

    def deploy_image_recognition_model(self):
        # Code for deploying image recognition model using TensorFlow
        pass

    def deploy_sentiment_analysis_model(self):
        # Code for deploying sentiment analysis model using TensorFlow
        pass

class PyTorch:
    def train_natural_language_understanding_model(self):
        # Code for training natural language understanding model using PyTorch
        pass

    def deploy_natural_language_understanding_model(self):
        # Code for deploying natural language understanding model using PyTorch
        pass
```