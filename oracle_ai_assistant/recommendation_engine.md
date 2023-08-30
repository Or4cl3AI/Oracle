```python
class RecommendationEngine:
    def __init__(self):
        self.collaborative_filtering = CollaborativeFiltering()
        self.machine_learning = MachineLearning()

    def get_personalized_recommendations(self, user_id):
        user_preferences = self.collaborative_filtering.get_user_preferences(user_id)
        historical_data = self.collaborative_filtering.get_historical_data(user_id)
        recommendations = self.machine_learning.generate_recommendations(user_preferences, historical_data)
        return recommendations


class CollaborativeFiltering:
    def get_user_preferences(self, user_id):
        # Retrieve user preferences from the database
        preferences = UserPreferences.objects.filter(user_id=user_id)
        return preferences

    def get_historical_data(self, user_id):
        # Retrieve historical data from the database
        historical_data = HistoricalData.objects.filter(user_id=user_id)
        return historical_data


class MachineLearning:
    def generate_recommendations(self, user_preferences, historical_data):
        # Apply machine learning algorithms to generate recommendations
        # ...
        recommendations = []
        return recommendations
```

In the `RecommendationEngine` class, we have a method `get_personalized_recommendations` that takes a `user_id` as input. It first retrieves the user preferences and historical data using the `CollaborativeFiltering` class. Then, it calls the `generate_recommendations` method of the `MachineLearning` class to generate personalized recommendations based on the user preferences and historical data. Finally, it returns the recommendations.

The `CollaborativeFiltering` class has methods `get_user_preferences` and `get_historical_data` that retrieve user preferences and historical data from the database, respectively.

The `MachineLearning` class has a method `generate_recommendations` that applies machine learning algorithms to generate recommendations based on the user preferences and historical data. Currently, it returns an empty list as a placeholder.

Please note that this code is just a basic example to illustrate the structure of the Recommendation Engine module. You may need to modify and extend it based on your specific requirements and the algorithms you want to use for generating recommendations.